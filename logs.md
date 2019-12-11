# 100 Days Of Code - Log

### Day 9: December 11, Wednesday

**Today's Progress**: I completed my first coding challenge as a part of my [JavaScript Algorithms and Data Structures Masterclass Course](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass). My nerves around these types of challenges are definitely improving with practice.

**Thoughts**: There is a LOT to know when it comes to JavaScript... That both excites and terrifies me :P

**Link(s) to work**
1. [02 - JS and CSS Clock](https://github.com/bonniepeters/JavaScript30)
<details>
  <summary>Code</summary>
  <p>
```javascript
const secondHand = document.querySelector('.second-hand');
const minuteHand = document.querySelector('.minute-hand');
const hourHand = document.querySelector('.hour-hand');
function setDate() {
const now = new Date();
const seconds = now.getSeconds();
const secondsDegrees = ((seconds / 60) * 360) + 90;
secondHand.style.transform = `rotate(${secondsDegrees}deg)`
const minutes = now.getMinutes();
const minutesDegrees = ((minutes / 60) * 360) + 90;
minuteHand.style.transform = `rotate(${minutesDegrees}deg)`
const hours = now.getHours();
const hoursDegrees = ((hours / 60) * 360) + 90;
hourHand.style.transform = `rotate(${hoursDegrees}deg)`
}
setInterval(setDate, 1000);
```
  </p>
</details>

2. [Valid Anagram](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass/learn/quiz/4410604#overview)<details><summary>Code</summary>
```javascript
function validAnagram(str1, str2) {
if (str1.length !== str2.length) {
return false
} else {
let sorted1 = str1.split("").sort().join("");
let sorted2 = str2.split("").sort().join("");
return (sorted1 !== sorted2 ? false : true);
}
}
```
</details>

### Day 8: December 10, Tuesday

**Today's Progress**: I started the JavaScript 30 course today. There were quite a few references I didn't fully get, but that was good becasue it forced me to learn above and beyond what was covered in the tutorial!

**Thoughts**: I'm excited to dive deeper into vanilla JavaScript and accomplishing things the long and technical way :)

**Link(s) to work**
1. [01 - JavaScript Drum Kit](https://github.com/bonniepeters/JavaScript30)

### Day 7: December 9, Monday

**Today's Progress**: I made it a whole week coding eveyday!

**Thoughts**: Though I like working through code challenges, I would like to also be working on a project, so I will probably return to my latest projet and then try to find another idea.

**Link(s) to work**
1. [Updated Portfolio Siter to Include (React.js)](https://github.com/bonniepeters/bonniepeters)
2. [Mumbling (JavaScript)](https://www.codewars.com/kata/mumbling/javascript)

### Day 6: December 8, Sunday

**Today's Progress**: I am now ranked at over 75 honor on codewars!

**Thoughts**: Need to spend some more time exploring the spread syntax in JavaScript

**Link(s) to work**
1. [You Are a Square (JavaScript)](https://www.codewars.com/kata/54c27a33fb7da0db0100040e)
2. [Highest and Lowest (JavaScript)](https://www.codewars.com/kata/554b4ac871d6813a03000035)

### Day 5: December 7, Saturday

**Today's Progress**: I made it through my first Saturday of 100 days of code!

**Thoughts** I'd like to spend some time learning more RegEx this week!

**Link(s) to work**
1. [Vowel Count (JavaScript)](https://www.codewars.com/kata/vowel-count/javascript)

### Day 4: December 6, Friday

**Today's Progress**: The last unfinished coding challenge remains unfinished... It was one I had attempted during an interview mockup. I spent another 30 minutes on it today and hit a wall again. I am really gonna celebrate the day that one is finished and marked off my list!

**Thoughts** Today was the first day so far that I didn't want to/didn't feel I had time to code for an hour, but I in my time anyway! Its not only a challenge, its a choice!

**Link(s) to work**
1. [Get hte Middle Character (JavaScript)](https://www.codewars.com/kata/get-the-middle-character/javascript)
2. [Shortest Word (JavaScript)](https://www.codewars.com/kata/shortest-word/javascript)

### Day 3: December 5, Thursday

**Today's Progress**: Even after just 3 days of focusing in on one language(JavaScript) I can find things coming more easily. While I appreciated the versatility in the materials we covered in my bootcamp, my brain definitely works best with zeroing in on one thing and doing that well.

**Thoughts** I love being able to review other people's solutions after completing a challegne. it is so interesting to see the dozens if not hundreds of ways to solve a single problem!

**Link(s) to work**
1. [JavaScript Training #15 (JavaScript)](https://www.codewars.com/kata/training-js-number-15-methods-of-number-object-tofixed-toexponential-and-toprecision/javascript)
2. [A wolf in Sheeps Clothing (JavaScript)](https://www.codewars.com/kata/a-wolf-in-sheeps-clothing/javascript)

### Day 2: December 4, Wednesday

**Today's Progress**: Today went a hell of a lot slower than yesterday. Only made it through one coding challenge, which was a little frustrating when compared to yesterday's 4.

**Thoughts** Today was a good reminder that its less about how much you get done and more about how much effort you put in. I set out to do two things today: 1) code for an hour 2) finish 3 coding challenges. I hit my first goal which is what was most important for the day.

**Link(s) to work**
1. [Sum of difference in array (JavaScript)](https://www.codewars.com/kata/sum-of-differences-in-array/javascript)

### Day 1: December 3, Tuesday

**Today's Progress**: During my bootcamp with General Assembly, we would often be asked to complete a codewars challenge. Most days we were given a coding challenge, I would become frustrated and discouraged and I rarely finished the challenge. I am starting my 100 days of code by going back through those challenges we were given and finishing them.

**Thoughts** Its funny to look back at how frustrated I was and how much easier the answers come to me now. I was able to quickly work through 4 of my unfinished problems on https://www.codewars.com/ within my hour of coding and tomorrow I will move on to the last 3 I left unfinished.

**Link(s) to work**
1. [Odd or Even? (JavaScript)](https://www.codewars.com/kata/odd-or-even/javascript)
2. [Find the smallest integer in an array (JavaScript)](https://www.codewars.com/kata/find-the-smallest-integer-in-the-array/javascript)
3. [Is the string uppercase? (JavaScript)](https://www.codewars.com/kata/is-the-string-uppercase/javascript)
4. [Who likes this? (JavaScript)](https://www.codewars.com/kata/who-likes-it/javascript)
