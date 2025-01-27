[<<<< Menu >>>>](../README.md)

#  שיעור שביעי - שלט רחוק וגלאי IR 

<br><br>


### כדי להשתמש בשלט רחוק עלינו להוסיף ספריית IRremote.h:

#### - יש לבחור את מנהל הסיפריות בצד שמאל.
#### - לרשום בחיפוש: "IRremote" ולהתקין את הספרייה המתאימה.
#### - ללחוץ על "install" ולהמתין עד לסיום ההתקנה.

![image001](data/image001.png)


### להלן הקוד לזיהוי הסיפרה '1' - יש להוסיף לחצנים נוספים:

```cpp

#include <IRremote.h>

int RECV_PIN = 11;
IRrecv irrecv(RECV_PIN);  // Creating IR receiver
decode_results results;  // Creating results variable

void setup()
{
  Serial.begin(9600);
  Serial.println("It Starts...");
  irrecv.enableIRIn();  // Start the receiver
}

void loop()
{ 
 
  if (irrecv.decode(&results)) // Test if receiver got anything into results?
  {
     Serial.println(results.value, HEX);
     
     if (results.value == 0xFF30CF)
     {
       Serial.println("You have pressed '1' :) ...."); 
     }
     
     irrecv.resume(); // Receive the next value
  }
  delay(10);
}


```
