
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled MCQ Example</title>
    <script>
         
         function updateProgressBar(progressPercentage) {
            var progressBarInner = document.querySelector('.progress-bar-inner');
            progressBarInner.style.width = progressPercentage + '%';
        }

        // Example: Set progress to 50% over 2 seconds
        var targetProgress = 16;
        var currentProgress = 0;
        var increment = 1; // Increment value per frame
        var interval = 20; // Duration between each frame (in milliseconds)

        var progressInterval = setInterval(function() {
            if (currentProgress < targetProgress) {
                currentProgress += increment;
                updateProgressBar(currentProgress);
            } else {
                clearInterval(progressInterval);
            }
        }, interval);
        document.addEventListener("DOMContentLoaded", function() {
            // Function to handle answer selection
            function handleAnswerSelection(answerButton) {
                // Remove the selected class from all answer boxes
                document.querySelectorAll('.answer-box').forEach(box => box.classList.remove('selected-answer'));

                // Add the selected class to the clicked answer box
                answerButton.classList.add('selected-answer');

                // Get the question and answer
                const question = document.getElementById('question').textContent.trim();
                const selectedAnswer = answerButton.dataset.answer;

                // Save the question and answer in localStorage
                localStorage.setItem(question, selectedAnswer);
            }

            // Event listeners for answer boxes
            document.getElementById('button1').addEventListener('click', function() {
                handleAnswerSelection(this);
            });

            document.getElementById('button2').addEventListener('click', function() {
                handleAnswerSelection(this);
            });

            document.getElementById('button3').addEventListener('click', function() {
                handleAnswerSelection(this);
            });

            document.getElementById('button4').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button5').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button6').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button7').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button8').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button9').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button10').addEventListener('click', function() {
                handleAnswerSelection(this);
            });
            document.getElementById('button11').addEventListener('click', function() {
                handleAnswerSelection(this);
            });

            // Check if there is a selected answer for the current question in localStorage
            const currentQuestion = document.getElementById('question').textContent.trim();
            const storedAnswer = localStorage.getItem(currentQuestion);

            if (storedAnswer) {
                // Find and highlight the corresponding answer box
                document.querySelectorAll('.answer-box').forEach(box => {
                    if (box.dataset.answer === storedAnswer) {
                        box.classList.add('selected-answer');
                    }
                });
            }
        });
    </script>
    <style>
        /* Styles for the border */
      

        /* Styles for the question container */
        .question-container {
            text-align: center;
            margin-top: 60px;
            padding: 10px; /* Add padding for better appearance */
            font-family: 'Segoe UI';
            font-size: 23px;
            font-weight: 590;
        }

        /* Additional styles for the h3 element (optional) */
        .question-container p {
            margin-top: -20px;
        }

        /* Styles for the slider */
       

        /* Styles for the answer boxes */
        .answer-boxes {
            display: flex;
            flex-direction: column; /* Stack boxes vertically */
            justify-content: space-between; /* Add space between boxes */
            align-items: center; /* Center the boxes horizontally */
            margin-top: 20px;
        }

        .answer-box {
            height: 50px;
            border: 1px solid #e5e7eb; /* Bottom border */
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-family: 'Segoe UI';
            border-radius: 5px;
            margin-bottom: 10px; /* Add space between boxes */
            font-size: 15px;
            font-weight: 600;
            padding-left: 40px;
            padding-right: 40px;
            min-width: 300px;
            background-color: white;
            transition: background-color 0.3s; /* Add smooth transition effect */
        }

        .answer-box:hover {
            background-color:  #e5e7eb;
        }

        /* Styles for selected answer box */
        .selected-answer {
            background-color:  #e5e7eb;
        }
        .button-container {
            text-align: center;
            margin-top: 30px;
            /* Adjust the margin as needed */
            margin-bottom: 40px;
        }

        .button {
            background-color: black;
            color: white;
            padding: 10px 15px;
            margin-right: 30px;
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 400;
            font-size: 15px;
            font-family: 'segoe UI';
            text-align: center;
            height: 45px;
            width: 90px;
        }

        .button a {
            color: white;
            text-decoration: none;
            /* Remove underline */
        }
        .border {
           
           border-bottom: 1px solid #e5e7eb; /* Bottom border */
       }
        .slider-container {
            margin-top: 13px; /* Adjust the margin as needed */
            padding: 10px;
            margin-bottom:13px; /* Add padding for better appearance */
            /* Add additional styles for the slider container */
        }

        .container {
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .progress-bar {
            width: 250px;
            background-color: #f3f3f3;
            border-radius: 20px;
            overflow: hidden;
            text-align: center;
        }

        .progress-bar-inner {
            background-color: black;
            height: 15px;
            width: 0%;
            transition: width 0.5s ease-in-out; /* Adjust transition duration as needed */
        }
    </style>
</head>
<body>

    <!-- Question section with border -->
    <div class="border">
        <!-- Slider container -->
        <div class="slider-container">
            <div class="container">
                <div class="progress-bar">
                    <!-- Progress bar inner (filled part) -->
                    <div class="progress-bar-inner"></div>
                </div>
            </div>
        
            <!-- Add your slider HTML and styles here -->
        </div>
    </div>

    <!-- Question container -->
    <div class="question-container">
        <p id="question">How'd you hear about us?</p>
    </div>

    <!-- Answer boxes -->
    <div class="answer-boxes">
        <div id="button1" class="answer-box" data-answer="Twitter">Twitter</div>
        <div id="button2" class="answer-box" data-answer="Word of mouth">Word of mouth</div>
        <div id="button3" class="answer-box" data-answer="Linkedin">Linkedin</div>
        <div id="button4" class="answer-box" data-answer="Instagram">Instagram</div>
        <div id="button5" class="answer-box" data-answer="Facebook">Facebook</div>
        <div id="button6" class="answer-box" data-answer="Google">Google</div>
        <div id="button7" class="answer-box" data-answer="Reddit">Reddit</div>
        <div id="button8" class="answer-box" data-answer="Youtube">Youtube</div>
        <div id="button9" class="answer-box" data-answer="Tiktok">Tiktok</div>
        <div id="button10" class="answer-box" data-answer="From an article or blog post">From an article or blog post</div>
        <div id="button11" class="answer-box" data-answer="other">other</div>
        </div>

    <div class="button-container">
        <button class="button"><a href='/life-style'>Next</a>  </button>
    </div>

   <!-- Add this line at the top of your script -->


</body>
</html>

