<h1>Learning Journal - Code 201-Day 03 : Bronwyn</h1>

Today was definitely more grueling than the first two! The frustrations more pronounced, but the victories sweeter. I thought I had a reasonable handle on FOR loops, but I knew I was a bit lost on WHILE loops. The lab assignments were definitely frustrating at times, because I felt like the concepts were just out of reach for much of the afternoon, I almost had them down, but then when I would test what I had coded it wouldn't work. It seemed right, but clearly was not. I really appreciated Aaron's patience with me as he explained the same WHILE, FOR, and IF/ELSE concepts to me in different ways until they started to coalesce into something I could get a handle on.

I managed to get through Question 6 with minimal mentoring from Sam (the best help was when he confirmed that a FOR loop was not going to get me where I wanted to be, so I spent my time figuring out a WHILE loop instead).

Question 7 started out okay, then went pear shape and didnt' work at all. But at the proverbial 11th hour, I finally got it! It took a really specific "hint" from Aaron, but once I had the one elusive piece "spelled out" for me, the rest of the logic tree fell into place. I stayed a few minutes late in order to test the solution I ended up with, and it worked!  

The issues I was having (with Question 7) had a lot to do with figuring out how to properly next the processes, and walking myself through each and every process the code was executing. The specific hint Aaron provided was the need to create a variable to store a boolean value of the FOR loop's comparison of the items in the array. That was of tremendous help!  Then I managed to work my way through the logic tree, and I managed to figure out how to jump out of the WHILE loop in short order.

Question 7's solution (it also helped to create some more specific variable names to use):
// Begin Question 7: answer should be a string, use an array, six attempts
var countriesLived = ['australia', 'ireland', 'scotland', 'thailand'];
var guessCountry = 0;

while (guessCountry < 6) {
  var answerSeven = prompt('Name a country (other than the U.S.) where you think Bronwyn has lived.').toLowerCase();
  var foundAnswer = false;
  for (var i = 0; i < countriesLived.length; i++) {
    console.log(answerSeven, countriesLived[0]);
    if (answerSeven === countriesLived[i]) {
      foundAnswer = true;
    }
  }
  if (foundAnswer === true) {
    alert("Correct");
    guessCountry = 6;
  } else {
    alert("Try again.")
    guessCountry++;
  }
};
