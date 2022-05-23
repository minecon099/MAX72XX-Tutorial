# MAX72XX-Tutorial
*A small tutorial to learn how to use your Matrix 72XX LED Screen, made by a beginner lol.*

## What the hell is an Arduino, and what is Matrix 72XX?
**The Arduino**
- So first things first, an Arduino (for my definition) is a super complex circuits board with a ton of addons, and I'm not kidding with the ton of addons at all. It's supposed to be oriented to literally anything including temperature measurement, to home security devices, to cash registers, to more stuff (again, not kidding. The amount of stuff you can do with Arduinos is stupidly high). And in this repository, I'll showcase the basics of using a MAX72XX LED Display.

**The Matrix72XX**
- The Matrix 72XX is essentialy a 8x8 LED display, it comes in that size and another one with the size of 8x32, no more, no less. You can connect more display by using a cable called "Female to Female" so you can nest more than a single 8x8 or 8x32 display and make it wider, but it's not available to make itself more higher than it's current height (8 leds) which is sad :(
- Am I going to use LedControl.h? Nope, it's a terrible documentation page and poorly desgined, instead I decided to rely on a much easier to learn option. Extracted from the site [Makerguides.com](https://www.makerguides.com/max7219-led-dot-matrix-display-arduino-tutorial/#types) I've decided to use the libraries MD_Parola.h, MD_72XX.h and SPI.h (We'll talk about the last one in the tutorial) that simplify the work of writing scrolling text and has animations support.

- [Check out MD_Parola's Github Repository!](https://github.com/MajicDesigns/MD_Parola) 
- [Check out MD_72XX's Github Repository too!](https://github.com/MajicDesigns/MD_MAX72xx)
- Couldn't find SPI.h's repo soo...

## So what will I need? - And what will I learn?
**Ingredients: **
- C++ previous knowledge, because experience is key for mastery at dominating this libraries
- 1x Arduino UNO (Preferred model, that's the one I'm using and it's the cheapest option for my case lol)
- 1x MAX7219-PCB (That's what we'll be using, even if there are better screens this will be our screen and your best friend in this tutorial)
- 1x Female to Male wire (AKA receptor to emissor wire for me)
- Time. A LOT.

**You'll learn:**
- How to code your MAX7219-PCB to display text
- How to take advantage of Scrolling text to break normal text capacity
- How to create animations in Small and Large displays, such as the basic 8x8 grid and the large 8x32 display

### Update status: https://img.shields.io/github/last-commit/minecon099/MAX72XX-Tutorial
