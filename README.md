LED Library - Arduino RGB LED Library
==================================================

Contribution
--------------------------------------

In the spirit of open source software development, please consider contributing to this Library.


Installation
--------------------------------------

1. Copy the source code to `\Arduino\arduino-1.0\libraries\LED`
2. Include the Library Header `#include <LED.h>` in your sketch.
3. Define your Pins `int LEDArray[] = {11,8,9};` First one is RED, Green, Blue.
4. Make your first LED Object `LED LED1(LEDArray);`



Blink
----------------------------
`````
#include <LED.h>

int LEDArray[] = {11,8,9}; // Red, Green, Blue
LED LED1(LEDArray);

void setup() {
}

void loop() {
  byte start_color3[] = {0, 0, 0};
  byte end_color3[] = {0, 255, 255};
  
  // Blink
  LED1.Fade(LEDArray, start_color3 , end_color3, 0); // 0 for no delay
  delay(100);
  LED1.Fade(LEDArray, end_color3 , start_color3, 0); // 0 for no delay
}
`````

Fade
---------------------------------


#include <LED.h>

int LEDArray[] = {11,8,9}; // Red, Green, Blue
LED LED1(LEDArray);

void setup() {
}

void loop() {
  byte start_color3[] = {255, 0, 0};
  byte end_color3[] = {0, 255, 255};
  
  // Blink
  LED1.Fade(LEDArray, start_color3 , end_color3, 5); 
  delay(100);
  LED1.Fade(LEDArray, end_color3 , start_color3, 5);
}



Pulse
---------------


#include <LED.h>

int LEDArray[] = {11,8,9}; // Red, Green, Blue
LED LED1(LEDArray);

void setup() {
}

void loop() {
  byte start_color3[] = {0, 0, 0};
  byte end_color3[] = {0, 255, 255};
  
  // Blink
  LED1.Fade(LEDArray, start_color3 , end_color3, 3); // 3 and 1 = Pulse effect
  delay(100);
  LED1.Fade(LEDArray, end_color3 , start_color3, 1); // 1
}


License
----------

Copyright (c) 2012 Benjamin Wüst
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
