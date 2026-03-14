# Entry 4
## 3/9/26

From my last blog entry I was still learning some finishing touches of the code and now I have done a few more lessons to get the main components of my game. Like I said from my last blog entry I have searched a bunch of these topics that would be important for my project. This was one of the last components that I needed which was a health bar. I am at the moment planning out how I want my game right now and I am using a google doc to help me plan where I want things like the requirements that I am going to need to create the game. I was planning to do a checklist of my requirements because the plan is useful for keeping track of dates but I wanted a separate sheet of paper so I can check off the requirements like this page needs this and that. It makes it easier to read what I feel like and shows me what I am missing and if I have done that specific task on it I just put a check mark on it. So far I went through some of the topics in my learning log that I would have to add and it looks like this. 

![pic](../blog4.png)

---

Since I have started planning I have one topic left which is adding a ai component to play with but I plan on doing that later on and incorporating it later on so I have something to add for my learning log also. I so far have completed one lesson after the last blog entry which was health bars and I learned this through the [kaboom website](https://kaboomjs.com/#health). I started working with some of the regular starter code that it gave and I tinkered in jsbin. After getting a gist of what I was learning I then tried to incorporate this into my practice code that I had making a health bar and this is what I looked at. Before the practice I went onto some websites to see how it looks like, just getting some examples and how they function such as [this website from free code camp](https://forum.freecodecamp.org/t/javascript-game-health-bar-using-constructor-prototype/282763)

```js
 const healthBar = add([
      rect(40, 6),
      pos(player.pos.x - 20, player.pos.y - 30),
      color(0, 255, 0),
      "healthBar"
  ]);
```
I first created the health bar itself and the position where I wanted the health bar to be, including the shape. This was the easy part as it was copying and pasting almost. After this I created the end where the character will die 

```js
 if (player.health <= 0) {
        destroy(player);
        wait(100, () => go("game"));
    }
```
However the next part was really tricky for me because in a way I had to create a conditional for if the player does this or that the health bar will drop. I created this code which was basically just the health bar color and if it reaches a certain health limit the color will go down just like in games when you get low health it will turn red. I then set the damage it would take per hit, I first tested this out using the `onKeyPress` where I pressed the key and it would decrease the health bar down. While I was doing this code I ran into an issue which was trying to update the health bar which when I clicked D once it only worked once and after it did not update the health bar. My code looked like this in the beginning. 

```js
healthBar.pos = player.pos.add(vec2(-20, -30));
healthBar.width = 100 * (player.health / 2);
```

---
I tried thinking of ways to make it update after each click on D and I came up with using `onUpdate` which basically just does what I want it to do, updating the health bar when I click D. I created a condition where if it reaches a certain health it would turn red and it will also update the health bar merging everything into one and it looked like this. I did this by watching some [videos](https://www.construct.net/en/tutorials/health-bar-275?utm_source=) I found online on how to create a health bar to see where I went wrong also.

---

```js
onUpdate(() => {
      healthBar.pos = player.pos.add(vec2(-20, -30));
      healthBar.width = 100 * (player.health / 2);

      if (player.health < 30) {
          healthBar.color = rgb(255, 0, 0); 
      } else if (player.health < 60) {
          healthBar.color = rgb(255, 165, 0); 
      } else {
          healthBar.color = rgb(0, 255, 0); 
      }
});
```
This finished the part I had for health bars and I even tested it out and it worked when I clicked D so now I am going to move onto developing my product. 

---

# Engineering Design Process
Right now in the engineering design process I have moved over one step from basically planning my process and everything and now taking all that information now combining it into making step 5 of the engineering design process which is creating the prototype of the MVP for now. I have just started to create this and it is going to take some time to develop the prototype and I am going to be here until around maybe the end of April or a little earlier. I started creating the background and also even created the different difficulty modes, including the sprites that I want to be in the game. I am thinking of choosing set sprites or finding a way to let the user choose, but for now I have created some set sprites to hold as a placeholder. I am happy with my progress so far and I just need to inch closer and closer to the final product and try to go beyond the MVP after. 

---

# Skills

---

# Time management 
This is an important skill to have right now as I feel that since we are inching closer to the deadline of the freedom project I have not really even started much and I need to start working on it more. But really finding that time out right now to spend some time on the freedom project is hard. Along with work from other classes after you do some work after a long period of time you would want some rest and after that you lose track of time leading you to have no time for things like the freedom project. I think now I am going to have to create a new schedule where it would be able to support some spare time for the freedom project as I am kind of far. My plan for my schedule is to go home then take around a thirty minute break then I will transition to homework and get it all done at once. Then I will give my mind another resting break, after resting I will transition little by little each day, inching into the MVP and getting little by little done. I will do more work on some days and a little less work on one day so it's balanced. Also in life managing your time getting to school on time I don't struggle with this but 

# Perseverance
This along with time management is a very important skill to me in life and to work on my freedom project at times where I really don't know where to start like what to create and how I want to create it. I feel no matter how much planning I do it doesn't really make much of a difference. It's more of a checklist and not a plan in a way to me. These challenges lead me to really want to give up and when hard challenges come I start taking breaks and when this happens I start procrastinating and it's hard to really motivate myself to do things. In the freedom project I have forced and pushed myself to do things myself. This includes work outside like homework and other things, I feel the load of homework that I have leads me to become more lazy and stay at home more often not wanting to really go out and I feel I need this exercise because I am getting a little big but also really for my own health because as homework and stuff is important it's important to maintain a good health too. I have taken these challenges on but despite this I still find a small spark to do the things I want and need to do. But really keep that balance between the two no matter what. Despite how difficult it is to learn a topic and create a website, in the end I still find a way to push through it with tenacity and get the job done. 


[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)



