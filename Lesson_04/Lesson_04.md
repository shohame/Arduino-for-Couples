[<<<< Menu >>>>](../README.md)

# שיעור רביעי - Tinkercad - רכיב אולטראסוני
&nbsp;&nbsp;



# מתחילים לעבוד עם [Tinkercad](https://www.tinkercad.com/):


<br><br>


### להתחלת מעגל חדש יש ללחוץ על +New:
![image001](../Lesson_03/data/image001.jpg)

### לבחור Circuit:
![image002](../Lesson_03/data/image002.jpg)

### לחיצה על הארדואינו אונו:
![image003](../Lesson_03/data/image003.jpg)

### לחיצה על משטח העבודה כדי להניח את הארדואינו:
![image004](../Lesson_03/data/image004.jpg)

### באופן דומה ללחוץ על ה-Breadboard Small ועל הלוח:
![image005](../Lesson_03/data/image005.jpg)

### כדי לחבר חוט מהאדמה (GND) אל המטריצה, נלחץ בנקודות הבאות:
![image006](../Lesson_03/data/image006.jpg)

### אפשר וכדאי לשנות את החוט לשחור (עבור GND):
![image007](../Lesson_03/data/image007.jpg)

### באופן דומה מחברים את ה-5V בצבע אדום:
![image008](../Lesson_03/data/image008.png)

### מוסיפים לד ונגד:
![image009](../Lesson_03/data/image009.png)

### לוחצים על הנגד מזינים את ערכו – 220 ובוחרים אום Ω:
![image010](../Lesson_03/data/image010.png)

### כדי לשנות את הקוד יש ללחוץ על Code:
![image011](../Lesson_03/data/image011.png)

### הקוד שמופיע בהתחלה בתוך ה-forever שהוא ה-loop מהבהב את הלד שעל הכרטיס – פין 13. אפשר לגרור אותו לפח:
![image012](../Lesson_03/data/image012.png)

### ולבנות קוד שממתג את רגל מספר 8 – כמו שעשינו בשיעור הראשון:
![image013](../Lesson_03/data/image013.png)

### נחבר את רגל 8 לאנודה ונריץ בלחיצה על כפתור Start Simulation:
![image014](../Lesson_03/data/image014.png)

### כאשר רוצים להעתיק קוד לסביבת הארדואינו, יש לפתוח את הקוד ולבחור ב-Blocks את Blocks + Code אז ניתן להעתיק את הקוד מימין:
![image015](../Lesson_03/data/image015.png)


<br><br>
<br><br>
<br><br>
<br><br>
### מדידת מרחק אולטראסוני עם חיישן HC-SR04:

#### המטרה: בניית מעגל המודד מרחק, אם המרחק קטן מ-20c”m  ידלק לד ! 

#### בשלב הראשון נבנה את המעגל ב-Tinkercad

#### שימו לב לבחור את הרכיב עם 4 פינים ולא 3 – זה הרכיב שיש לנו הוא נמצא ב-All:

![image016](data/image001.png)


### [נסו לחפש את הרכיב... אבל אם לא תמצאו לחצו כאן :)](data/Find_4_legs_US_in_Tinkercad.gif)

### וכמובן את הארדואינו והמטריצה של החיבורים:

![image017](data/image002.png)

### מחברים את האדמה וה-5V  ובוחרים 2 פינים דיגיטלים (2-13) שיהיו ה-Trig  וה-ECHO ומחברים אותם.
### לכתיבת הקוד יש להגדיר משתנה בשם "מרחק" – distance או בקיצור dist, ולקרא את המרחק מהרכיב באופן הבא:

![image018](data/image003.png)

### הדפיסו את המרחק הנמדד, בדקו האם הוא מתחת 20c”m - הדליקו או כבו את הלד הבנוי על הארדואינו בהתאם למרחק. 
### את כל הקוד שימו בבלוק ב-forever  שהוא ה-loop.
### כאשר מריצים את הסימולציה אפשר לבחור ברכיב האולטראסוני, לקרב או להרחיק ממנו עיגול ולבדוק את תקינות המעגל והקוד.
### כשהכל עובד עוברים לבניית המעגל והעתקת הקוד כפי שעשינו במעגל הקודם. 


### אם אתם צריכים עזרה, תגללו למטה...

<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>


### עזרה ראשונה - הינה הבלוקים הנדרשים:

![image019](data/image004.png)


### אם אתם צריכים עזרה נוספת תמשיכו לגלול....

<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>
<br><br><br><br><br><br><br><br>

### המעגל למדידת מרחק ב- Tinkercad(צריך להוסיף לד ונגד):

![image020](data/image005.png)


### והקוד שיש להכניס:

![image021](data/image006.png)
