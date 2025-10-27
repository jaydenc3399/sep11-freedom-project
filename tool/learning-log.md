# Tool Learning Log

## Tool: **Kaboom**

## Project: Offline game where you start as a circle and you can kill other circles with a gun or maybe the body and you  can shoot these small circles out that act as bullets 

---

### 9/29/25:
* ## [Kaboom Website](https://kaboomjs.com/doc/setup)
     * Website used to get a CDN provider easiest and fastest way to start Kaboom
* ## [Second kaboom Website](https://kaboomjs.itch.io/kaboom)

 ```js
 <script>
    kaboom();
    loadSprite("bean", "bean.png");
    onLoad(() => {
        const player = add([
            sprite("bean"),
            pos(120, 80),
            area(),
            body(),
        ]);
    });
</script>
```

---

## Another thing that I tried was adding some color to the sprite

```js
 const player = add([
            sprite("bean"),
            pos(120, 80),
            area(),
            body(),
            color(255, 0, 0)
        ]);
```
 * ### I found that it is hard to change the color of a sprite using javascript
 * ### I added the color red but it just turned the whole image of my sprite red

---


### In the beginning I tried to start off by creating something simple like a sprite since in all the examples I saw they included sprites. I created this on pickcode.

---

  ####   *`kaboom()`-  Without this nothing will show up
  ####   * `LoadSprite` was used to load the iamge and name it
  ####   * `onLoad`- runs my code after the iamge loads
  ####   * `const player =add([])` adds or creates a new object into the game
  ####   * I gave it a position and named the sprite inside the array

  ----

  ## Tinkering
  * I made some slight changes and played around with the position a little bit and changed it to different locations
  * I tried entering a number for the area and body but nothing happened
  * The numebrs I changed were like a number grid where the first numebr controls x and the second number controls y

  ```js
    pos(140, 90),
```


---
# Questions
* One question that I have is that for the part where I use onLoad is there something else I can replace it for like a different code that will still make my code work?

# Try next
One thing that I am going to try enxt that I did not do this time would be to maybe animate the character/sprite because in this one I took it a little slower and I only changed the positioning a little bit so next time I am going to learn how to animate the sprite.

### 10/27/25
* ## Kaboom (Animation)
* [Kaboom Animation Video](https://www.youtube.com/watch?v=n-q0pKGhxyw)
* I used this video to help me learn how to move the spirte using the arrows keys on the computer

---


## Tinkering On pickcode
On pickcode I tried to add what I learned in the video and some help online to create a command where it would move my sprite based on the arrow i click

```js
onKeyDown("left", () => {
            player.move(-SPEED, 0);
        });

        onKeyDown("right", () => {
            player.move(SPEED, 0);
        });

        onKeyDown("up", () => {
            player.move(0, -SPEED);
        });

        onKeyDown("down", () => {
            player.move(0, SPEED);
        });
```
* My code looked like this and the speed inside the parenthesis corresponds to the varaible tht I named whcih controls the speed
* This code allows me to click or hold the arrow keys making my sprite move in the direction that I desire

--- 

### Another thing that I tried to do was remove the number 0 in the parenthesis and see if it would change anything, it looked like this 

```js
onKeyDown("down", () => {
            player.move(, SPEED);
        });
```

---
### This caused my code to have a error on pickcode and I was not able to see anything on my screen except a error message so I placed it back

After thinking for a little bit on what I could change I looked at how I was only able to control the the sprite using the keys so I wondered can I change it to a specific key that will activate the sprite to move in a certain direction. So I tried this out in the code 

```js
 onKeyDown("s", () => {
            player.move(-SPEED, 0);
        });

        onKeyDown("a", () => {
            player.move(SPEED,0 );
        });

        onKeyDown("w", () => {
            player.move(0, -SPEED);
        });

        onKeyDown("d", () => {
            player.move(0, SPEED);
        });
```
After trying this I pressed the keys and it allowed the sprite to move in the direction I wanted by clicking that key I designated the direction to move to. Which helped me realize I dont have to just code it directly to function on the arrows. 


## Try next: Something that I would love to try next would be to animate the spirte where it can create some affects like a kaboom or a explosion and see how I can incoperate this into my game later on for the freedom project. Another thing I will try next is maybe trying to make it so that the letters like the ones that control the sprites direction if I can assign a second key to it so that it will respond to any of the two keys I assigned to it. 



<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
