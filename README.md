#include <Wire.h>
#include <LiquidCrystal_I2C.h>
LiquidCrystal_I2C lcd(39,16,2);
int ledspin=3,buzzer=4,motor=5,pushbuttom=7,smokesensor=A5,
tempsensor=A0,d=2000;
void setup()  
{
 lcd.begin(16,2); 
 lcd.begin();
 lcd.backlight();
 lcd.setCursor(0,0);
 pinMode(ledspin,OUTPUT);
 pinMode(buzzer,OUTPUT);
 pinMode(motor,OUTPUT);
 pinMode(pushbuttom,OUTPUT);
 pinMode(smokesensor,INPUT);
 pinMode(tempsensor,INPUT);
}

void loop()
{ 
  float r = analogRead(A0);
  float v = r*5/1023;
  float t = (v-0.5)*100;
  lcd.setCursor(0,0);
  lcd.print("temperature :");
  lcd.print(t);
  delay(2000);
 if (t >80)
 {
  int smoke = digitalRead(A5);
  if (smoke==HIGH)
 {
  digitalWrite(3,HIGH);
  digitalWrite(4,HIGH);
  digitalWrite(5,HIGH);
  }
  if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
  {
  lcd.setCursor(1,1);
  lcd.print(10);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
   if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
  {  lcd.setCursor(1,1);
  lcd.print(9);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
  }
    if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {   lcd.setCursor(1,1);
  lcd.print(8);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
    if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {   lcd.setCursor(1,1);
    lcd.print(7);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
    if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {     lcd.setCursor(1,1);
  lcd.print(6);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
 
  delay(t);
   }
   if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {  lcd.setCursor(1,1);
  lcd.print(5);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
    if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {    lcd.setCursor(1,1);
  lcd.print(4);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
  if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {    lcd.setCursor(1,1);
  lcd.print(3);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   } 
   if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {    lcd.setCursor(1,1);
  lcd.print(2);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
    if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {     lcd.setCursor(1,1);
  lcd.print(1);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
   }
   if (digitalRead(pushbuttom)==HIGH)
  { 
    digitalWrite(3,LOW);
    digitalWrite(4,LOW);
    digitalWrite(5,LOW);
  }
   else
   {     lcd.setCursor(1,1);
  lcd.print(0);
  delay(t);
  lcd.setCursor(1,1);
  lcd.print("  ");
  delay(t);
  digitalWrite(3,LOW);
  digitalWrite(4,LOW);
  digitalWrite(5,LOW);
   }
 }
 }
}
