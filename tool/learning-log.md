# Tool Learning Log

## Tool: **Kaboom**

## Project: **X**

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
One thing taht I am going to try enxt that I did not do this time would be to maybe animate the character/sprite because in this one I took it a little slower and I only changed the positioning a little bit so next time I am going to learn how to animate the sprite.

### X/X/XX:
* Text


<!--
* Links you used today (websites, videos, etc)
* Things you tried, progress you made, etc
* Challenges, a-ha moments, etc
* Questions you still have
* What you're going to try next
-->
