---
layout: default
title: "Cognitive Impasse: Progressive Mental Block"
---

# Statement
This is the introductory statement for the paper. Please read it carefully before taking the quiz.

## Quiz Section

<div id="quiz-container">
  <p>Question: True or False - [Insert Question Here]</p>
  <button class="answer-button" onclick="checkAnswer(true)">True</button>
  <button class="answer-button" onclick="checkAnswer(false)">False</button>
  <p id="feedback" style="display:none;">Incorrect! The correct answer is [Explanation Here]</p>
</div>

<div id="main-paper" style="display:none;">
  <h2>The Paper</h2>
  <p>Here is the main content of the interactive paper. It will be revealed once the quiz is completed.</p>
</div>

<script>
  function checkAnswer(isTrue) {
    let correct = true; // Set the correct answer here
    let feedback = document.getElementById('feedback');
    let buttons = document.getElementsByClassName('answer-button');

    if (isTrue !== correct) {
      feedback.style.display = 'block';
      feedback.innerText = "Incorrect! The correct answer is [Explanation Here]";
      buttons[0].style.backgroundColor = isTrue ? 'red' : '';
      buttons[1].style.backgroundColor = !isTrue ? 'red' : '';
    } else {
      feedback.style.display = 'none';
      document.getElementById('quiz-container').style.display = 'none';
      document.getElementById('main-paper').style.display = 'block';
    }
  }
</script>

<style>
  .answer-button {
    margin: 5px;
    padding: 10px;
    font-size: 16px;
    cursor: pointer;
  }
</style>
