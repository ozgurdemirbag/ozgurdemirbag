#include <FastLED.h>
#define LED_PIN     2
#define NUM_LEDS    12

int strobo_1 = 30;
int strobo_2 = 80;
int strobo_3 = 50;
int strobo_4 = 100;

int freq_1 = 10;
int freq_2 = 30;
int freq_3 = 100;

int freq_pattern_1 = 40;

CRGB leds[NUM_LEDS];


void setup() {
  FastLED.addLeds<WS2812, LED_PIN, GRB>(leds, NUM_LEDS);
}


void rosso() {
  
  for (int i = 0; i <= 3; i++) {
 //KIRMIZI      
  leds[0]=CRGB (255,0,0);
  leds[1]=CRGB (255,0,0);
  leds[2]=CRGB (255,0,0);
  leds[3]=CRGB (255,0,0);
  
 
  FastLED.show();
  delay(strobo_1);
  
  FastLED.clear ();
  delay(strobo_1);
  
  FastLED.show();
  delay(strobo_1);
  }
}


void bianco()  {

for (int i = 0; i <= 3; i++) {
  //BEYAZ
  leds[4]=CRGB (255,255,255);
  leds[5]=CRGB (255,255,255);
  leds[6]=CRGB (255,255,255);
  leds[7]=CRGB (255,255,255);


  FastLED.show();
  delay(strobo_1);
  
  FastLED.clear ();
  delay(strobo_1);
  
  FastLED.show();
  delay(strobo_1);
  
 } 
}

void blu()  {

for (int i = 0; i <= 3; i++) {
 
  //MAVİ
  leds[8]=CRGB (0,0,255);
  leds[9]=CRGB (0,0,255);
  leds[10]=CRGB (0,0,255);
  leds[11]=CRGB (0,0,255);

  FastLED.show();
  delay(strobo_1);
  
  FastLED.clear ();
  delay(strobo_1);
  
  FastLED.show();
  delay(strobo_1);
  
  }
}

void mix_rwb()  {

for (int i = 0; i <= 6; i++) {

  //KIRMIZI
  leds[0]=CRGB (255,0,0);
  leds[1]=CRGB (255,0,0);
  leds[2]=CRGB (255,0,0);
  leds[3]=CRGB (255,0,0);
  
  //BEYAZ
  leds[4]=CRGB (255,255,255);
  leds[5]=CRGB (255,255,255);
  leds[6]=CRGB (255,255,255);
  leds[7]=CRGB (255,255,255);

  //MAVİ
  leds[8]=CRGB (0,0,255);
  leds[9]=CRGB (0,0,255);
  leds[10]=CRGB (0,0,255);
  leds[11]=CRGB (0,0,255);
  

  FastLED.show();
  delay(strobo_1);
  
  FastLED.clear ();
  delay(strobo_1);
  
  FastLED.show();
  delay(strobo_1);
  
  }
 
}


void mix_rb()  {

for (int i = 0; i <= 3; i++) {

  //KIRMIZI
  leds[0]=CRGB (255,0,0);
  leds[1]=CRGB (255,0,0);
  leds[2]=CRGB (255,0,0);
  leds[3]=CRGB (255,0,0);
  leds[4]=CRGB (255,0,0);
  

  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);

  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);

}

for (int i = 0; i <= 3; i++) {
  
 //MAVİ 
  leds[8]=CRGB (0,0,255);
  leds[9]=CRGB (0,0,255);
  leds[10]=CRGB (0,0,255);
  leds[11]=CRGB (0,0,255);
  
  
  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);

  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);
  
  }
 
}

void mix_rl_lr()  {

 for (int i = 0; i <= 3; i++) {
  
  //KIRMIZI 
  leds[0]=CRGB (255,0,0);
  leds[1]=CRGB (255,0,0);  
  leds[2]=CRGB (255,0,0);


  //MAVİ
  leds[9]=CRGB (0,0,255);
  leds[10]=CRGB (0,0,255);
  leds[11]=CRGB (0,0,255);

  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);
}

 for (int i = 0; i <= 3; i++) {


  //KIRMIZI
  leds[3]=CRGB (255,0,0);
  leds[4]=CRGB (255,0,0);
  leds[5]=CRGB (255,0,0);
  
  //MAVİ
  leds[7]=CRGB (0,0,255);  
  leds[8]=CRGB (0,0,255);
  leds[9]=CRGB (0,0,255);
  
  
  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);

  }
}


void mix_rl_w_lr()  {

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
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);
}

 
 for (int i = 0; i <= 3; i++) {
  
  leds[3]=CRGB::Red;
  leds[4]=CRGB::Red;

  leds[5]=CRGB::Black;
  leds[6]=CRGB::Black;

  leds[7]=CRGB::Blue;
  leds[8]=CRGB::Blue;
 
  FastLED.show();
  delay(strobo_1);
  FastLED.clear ();
  delay(strobo_1);

  }
}

//*
void rosso_static() {  
       
  leds[0]=CRGB (255,0,0);
  leds[1]=CRGB (255,0,0);
  leds[2]=CRGB (255,0,0);
  leds[3]=CRGB (255,0,0);

  FastLED.show();
  delay(strobo_3);
  
  FastLED.clear();
  delay(strobo_3);

}

void bianco_static()  {
 
  leds[4]=CRGB (255,255,255);
  leds[5]=CRGB (255,255,255);
  leds[6]=CRGB (255,255,255);
  leds[7]=CRGB (255,255,255);
  


  FastLED.show();
  delay(strobo_3);
  
  FastLED.clear();
  delay(strobo_3);
    
}


void blu_static()  {

  leds[8]=CRGB (0,0,255);
  leds[9]=CRGB (0,0,255);
  leds[10]=CRGB (0,0,255);
  leds[11]=CRGB (0,0,255);


  FastLED.show();
  delay(strobo_3);
  
  FastLED.clear();
  delay(strobo_3);
  
}


// Pattern 1

void pattern_1()  {

  for (int i = 0; i <= 3; i++) {  
    
    leds[0]=CRGB (255,0,0);
    leds[1]=CRGB (255,0,0);
    leds[2]=CRGB (255,0,0);

    leds[9]=CRGB (0,0,255);
    leds[10]=CRGB (0,0,255);
    leds[11]=CRGB (0,0,255);

    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1);
    }

  for (int i = 0; i <= 3; i++) {
 
    leds[3]=CRGB (255,0,0);
    leds[4]=CRGB (255,0,0);
    leds[5]=CRGB (255,0,0);

    leds[6]=CRGB (0,0,255);
    leds[7]=CRGB (0,0,255);
    leds[8]=CRGB (0,0,255);

  
    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
    }
}


// Pattern 2

void pattern_2()  {

  for (int i = 0; i <= 3; i++) {  
    
    leds[0]=CRGB (255,0,0);
    leds[1]=CRGB (255,0,0);
    leds[2]=CRGB (255,0,0);

    leds[9]=CRGB (0,0,255);
    leds[10]=CRGB (0,0,255);
    leds[11]=CRGB (0,0,255);

    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1);
    }

 
  for (int i = 0; i <= 3; i++) {
  
    leds[3]=CRGB (255,0,0);
    leds[4]=CRGB (255,0,0);
    leds[5]=CRGB (255,0,0);

      
    leds[6]=CRGB (0,0,255);
    leds[7]=CRGB (0,0,255);
    leds[8]=CRGB (0,0,255);

  
    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
    }
   
}



//****************************************************************


void white_blink() {

  for (int i = 0; i <= 3; i++) {
    
    leds[4]=CRGB (255,255,255);
    leds[5]=CRGB (255,255,255);
    leds[6]=CRGB (255,255,255);
    leds[7]=CRGB (255,255,255);
    

    
    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
    
    leds[0]=CRGB (255,255,255);
    leds[1]=CRGB (255,255,255);
    leds[2]=CRGB (255,255,255);
    leds[3]=CRGB (255,255,255);
   
   

    
    leds[8]=CRGB (255,255,255);
    leds[9]=CRGB (255,255,255);
    leds[10]=CRGB (255,255,255);
    leds[11]=CRGB (255,255,255);


    FastLED.show();
    delay(freq_pattern_1);
    FastLED.clear ();
    delay(freq_pattern_1); 
    
  }

}


void loop() {


//--------------------------------------- ADIM 1
rosso();
delay (strobo_2);

blu();
delay(strobo_2);

rosso();
delay (strobo_2);

blu();
delay(strobo_2);

//-------------------------------------- ADIM 2

mix_rwb();
delay(strobo_2);

//-------------------------------------- ADIM 3


//-------------------------------------- ADIM 4

mix_rb();
delay(strobo_2);

//-------------------------------------- ADIM 5

  
  for (int i = 0; i <= 3; i++) {
    mix_rl_lr(); 
   delay(strobo_1);
  }

//-------------------------------------- ADIM 6

bianco();
delay(strobo_2);


//-------------------------------------- ADIM 7

  for (int i = 0; i <= 6; i++) {
    mix_rl_w_lr();
    delay(strobo_1);
  }

//-------------------------------------- ADIM 8


  for (int i = 0; i <= 6; i++) {
    rosso();
    delay (strobo_2);

    blu();
    delay(strobo_2);

    rosso();
    delay (strobo_2);

    blu();
    delay(strobo_2);
  }


//-----------------------------------  ADIM 9

 for (int i = 0; i <= 6; i++) {
    pattern_1();
 }


//------------------------------------ ADIM 10


for (int i = 0; i <= 6; i++) {
    pattern_2();
 }
 
 //----------------------------------- ADIM 11


//white_blink();


//------------------------------------- ADIM 12



     for (int i = 0; i <= 30; i++) {
      
          for (int i = 0; i <= 0; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
      }
      
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 1; i <= 1; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 2; i <= 2; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
        for (int i = 0; i <= 30; i++) {
      
          for (int i = 3; i <= 3; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
        for (int i = 0; i <= 30; i++) {
      
          for (int i = 4; i <= 4; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
        for (int i = 0; i <= 30; i++) {
      
          for (int i = 5; i <= 5; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 6; i <= 6; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 7; i <= 7; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 8; i <= 8; i++) {
          leds[i] = CRGB::Red;
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 9; i <= 9; i++) {
          leds[i] = CRGB::Red;  
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 10; i <= 10; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 11; i <= 11; i++) {
          leds[i] = CRGB::Red;  
          FastLED.show();  
          }
          FastLED.clear ();
     }  
//////////////// <<<<<<<<<<<<

for (int i = 0; i <= 30; i++) {
      
          for (int i = 11; i <= 11; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
      }
      
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 10; i <= 10; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 9; i <= 9; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
        for (int i = 0; i <= 30; i++) {
      
          for (int i = 8; i <= 8; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
        for (int i = 0; i <= 30; i++) {
      
          for (int i = 7; i <= 7; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
        for (int i = 0; i <= 30; i++) {
      
          for (int i = 6; i <= 6; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 5; i <= 5; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 4; i <= 4; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 3; i <= 3; i++) {
          leds[i] = CRGB::Red;
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 2; i <= 2; i++) {
          leds[i] = CRGB::Red;  
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 1; i <= 1; i++) {
          leds[i] = CRGB::Red; 
          FastLED.show();  
          }
          FastLED.clear ();
          
      }
       for (int i = 0; i <= 30; i++) {
      
          for (int i = 0; i <= 0; i++) {
          leds[i] = CRGB::Red;  
          FastLED.show();  
          }
          FastLED.clear ();
     }  



//------------------------------------ ADIM 13
 
white_blink();      
   
for (int i = 0; i <= 6; i++) {


    for (int i = 0; i <= 3; i++) {
      
        for (int i = 12; i >= 0; i--) {
          leds[i] = CRGB::Red; 
          FastLED.show();         
          }

          FastLED.clear ();
     }
      
              
     for (int i = 0; i <= 3; i++) {
      
        for (int i = 0; i <= 12; i++) {
        leds[i] = CRGB::White; 
        FastLED.show();  
        }
        FastLED.clear ();
     }

      for (int i = 0; i <= 3; i++) {
      
          for (int i = 0; i <= 12; i++) {
          leds[i] = CRGB::Blue; 
          FastLED.show();  
          }
          FastLED.clear ();
      }
}


//----------------------------------- ADIM 14

              
}
