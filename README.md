//--Özgür Demirbağ
//--Ozgur_Led12_2022
//--16/07/2022
//-- This is made for home alarm. Cannot be used outside
//--Bu ev alarmı için yapılmıştır. Dışarıda kullanılamaz

#include <FastLED.h>
#include "colorutils.h"
#include "colorpalettes.h"
#define __INC_COLORPALETTES_H
#define FASTLED_INTERNAL
#define LED_PIN  2
#define NUM_LEDS 12

int strobo_0 = 5;
int strobo_1 = 10;
int strobo_2 = 20;
int strobo_3 = 30;
int strobo_4 = 40;
int strobo_5 = 50;
int strobo_6 = 60;
int strobo_7 = 70;
int strobo_8 = 80;
int strobo_9 = 90;
int strobo_10 = 100;
int strobo_11 = 110;
int strobo_12 = 120;

int freq_1 = 10;
int freq_2 = 30;
int freq_3 = 100;
int freq_pattern_1 = 40;

CRGB leds[NUM_LEDS];

void setup() {
    FastLED.addLeds<WS2812, LED_PIN, GRB>(leds, NUM_LEDS);

}

void S1() { 
for (int i = 0; i <= 11; i++) {     
          leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_10);       
          FastLED.clear ();
} 
         for (int i = 11; i >= 0; i--) {     
          leds[i] = CRGB::Red;
          FastLED.show();
          delay(strobo_10);                 
          FastLED.clear ();
}}  
void S2() {
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[11] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;
          FastLED.show();  
         }
         FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Red;
          leds[9] = CRGB::Blue;
          FastLED.show();  
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Red;
          leds[8] = CRGB::Blue;
          FastLED.show();  
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Red;
          leds[7] = CRGB::Blue;
          FastLED.show();  
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[6] = CRGB::Blue;
          FastLED.show();  
         }
          FastLED.clear (); 
}
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Blue;
          leds[6] = CRGB::Red;
          FastLED.show();  
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Blue;
          leds[7] = CRGB::Red;
          FastLED.show();  
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Blue;
          leds[8] = CRGB::Red;
          FastLED.show();  
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Blue;
          leds[9] = CRGB::Red;
          FastLED.show();  
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[1] = CRGB::Blue;
          leds[10] = CRGB::Red;
          FastLED.show();  
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Blue;
          leds[11] = CRGB::Red;
          FastLED.show();  
         }
          FastLED.clear ();
}}

void S3() { 
     for (int i = 0; i <= 11; i++) {     
          leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_9);       
          FastLED.clear ();
} 
         for (int i = 11; i >= 0; i--) {     
          leds[i] = CRGB::Blue;
          FastLED.show();
          delay(strobo_9);                 
          FastLED.clear ();
}}  
void S4() {
for (int i = 0; i <= 3; i++) {
      
      leds[0]=CRGB::Red;
      leds[1]=CRGB::Red;
      leds[2]=CRGB::Red;
      leds[3]=CRGB::Red;
   
      FastLED.show();
      delay(strobo_3);
  
      FastLED.clear ();
      delay(strobo_3);
  
      FastLED.show();
      delay(strobo_3);
}}

void S5()  {
for (int i = 0; i <= 3; i++) {
 
     leds[4]=CRGB::White;
     leds[5]=CRGB::White;
     leds[6]=CRGB::White;
     leds[7]=CRGB::White;

     FastLED.show();
     delay(strobo_3);
  
     FastLED.clear ();
     delay(strobo_3);
  
     FastLED.show();
     delay(strobo_3);  
}}
void S6()  {
for (int i = 0; i <= 3; i++) {
 
     leds[8]=CRGB::Blue;
     leds[9]=CRGB::Blue;
     leds[10]=CRGB::Blue;
     leds[11]=CRGB::Blue;

    FastLED.show();
    delay(strobo_3);
  
    FastLED.clear ();
    delay(strobo_3);
  
    FastLED.show();
    delay(strobo_3);
  
}}
void S7()  {
for (int i = 0; i <= 6; i++) {
 
    leds[0]=CRGB::Red;
    leds[1]=CRGB::Red;
    leds[2]=CRGB::Red;
    leds[3]=CRGB::Red;
 
    leds[4]=CRGB::White;
    leds[5]=CRGB::White;
    leds[6]=CRGB::White;
    leds[7]=CRGB::White;

    leds[8]=CRGB::Blue;
    leds[9]=CRGB::Blue;
    leds[10]=CRGB::Blue;
    leds[11]=CRGB::Blue;
  
    FastLED.show();
    delay(strobo_3);
  
    FastLED.clear ();
    delay(strobo_3);
  
    FastLED.show();
    delay(strobo_3);  
}}
void S8()  {
for (int i = 0; i <= 3; i++) {

  leds[0]=CRGB::Red;
  leds[1]=CRGB::Red;
  leds[2]=CRGB::Red;
  leds[3]=CRGB::Red;
  leds[4]=CRGB::Red;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
  
}
for (int i = 0; i <= 3; i++) {  

  leds[7]=CRGB::Blue;
  leds[8]=CRGB::Blue;
  leds[9]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[11]=CRGB::Blue;
    
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 

///////////
}
for (int i = 0; i <= 3; i++) {  

  leds[4]=CRGB::White;
  leds[5]=CRGB::White;
  leds[6]=CRGB::White;
  leds[7]=CRGB::White;
 
    
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 

//////////////

  
}}
void S9()  {
for (int i = 0; i <= 3; i++) { 

  leds[0]=CRGB::Red;
  leds[1]=CRGB::Red;  
  leds[2]=CRGB::Red;

  leds[9]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[11]=CRGB::Blue;

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
}
 for (int i = 0; i <= 3; i++) {

  leds[3]=CRGB::Red;
  leds[4]=CRGB::Red;
  leds[5]=CRGB::Red;
  
  leds[7]=CRGB::Blue;  
  leds[8]=CRGB::Blue;
  leds[9]=CRGB::Blue;
   
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
}}

void S10()  {
for (int i = 0; i <= 3; i++) {
  
  leds[0]=CRGB::Red;
  leds[1]=CRGB::Red;
  leds[2]=CRGB::Red;
  
  leds[5]=CRGB::White;
  leds[6]=CRGB::White;

  leds[9]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[11]=CRGB::Blue;

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
}

 for (int i = 0; i <= 3; i++) {
  
  leds[3]=CRGB::Red;
  leds[4]=CRGB::Red;

  leds[5]=CRGB::Black;
  leds[6]=CRGB::Black;

  leds[7]=CRGB::Blue;
  leds[8]=CRGB::Blue;
 
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
}}
void KIRMIZI_static() {  
       
  leds[0]=CRGB::Red;
  leds[1]=CRGB::Red;
  leds[2]=CRGB::Red;
  leds[3]=CRGB::Red;

  FastLED.show();
  delay(strobo_5);
  
  FastLED.clear();
  delay(strobo_5);
}

void BEYAZ_static()  {
 
  leds[4]=CRGB::White;
  leds[5]=CRGB::White;
  leds[6]=CRGB::White;
  leds[7]=CRGB::White;
  
  FastLED.show();
  delay(strobo_5);
  
  FastLED.clear();
  delay(strobo_5);    
}

void MAVI_static()  {

  leds[8]=CRGB::Blue;
  leds[9]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[11]=CRGB::Blue;

  FastLED.show();
  delay(strobo_5);
  
  FastLED.clear();
  delay(strobo_5);   
}

void pattern_1()  {
for (int i = 0; i <= 3; i++) {  
    
    leds[0]=CRGB::Red;
    leds[1]=CRGB::Red;
    leds[2]=CRGB::Red;

    leds[9]=CRGB::Blue;
    leds[10]=CRGB::Blue;
    leds[11]=CRGB::Blue;

    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1);
}

for (int i = 0; i <= 3; i++) {
 
    leds[3]=CRGB::Red;
    leds[4]=CRGB::Red;
    leds[5]=CRGB::Red;

    leds[6]=CRGB::Blue;
    leds[7]=CRGB::Blue;
    leds[8]=CRGB::Blue;

    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
}}

void pattern_2()  {
  for (int i = 0; i <= 3; i++) {  
    
    leds[0]=CRGB::Red;
    leds[1]=CRGB::Red;
    leds[2]=CRGB::Red;

    leds[9]=CRGB::Blue;
    leds[10]=CRGB::Blue;
    leds[11]=CRGB::Blue;

    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1);
}

  for (int i = 0; i <= 3; i++) {
  
    leds[3]=CRGB::Red;
    leds[4]=CRGB::Red;
    leds[5]=CRGB::Red;
     
    leds[6]=CRGB::Blue;
    leds[7]=CRGB::Blue;
    leds[8]=CRGB::Blue;
  
    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
}}

void white_blink() {
for (int i = 0; i <= 3; i++) {
    
    leds[4]=CRGB::White;
    leds[5]=CRGB::White;
    leds[6]=CRGB::White;
    leds[7]=CRGB::White;
        
    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
    
    leds[0]=CRGB::White;
    leds[1]=CRGB::White;
    leds[2]=CRGB::White;
    leds[3]=CRGB::White;
       
    leds[8]=CRGB::White;
    leds[9]=CRGB::White;
    leds[10]=CRGB::White;
    leds[11]=CRGB::White;

    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1);     
}}

void S11() {
for (int i = 0; i <= 3; i++) {

  leds[0]=CRGB::Red;
  leds[1]=CRGB::Red;
  leds[2]=CRGB::Red;
  leds[3]=CRGB::Red;
  leds[4]=CRGB::Red;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
  
}
for (int i = 0; i <= 3; i++) {  

  leds[7]=CRGB::Blue;
  leds[8]=CRGB::Blue;
  leds[9]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[11]=CRGB::Blue;
    
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);
  }
for (int i = 0; i <= 3; i++) { 
  //leds[0]=CRGB::White;
  leds[5]=CRGB::White;
  leds[6]=CRGB::White;
  //leds[11]=CRGB::White;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 

}}

void S12() {
for (int i = 0; i <= 11; i++) {     
          leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
} 
         for (int i = 11; i >= 0; i--) {     
          leds[i] = CRGB::White;
          FastLED.show();
          delay(strobo_12);                 
          FastLED.clear ();
}}
void S13() {
for (int i = 0; i <= 3; i++) {
 
  leds[0]=CRGB::Yellow; 
  leds[1]=CRGB::Yellow; 
  leds[2]=CRGB::Yellow; 
  leds[3]=CRGB::Yellow; 
  leds[4]=CRGB::Yellow;
  
  FastLED.show();
  delay(strobo_5);
  FastLED.clear ();
  delay(strobo_5);

  FastLED.show();
  delay(strobo_5);
  FastLED.clear ();
  delay(strobo_5);  
}
for (int i = 0; i <= 3; i++) {  
  
  leds[7]=CRGB::Blue;
  leds[8]=CRGB::Blue;
  leds[9]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[11]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_5);
  FastLED.clear ();
  delay(strobo_5);

  FastLED.show();
  delay(strobo_5);
  FastLED.clear ();
  delay(strobo_5); 
  
 }
for (int i = 0; i <= 3; i++) { 
  leds[5]=CRGB::Red;
  leds[6]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_5);
  FastLED.clear ();
  delay(strobo_5);

  FastLED.show();
  delay(strobo_5);
  FastLED.clear ();
  delay(strobo_5);   

}}
void S14() {
for (int i = 0; i <= 11; i++) {     
          leds[i] = CRGB::Yellow;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
      } 
         for (int i = 11; i >= 0; i--) {     
          leds[i] = CRGB::Blue;
          FastLED.show();
          delay(strobo_12);                 
          FastLED.clear ();
}}
void S15 () {
for (int i = 0; i <= 11; i++) {
          leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_6);                
}          
for (int i = 0; i <= 11; i++) {
          leds[i] = CRGB::DarkRed;
          FastLED.show();  
          delay(strobo_6);                
}     
for (int i = 0; i <= 11; i++) {     
          leds[i] = CRGB::Blue;
          FastLED.show();  
          delay(strobo_6);               
}    
for (int i = 0; i <= 11; i++) {     
          leds[i] = CRGB::DarkBlue;
          FastLED.show();  
          delay(strobo_6);               
}
for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::White;
          FastLED.show();  
          delay(strobo_6);                 
}  
for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_6);                 
}      
          for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::DarkRed;
          FastLED.show();  
          delay(strobo_6);               
}
for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::White;
          FastLED.show();  
          delay(strobo_6);                 
}
  for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_6);                
} 
for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::Blue;
          FastLED.show();  
          delay(strobo_6); 

} 
for (int i = 0; i <=11 ; i++) {     
          leds[i] = CRGB::Orange;
          FastLED.show();  
          delay(strobo_6); 

}}
void S16 () {
for (int i = 0; i <= 3; i++) { 
  leds[0]=CRGB::Blue;
  leds[1]=CRGB::Red;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}
for (int i = 0; i <= 3; i++) { 
  leds[11]=CRGB::Blue;
  leds[10]=CRGB::Red;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}
for (int i = 0; i <= 3; i++) { 
  leds[2]=CRGB::Red;
  leds[3]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}
for (int i = 0; i <= 3; i++) { 
  leds[9]=CRGB::Red;
  leds[8]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 

} 
for (int i = 0; i <= 3; i++) { 
  leds[4]=CRGB::Red;
  leds[5]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}
for (int i = 0; i <= 3; i++) { 
  leds[7]=CRGB::Red;
  leds[6]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}}

void S17 () {
  
for (int i = 0; i <= 3; i++) { 
  leds[0]=CRGB::Red;
  leds[1]=CRGB::Red;
  leds[2]=CRGB::Red;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}
for (int i = 0; i <= 3; i++) { 
  leds[11]=CRGB::Blue;
  leds[10]=CRGB::Blue;
  leds[9]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}

  for (int i = 0; i <= 3; i++) { 
  leds[3]=CRGB::Red;
  leds[4]=CRGB::Red;
  leds[5]=CRGB::Red;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 
}
for (int i = 0; i <= 3; i++) { 
  leds[6]=CRGB::Blue;
  leds[7]=CRGB::Blue;
  leds[8]=CRGB::Blue;
  
  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3);

  FastLED.show();
  delay(strobo_3);
  FastLED.clear ();
  delay(strobo_3); 

}}
void S18 () {
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[11] = CRGB::Blue;
          FastLED.show();  
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;
          FastLED.show();  
         }
         FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Red;
          leds[9] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Red;
          leds[8] = CRGB::Blue;
          FastLED.show();  
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Red;
          leds[7] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[6] = CRGB::Blue;
          FastLED.show();  
         }
          FastLED.clear (); 
}

for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::White;
          leds[6] = CRGB::White;
          FastLED.show();
}
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Red;
          leds[7] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Red;
          leds[8] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Red;
          leds[9] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;
          FastLED.show();  
}
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[11] = CRGB::Blue;
          FastLED.show();  
         }
          FastLED.clear ();
}}

void S19 () {
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[11] = CRGB::Blue;

    FastLED.show();
    delay(strobo_2);
    }  
    FastLED.clear ();
    delay(strobo_2);

    FastLED.show();
    delay(strobo_2);

}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;

    FastLED.show();
    delay(strobo_2);
    }  
    FastLED.clear ();
    delay(strobo_2);

    FastLED.show();
    delay(strobo_2);
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Red;
          leds[9] = CRGB::Blue;

    FastLED.show();
    delay(strobo_2);
    }  
    FastLED.clear ();
    delay(strobo_2);

    FastLED.show();
    delay(strobo_2);
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Red;
          leds[8] = CRGB::Blue;

    FastLED.show();
    delay(strobo_2);
    }  
    FastLED.clear ();
    delay(strobo_2);

    FastLED.show();
    delay(strobo_2);
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Red;
          leds[7] = CRGB::Blue;

    FastLED.show();
    delay(strobo_2);
    }  
    FastLED.clear ();
    delay(strobo_2);

    FastLED.show();
    delay(strobo_2);
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[6] = CRGB::Blue;
          
    FastLED.show();
    delay(strobo_2);
    }  
    FastLED.clear ();
    delay(strobo_2);

    FastLED.show();
    delay(strobo_2); 
}
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[6] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);   
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Red;
          leds[7] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);    
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Red;
          leds[8] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);  
          }
           FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Red;
          leds[9] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);   
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);    
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[11] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);   
         }
          FastLED.clear ();             
}}

void S20 () {
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[11] = CRGB::Blue;

    FastLED.show();
    delay(strobo_0);
    }  
    FastLED.clear ();
    delay(strobo_0);

    FastLED.show();
    delay(strobo_0);

}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[0] = CRGB::Red;
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;
          leds[11] = CRGB::Blue;

    FastLED.show();
    delay(strobo_0);
    }  
    FastLED.clear ();
    delay(strobo_0);

    FastLED.show();
    delay(strobo_0);
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[2] = CRGB::Red;
          leds[1] = CRGB::Red;
          leds[0] = CRGB::Red;
          leds[9] = CRGB::Blue;
          leds[10] = CRGB::Blue;
          leds[11] = CRGB::Blue;
          
    FastLED.show();
    delay(strobo_0);
    }  
    FastLED.clear ();
    delay(strobo_0);

    FastLED.show();
    delay(strobo_0);
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[3] = CRGB::Red;
          leds[2] = CRGB::Red;
          leds[1] = CRGB::Red;
          leds[0] = CRGB::Red;
          leds[8] = CRGB::Blue;
          leds[9] = CRGB::Blue;
          leds[10] = CRGB::Blue;
          leds[11] = CRGB::Blue;

    FastLED.show();
    delay(strobo_0);
    }  
    FastLED.clear ();
    delay(strobo_0);

    FastLED.show();
    delay(strobo_0);
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[4] = CRGB::Red;
          leds[3] = CRGB::Red;
          leds[2] = CRGB::Red;
          leds[1] = CRGB::Red;
          leds[0] = CRGB::Red;
          leds[7] = CRGB::Blue;
          leds[8] = CRGB::Blue;
          leds[9] = CRGB::Blue;
          leds[10] = CRGB::Blue;
          leds[11] = CRGB::Blue;

    FastLED.show();
    delay(strobo_0);
    }  
    FastLED.clear ();
    delay(strobo_0);

    FastLED.show();
    delay(strobo_0);
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[4] = CRGB::Red;
          leds[3] = CRGB::Red;
          leds[2] = CRGB::Red;
          leds[1] = CRGB::Red;
          leds[0] = CRGB::Red;
          leds[6] = CRGB::Blue;
          leds[7] = CRGB::Blue;
          leds[8] = CRGB::Blue;
          leds[9] = CRGB::Blue;
          leds[10] = CRGB::Blue;
          leds[11] = CRGB::Blue;
          
    FastLED.show();
    delay(strobo_0);
    }  
    FastLED.clear ();
    delay(strobo_0);

    FastLED.show();
    delay(strobo_0); 

}
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[6] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);   
          }
          FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[4] = CRGB::Red;        
          leds[6] = CRGB::Blue;
          leds[7] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);    
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[4] = CRGB::Red;
          leds[3] = CRGB::Red;
          leds[8] = CRGB::Blue;
          leds[7] = CRGB::Blue;
          leds[6] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);  
          }
           FastLED.clear ();
}    
for (int i = 0; i <= 5; i++) {     
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[4] = CRGB::Red;
          leds[3] = CRGB::Red;
          leds[2] = CRGB::Red;
          leds[9] = CRGB::Blue;
          leds[8] = CRGB::Blue;
          leds[7] = CRGB::Blue;
          leds[6] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);   
         }
          FastLED.clear ();
}     
for (int i = 0; i <= 5; i++) {
for (int i = 0; i <= 11; i++) {
          leds[5] = CRGB::Red;
          leds[4] = CRGB::Red;
          leds[3] = CRGB::Red;
          leds[2] = CRGB::Red;
          leds[1] = CRGB::Red;
          leds[10] = CRGB::Blue;
          leds[9] = CRGB::Blue;
          leds[8] = CRGB::Blue;
          leds[7] = CRGB::Blue;
          leds[6] = CRGB::Blue;
          FastLED.show();
          delay(strobo_1);    
          }
          FastLED.clear ();  

}}

void S21 () {

for (int i = 0; i <= 11; i++) {  
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
FastLED.show();   
}
for (int i = 0; i <= 10; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 9; i++) {  
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 8; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
          FastLED.show(); 
}
for (int i = 0; i <= 7; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
         FastLED.show(); 
}
for (int i = 0; i <= 6; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 5; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
leds[5]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 4; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
leds[5]=CRGB::Red;
leds[4]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 3; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
leds[5]=CRGB::Red;
leds[4]=CRGB::Red;
leds[3]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 2; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
leds[5]=CRGB::Red;
leds[4]=CRGB::Red;
leds[3]=CRGB::Red;
leds[2]=CRGB::Red;     
       FastLED.show();      
}      
for (int i = 0; i <= 1; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
leds[5]=CRGB::Red;
leds[4]=CRGB::Red;
leds[3]=CRGB::Red;
leds[2]=CRGB::Red;
leds[1]=CRGB::Red;
       FastLED.show(); 
}
for (int i = 0; i <= 0; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Red;
leds[10]=CRGB::Red;
leds[9]=CRGB::Red;
leds[8]=CRGB::Red;
leds[7]=CRGB::Red;
leds[6]=CRGB::Red;
leds[5]=CRGB::Red;
leds[4]=CRGB::Red;
leds[3]=CRGB::Red;
leds[2]=CRGB::Red;
leds[1]=CRGB::Red;
leds[0]=CRGB::Red;
       FastLED.show(); 
       
}}

void S22 () {
for (int i = 0; i <= 11; i++) {  
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
 FastLED.show();
}
for (int i = 0; i <= 10; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
    FastLED.show();
}
for (int i = 0; i <= 9; i++) {  
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
    FastLED.show();
}
for (int i = 0; i <= 8; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
    FastLED.show(); 
}
for (int i = 0; i <= 7; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
    FastLED.show();

}
for (int i = 0; i <= 6; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
    FastLED.show();
 
}
for (int i = 0; i <= 5; i++) {   
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
leds[5]=CRGB::Blue;
    FastLED.show();
}
for (int i = 0; i <= 4; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
leds[5]=CRGB::Blue;
leds[4]=CRGB::Blue;
    FastLED.show();
}
for (int i = 0; i <= 3; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
leds[5]=CRGB::Blue;
leds[4]=CRGB::Blue;
leds[3]=CRGB::Blue;
    FastLED.show();
 
}
for (int i = 0; i <= 2; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
leds[5]=CRGB::Blue;
leds[4]=CRGB::Blue;
leds[3]=CRGB::Blue;
leds[2]=CRGB::Blue;     
    FastLED.show();
      
}      
for (int i = 0; i <= 1; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
leds[5]=CRGB::Blue;
leds[4]=CRGB::Blue;
leds[3]=CRGB::Blue;
leds[2]=CRGB::Blue;
leds[1]=CRGB::Blue;
    FastLED.show();

}
for (int i = 0; i <= 0; i++) {
leds[i] = CRGB::Red;
          FastLED.show();  
          delay(strobo_12);       
          FastLED.clear ();
          
leds[11]=CRGB::Blue;
leds[10]=CRGB::Blue;
leds[9]=CRGB::Blue;
leds[8]=CRGB::Blue;
leds[7]=CRGB::Blue;
leds[6]=CRGB::Blue;
leds[5]=CRGB::Blue;
leds[4]=CRGB::Blue;
leds[3]=CRGB::Blue;
leds[2]=CRGB::Blue;
leds[1]=CRGB::Blue;
leds[0]=CRGB::Blue;
    FastLED.show();

/////////////////////////////////////////////////////////////////
                                  
}}

void loop() {
//---------------------------------------

S1();////0-11 KIRMIZI YÜRÜR
delay (strobo_12);
//---------------------------------------

S1();
delay (strobo_12);
//---------------------------------------

S2();////0-11 KIRMIZI YANARKEN GERİYE DOĞRU 11-0 MAVİ YANAR
delay (strobo_12);
//---------------------------------------

S2();
delay (strobo_12);
//---------------------------------------

S3();////0-11 KIRMIZI SONRA 11-0 MAVİ YÜRÜR
delay (strobo_9);
//---------------------------------------

S4();////0-3  KIRMIZI
delay(strobo_8);
//---------------------------------------

S6();////11-8  MAVİ
delay (strobo_8);
//---------------------------------------

S5();////4-7 BEYAZ
delay (strobo_8);
//---------------------------------------

S4();////0-3  KIRMIZI
delay (strobo_8);
//---------------------------------------

S5();////4-7 BEYAZ
delay (strobo_8);
//---------------------------------------

S6();////11-8  MAVİ
delay (strobo_8);
///---------------------------------------

S7();////0-3 KIRMIZI  4-7 BEYAZ  8-11 MAVİ
delay (strobo_8);
//---------------------------------------

S8();////0-3 KIRMIZI  4-7 MAVİ  8-11 BEYAZ
delay (strobo_8);
//---------------------------------------

for (int i = 0; i <= 3; i++) {
S9(); ////0-3 KIRMIZI  9-11 MAVİ -- 3-5 KIRMIZI 7-9 MAVİ
delay (strobo_3);}
//---------------------------------------

for (int i = 0; i <= 6; i++) {
S10();////0-3 KIRMIZI 5-6 BEYAZ 9-11 MAVİ   -- 3-4 KIRMIZI 7-8 MAVİ
delay(strobo_3);}
//---------------------------------------

for (int i = 0; i <= 6; i++) {
S4();////0-3  KIRMIZI
delay (strobo_8);
//---------------------------------------

S6();////11-8  MAVİ
delay (strobo_8);
//---------------------------------------

S4();////0-3  KIRMIZI
delay (strobo_8);
//---------------------------------------

S6();////11-8  MAVİ
delay (strobo_8);}
//---------------------------------------

for (int i = 0; i <= 6; i++) {
pattern_1();}
//---------------------------------------

for (int i = 0; i <= 6; i++) {
pattern_2();}
//---------------------------------------

white_blink();////4-7 BEYAZ 0-3 BEYAZ 8-11 BEYAZ
//---------------------------------------

S11();////0-4 KIRMIZI 7-11 MAVİ 5-6 BEYAZ
delay (strobo_3);
//---------------------------------------

S12();//// 0-11 KIRMIZI YÜRÜR SONRA 11-0 BEYAZ
delay (strobo_10);
//---------------------------------------

S13();////0-4 KIRMIZI 7-11 MAVİ  5 KIRMIZI 6 MAVİ 
delay (strobo_5);
//---------------------------------------

S14();//// 0-11 YEŞİL YÜRÜR SONRA 11-0 MAVİ
delay (strobo_12);
//--------------------------------------- 

S15();///0-11 YÜRÜYEN RENKLER
//---------------------------------------
 
S16();//// İKİLİ ÇAKAR
delay (strobo_3);
//---------------------------------------

S17();//// ÜÇLÜ ÇAKAR
delay (strobo_3);
//--------------------------------------- 

S18();//// 0-5 KIRMIZI YÜRÜR SONRA 6-11 MAVİ KARŞILIKLI
delay (strobo_3);
//---------------------------------------

S19();//// 0-5 KIRMIZI 6-11 MAVİ YAVAŞ GELİR HIZLI GERİ DÖNER 
delay (strobo_3);
//----------------------------------------

S20();//// 0-5 KIRMIZI 6-11 MAVİ YAVAŞ GELİR YAVAŞ DÖNER
//----------------------------------------

S21();//// 0-11 ARASI KIRMIZI YÜRÜR 11 DEN 0 A KADAR KIRMIZI SIRALI BEKLER
//----------------------------------------

S22();////0-11 ARASI KIRMIZI YÜRÜR 11 DEN 0 A KADAR MAVİ SIRALI BEKLER
//----------------------------------------

white_blink();        
for (int i = 0; i <= 6; i++) {
for (int i = 0; i <= 3; i++) {      
for (int i = 11; i >= 0; i--) {
          leds[i] = CRGB::Red; 
          FastLED.show();         
}
          FastLED.clear ();
}                 
for (int i = 0; i <= 3; i++) {     
        for (int i = 0; i <= 11; i++) {
        leds[i] = CRGB::White; 
        FastLED.show();  
}
        FastLED.clear ();
}
for (int i = 0; i <= 3; i++) {      
         for (int i = 0; i <= 11; i++) {
         leds[i] = CRGB::Blue; 
         FastLED.show();  
}
         FastLED.clear ();     
}
for (int i = 0; i <= 3; i++) {     
          for (int i = 0; i <= 11; i++) {
          leds[i] = CRGB::Yellow; 
          FastLED.show();  
}
          FastLED.clear ();
}
for (int i = 0; i <= 3; i++) {     
          for (int i = 0; i <= 11; i++) {
          leds[i] = CRGB::Green; 
          FastLED.show();  
}
          FastLED.clear ();                     
          }}}
