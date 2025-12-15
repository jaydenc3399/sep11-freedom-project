# Entry 2
##### 12/15/2025

# Content 
This is a few weeks after the first blog that I have written. Right now I am still tinkering with my code a few times a week and I am still processing my code snippets and thiings that I have changed in my code on github and my ide. I have been wathcing videos, looking at examples and sometimes asking the internet for examples and help. I am making sure that I know the basics of kaboom.js before I can move onto anything else. I have moved a little bit into the features that I will need in my game like adding explosion feautures, effects, sounds, animations, and more. As of now we are still continuing to learn out tool and get the hang of it before we go on. Here is some of the code that I have been working on that I learned, that I thought was a little easy but also beneifical to my topic that I was doing. `Set gravity` which just makes the sprite jump or in this case in my code it just makes the sprite go down. I wanted to find a way where I can loop this animation and make it repeat using kaboom js so I went onto this wesbite so learn how to. [Stack overflow](https://stackoverflow.com/questions/71512546/how-can-i-make-kaboom-js-sprite-animations-repeat) I used this website to learn how to tinker and make my code loop 

```
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

---

In this part of the code I tinkered around with it a little changing the numbers inside the wait to a negative number 
```js
 onKeyPress("space", () => { 
    explode(player.pos);
    destroy(player);

    // Restart the game after a short d
    wait(-0.5, () => {
      go("game");
    });
  });
});
```

---

After testing out both positive and negative numbers this is the conclusion that I came across. The higher the number for the positive the longer the wait would be. For the negative the numbers the animation would play really quickly then go back to normal. I also tried to edit the number and it higher but I found that: 

```js
 wait(-0.5, () => {
```

---

If the number is too big and the wait time is too long, if the page cannot fit it then it just goes back to standard position after it reaches the end of the frame. Once the number is too big if it goes past the page the animation will not repeat and also it will return the sprite back to normal position and not move despite using such a high number. 

---

Another part I tinkered with in my code was this part of my code which was already inside, I tried to change my expldoe function, the particles inside to be a different color and I was able to do it with this code. 

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
---

The part that I added into my code was ` I addded the `color(255, Math.random() * 155 + 100, 0)`. This allows the particles to change colors to a orangish and yellow color. In my opinion these were like small parts of code but they will be really cruical in the future when I am working on my freedom project because these small componets will come together to form the final product so doing this now is not a waste. 

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
