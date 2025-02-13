# Timer and TimerTask

`Timer` = Class that schedules tasks at specific times or periodically 
Useful for: sending notifications, scheduled updates, repetitive actions.

---
## Example: Timer with Repeated Task
`TimerTask` Represents the task that will be executed by the Timer.
            You will extend the TimerTask class to define your task
            Create a subclass of TimerTask and @Override run().
```java
import java.util.Timer;
import java.util.TimerTask;

public class TimerExample {
    public static void main(String[] args) {
        Timer timer = new Timer();
        
        TimerTask task = new TimerTask() {
            int counter = 3; // Run 3 times
            
            @Override
            public void run() {
                System.out.println("Timer task executed");
                counter--;
                if (counter <= 0) {
                    System.out.println("Task completed");
                    timer.cancel();
                }
            }
        };

        timer.schedule(task, 0, 1000); // Execute every 1 second
        or
        or timer.scheduleAtFixedRate(task, 0, 1000);
    }
}
```
