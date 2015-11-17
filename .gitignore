#include <PWM.h>

const int bPin = 2;     // номер входа, подключенный к кнопке
const int mPin =  9;      // номер выхода светодиода

// переменные

int bState = 0;         // переменная для хранения состояния кнопки
unsigned long f = 1000; // частота 1 - 2000000 (Гц) 
void setup() {
  //  пин, подключенный к кнопке, как вход
  pinMode(bPin, INPUT);   
  // пин, подключенный к мотору, как выход
  pinMode(mPin, OUTPUT);     
  
}
 
void loop(){
  // считываем значения с входа кнопки
  bState = digitalRead(bPin);
 
  // проверяем нажата ли кнопка
  // если нажата, то buttonState будет HIGH:
  if (bState == HIGH) {   
    // включаем мотор
   // и меняем частоту
   SetPinFrequency(mPin, 1200);
   delay(500);
   
   SetPinFrequency(mPin, 1400);
   delay(500);
  
   SetPinFrequency(mPin, 1600);
   delay(500);
   
   SetPinFrequency(mPin, f);
   delay(500);
   
   //  выключаем мотор
    digitalWrite(mPin, LOW);
  }
  else {
    // не включаем мотор
    digitalWrite(mPin, LOW);
  }
}
