**Deadlock** is a process when two threads wait for resources that are being blocked by each other.

*For example*:
Thread1 wants to lock 2 resources: lockA and lockB in order to lockA will be blocked earlier than lockB.
Thread2 wants to same 2 resources in order to lockB will be blocked earlier than lockA.
It causes that Thread1 will be wait for releasing lockB while Thread2 will be wait for releasing lockA. 

    public class TestDeadlockExample1 {  
        public static void main(String[] args) {  
            final String resource1 = "lock1";  
            final String resource2 = "lock2";  
            // t1 tries to lock resource1 then resource2    
		    Thread t1 = new Thread() {  
            public void run() {  
                    synchronized (resource1) {  
                        System.out.println("Thread 1: locked resource 1");  
                        try {  
                            Thread.sleep(100);  
                        } catch (Exception e) {  
                        }  
      
                        synchronized (resource2) {  
                            System.out.println("Thread 1: locked resource 2");  
                        }  
                    }  
                }  
            };  
      
            // t2 tries to lock resource2 then resource1    
            Thread t2 = new Thread() {  
                public void run() {  
                    synchronized (resource2) {  
                        System.out.println("Thread 2: locked resource 2");  
      
                        try {  
                            Thread.sleep(100);  
                        } catch (Exception e) {  
                        }  
      
                        synchronized (resource1) {  
                            System.out.println("Thread 2: locked resource 1");  
                        }  
                    }  
                }  
            };  
            t1.start();  
            t2.start();  
        }  
    }

