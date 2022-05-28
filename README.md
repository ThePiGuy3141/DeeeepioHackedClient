## For v3, use https://hacked-deeeep.glitch.me  

## For v4, read below
### Pt. 1 — Enabling Commands!
> 1. Go to https://beta.deeeep.io

> 2. Open DevTools (yes that's what it's called) by using ctrl/cmd + shift + I (that's an i not an L)

> 3. At the top, go to the sources tab

> 4. Find the index.js file in beta.deeeep.io/assets/index.xxxxx.js

> 5. Look towards the bottom and click the pretty-print button

> 5a. Now you will see 50080-ish lines of code, don't be scared

> 6. Use the "find" function (ctrl/cmd + F) and find "constructor"

> 7. Go to the very last one, 121/121. It should be at line 41672 or somewhere around there give or take 50-100 lines.

> 8. Now click on any one of these line numbers

> 9. Now you will see this. It may look a bit different depending on the line you clicked on. But the line number should turn blue.

> 10. If you look to the right, you will see that this new interesting thing that makes no sense has appeared

### Pt. 2 — Getting the Commands to Work!
> 11. Now that you have the breakpoint thing added, press the play button. Yes, the depio play button. Do not touch random things in DevTools.

> 12. Now it will get stuck here with a message saying "Pause in debugger"

> 13. In DevTools, go to the Console tab

> 14. Put this in the console:
```
window.game = this
```

> 15. You will get a response ~~it will deez nutz you~~

> 16. Press the unpause button in the debug thing that popped-up in step 12. Note that it's the blue button, I REPEAT THE BLUE BUTTON!

> 17. Now there will be 2 outcomes:  
>   a. It shows the evo menu, in this case, proceed on to step 18  
>   b. It returns you to the menu page. Press play again. This time, simply unpause the debugger. DO NOT PASTE THE COMMAND IN STEP 14 INTO THE CONSOLE AGAIN!

> 18. Choose an animal *\*duh\**

### Pt. 3 — ACTUALLY GETTING THE HACKS TO WORK!!!

> 19. There are various hacks you can use, I will list them below. Paste these commands into the console (the thing you used in step 14)

### **HACKS!!**

### **Transparent terrain**

> ### **Ground:**
> ```
> setInterval(function () {
> for (let i = 0; i < game.currentScene.terrainManager.terrains.length; i++) {
>     game.currentScene.terrainManager.terrains[i].alpha = 0.5;
> }
> }, 10);
> ```

> ### **Ceiling (the thing that turns transparent when you go through them)**
> ```
> setInterval(function () {
> game.currentScene.ceilingsContainer.alpha = 0.3
> }, 10);
> ```

### **Infinite zoom**

> ```
> setInterval(function () {
> game.viewport.clampZoom({
>     minWidth: 0,
>     maxWidth: 1e7,
> })
> }, 10);
> ```

### **Anti-ink and anti-darkness (in deep)**

> ```
> setInterval(function () {
>     game.currentScene.terrainManager.shadow.setShadowSize(1000000)
> }, 10);
> ```

### **All in one hacks**

> ```
> setInterval(function () {
> for (let i = 0; i < game.currentScene.terrainManager.terrains.length; i++) {
>     game.currentScene.terrainManager.terrains[i].alpha = 0.5;
> }
> game.currentScene.ceilingsContainer.alpha = 0.3
> game.viewport.clampZoom({
>     minWidth: 0,
>     maxWidth: 1e7,
> })
> game.currentScene.terrainManager.shadow.setShadowSize(1000000)
> }, 10);
> ```
