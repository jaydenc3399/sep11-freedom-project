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

---

# Engineering Design Process
Right now I still feel that I am still in the same spot right now which is still researching the problem and trying to find ways to build onto my product. Trying to find ways online and learning how to make these games more fun and intresting with cool animation effects and more to make the game more interactive and a little more addicting then your normal regular games. I would say im inching a little into brainstorming my possible solutions for my product right now. At the momment right now I have found a few animations like exploding and some sound effects to add but it still needs some more intresting ones so I a going to continue to research for more to better imporve the experience for users. 

# Skills

---

# Time mangment
I feel as of right now its a little harder to manage my time because with basketball practice and other extra cirruculars in school going on like clubs, NHS and really jsut trying to get a balance of everything has been a little difficult. But I would say having a well developed plan is the best thing to do like on a piece of paper I create like a list of things that I need to complete before the day ends when I get home after practice or after a club or something. I am able to check off one by one each task as it makes it easier to keep track of things because I feel like its really easily to lose track of something and you end up forgetting to do it. It happened to me last year for my spansih homework where I did not write it down and I ended up forgetting. So creating this schedule and knowing when to do what and when certain things are due were really important to me and making sure that there was some extra spare free time at the end for me to debrief and relax so that my whole day after I cam back from school would not be so stressful. Mainting this balanced scehdule and time and pushing things that are due sooner to a priority has become like natural to me now as I got used to it so I would say jsut getting into that flow and mentality with a scedhule because it helps you keep track of things so that you can turn it in on time and sometimes with my extra time I would brain storm the freedom project ideas and solutions that I could come up with in my head saving a little time for everything. 

# Perserverance
I would say out of all the skills this is a really important skill on the top because I feel as we freshmans and sophmores transition to junior year the workload just becomes a lot to bare where the work jsut stacks up and the stress will continue to build up and that is part of life but some people see this as too much stress and tend to give up or slack off on things just because its hard and also it is a lot of pressure and work to do and this stress gets put on them and they feel as if it is too much and give up. In my year as a junior I feel like it is hard to balance a lot of things that are happeing and to actually stay motivated and on task because it is always so much work and you just wanna slack off and take a break at most times because it is too difficult or your too lazy. Same goes for things like the freedom project and coding where its hard to take ti

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
