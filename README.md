
import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        Scanner reader = new Scanner(System.in);
 
        
        BoundedCounter minutes = new BoundedCounter(59);
        BoundedCounter hours = new BoundedCounter(23);
        BoundedCounter seconds = new BoundedCounter(59);
        
        //Change int variables (s,m,h) to the preferred number
        System.out.print("seconds: ");
        // s stands for seconds
        int s = 0;
        System.out.print("minutes: ");
        // m stands for minutes
        int m = 0;
        // h stands for hour
        System.out.print("hours: ");
        int h = 0;
          
        // values are set to 0, please see above to update preference
        seconds.setValue(s);
        minutes.setValue(m);
        hours.setValue(h);
        
        int i = 0;
        
        // Change value 121 in while parameter to indicate when couting should stop
        while (i < 121) {

            System.out.println(hours + ":" + minutes + ":" + seconds);
            seconds.next();
            
            if (seconds.getValue()== 0) {
                minutes.next();
            
            if (minutes.getValue() == 0) {
                hours.next();
            }
            }
            i++;

        }
    }
}
