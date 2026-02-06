# Entry 3
##### 2/2/26

# Content/ progress in general over break 
From my last blog entry I have just been addng onto my learning log. I would say that it is hard to find videos online youtube because they only show videos of people building websites and not really the fundamentals of kaboom. For now I have been using Ai to give me topics that I would need for the games. I asked it for a bullet point list and I found which one matched and that I did not use. With this I grabbed the topic that I did not do and had the right criterias. I would take this and copy the topic to google and youtube to look for lessons that suited this topic and with that I was able to find something to learn. With these videos and websites I was able to continue tinkering with my code. One of these websites that which I used when I was learning was [KAPLAY](https://kaplayjs.com/docs/api/ctx/onCollide/). On this website I was able to look at one of the topics that I was recommended for my game which was onCollide. After looking at some examples of how it works which was when something hits with a certain object like a enemy in my game it will run the given code that is inputted. I started to do some practice on my own on how this might work. In the beginning I started with something simple which was just basically `onCollide` print this in the console.log. 
```js
player.onCollide("enemy", () => {
  console.log("Ouch!");
});
```
After thinking of what I could add on this I thought about the previous things that I have added to my code so far like the sound effects and maybe I could add some color to it in order to make it like stand out more. So with this I added onto the function. 
```js
player.onCollide("enemy", (enemy) => {
    play("boom")
 player.color = rgb(255, 0, 0)
  wait(0.1, () => player.color = rgb())
```
I made it so that once it collides with the enemy not only will the sound effect play but there would also be a color change. I did all of this code onto my pickcode where it was saved and I also processed this into my learning log. Moving on we did not really do much learning logs after that and I kind of slacked off I went onto winter break which I used some free time to really jsut brainstorm things that I should do. This small idea came up to me which was basically like a timer for my game which I felt that it did not really have much of a impact but I feel that it could be beneifical for my game in the future which is bascially just a timer. I was thinking maybe I can make a timer so that the game would only last a certain time so that it would be more intense or competitive. So I first looked for places where I can learn this and I came across kaboom.js there webite and I searched timers and there it was. I used [kaboom.js timer](https://kaboomjs.com/#timer) to learn about the different things that make up this concept. In the end I found four important key topics which were `dt()` how much time has passed `wait()` `loop()` and `onUpdate()`. I learned about all their functions, I then went to create a seperate pickcode and I tried to jsut create a timer alone so I dont mess up my code. With this I used some of the code from their website and created this which was a simple stopwatch in a way. 
```js
let timeLeft = 20

onUpdate(() => {
  timeLeft -= dt()

  if (timeLeft <= 0) {
    timeLeft = 0
    go("gameover")
  }
})
```
---
This counted down to like twenty seconds but I found a problem, after I saw that it wasnt really appearing on the screen or anything and I figured that it might be wrong so I did some research online and found out that it was counting but it was doing that like inside the code where I could not see it nor could the player be able to see it. I thought about what do I need to do or like add in order for it to add the timer onto the screen like a display. At first I was really stuck on how to add this so I started simple and did some simple text to display 

```js 
let timeLeft = 30

const timer = add([
  text("30"),
  pos(20, 20),
  fixed(),
])
```
I thought about my code and I realized that I did not really need a function so I erased it. After thinking for a while I went back to previous things that we learned such as `math.ceil`  and that helped me to create this line of code 
```js
  timer.text = Math.ceil(timeLeft).toString()
})
```
With this I was able to piece the whole code together. 
```
const timerText = add([
  text("10"),       // initial text
  pos(20, 20),      // position on screen
  fixed(),          // stays in the corner (UI)
])

timerText.onUpdate(() => {
  timeLeft -= dt()                       // same countdown
  timerText.text = Math.ceil(timeLeft)   // THIS line shows it
})
---



