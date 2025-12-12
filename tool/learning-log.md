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


# 11/10
[Kaboom set gravity link](https://kaboomjs.com)
* This time I learned something simple for now it was just `setting gravity` which bascially moved my sprite in the direction of down

```js
setgravity(2400)
```
* I did a few thigns to tinker with this and one was changing the numbers
* I realized as I changed the numbers when I set a smaller number it changed the speed slower
* Changing a high number would increase the speed

### I wodnered what would happen if I changed positive 2400 to negative so I tried it

```js
segravity(-2400)
```

### This time it moved my sprite in the upward motion instead of the down when it was positive

---

* I struggled to find some youtube videos to explode my sprite like when clicked so I went onto chat gpt to help me
* I asked it to teach me how to explode a circle when clicked and this is what I amde from it

```js
function explode(origin) {
  const numParticles = 1;
  const radius = 8;

  for (let i = 0; i < numParticles; i++) {
    const angle = (2 * Math.PI * i) / numParticles;
    const dir = vec2(Math.cos(angle), Math.sin(angle));
```

I changed around the `const numParticles` around to play with it a little bit and it changed the amount when clicked
I also changed
```js
onKeyPress("space", () => {
```
I changed this one for the click so now when I press space it explodes into particles
## Try next
Something that I will try next is maybe figuring out how to move the sprite left to right on its own because this setgravity only goes up and down and I already used both the positive and negative sign so I want to find a way now to make it go left or right instead of jsut up or down. Also another thing would be to find a way to make this motion of exploding repeat like a loop or something.

# 11/17
This time I tinkered trying to make a animation repeat for example i tested out the `set gravity` feature which just makes the sprite jump or in this case in my code it just makes the sprite go down. I wanted to find a way where I can loop this animation and make it repeat using kaboom js so I went onto this wesbite so learn how to. 
[Stack overflow](https://stackoverflow.com/questions/71512546/how-can-i-make-kaboom-js-sprite-animations-repeat)
I used this website to learn how to tinker and make my code loop 

---

```js
 onKeyPress("space", () => { 
    explode(player.pos);
    destroy(player);

    // Restart the game after a short d
    wait(0.5, () => {
      go("game");
    });
  });
});
```
This was the code, I took some of it from online to copy into my code so that I could edit it and see what it does. So this was the preview code and these are the changes that I made. 

* I tried to change the wait to a few seconds and I tested the numbers from postive to negative
* The higher the number for the positive the longer the wait would be
* For the negative the numbers the animation would play really quickly then go back to normal
  
I also tried to edit the number and it higher but I found that:

* IF the number is too big and the wait time is too long, if the page cannot fit it then it just goes back to standard position after it reaches the end of the frame
* Once the number is too big if it goes past the page the animation will not repeat and also it will return the sprite back to normal position and not move despite using such a high #

# Try next:
Something that I will do is experiment with more animations and the key aspects that will make my gaem more fun and create like a sound effect or a visual like explosion. Visual effects that will add some wow to my game and trying to learn more about the basics of kaboom also because I feel as if I have not fully masered the basics of kaboom yet. 




# 12/1 
### This time I went online and tinkered in my [pick ocde](https://app.pickcode.io/project/cmg5b8cve009okj2ewj08abpy) with changing color particlecs. In the beginning it was hard for me to find examples and lessons on how to do this but after I went onto Ai and asked it to teach me. I went onto my code and edited this onto it. 

```js
function explode(origin) {
    const numParticles = 20;

    for (let i = 0; i < numParticles; i++) {
        const angle = Math.random() * Math.PI * 2;
        const dir = vec2(Math.cos(angle), Math.sin(angle));
        const speed = Math.random() * 150 + 150;

        add([
            pos(origin.add(dir.scale(5))), 
            circle(Math.random() * 6 + 4),
            color(255, Math.random() * 155 + 100, 0),
            area(),                     
            move(dir.scale(speed)),
            lifespan(1, { fade: 0.5 }),
        ]);
    }
}
```
### * I addded the `color(255, Math.random() * 155 + 100, 0)
### *  THis allows the particles to change colors to a orangish and yellow color
### * In the code now we can see all the particles that split off from one single sprite when clicking D 
### * `pos(origin.add(dir.scale(5))), ` 
* I tinkered with this part changing the numbers and it casue the particles to be more spread out when d is clicked
* The higher the number than the particles would be more spread out.
* The lower the numnber the particles would be mroe compacted and less spread out

### Try next
#### Something that I want to try next is to maybe find a way to enlarge the particles so when I click they would be a little bigger and after the explosion the particles would dissapear and the blob or spirte would be gone since the game like they would die so thats one thing I will try to do next time. 

# 12/8
## This time I tried to make it so when the sprite explodes into particles there will be like a sort of sound effect to it and I tinkered this into my pickcode and watched how it works. 
* At first I imported the sprite and the song and sounf effect that I wanted
* It looked like this

---
```js
loadSprite("bean", "https://kaboomjs.com/sprites/bean.png");
loadSound("boom", "https://kaboomjs.com/sounds/boom.mp3");
```

* This made sure that the sprite loaded and then next the sound would be imported when I click the key to make it explode
### THis is the code that I added to make this work

```onKeyPress("d", () => { 
    play("boom");        
    explode(player.pos); 
    destroy(player);    

    
    wait(100, () => {
      go("game");
    });
  });
});
```
* I was able to click D and there was a sound of effect that said like "boom"
* I started exploring for some more sound effects that I would be able to add also and found a few different ones
```js
onKeyDown("left",  () => player.move(-SPEED, 0));
  onKeyDown("right", () => player.move(SPEED, 0));
  onKeyDown("up",    () => player.move(0, -SPEED));
  onKeyDown("down",  () => player.move(0, SPEED));
```
* This was the code that helped me to move the sprite around and by including this into the code it allows me to move it around
* and by click d and changing it around I can make it on which key I want to explode the sprite
* by click d more I can get more particles to appear also

---


## Try next: Something that I will try next time is maybe adding another sprite like a enemy and make them interact with one another like a shooting came where on contact one of them will explode on their own instead of me having to click the key d in order for the sprite to explode into particles. 

---
* 
<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
