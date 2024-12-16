[<<<< Menu >>>>](../README.md)

# שיעור שלישי - בניית המשחק
&nbsp;&nbsp;

# בניית המשחק

### מבנה המשחק:

![Picture 22](../Lesson_02/data/image002.png)


### המעגל של המקלות והמשטחים:

![Picture 3](../Lesson_02/data/image003.jpg)



### המעגל של הלדים - ירוק \ אדום:

![Picture 4](../Lesson_02/data/image004.jpg)

### המעגל של הלדים - מי ניצח:

![Picture 5](../Lesson_02/data/image005.png)


### המעגל המלא:

![Picture 6](../Lesson_02/data/image006.png)

<br><br><br>

### הקוד:

```cpp

int Player_1_V = 0;
int Player_2_V = 0;

int Led_Color = 0;

int Stop = 0;

int GREEN = 1;  // Green connected to the GND = 0V
int RED = 2;    // Red connected to the 5V

int Someone_Won = 0;  // 0 - No one!

int LedPin_Color_Green = 8;
int LedPin_Color_Red = 9;

int LedPin_Player_1 = 6;
int LedPin_Player_2 = 7;

void setup() 
{
  randomSeed(analogRead(0) + analogRead(5));
  pinMode(LedPin_Color_Green, OUTPUT);
  pinMode(LedPin_Color_Red, OUTPUT);
  pinMode(LedPin_Player_1, OUTPUT);
  pinMode(LedPin_Player_2, OUTPUT);
  Serial.begin(9600);  // Begin the serial communication
}

void loop() 
{
  digitalWrite(LedPin_Color_Green, LOW);  // Turn off Green led
  digitalWrite(LedPin_Color_Red, LOW);    // Turn off Red led
  digitalWrite(LedPin_Player_1, LOW);     // Turn off Player 1 led
  digitalWrite(LedPin_Player_2, LOW);     // Turn off Player 2 led

  delay(2000);  // Pause  for 2 seconds

  Led_Color = random(1, 3);  // Choose a random number (1 or 2) represent Green / Red

  if (Led_Color == GREEN)  // Turn on the right color
  {
    Serial.println("Green LED on");
    digitalWrite(LedPin_Color_Green, HIGH);
  } 
  else 
  {
    Serial.println("Red LED on");
    digitalWrite(LedPin_Color_Red, HIGH);
  }

  Someone_Won = 0;  // 0 - No one!

  while (Someone_Won == 0)  // Wait for a player to touch a target
  {
    Player_1_V = analogRead(A1);
    Player_2_V = analogRead(A2);

    Serial.print("Player 1 V = ");
    Serial.print(Player_1_V);
    Serial.print("; \t Player 2 V = ");
    Serial.println(Player_2_V);

    // Testing Player 1 if he is hitting and if he is correct:
    if (Player_1_V < 400)  // Dose Player 1 touch the Green -> GND = 0V (< 512)
    {
      if (Led_Color == GREEN) 
      {
        Someone_Won = 1;
      } 
      else 
      {
        Someone_Won = 2;
      }
    }

    if (Player_1_V > 600)  // Dose Player 1 touch the Red -> 5V (> 512)
    {
      if (Led_Color == RED) 
      {
        Someone_Won = 1;
      } 
      else 
      {
        Someone_Won = 2;
      }
    }

    // Testing Player 2 if he is touching and if he is correct:

    if (Player_2_V < 400)  // Dose Player 2 touch the Green -> GND = 0V (< 512)
    {
      if (Led_Color == GREEN) 
      {
        Someone_Won = 2;
      } 
      else 
      {
        Someone_Won = 1;
      }
    }

    if (Player_2_V > 600)  // Dose Player 2 touch the Red -> 5V (> 512)
    {
      if (Led_Color == RED) 
      {
        Someone_Won = 2;
      } 
      else 
      {
        Someone_Won = 1;
      }
    }
  }

  if (Someone_Won == 1) 
  {
    Serial.println("********* Player ---- 1 ---- WON *********");
    digitalWrite(LedPin_Player_1, HIGH);
  }

  if (Someone_Won == 2) 
  {
    Serial.println("********* Player ---- 2 ---- WON *********");
    digitalWrite(LedPin_Player_2, HIGH);
  }

  delay(2000);  // Wait for 2000 millisecond(s)
}
```

<br><br><br>
<br><br><br>


# מתחילים לעבוד עם [Tinkercad](https://www.tinkercad.com/):

<br><br>


### להתחלת מעגל חדש יש ללחוץ על +New:
![image001](data/image001.jpg)

### לבחור Circuit:
![image002](data/image002.jpg)

### לחיצה על הארדואינו אונו:
![image003](data/image003.jpg)

### לחיצה על משטח העבודה כדי להניח את הארדואינו:
![image004](data/image004.jpg)

### באופן דומה ללחוץ על ה-Breadboard Small ועל הלוח:
![image005](data/image005.jpg)

### כדי לחבר חוט מהאדמה (GND) אל המטריצה, נלחץ בנקודות הבאות:
![image006](data/image006.jpg)

### אפשר וכדאי לשנות את החוט לשחור (עבור GND):
![image007](data/image007.jpg)

### באופן דומה מחברים את ה-5V בצבע אדום:
![image008](data/image008.png)

### מוסיפים לד ונגד:
![image009](data/image009.png)

### לוחצים על הנגד מזינים את ערכו – 220 ובוחרים אום Ω:
![image010](data/image010.png)

### כדי לשנות את הקוד יש ללחוץ על Code:
![image011](data/image011.png)

### הקוד שמופיע בהתחלה בתוך ה-forever שהוא ה-loop מהבהב את הלד שעל הכרטיס – פין 13. אפשר לגרור אותו לפח:
![image012](data/image012.png)

### ולבנות קוד שממתג את רגל מספר 8 – כמו שעשינו בשיעור הראשון:
![image013](data/image013.png)

### נחבר את רגל 8 לאנודה ונריץ בלחיצה על כפתור Start Simulation:
![image014](data/image014.png)

### כאשר רוצים להעתיק קוד לסביבת הארדואינו, יש לפתוח את הקוד ולבחור ב-Blocks את Blocks + Code אז ניתן להעתיק את הקוד מימין:
![image015](data/image015.png)


