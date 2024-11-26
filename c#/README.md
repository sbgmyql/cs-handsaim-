# מבחן במחשבים חומר פתוח
## הדפסה של דברים 
כך מדפיסים טקסט בסיסי
> שימו לב יש להקפיד על אותיות גדולות וקטנות 
```c#
Console.Write("text");
Console.WriteLine("text");
```
<br>

:אפשר גם להדפיס משתנים עם הטקסט על ידי הוספת: "+", לדוגמה
```c#
int num = 4;
Console.Write("num = "+ num);
```
>פלט <br>
num = 4

<br>

-ההבדל בין
```c#
Console.Write("text");
```
-ל
```c#
Console.WriteLine("text");
```
הוא שהשני פותח שורה חדשה <u>אחריו</u>

<br>
אפשר גם להוסיף שורה חדשה בצורה הזו

```c#
Console.Write("text\n");
```
כלומר זה עושה אותו הדבר כמו זה 

```c#
Console.WriteLine("text");
```
<br>

## קליטת ערכים

קליטת ערכים מתבצעת על יד הפקודה
```c#
Console.Read();
```
`Parse(). `במקרה בוא רוצים להמיר את מה שנקלט למשתנה אחר יש להוסיף את סוג המשתנה ובצורה הזו
```c#
int.Parse(Console.Read());
```
את מה שמתקבל יש לקלוט בצורה כלשהי, כמו לשים במשתנה או להדפיס
```c#
Console.Write("enter a number");
int num = int.Parse(Console.Read())
```
אפשר להוסיף שורה אחרי הקלט באותה צורה כמו בפלט לדוגמא 

```c#
Console.ReadLine();
```
<br>

## תגובות
 יש שתי צורות לרשום תגובות
 ```c#
 //
 // this is a one line comment
 //
 /*

 this is a molti line comment
 
 */
 ```
 תגובות אפשר לרשום באופן חופשי והתוכנה מתעלמת מהם 
 
 יש להסביר אם בתגובות מה רשמתם בקוד לבני אדם על מנת להסביר להם מה רשום בקוד (ארול דורש להשתמש בהם במבחנים)

<br>

## משתנים 
משתנים מוגדרים על ידי סוג ואז שם לדוגמא

```C#
int num ;
string str ;
char character ;

```
אפשר גם אחרי המשתנה להוסיף = ואז את מה שרוצים שהיה במשתנה לדוגמא 
```c#
int myNum = 5;               // Integer (whole number)
double myDoubleNum = 5.99D;  // Floating point number 
char myLetter = 'D';         // Character (one letter only be aware to use ' and not ")
bool myBool = true;          // Boolean (true or false  only )
string myText = "Hello";     // String (text)

```
הנרשם כך `float` יש גם משתנה מסוג 
```c#
float myFloatNum = 5.99F;
```

 `double` להתייחס עליו כמו משתנה משתנה זה **לא נלמד** אבל אם הוא יופע שתדעו איך להשתמש בוא יש להתייחס עליו כמו 

אחרי הגדרת המשתנה אפשר לקבוע לו ערך על ידי רשימת שם המשתנה = ואז הערך לדוגמא
``` c#
num = 5
```
:הפעולות שניתן איתם לבצע פעולות על משתנים הם 
```c#
+ // addition
- // subtrction
% // modulo
* // multiplication
/ // division
+= //short for var = var + somthing
-= //short for var = var - somthing
*= //short for var = var * somthing
%= //short for var = var % somthing
/= //short for var = var / somthing
++ // adds one to the variable 
-- // removes one from the variable
```

## תנאים

תנאי `if` מאפשרים לבצע קוד בהתאם לתנאים מסוימים. לדוגמה, אם אנחנו רוצים לבדוק אם מספר הוא חיובי, נוכל לכתוב כך:
```c#
int num = 10;

if (num > 0)
{
    Console.WriteLine("המספר חיובי");
}
else
{
    Console.WriteLine("המספר אינו חיובי");
}
```
הצורה שבה אנו רושמים את התנאי היא 

```c#
if (condition){
    //code
}
else if (condition){
    //code
}
else {
    //code if no condition is met 
}
```
ההתניות שאנו מכירים הם 

```c#
== //for equal
<= //smaller or equal to 
>= //bigger or equal to 
!= // not equal 
< // smaller then
> // bigger then  
```
בנוסף יש צורות לוגיות לשילוב בתוצאות כמו 
```c#
|| // a || b is the same as a or b 
&& // a && b is the same as a and b 

```
 

## לופים 

### for 
מבנה הלופ
```c#
for (int i = start; i< end ; i++ ){
    // the parmeters like < and ++ can be changed
    // code
}
```
סימו לב שאם אתם תגדירו משתנה בתוך הלולאה (כמו בדוגמה מעל) אז אי אפשר היה לגשת אל המשתנה אשר בדוגמה הוא i

במידה ואתם רוצים לגשת על המשתנה אחרי הלולאה יש לרשום כך
```c
int i ;
for (i = start ; i < end ; i++){
    // code
}
```
### while
מבנה הלופ
```c# 
while(condtion){
    //code
}
```
## random
בישביל להשתמש יש לרשום בהתחלה 
```c#
var rand = new Random();

rand.Next(a, n+1) // returns a number beteen a to n (a < n)
rand.NextDouble() // returns a number beteen 0.0 to 1.0 for exemple 0.53242
// there is no way to set a range for this use mathmatical operthion to make it as a range 
```

## math 
בספריה יש הרבה פונקציות לדוגמה 
```c#
Math.Max(5, 10); //returns the biggest number for exemple 10
Math.Min(5, 10); //returns the smallest number for exemple 5
Math.Sqrt(64); // returns the squre root for exemple 8
Math.Round(9.54); // rounds the number (returns as dubble) for exemple 10.00
Math.Abs(-4.7); // return the absole value of a number (the number in the positive form) for exemple 4.7
```