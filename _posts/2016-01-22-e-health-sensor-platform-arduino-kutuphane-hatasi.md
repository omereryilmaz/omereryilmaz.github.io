---
layout: post
title: e-Health Sensor Platform Arduino Kütüphane Hatası
date: 2016-01-22 01:04
image: ehealth-kutuhane-hatasi.png
comments: true
categories: [Arduino]
---
<span style="color:#000000;">Eğer e-Health Sensör Shild'inizi Arduino ile kullanmaya kalktığınızda aşağıdaki gibi kütüphane dosyalarından kaynaklanan bir hata alırsanız;</span>
<pre class="height-mode:1 height:100 height-unit:1 width-set:true width-mode:1 width:100 width-unit:1 h-align:2 minimize:true lang:default decode:true ">Arduino: 1.6.7 (Windows 10), Board: "Arduino/Genuino Uno"

In file included from C:Program Files (x86)ArduinolibrarieseHealthutils/i2c.h:6:0,

                 from C:Program Files (x86)ArduinolibrarieseHealtheHealth.cpp:41:

C:Program Files (x86)ArduinolibrarieseHealthutils/defs.h:84:0: warning: "PI" redefined [enabled by default]

 #define PI  3.14159265359

 ^

In file included from C:Program Files (x86)ArduinolibrarieseHealtheHealth.h:36:0,

                 from C:Program Files (x86)ArduinolibrarieseHealtheHealth.cpp:33:

C:Program Files (x86)Arduinohardwarearduinoavrcoresarduino/Arduino.h:47:0: note: this is the location of the previous definition

 #define PI 3.1415926535897932384626433832795

 ^

In file included from C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:33:0:

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.h:149:15: error: 'prog_uint8_t' has not been declared

      PROGMEM  prog_uint8_t *array);

               ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.h:149:29: warning: '__progmem__' attribute ignored [-Wattributes]

      PROGMEM  prog_uint8_t *array);

                             ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:41:11: error: 'prog_uint8_t' does not name a type

  PROGMEM  prog_uint8_t eHealthLogo[] = {

           ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:109:10: error: 'prog_uint8_t' does not name a type

 PROGMEM  prog_uint8_t cookingLogo[] = {

          ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp: In member function 'void eHealthDisplayClass::init()':

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:201:21: error: 'eHealthLogo' was not declared in this scope

   image(0,64,128,64,eHealthLogo);

                     ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:204:35: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   writeLCD("www.cooking-hacks.com");  delay(4000);

                                   ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:209:21: error: 'cookingLogo' was not declared in this scope

   image(0,64,128,64,cookingLogo); delay(3000);

                     ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp: In member function 'void eHealthDisplayClass::initValuesScreen()':

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:231:39: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(99, 60); writeLCD("Pose");   delay(100);

                                       ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:232:45: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(1,60); writeLCD("CURRENT DATA");  delay(100);

                                             ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:233:45: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(1, 47); writeLCD("Pulse (bpm)");  delay(100);

                                             ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:234:45: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(1, 35); writeLCD("Conductance");  delay(100);

                                             ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:235:40: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(1, 22); writeLCD("Oxygen");   delay(100);

                                        ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:236:36: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(90, 22); writeLCD("%");    delay(100);

                                    ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:237:44: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(1, 9); writeLCD("Temperature");  delay(100);

                                            ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:238:36: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(105, 9); writeLCD("C");    delay(100);

                                    ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp: In member function 'void eHealthDisplayClass::initECGScreen()':

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:331:38: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(42, 52); writeLCD("ECG");

                                      ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:332:40: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   coordinates(100, 52); writeLCD( "cpm");

                                        ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp: In member function 'void eHealthDisplayClass::initAirFlowScreen()':

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:419:18: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

   writeLCD( "bpm");

                  ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp: In member function 'void eHealthDisplayClass::printAirFlowScreen()':

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:470:21: warning: deprecated conversion from string constant to 'char*' [-Wwrite-strings]

     writeLCD("Apnea");

                     ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp: At global scope:

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:663:20: error: 'prog_uint8_t' has not been declared

           PROGMEM  prog_uint8_t *array)

                    ^

C:Program Files (x86)ArduinolibrarieseHealtheHealthDisplay.cpp:663:34: warning: '__progmem__' attribute ignored [-Wattributes]

           PROGMEM  prog_uint8_t *array)

                                  ^

exit status 1
Error compiling.

  This report would have more information with
  "Show verbose output during compilation"
  enabled in File &gt; Preferences.
</pre>
<span style="color:#000000;">Hatayı gidermek için;</span>
<span style="color:#000000;">"C:Program Files (x86)Arduinolibraries"</span>

<span style="color:#000000;">Klasöründeki "eHealth" kütüphane dosyasının içine girin ve oradaki "eHealthDisplay.h" nin <strong>en üstüne</strong> aşağıdaki kodu ekleyiniz.</span>
<pre class="lang:default decode:true ">#ifndef prog_uint8_t
#define prog_uint8_t const uint8_t
#endif</pre>
<span style="color:#000000;">Yukarıdaki kodu ilgili kütüphanenin en üst kısmına eklemeniz önemli çünkü başka yere eklemeniz durumunda kod yapısını bozacağından elde edeceğiniz değerlerde hatalar meydana gelecektir.</span>

&nbsp;
