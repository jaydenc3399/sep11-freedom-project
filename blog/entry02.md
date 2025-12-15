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
[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
