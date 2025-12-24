# Entry 2
## 12/15/2025

# Content 
This is a few weeks after the first blog that I have written. Right now I am still tinkering with my code a few times a week and I am still processing my code snippets and things that I have changed in my code on github and my ide. I have been watching videos, looking at examples and sometimes asking the internet for examples and help. I am making sure that I know the basics of kaboom.js before I can move onto anything else. I have moved a little bit into the features that I will need in my game like adding explosion features, effects, sounds, animations, and more. As of now we are still continuing to learn our tool and get the hang of it before we go on. Here is some of the code that I have been working on that I learned, that I thought was a little easy but also beneficial to my topic that I was doing. `Set gravity` which just makes the sprite jump or in this case in my code it just makes the sprite go down. I wanted to find a way where I could loop this animation and make it repeat using kaboom js so I went onto this website to learn how to. [Stack overflow](https://stackoverflow.com/questions/71512546/how-can-i-make-kaboom-js-sprite-animations-repeat) I used this website to learn how to tinker and make my code loop. I also watched a video and tried to see what a game with kaboom.js would look like if you incoperated the code in it so I watched this [youtube video](https://www.youtube.com/watch?v=HzyRsZ6tiMk) and went through each step one by one to see how this person made a code so I would have like some inspiration. I checked out multiple videos such as this [astreiod game](https://www.youtube.com/watch?v=9NTL69AS4z0) to see waht type of code they use and their functions and seeing if I could incorperate any of the code used in this video to help me create my game. 

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

After testing out both positive and negative numbers this is the conclusion that I came across. The higher the number for the positive the longer the wait would be. For the negative numbers the animation would play really quickly then go back to normal. I also tried to edit the number and it higher but I found that: 

```js
 wait(-0.5, () => {
```

---

If the number is too big and the wait time is too long, if the page cannot fit it then it just goes back to standard position after it reaches the end of the frame. Once the number is too big if it goes past the page the animation will not repeat and also it will return the sprite back to normal position and not move despite using such a high number. 

---

Another part I tinkered with in my code was this part of my code which was already inside, I tried to change my explode function, the particles inside to be a different color and I was able to do it with this code. 

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

The part that I added into my code was ` I added the `color(255, Math.random() * 155 + 100, 0)`. This allows the particles to change colors to an orangish and yellow color. In my opinion these were like small parts of code but they will be really crucial in the future when I am working on my freedom project because these small components will come together to form the final product so doing this now is not a waste. 

---

# Plans over break 
My plan over the break is to continue tinkering with my tool over the break by watching some more youtube videos online and taking more notes on it in my learning log despite their being no learning log due. I think I will try my best to tinker and dedicate some time. Right now I have actually watched one video on my own and I took some notes seperatly somewhere else and I have y code on pickcode right now and I am going to copy it into my ide later so that I can have it stored. Right now I am planning to do like some tinkering two days a week at least or if not once becasue I have some other work to do for other classes but I am going to dedicate some time tinkering a litlte bit and finding some youtube videos and websites that could be beneifical to me. At the momment it is kind of hard to find some youtube videos on kaboom so I am trying to just find some websites online and continue from there. 

# Engineering Design Process
Right now I still feel that I am still in the same spot right now which is still researching the problem and trying to find ways to build onto my product. Trying to find ways online and learning how to make these games more fun and interesting with cool animation effects and more to make the game more interactive and a little more addicting then your normal regular games. I would say I'm inching a little into brainstorming my possible solutions for my product right now. At the moment right now I have found a few animations like exploding and some sound effects to add but it still needs some more interesting ones so I am going to continue to research for more to better improve the experience for users. 

# Skills

---

# Time management
I feel as of right now it's a little harder to manage my time because with basketball practice and other extra curricular activities in school going on like clubs, NHS and really just trying to get a balance of everything has been a little difficult. But I would say having a well developed plan is the best thing to do, like on a piece of paper I create a list of things that I need to complete before the day ends when I get home after practice or after a club or something. I am able to check off one by one each task as it makes it easier to keep track of things because I feel like it's really easy to lose track of something and you end up forgetting to do it. It happened to me last year for my Spanish homework where I did not write it down and I ended up forgetting. So creating this schedule and knowing when to do what and when certain things are due were really important to me and making sure that there was some extra spare free time at the end for me to debrief and relax so that my whole day after I came back from school would not be so stressful. Maintaining this balanced schedule and time and pushing things that are due sooner to a priority has become like natural to me now as I got used to it so I would say just getting into that flow and mentality with a schedule because it helps you keep track of things so that you can turn it in on time and sometimes with my extra time I would brain storm the freedom project ideas and solutions that I could come up with in my head saving a little time for everything. 

# Perseverance
I would say out of all the skills this is a really important skill on the top because I feel as we freshmen and sophomores transition to junior year the workload just becomes a lot to bare where the work just stacks up and the stress will continue to build up and that is part of life but some people see this as too much stress and tend to give up or slack off on things just because its hard and also it is a lot of pressure and work to do and this stress gets put on them and they feel as if it is too much and give up. In my year as a junior I feel like it is hard to balance a lot of things that are happening and to actually stay motivated and on task because it is always so much work and you just wanna slack off and take a break at most times because it is too difficult or you're too lazy. Same goes for things like the freedom project and coding where its hard to understand things and its easy to give up but with the right people and patience you can get through it because with a good support system you are able to tackle challenges that seem so difficult but with the right guidance and support it makes challenges much smoother and easier. 

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)





