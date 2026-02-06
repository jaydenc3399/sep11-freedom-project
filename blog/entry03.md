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
```js
const timerText = add([
  text("10"),       
  pos(20, 20),    
  fixed(),          
])

timerText.onUpdate(() => {
  timeLeft -= dt()                       
  timerText.text = Math.ceil(timeLeft)   
})
```

---

Over the break I only did one lesson and I also searched some potential topics that I could learn when I get back to school. One topic that I thoguht wass very important to learn about would be like health bars because I was doing some sort of shooting game so I needed some sort of health bar. To also take some damage also and I looked online but I could not really find good websites to learn about this. I went onto ai and  asked it to generate me some websites that are the best for this specfic topic of health bars. It gave me this [js progress bar](https://www.w3schools.com/howto/howto_js_progressbar.asp?utm_source=chatgpt.com) it told me that I can use this and build onto the code to make it act like health bars instead of a progress bar. I took this website and I threw it onto my SEP notes so that I can revist this some other time.

---

# Plan on learning next
Things that I plan to learn next is first of all getting a gist of how to make the health bar turning it from a progress bar into a health bar. Then also seeing how I can make it when someone shoots a bullet it will take damage and that health bar will go down. I want to also try to learn how to put like a automatic ai robot onto the enemy player where like when you join the game there is options to play with a friend like a two player game or jsut play online offline with a bot. I looked at one website so far from [the total beginners guide](https://www.gamedev.net/tutorials/programming/artificial-intelligence/the-total-beginners-guide-to-game-ai-r4942/) so far I found this website for this and I plan to learn about this and how I can integrate this into my game and maybe also setting a level of easy, medium, or hard is a idea that I have in mind but for now just these are what I am planning to learn next. 

---

# Engineering Design Process
Right now I  feel that I am still in the same spot right now which is still researching the problem and trying to find ways to build onto my product. I have been using ai a little more often in order to find websites that I can use to learn about specific topics. I am inching a litte into brainstorming the problem now also like ways on how I can make this a offline game but I am mostly centered around the learning right now and the key components that I will need in order to build this website. Other than that I feel that I have made some progress so far into brainstorming the solutions. I am trying to take my time in learning this code because it gets confusing really easily so I am only devoting some time to brainstorming the soultion and the rest of my time to learning the fundamentals of kaboom. 

---

# Skills


