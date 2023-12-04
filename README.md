[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/C-6tAFub)
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Quiz project</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        #quiz-container {
            max-width: 600px;
            margin: 50px auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        .question {
            margin-bottom: 20px;
        }

        .options {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        .option {
            margin: 10px;
        }

        #result {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div id="quiz-container">
        <div class="question" id="question1">
            <h2>Question 1: What is the capital of France?</h2>
            <div class="options">
                <div class="option">
                    <input type="radio" name="q1" value="paris"> Paris
                </div>
                <div class="option">
                    <input type="radio" name="q1" value="london"> London
                </div>
                <div class="option">
                    <input type="radio" name="q1" value="berlin"> Berlin
                </div>
            </div>
        </div>

        <div class="question" id="question2">
            <h2>Question 2: What is the largest mammal?</h2>
            <div class="options">
                <div class="option">
                    <input type="radio" name="q2" value="elephant"> Elephant
                </div>
                <div class="option">
                    <input type="radio" name="q2" value="bluewhale"> Blue Whale
                </div>
                <div class="option">
                    <input type="radio" name="q2" value="lion"> Lion
                </div>
            </div>
        </div>

        <div class="question" id="question3">
            <h2>Question 3: Which programming language is this quiz written in?</h2>
            <div class="options">
                <div class="option">
                    <input type="radio" name="q3" value="java"> Java
                </div>
                <div class="option">
                    <input type="radio" name="q3" value="python"> Python
                </div>
                <div class="option">
                    <input type="radio" name="q3" value="javascript"> JavaScript
                </div>
            </div>
        </div>

        <button onclick="calculateResult()">Submit</button>
        <div id="result"></div>
    </div>

    <script>
        function calculateResult() {
            // You can implement your logic here to calculate the result based on user's answers
            // For simplicity, let's assume correct answers are "paris", "bluewhale", "javascript" for questions 1, 2, and 3 respectively
            var q1Answer = document.querySelector('input[name="q1"]:checked').value;
            var q2Answer = document.querySelector('input[name="q2"]:checked').value;
            var q3Answer = document.querySelector('input[name="q3"]:checked').value;

            var correctAnswers = 0;

            if (q1Answer === "paris") {
                correctAnswers++;
            }

            if (q2Answer === "bluewhale") {
                correctAnswers++;
            }

            if (q3Answer === "javascript") {
                correctAnswers++;
            }

            var resultElement = document.getElementById('result');
            resultElement.innerText = "Your score: " + correctAnswers + " out of 3";
        }
    </script>
</body>
</html>
