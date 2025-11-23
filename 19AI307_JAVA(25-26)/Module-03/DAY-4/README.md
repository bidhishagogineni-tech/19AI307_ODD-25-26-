# Ex.No:3(D)    INTERFACE 

## QUESTION:
You are programming bots that analyze weather data. Each bot must implement a common interface and give a prediction.


 Bot Types:

SunBot: Predicts "HOT" if temperature > 30, else "MODERATE".

RainBot: Predicts "COLD" if temperature < 20, else "WARM".

Input:

temperature
botType (1 for SunBot, 2 for RainBot)Output:
Prediction as a string.

<img width="155" height="134" alt="image" src="https://github.com/user-attachments/assets/abc31f61-6641-443a-b09f-0ca694e60125" />


## AIM:
To develop a Java program using interfaces where different weather bots (SunBot and RainBot) implement a common prediction method. The program should take temperature and bot type as input and return the appropriate weather prediction based on each bot’s logic.

## ALGORITHM :
1.Read temperature and bot type (1 or 2).
2.If bot type is 1 (SunBot):
  If temperature > 30 → print "HOT"
  Else → print "MODERATE"
3.If bot type is 2 (RainBot):
  If temperature < 20 → print "COLD"
  Else → print "WARM"
4.End program.
## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: GOGINENI BIDHISHA
RegisterNumber: 212223040048 
*/
```

## SOURCE CODE:
```
import java.util.*;
interface bot
{
    String predict(int tem);
}
class SunBot implements bot
{
    public String predict(int tem)
    {
        if(tem>30)
        {
            return "HOT";
        }
        else
        {
            return "MODERATE";
        }
    }
}
class RainBot implements bot
{
    public String predict(int tem)
    {
        if(tem<20)
        {
            return "COLD";
        }
        else
        {
            return "WARM";
        }
    }
}
public class prog
{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        int tem=sc.nextInt();
        int type=sc.nextInt();
        bot b;
        if(type==1)
        {
            b=new SunBot();
        }
        else
        {
            b=new RainBot();
        }
        System.out.println(b.predict(tem));
    }
}

```






## OUTPUT:

<img width="362" height="167" alt="image" src="https://github.com/user-attachments/assets/7aed5b5a-eade-4afd-b7bf-e41b051580b1" />


## RESULT:
The program successfully predicts weather conditions based on the selected bot.
