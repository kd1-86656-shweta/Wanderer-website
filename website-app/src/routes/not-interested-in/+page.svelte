<!DOCTYPE html>
<html lang="en">

<head>
    <!-- Include the common styles -->
    <script>
        function updateProgressBar(progressPercentage) {
           var progressBarInner = document.querySelector('.progress-bar-inner');
           progressBarInner.style.width = progressPercentage + '%';
       }

       // Example: Set progress to 50% over 2 seconds
       var targetProgress = 56;
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
   </script>


    <!-- Specific styles for this route -->
    <style>
        /* Styles for the border */
        .border {
           
            /* Top border */
            border-bottom: 1px solid #e5e7eb;
            /* Bottom border */
        }

        /* Styles for the question container */
        .question-container {
            text-align: center;
            margin-top: 20px;
            padding: 10px;
            /* Add padding for better appearance */
            font-family: 'Segoe UI';
            font-size: 23px;
            font-weight: 590;
        }

        /* Additional styles for the h3 element (optional) */
        .question-container p {
            margin-top: -20px;
        }

        /* Styles for the slider */
        .slider-container {
            margin-top: 20px;
            /* Adjust the margin as needed */
            padding: 20px;
            /* Add padding for better appearance */
            /* Add additional styles for the slider container */
        }

        /* Updated styles for the answer boxes container */
        .answer-boxes {
            display: flex;
            justify-content: center;
            /* Center the boxes horizontally */
            align-items: center;
            margin-top: 10px;
        }

        /* Updated styles for individual answer box */
        .answer-box {
            height: 40px;
            border: 1px solid #e5e7eb;
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-family: 'Segoe UI';
            border-radius: 5px;
            margin-bottom: 10px;
            font-size: 14px;
            font-weight: 600;
            padding-left: 10px;
            padding-right: 10px;
            min-width: 180px;
            margin-right: 10px;
            /* Add space between boxes */
        }

        .answer-box a {
            color: black;
            text-decoration: none;
            /* Remove underline */
        }

        .selected-answer {
            background-color: black;
            color: white;
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

        #result {
            margin-top: 20px;
            font-family: 'Segoe UI';
            font-size: 16px;
            font-weight: 600;
        }

        #answer-list {
            margin-top: 20px;
            font-family: 'Segoe UI';
            font-size: 16px;
            font-weight: 600;
        }
        .answer-box:hover {
            background-color:  #e5e7eb;
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
            transition: width 0ms ease-in-out; /* Adjust transition duration as needed */
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
        <p>Are there any industries you're not interested in ?</p>
    </div>
    <!-- Answer boxes -->

 <div class="answer-boxes">
        <div id="button1" class="answer-box" data-answer="Agriculture">Agriculture</div>
        <div id="button2" class="answer-box" data-answer="Automative">Automative</div>
        <div id="button3" class="answer-box" data-answer="Banking">Banking</div>
    </div>
    <div class="answer-boxes"> 
        <div id="button4" class="answer-box" data-answer="Biotechnology"> Biotechnology</div>
        <div id="button5" class="answer-box" data-answer="Construction">Construction</div>
        <div id="button6" class="answer-box" data-answer="Consumer goods">Consumer goods</div>
    </div>
    <div class="answer-boxes">
        <div id="button7" class="answer-box" data-answer="Education">Education</div>
        <div id="button8" class="answer-box" data-answer="Energy">Energy</div>
        <div id="button9" class="answer-box" data-answer="Entertainment">Entertainment</div>
    </div>
    <div class="answer-boxes">
        <div id="button10" class="answer-box" data-answer="Fashion"> Fashion</div>
        <div id="button11" class="answer-box" data-answer="Financial Services">Financial Services</div>
        <div id="button12" class="answer-box" data-answer="Food & Bevrages">Food & Beverages</div>
    </div>
    <div class="answer-boxes">
        <div id="button13" class="answer-box" data-answer="Healthcare">Healthcare</div>
        <div id="button14" class="answer-box" data-answer="Hospitality">Hospitality</div>
        <div id="button15" class="answer-box" data-answer="Information Technology">Information Technology</div>
    </div>
    <div class="answer-boxes">
        <div id="button16" class="answer-box" data-answer="Insurance">Insurance</div>
        <div id="button17" class="answer-box" data-answer="Manufacturing">Manufacturing</div>
        <div id="button18" class="answer-box" data-answer="Media">Media</div>
    </div>
    <div class="answer-boxes">
        <div id="button19" class="answer-box" data-answer="Mining">Mining</div>
        <div id="button20" class="answer-box" data-answer="Pharmaceuticals">Pharmaceuticals</div>
        <div id="button21" class="answer-box" data-answer="Real Estate">Real Estate</div>
    </div>
    <div class="answer-boxes">
        <div id="button22" class="answer-box" data-answer="Retail">Retail</div>
        <div id="button23" class="answer-box" data-answer="Telecommunications">Telecommunications</div>
        <div id="button24" class="answer-box" data-answer="Transportation">Transportation</div>
    </div>
    <div class="answer-boxes">
        <div id="button25" class="answer-box" data-answer="Travel">Travel</div>
        <div id="button26" class="answer-box" data-answer="Utilities">Utilities</div>
        <div id="button27" class="answer-box" data-answer="Other">Other</div>
    </div>
    <div class="button-container">
        <button class="button"><a href='/import'>Next</a>  </button>
    </div>

</body>


<script>
    let selectedAnswers = [];

    document.addEventListener("DOMContentLoaded", function() {
        // Function to handle answer selection
        function handleAnswerSelection(answerButton) {
            // Toggle the selection status
            answerButton.classList.toggle('selected-answer');

            // Get the selected answer
            const selectedAnswer = answerButton.dataset.answer;

            // Check if the answer is already selected
            const index = selectedAnswers.indexOf(selectedAnswer);
            if (index === -1) {
                // If not selected, add it to the array
                selectedAnswers.push(selectedAnswer);
            } else {
                // If already selected, remove it from the array
                selectedAnswers.splice(index, 1);
            }

            // Save the selected answers to localStorage
            const question = document.querySelector('.question-container p').textContent.trim();
            localStorage.setItem(question, JSON.stringify(selectedAnswers));
        }

        // Event listeners for answer boxes
        const answerBoxes = document.querySelectorAll('.answer-box');
        answerBoxes.forEach(box => {
            box.addEventListener('click', function() {
                handleAnswerSelection(this);
            });
        });

        // Check if there are selected answers stored in localStorage
        const question = document.querySelector('.question-container p').textContent.trim();
        const storedAnswers = localStorage.getItem(question);
        if (storedAnswers) {
            // Parse the stored answers and highlight the corresponding answer boxes
            const parsedAnswers = JSON.parse(storedAnswers);
            answerBoxes.forEach(box => {
                if (parsedAnswers.includes(box.dataset.answer)) {
                    box.classList.add('selected-answer');
                }
            });
        }
    });
</script>

</html>
