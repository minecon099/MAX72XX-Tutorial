# Lesson 1 - Connectin' Pins
## Learn about your display
Quite simple actually, this is a MAX7219, it has an 8x8 LED display of a single color (usually red or blue) and has 5 pins that can be connected into pins for "GROUND", "5V" and more pins (We'll talk about connections later too!) as well as other 5 pins that can be used to connect another 8x8 or 8x32 display which can increase its length (but never it's height sadly), it's last "official" developer used the nowadays outdated library LedControl.h to use your panel. But that's a really old and lame option for our times, so instead we'll be using 3 new libraries (shown later in this tutorial) and we'll be able to use both models for any cassion.

## Connect your display
You may spot that some of you know literally nothing of what you are using, what are those funny letters on the place like "CLK" "CS"... Welp, those pins are they key  booting up your screen and printng messages to! (We'll get to that later).
So, first you need to know which pin belongs to which pin, so grab your female to male wire and follow the next steps:
*Note that we'll use model MAX7219 for this lesson. Both 8x8 and 8x32 models for this display work fine though.*
- Connect pin "5V" to the pin "VCC" of your MAX7219
- Connect pin "GND" (Just below "5V" pin) to the pin "GND" of your MAX7219
- Connect pin "11" (AKA MOSI) to the pin "DIN" of your MAX7219
- Connect pin "3" (AKA "SS") to the pin "CS" of your MAX7219
- Connect pin "13" (AKA "SCK") to the pin "CLK" of your MAX7219

Got it? - You should be able to know with any reaction at all, like your screen's LEDs turning on or something like that, don't worry if you don't get that reaction though, you'll know later on about how do we turn on those.
## Setup your display
Download (preferably) Arduino IDE at it's latest version, you can get it [here](https://www.arduino.cc/en/software) and use preferably the version 1.8 if you want a more stable enviroment.
Then, download the following libraries to make your display work: (You can download them on Tools → Manage Libraries)
- MD_Parola
- MD_MAX72XX (Dependency of MD_Parola)
- SPI (Additional, still required for this tutorial (I think?))

Finally, just include the libraries in your code with the following code:
```cpp
#include <MD_Parola.h>
#include <MD_MAX72XX.h>
#include <SPI.h>
```
And to add your hardware specifications you can type the following code depending on your model:

**For 8x8 model:**
```cpp
#define HARDWARE_TYPE MD_MAX72XX::FC16_HW
#define MAX_DEVICES 1
#define CS_PIN 3
```
**For 8x32 model:**
```cpp
#define HARDWARE_TYPE MD_MAX72XX::FC16_HW
#define MAX_DEVICES 4
#define CS_PIN 3
```
### Yahoo! - You completed Lesson 1! 🎉
