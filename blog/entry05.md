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
This was the map they gave where the $, % and ^^ all corresponded to like a specific thing when you use http-server. I started to like think about this in plain english first like symbols are equal to whatever code I make them like rectangles or anything. I could use this for my map in my game, before I actually put this on my game I went online to search for some websites where people didn't and a place where I could learn and like double check. I foudn this pdf online [add level pdf](https://i.ritzastatic.com/makejavascriptgamesbook/e-books/make-javascript-games-book.pdf) where it was bascially like a manual to create a game with multiple componenets and I found `add level` in it. After learning and reading these examples I looked on github and some online sites for more examples like on [git hub](https://gist.github.com/VictorCabello/940c11251a4e55387ab63bb96ab57010). I took all this knwoedge I learned and then went to code on my website with it. I first went to pick code and made something random for now and it looked like this:
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

I used this for my game the map, this was not the only thing I practiced, I worked on like a more key basic componemt of kaboom but I felt I didnt really get to fully understand it so I went on kaboom website to check `onKeypress` which we kind of learned in class but I wanted like a sort of review. [Kaboom onkeypress](https://kaboomjs.com/#onKeyPress) I took some examples from their webite

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

## How I finished mt MVP 
Over the spring break I started working on my [MVP](https://github.com/jaydenc3399/sep11-freedom-project/blob/main/index.html) kind of late and I sort of had to rush things, there was only around 4 days left to break ends. I used my plan to help guide me but I did tweak soem things from the orignal plan itself and sort of improvised. I first started by uplodaing my sprites using loadSprite and at first the sprite did not load. 

```js
loadSprite("mouse", "mouse.png");
loadSprite("cat", "cat.jpg");
```
THis was my code for my sprites and for some reason even with the correct code this did not work. After being stuck for a while I went online google to ask how can I fix this code of mine and why my sprites were being loaded. It told me that I did not have the src for the kaboom thats why the kaboom `load sprite` did not work so after placing the link. 
```js
 <script src="https://unpkg.com/kaboom@3000.1.17/dist/kaboom.js"></script>
```
The sprites loaded and then I went on to creating my map which was what I was tinkering with above in the lessons. After I set the spawn points for each of the sprites on the map with the specific keys that would correspond to them like WAD for the mouse and arrow keys for the cat and I made them shoot with different keys like x and n. X for the mouse and n for the cat. After I tried to make the map a little more intresting to I added a function if they step on the small tiny yellow dots on the map there would be like a sparkle effect. After this I took a small break and continued after with the health bars and score boards coding it so that when it reaches to three points the game is over. I also coded if one gets hit with another laser they will take damage but there will be a invulnerbility phase after being hit. 

```js
if (mouseMatchPoints >= 3 || catMatchPoints >= 3) {
                    let winMsg = "CAT WINS";
                    if (mouseMatchPoints >= 3) { winMsg = "MOUSE WINS"; }
```
THis was the code I created for the matches if one wins, a conditional. I created two modes for one and where multiplayer you can shoot your friend with the lasers while dodging incoming obstacles but also a solo mode where they can play alone trying to doge obstacles and reach the flag. I sort of did a tom and jerry game in a way with the sprites and just innovated and incoperated differnt things into the freedom project. 

---

# Engineering Design Process
Right now on the engineering design process I am on the step where I created the prototype and in a way testing it out with my peers and asking them if they like the game and also letting multiple people try to see if there are any bugs with the game or anything. I am inching a little towards the step 7 where it is imporving as needed taking some feedback so far like flipping the sides of my sprites and also allowing the sprites to be able to rotate their body and shoot backwards because the momment I can only make the sprites shoot foward. So as of now I am in between 6 to 7 taking the feedpack from my peers and evalutating their problems, trying to solve it to their suggestions. 

---

# Skills

---

# Time managment & Perserverance
I would say in general this was a skill that really got me through this freedom project because in the beginning I was relly struggling and I did not really know how to start my freedom project and also really jsut trying to find that time where I can take out to start the freedom proejct from all the works from my other classes like the Ap's where the all gave spring assignments. It was hard to really just take some time out as once I did some homeowrk for another class I would want to take a break 





[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
