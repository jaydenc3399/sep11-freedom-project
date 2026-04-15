# Entry 5
### 4/13/26

# Content 
From the last blog entry that I have done I was still in the process of learning. Now over the break and a little before I took some time to learn my tool because I saw my friend Edward ffor his background he was using kaboom also. He had this cool background that he created using kaboom. I then asked him where and how he got that and I went onto the kaboom website and he showed me it. This was called [add level](https://kaboomjs.com/#addLevel). It was bascailly just creating a background itself and naming certain signs in the map for a certain shape or something. I didnt really learn how to do this first so I just went straight to test it out on my project. I used  "^": () => [rect(48,16), area(), color(255,0,0). And this on my page appeared with a rectangle with a certain width. I used there example as my guide to create my map. 
```"                          $",
    "                          $",
    "           $$         =   $",
    "  %      ====         =   $",
    "                      =    ",
    "       ^^      = >    =   &",
    "===========================",
```
This was the map they gave where the $, % and ^^ all corresponded to like a specific thing when you use http-server. I started to like think about this in plain english first like symbols are equal to whatever code I make them like rectangles or anything. I could use this for my map in my game, before I actually put this on my game I went online to search for some websites where people didn't and a place where I could learn and like double check. I foudn this pdf online (https://i.ritzastatic.com/makejavascriptgamesbook/e-books/make-javascript-games-book.pdf) [add level pdf] where it was bascially like a manual to create a game with multiple componenets and I found `add level` in it. After learning and reading these examples I looked on github and some online sites for more examples like on (https://gist.github.com/VictorCabello/940c11251a4e55387ab63bb96ab57010) [git hub]. I took all this knwoedge I learned and then went to code on my website with it. I first went to pick code and made something random for now and it looked like this:
```js
addLevel(map, {
  tileWidth: 32,
  tileHeight: 32,

  tiles: {
    "=": () => [
      rect(32, 32),
      color(100, 100, 255),
    ],

    "#": () => [
      rect(32, 32),
      color(150, 75, 0),
    ],

    "@": () => [
      rect(32, 32),
      color(0, 255, 0),
     
    ],

   
  },
})
```

---


This was the like key in a map where I made it correspond to something on the map. It looked like this: 

---

```js
const map = [
  "========================",
  "=                      =",
  "=         ###          =",
  "=        #####         =",
  "=       #######        =",
  "=        #####         =",
  "=         ###          =",
  "=          @           =",
  "=                      =",
  "========================",
]
```

---

### I later used this on my freedom project to create my map which was this 
```js 
 addLevel([
            "                                                                                ",
            "    ====                                                                ====    ",
            "    ==                              $$                                  ==      ",
            "    ====                $$          ^^          $$                      ====    ",
            "                      ======      ======      ======                            ",
            "                                                                                ",
            "            ====                                            ====                ",
            "            ====            ^^              ^^              ====                ",
            "    ============      ==============================      ============          ",
            "    ====        ====  ====                      ====  ====        ====    f     ",
            "================================      ==========================================",
        ], {
```

---
* // "=" is a solid wall
* // "$" defines a dot where it will explode to sparkles when stepped on
* // "^" defines a red obstacle (the laser)
* // "f" defines the blue finish flag (Only appears in Solo Mode)

----

I used this for my game the map, this was not the only thing I practiced, I worked on like a more key basic componemt of kaboom but I felt I didnt really get to fully understand it so I went on kaboom website to check `onKeypress` which we kind of learned in class but I wanted like a sort of review. [kaboom onkeypress](https://kaboomjs.com/#onKeyPress) I took some examples from their webite

```js
onKeyPress(() => {
    restart()
})
```

I took this code and I tried to apply it to my own game, like pressing c to restart the game and then use x as like a super power. I might jsut make the superpower a cool effect and thats it, wont do anythign besides intimidation. I then added this onto my code after thinking for a ltitle bit. 

```js
onKeyPress("r", () => {
    go("game");
});
```
I added this to when I started my game with the `go(game)` which bascially jsut restarts my game when the user clicks r and it worked perfectly. After this I tried to add a specila effect using onKeyPress and it turned out like this 
```js
onKeyPress("s", () => {
    sparkle(vec2(rand(100, 540), rand(100, 380)));
});
```
With this I created a code where When I clck s theres a special effect. This was used for my tinkering on pickcode and I later applied this onto my MVP where I made my sprite jump and move using WASD and arrow keys and shooting bullets using S.
```js
onKeyPress(s, () => { // Shoot
                if(gameActive == false) return;
                let dir = LEFT;
                if(p.is("mouse") == true) { dir = RIGHT; }
                add([rect(20,10), pos(p.pos.add(20,20)), color(bCol), area(), move(dir, 1100), "bullet", {target}]);
            });
```

---

This was the code for my freedom project where if they clicked s it would shoot but for the walking commands and jump I used `bind` which I found online and it allows users to customize how terminal keys and keyboard shortcuts behave. I applied this to my W, A and D command and for for X also.

```js
bind(p1, "a", "d", "w", "x",
if(p2) bind(p2, "left", "right", "up", "n", [255,0,0], "mouse");
```
It just connects the keys bascially and links them to my mouse sprite that I have. These were the main things I learned on my learning log and applied to my freedom project MVP. 

---

# Engineering Design Process
Right now on the engineering design process I am on the step where I created the prototype which is my MVP and 




[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
