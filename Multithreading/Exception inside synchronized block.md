What will happen if exception will be thrown inside synchronized block?

```
private void doSomething() throws Exception {...}

synchronized (lock) {   
    doSomething();       
}
```

The **lock is guaranteed to be terminated** in all cases, and an exception is no exception (pun intended).
