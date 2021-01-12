#### [1115. 交替打印FooBar](https://leetcode-cn.com/problems/print-foobar-alternately/)

难度中等85

我们提供一个类：

```
class FooBar {
  public void foo() {
    for (int i = 0; i < n; i++) {
      print("foo");
    }
  }

  public void bar() {
    for (int i = 0; i < n; i++) {
      print("bar");
    }
  }
}
```

两个不同的线程将会共用一个 `FooBar` 实例。其中一个线程将会调用 `foo()` 方法，另一个线程将会调用 `bar()` 方法。

请设计修改程序，以确保 "foobar" 被输出 n 次。

 

**示例 1:**

```
输入: n = 1
输出: "foobar"
解释: 这里有两个线程被异步启动。其中一个调用 foo() 方法, 另一个调用 bar() 方法，"foobar" 将被输出一次。
```

**示例 2:**

```
输入: n = 2
输出: "foobarfoobar"
解释: "foobar" 将被输出两次。
```





#### 原子变量(280 ms)

```c++
class FooBar {
private:
    int n;
		atomic<int> foo_time;
    atomic<int> bar_time;
  
public:
    FooBar(int n) {
        atomic_init(&foo_time, -1);
        atomic_init(&bar_time, -1);
        this->n = n;
    }

    void foo(function<void()> printFoo) {
        
        for (int i = 0; i < n; i++) {
            while (bar_time.load() != i - 1)
                this_thread::yield();
        	// printFoo() outputs "foo". Do not change or remove this line.
        	printFoo();
            foo_time.store(i);
        }
    }

    void bar(function<void()> printBar) {
        
        for (int i = 0; i < n; i++) {
            while (foo_time.load() != i)
                this_thread::yield();
        	// printBar() outputs "bar". Do not change or remove this line.
        	printBar();
            bar_time.store(i);
        }
    }
};
```





#### 条件变量

```c++
class FooBar {
private:
    int n;
    int foo_time, bar_time;
    condition_variable c1, c2;
    mutex _m;

public:
    FooBar(int n) {
        this->n = n;
        foo_time = -1;
        bar_time = -1;
    }

    void foo(function<void()> printFoo) {
        for (int i = 0; i < n; i++) {
            unique_lock<mutex> guard(_m);
            c2.wait(guard, [&]() {
                return bar_time == i - 1;
            });
        	// printFoo() outputs "foo". Do not change or remove this line.
        	printFoo();
            foo_time = i;
            c1.notify_one();
        }
    }

    void bar(function<void()> printBar) {
        
        for (int i = 0; i < n; i++) {
            unique_lock<mutex> guard(_m);
            c1.wait(guard, [&]() {
                return foo_time == i;
            });
        	// printBar() outputs "bar". Do not change or remove this line.
        	printBar();
            bar_time = i;
            c2.notify_one();
        }
    }
};
```



#### pthread_mutex_t

```c++
class FooBar {
private:
    int n;
    mutex _m;
    pthread_mutex_t m1, m2;

public:
    FooBar(int n) {
        this->n = n;
        m1 = PTHREAD_MUTEX_INITIALIZER;
        m2 = PTHREAD_MUTEX_INITIALIZER;
        pthread_mutex_lock(&m2);
    }
    

    void foo(function<void()> printFoo) {
        for (int i = 0; i < n; i++) {
            pthread_mutex_lock(&m1);
        	  // printFoo() outputs "foo". Do not change or remove this line.
        	  printFoo();
            pthread_mutex_unlock(&m2);
        }
    }

    void bar(function<void()> printBar) {
        for (int i = 0; i < n; i++) {
            pthread_mutex_lock(&m2);
        	  // printBar() outputs "bar". Do not change or remove this line.
        	  printBar();
            pthread_mutex_unlock(&m1);
        }
    }
};
```

