# Tertiary Text

> Updated to work with SDK 4.0

### Simple Texting from your Wrist!
Type using your Pebble! Tertiary text presents a solution for a quick and efficient method of entering text using only the Pebble itself. By fully utilizing the three buttons and narrowing down the selection each time, it is possible to hit all twenty-six characters of the alphabet in three button strokes. It looks a little clunky at first, but in almost no time the letters become muscle memory and your speed greatly improves.

### Tertiary Text in Action!
![Tertiary Text in action](https://raw.github.com/vgmoose/tertiary_text/master/docs/peb.gif)

### How to Type
The process may be effective, but it admittedly isn't the most straightforward. Check the animation above to get a better idea of how it functions. Also see the diagram below:

![Diagram](https://raw.github.com/vgmoose/tertiary_text/master/docs/diagram.png)

On the start screen, all 26 letters + the space are shown in three groups of nine, one group corresponding to each button. Selecting the top button then, for example, breaks it down into the group of nine, dividing that one into three groups of three, again one group for each button. The second click will then do the same thing to the selected group, making three groups of one letter each. The third and final click will then select the letter that it corresponds to, and successfully type it!

### Extra characters and symbols
Of course there are more than the 26 lower case letters that need to be typed, and have we not just made use of all the three available buttons? Well, there is something else we can do, despite having a limited number of buttons to work with:

![Holding for more things](https://raw.github.com/vgmoose/tertiary_text/master/docs/pebuse.png)![Holding for more things](https://raw.github.com/vgmoose/tertiary_text/master/docs/pebcaps.png)![Holding for more things](https://raw.github.com/vgmoose/tertiary_text/master/docs/peblow.png)![Holding for more things](https://raw.github.com/vgmoose/tertiary_text/master/docs/pebnum.png)

### API 
Implementing Tertiary text is straightfoward. Simply add the **tertiary_text.h** and **tertiary_text.c** files from the **src** directory to your app's source directory, and add the following code in the file where you want to invoke it:
```C
#include "tertiary_text.h"
```
After this, Tertiary Text can be invoked via a pop-up window by using the following method:
```C
void tertiary_text_prompt( const char* title, TertiaryTextCallback callback, void* extra );
```
It takes a title for the window, as well as a callback as input. The callback function should be of the form:
```C
void(* TertiaryTextCallback)( const char* result, size_t result_length, void* extra );
```

For more detailed information on the API, check out [tertiary_text.h](https://github.com/vgmoose/tertiary_text/blob/master/src/tertiary_text.h). For a very simple example app, check out [main.c](https://github.com/vgmoose/tertiary_text/blob/master/src/main.c). It will log the typed text. More information about logging is available [here](http://developer.getpebble.com/docs/c/group___logging.html).

### Contributing
I'm open to any and all contributions! I very much want Tertiary Text to
become as easy-to-use as possible to allow any Pebble app to integrate their
own keyboard without making a big deal out of it. If you see literally any
change at all, feel free to make a pull request.

### Download
Visit the offical project page [here](http://rickyayoub.com/pebble/) for official Tertiary Text downloads and .pbw files.

### Applications
- [Notification Center](https://play.google.com/store/apps/details?id=com.matejdro.pebblenotificationcenter) by **Matej dro**
- [Pebble Translator](http://pblweb.com/appstore/532000f7237858d2500001b1/) by [**Patrick Balestra**](http://www.patrickbalestra.com/)
- [Pebble Communicator](https://play.google.com/store/apps/details?id=pt.joaopluis.communicator) by **João Luís**
- [1.x] [Pebble Messenger](http://forums.getpebble.com/discussion/7954/android-pebble-messenger-whatsapp-sms-quick-responses-typing) by **maveok**
- [1.x] [Formula Calculator](http://forums.getpebble.com/discussion/5285/watch-app-formula-calculator) by **moridh**

### License
Tertiary Text is licensed under the [MIT License](https://github.com/vgmoose/tertiary_text/blob/master/LICENSE.txt).
