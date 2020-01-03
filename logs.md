# 100 Days Of Code - Log
### Day 21: January 2, Thursday

**Today's Progress**:

**Link(s) to work**
1. [Technical Documentation Page](https://codepen.io/Bpeters23/pen/VwYrPrY)

### Day 20: December 30, Monday

**Today's Progress**:

**Link(s) to work**
1. [Product Landing Page](https://codepen.io/Bpeters23/pen/vYEegxG)

### Day 19: December 27, Friday

**Today's Progress**: I've all but finished freeCodeCamp's Responsive Web Design Certification. All that's left now with it is finishing the projects. I wrapped up two of them today :)

**Link(s) to work**
1. [Tribute Page](https://codepen.io/Bpeters23/pen/GRgvopB)
2. [Survey Form](https://codepen.io/Bpeters23/pen/BaydKqp)

### Day 18: December 24, Tuesday

**Today's Progress**: I'm to a point in my code now, that I would like to start refactoring each solution I come to.

**Thoughts**: Somedays I don't have thoughts...

**Link(s) to work**
1. [Stop gninnips my words (JavaScript)](https://www.codewars.com/kata/stop-gninnips-my-sdrow/javascript)
<details><summary>Code</summary>
<p> 1

```javascript
function spinWords(str){
    temp = str.split(" ");
    let arr = []
    for (let word of temp) {
        if (word.length > 4) {
            arr.push(word.split("").reverse().join(""));
        } else {
            arr.push(word)
        }
    } return arr.join(" ");
};
```

</p>
<p> 1 Refactored

```javascript
function spinWords(str) {
    return str.split(" ").map((word) => {
        return (word.length > 4) ? word.split("").reverse().join("") : word;
    }).join(" ");
};
```

</p>
</details>

### Day 17: December 23, Monday

**Today's Progress**: I coded! some days, its not about what you code but rather the effort to code something.

**Thoughts**: 100 days straight of coding an hour each day doesn't seem to be quite attainable for me, but making an effort every days does. This week has been rough with my dog having surgery and needing to be watched constantly now, but I am still making progress!

**Link(s) to work**
1. [Repeat String (JavaScript)](https://www.codewars.com/kata/string-repeat/javascript)
2. [Return Negative (JavaScript)](https://www.codewars.com/kata/return-negative/javascript)
3. [Remove First and Last (JavaScript)](https://www.codewars.com/kata/remove-first-and-last-character/javascript)
4. [Remove Spaces (JavaScript)](https://www.codewars.com/kata/remove-string-spaces/javascript)
<details><summary>Code</summary>
<p> 1

```javascript
function repeatStr (n, s) {
  return s.repeat(n);
};
```

</p>
<p> 2

```javascript
function makeNegative(num) {
  return num < 0 ? num : -(num);
};
```

</p>
<p> 3

```javascript
function removeChar(str){
  return str.slice(1,-1)
};
```

</p>
<p> 4

```javascript
function noSpace(x){
  return x.replace(/\s/g, '');
};
```

</p>
</details>

### Day 16: December 21, Saturday

**Today's Progress**:

**Thoughts**:

**Link(s) to work**
1. [Square Every Digit (JavaScript)](https://www.codewars.com/kata/546e2562b03326a88e000020/solutions/javascript)
<details><summary>Code</summary>
<p>

```javascript
function squareDigits(num){
    let arr = num.toString().split('').map((int) => {
      return parseInt(int * int);
    });
    return parseInt(arr.join(""));
  }
```

</p>
</details>

### Day 15: December 19, Thursday

**Today's Progress**: I learned a bit more about Recursion today. It still feels a bit foreign, but I am able to work through the simpler problems in recursion. I think I still prefer loops though :P

**Thoughts**: I'm not entirely sure why recursion is a thing considering it can be accomplished in other ways.

**Link(s) to work**
1. [Recursive Functions (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
 - Power
 - Factorial
 - Product of Array
 - Range
 - Fibonacci
 - Reverse
<details><summary>Code</summary>
<p> Power

```javascript
function power(base, exponent){
  if (exponent < 0) return 1;
  return base * power(base, exponent - 1);
}
```

</p>
<p> Factorial

```javascript
function factorial(num){
  if (num < 0) return 1;
  return num * factorial(num-1)
}
```

</p>
<p> Product of Array

```javascript
function productOfArray(arr) {
  if (arr.length < 0) return 1;
  return arr[0] * productOfArray(arr.slice(1))
}
```

</p>
<p> Range

```javascript
function recursiveRange(num){
  if (num < 0) return 0;
  return num += recursiveRange(num-1)
}
```

</p>
<p> Fibonacci

```javascript
function fib(num){
  if (num <= 2) return 1;
  return fib(num-1) + fib(num-2);
}
```

</p>
<p> Reverse

```javascript
function reverse(str){
  if (str === "") return "";
  return reverse(str.substr(1)) + str.charAt(0);
}
```

</p>
</details>

### Day 14: December 18, Wednesday

**Today's Progress**: Today I finished the Applied Visual Desgin section of Free Code Camp's Responsive We Design Certification.

**Thoughts**: The more I know, the more I know I don't know much :P

**Link(s) to work**
1. [Max Subarray - O(N) - (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
<details><summary>Code</summary>
<p>

```javascript
function maxSubarraySum(arr, subLength){
  if (subLength > arr.length) return null;
  let maxSum = 0;
  let tempSum = 0;
  for (let i = 0; i < subLength; i++){
    maxSum += arr[i];
  }
  tempSum = maxSum;
  for (let j = subLength; j < arr.length; j++) {
    tempSum = tempSum - arr[j - subLength] + arr[j];
    maxSum = Math.max(maxSum, tempSum);
  } return maxSum;
}
```

</p>
</details>

### Day 13: December 17, Tuesday

**Today's Progress**:

**Thoughts**:

**Link(s) to work**
1. [Average Pair - O(N) - (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
2. [Is Subsequence - O(N) - (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
<details><summary>Code</summary>
<p> 1

```javascript
function averagePair(arr, av) {
  if (arr.length < 2) return false
  let left = 0
  let right = arr.length - 1
  let temp = -Infinity
  while (left < right) {
    temp = (arr[left] + arr[right]) / 2
    if (temp == av) {
      return true
    } else if (temp > av) {
      right--;
    } else {
      left++;
    }
  } return false
}
```

</p>
<p> 2
  
```javascript
function isSubsequence(str1, str2) {
  let i = 0;
  let j = 0;
  while (j < str2.length) {
    if (str2[j] == str1[i]) i++;
    console.log(str2[j])
    if (i == str1.length) return true;
    j++;
  }
  return false;
}
```

</p>
</details>

### Day 12: December 16, Monday

**Today's Progress**: I feel that I'm actually able to answer more complex questions like the ones that might be asked in a technical interview.

**Thoughts**: I've been falling quite behind when it comes to the social media aspect of this challenge. I definitely need to improve on that.

**Link(s) to work**
1. [Count Unique Values - O(N) - (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
2. [Value Frequency Comarison - O(N) - (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
3. [Duplicate Check - O(N) - (JavaScript)](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass)
<details><summary>Code</summary>
<p> 1

```javascript
function countUniqueValues(arr) {
  if (arr.length == 0) return 0;
  let left = 0;
  for (let right = 1; right < arr.length; right++) {
    if (arr[left] !== arr[right]) {
      left++;
      arr[left] = arr[right];
    }
  }
  return left + 1;
}
```

</p>
<p> 2

```javascript
function sameFrequency(num1, num2) {
  if (num1.toString().length !== num2.toString().length) {
    return false;
  }
  else {
    let sorted1 = num1.toString().split("").sort().join("");
    let sorted2 = num2.toString().split("").sort().join("");
    return (sorted1 !== sorted2 ? false : true);
  }
}

function sameFrequency(num1, num2){
  let strNum1 = num1.toString();
  let strNum2 = num2.toString();
  if(strNum1.length !== strNum2.length) return false;
  
  let countNum1 = {};
  let countNum2 = {};
  
  for(let i = 0; i < strNum1.length; i++){
    countNum1[strNum1[i]] = (countNum1[strNum1[i]] || 0) + 1
  }
  
  for(let j = 0; j < strNum1.length; j++){
    countNum2[strNum2[j]] = (countNum2[strNum2[j]] || 0) + 1
  }
  
  for(let key in countNum1){
    if(countNum1[key] !== countNum2[key]) return false;
  }
 
  return true;
}
```

</p>
<p> 3

```javascript
function areThereDuplicates() {
  let counter = {}
  for (let argument in arguments) {
    counter[arguments[argument]] = (counter[arguments[argument]] || 0) + 1
  }
  for (let key in counter) {
    if (counter[key] > 1) {
      return true
    }
  }
  return false;
}
```

</p>
</details>

### Day 11: December 15, Sunday

**Today's Progress**: I've leveled up to 6 kyu on codewars :)

**Thoughts**: As I thought might happen at some point, there was a two day strek of NOT coding this weekend. I am actually proud of myself for putting it aside for a couple days to just spend time with family though. its back to it this week! 

**Link(s) to work**
1. [Multiples of 3 or 5 (JavaScript)](https://www.codewars.com/kata/multiples-of-3-or-5/javascript)
2. [Find the odd int (JavaScript)](https://www.codewars.com/kata/find-the-odd-int/javascript)
<details><summary>Code</summary>
<p> 1

```javascript
function solution(number) {
  let total = 0;
  for (let i = number-1; i >= 0; i--){
    if (i % 3 == 0 || i % 5 == 0) {
      total += i
    }
  } return total
}
```

</p>
<p> 2

```javascript
function findOdd(A) {
  let counter = {}
  for (let integer of A) {
    if (counter[integer]) {
      counter[integer] += 1;
    } else {
      counter[integer] = 1;
    }
  }
  for (let num in counter) {
    if (counter[num] % 2 === 1)
      return parseInt(num)
  }
}
```

</p>
</details>

### Day 10: December 12, Thursday

**Today's Progress**: I am in the double digits! 10 days straight!

**Thoughts**: Today I had a conversation with a friend about finding work where we can support what we are most passionate about. So not to do the thing we love, but to be a strong proponent of the mission of that thing. It had me thinking about what that might be for me. I would really love to be ina position one day that supports young people taking an alternative approach to education and acheiving success in a chosen career. 

**Link(s) to work**
1. [03 - CSS Variables (JavaScript + CSS)](https://github.com/bonniepeters/JavaScript30)
2. [Disemvowel Trolls (JavaScript)](https://www.codewars.com/kata/disemvowel-trolls/javascript)
3. [Exes and Ohs (JavaScript)](https://www.codewars.com/kata/55908aad6620c066bc00002a/solutions/javascript)
<details><summary>Code</summary>
<p> 1

```javascript
const inputs = document.querySelectorAll(".controls input");
function handleUpdate() {
  const suffix = this.dataset.sizing || "";
  document.documentElement.style.setProperty(`--${this.name}`,
 this.value + suffix)
}
inputs.forEach(input => input.addEventListener('change', 
handleUpdate));
inputs.forEach(input => input.addEventListener('mousemove', 
handleUpdate));
```

</p>
<p> 2

```javascript
function disemvowel(str) {
  return str.replace(/[aeiou]/gi, '');
}
```

</p>
<p> 3

```javascript
function XO(str) {
  let xCount = 0
  let oCount = 0
  for (let char of str) {
    if (char.toLowerCase() == 'x') {
      xCount += 1;
    }
    else if (char.toLowerCase() == 'o') {
      oCount += 1;   
    }
  } return (xCount == oCount)
}
```

</p>
</details>

### Day 9: December 11, Wednesday

**Today's Progress**: I completed my first coding challenge as a part of my [JavaScript Algorithms and Data Structures Masterclass Course](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass). My nerves around these types of challenges are definitely improving with practice.

**Thoughts**: There is a LOT to know when it comes to JavaScript... That both excites and terrifies me :P

**Link(s) to work**
1. [02 - JS and CSS Clock](https://github.com/bonniepeters/JavaScript30)
2. [Valid Anagram](https://www.udemy.com/course/js-algorithms-and-data-structures-masterclass/learn/quiz/4410604#overview)
<details><summary>Code</summary>
<p> 1

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
<p> 2

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

</p>
</details>

### Day 8: December 10, Tuesday

**Today's Progress**: I started the JavaScript 30 course today. There were quite a few references I didn't fully get, but that was good becasue it forced me to learn above and beyond what was covered in the tutorial!

**Thoughts**: I'm excited to dive deeper into vanilla JavaScript and accomplishing things the long and technical way :)

**Link(s) to work**
1. [01 - JavaScript Drum Kit](https://github.com/bonniepeters/JavaScript30)

<details><summary>Code</summary>
<p>

```javascript
  function removeTransition(e) {
    if (e.propertyName !== 'transform') return;
    e.target.classList.remove('playing');
  }

  function playSound(e) {
    const audio = document.querySelector(`audio[data-key="${e.keyCode}"]`);
    const key = document.querySelector(`div[data-key="${e.keyCode}"]`);
    if (!audio) return;

    key.classList.add('playing');
    audio.currentTime = 0;
    audio.play();
  }

  const keys = Array.from(document.querySelectorAll('.key'));
  keys.forEach(key => key.addEventListener('transitionend', removeTransition));
  window.addEventListener('keydown', playSound);
```

</p>
</details>

### Day 7: December 9, Monday

**Today's Progress**: I made it a whole week coding eveyday!

**Thoughts**: Though I like working through code challenges, I would like to also be working on a project, so I will probably return to my latest projet and then try to find another idea.

**Link(s) to work**
1. [Updated Portfolio Site to Include Resume (React.js)](https://github.com/bonniepeters/bonniepeters)
2. [Mumbling (JavaScript)](https://www.codewars.com/kata/mumbling/javascript)

<details><summary>Code</summary>
<p> 1

```
<a className="nav-link" href={process.env.PUBLIC_URL + "/Resume.pdf"} target="_blank">Resume</a>
```

</p>
<p> 2

```javascript
function accum(s) {
  s = s.split("");
  repeatArr = [];
  for (let i = 0; i < s.length; i++) {
    repeatArr.push(s[i].repeat(i + 1).toLowerCase() + "-");
  }
  let capitalizeArr = [];
  for (let x = 0; x < repeatArr.length; x++) {
    capitalizeArr.push(
      repeatArr[x].charAt(0).toUpperCase() + repeatArr[x].slice(1)
    );
  }
  newStr = capitalizeArr.join("");
  return newStr.substring(0, newStr.length - 1);
}
```

</p>
</details>

### Day 6: December 8, Sunday

**Today's Progress**: I am now ranked at over 75 honor on codewars!

**Thoughts**: Need to spend some more time exploring the spread syntax in JavaScript

**Link(s) to work**
1. [You Are a Square (JavaScript)](https://www.codewars.com/kata/54c27a33fb7da0db0100040e)
2. [Highest and Lowest (JavaScript)](https://www.codewars.com/kata/554b4ac871d6813a03000035)

<details><summary>Code</summary>
<p> 1

```javascript
var isSquare = function(n){
  return Math.sqrt(n) % 1 === 0;
}
```

</p>
<p> 2

```javascript
function highAndLow(numbers){
    let arr = numbers.split(" ")
    return `${(Math.max(...arr))} ${(Math.min(...arr))}`
}
```

</p>
</details>

### Day 5: December 7, Saturday

**Today's Progress**: I made it through my first Saturday of 100 days of code!

**Thoughts** I'd like to spend some time learning more RegEx this week!

**Link(s) to work**
1. [Vowel Count (JavaScript)](https://www.codewars.com/kata/vowel-count/javascript)

<details><summary>Code</summary>
<p>

```javascript
function getCount(str) {
    return (str.match(/[aeiou]/gi) || []).length;
}
```

</p>
</details>

### Day 4: December 6, Friday

**Today's Progress**: The last unfinished coding challenge remains unfinished... It was one I had attempted during an interview mockup. I spent another 30 minutes on it today and hit a wall again. I am really gonna celebrate the day that one is finished and marked off my list!

**Thoughts** Today was the first day so far that I didn't want to/didn't feel I had time to code for an hour, but I in my time anyway! Its not only a challenge, its a choice!

**Link(s) to work**
1. [Get the Middle Character (JavaScript)](https://www.codewars.com/kata/get-the-middle-character/javascript)
2. [Shortest Word (JavaScript)](https://www.codewars.com/kata/shortest-word/javascript)

<details><summary>Code</summary>
<p> 1

```javascript
function getMiddle(s)
{
    let middlePosition = Math.floor(s.length / 2)
    if (s.length % 2 == 0) {
        return `${s[middlePosition - 1]}${s[middlePosition]}`
    } else {
        return `${s[middlePosition]}`
    }
}
```

</p>
<p> 2

```javascript
function findShort(s) {
    let wordArr = s.split(" ")
    let shortestWordCount = wordArr[0].length
    for (let i = 1; i < wordArr.length; i++){
        if (wordArr[i].length < shortestWordCount) {
            shortestWordCount = wordArr[i].length
        }
    } return shortestWordCount
}
```

</p>
</details>

### Day 3: December 5, Thursday

**Today's Progress**: Even after just 3 days of focusing in on one language(JavaScript) I can find things coming more easily. While I appreciated the versatility in the materials we covered in my bootcamp, my brain definitely works best with zeroing in on one thing and doing that well.

**Thoughts** I love being able to review other people's solutions after completing a challegne. it is so interesting to see the dozens if not hundreds of ways to solve a single problem!

**Link(s) to work**
1. [JavaScript Training #15 (JavaScript)](https://www.codewars.com/kata/training-js-number-15-methods-of-number-object-tofixed-toexponential-and-toprecision/javascript)
2. [A wolf in Sheeps Clothing (JavaScript)](https://www.codewars.com/kata/a-wolf-in-sheeps-clothing/javascript)

<details><summary>Code</summary>
<p> 1

```javascript
function howManySmaller(arr,n){
    arr = arr.map(num => parseFloat(num.toFixed(2)))
    arr = arr.filter(num => num < n)
    return arr.length;
}
```

</p>
<p> 2

```javascript
function warnTheSheep(queue) {
    queue = queue.reverse()
    if (queue[0] == "wolf") {
        return `Pls go away and stop eating my sheep`
    } else {
        return `Oi! Sheep number ${queue.indexOf("wolf")}! You are about to be eaten by a wolf!`
    }
}
```

</p>
</details>

### Day 2: December 4, Wednesday

**Today's Progress**: Today went a hell of a lot slower than yesterday. Only made it through one coding challenge, which was a little frustrating when compared to yesterday's 4.

**Thoughts** Today was a good reminder that its less about how much you get done and more about how much effort you put in. I set out to do two things today: 1) code for an hour 2) finish 3 coding challenges. I hit my first goal which is what was most important for the day.

**Link(s) to work**
1. [Sum of difference in array (JavaScript)](https://www.codewars.com/kata/sum-of-differences-in-array/javascript)

<details><summary>Code</summary>
<p>

```javascript
function sumOfDifferences(arr) {
    if (arr.length <= 1) {
      return 0;
    } else {
      arr = arr.sort(function(a, b) {
        return b - a;
      });
      let difference;
      let differenceArr = [];
        for (let i = 0; i < arr.length-1; i++) {
            difference = arr[i] - arr[i + 1];
            differenceArr.push(difference);
        } let sum = 0;
        for (let j = 0; j <= differenceArr.length-1; j++) {
            sum += differenceArr[j];
        } return sum
    }
  }
```

</p>
</details>

### Day 1: December 3, Tuesday

**Today's Progress**: During my bootcamp with General Assembly, we would often be asked to complete a codewars challenge. Most days we were given a coding challenge, I would become frustrated and discouraged and I rarely finished the challenge. I am starting my 100 days of code by going back through those challenges we were given and finishing them.

**Thoughts** Its funny to look back at how frustrated I was and how much easier the answers come to me now. I was able to quickly work through 4 of my unfinished problems on https://www.codewars.com/ within my hour of coding and tomorrow I will move on to the last 3 I left unfinished.

**Link(s) to work**
1. [Odd or Even? (JavaScript)](https://www.codewars.com/kata/odd-or-even/javascript)
2. [Find the smallest integer in an array (JavaScript)](https://www.codewars.com/kata/find-the-smallest-integer-in-the-array/javascript)
3. [Is the string uppercase? (JavaScript)](https://www.codewars.com/kata/is-the-string-uppercase/javascript)
4. [Who likes this? (JavaScript)](https://www.codewars.com/kata/who-likes-it/javascript)

<details><summary>Code</summary>
<p> 1

```javascript
function oddOrEven(array) {
    let sum = 0;
    for (let i = 0; i < array.length; i++) {
        sum += array[i]
    }
    if (sum % 2 == 0) {
        return "even"
    } else {
        return "odd"
    }
}
```

</p>
<p> 2

```javascript
class SmallestIntegerFinder {
    findSmallestInt(args) {
        let smallestInt = args[0]
        for (let i = 0; i < args.length; i++) {
            if (args[i] < smallestInt) {
                smallestInt = args[i]
            }
        }
        return smallestInt
    }
}
```

</p>
<p> 3

```javascript
String.prototype.isUpperCase = function() {
  return this.valueOf().toUpperCase() === this.valueOf();
}
```

</p>
<p> 4

```javascript
function likes(names) {
    if (names.length == 0) {
        return `no one likes this`
    } else if (names.length == 1) {
        return `${names[0]} likes this`
    } else if (names.length == 2) {
        return `${names[0]} and ${names[1]} like this`
    } else if (names.length == 3) {
        return `${names[0]}, ${names[1]} and ${names[2]} like this`
    } else {
        return `${names[0]}, ${names[1]} and ${names.length -2} others like this`
    }
}
```

</p>
</details>
