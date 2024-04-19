<!DOCTYPE html>
<html lang="en">
<head>
    <script>
        function updateProgressBar(progressPercentage) {
           var progressBarInner = document.querySelector('.progress-bar-inner');
           progressBarInner.style.width = progressPercentage + '%';
       }

       // Example: Set progress to 50% over 2 seconds
       var targetProgress = 80;
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
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled MCQ Example</title>
    <style>
        /* Your CSS styles here */
        /* Styles for the border */
        .border {
            border-bottom: 1px solid #e5e7eb; /* Top border */
           
        }

        /* Styles for the question container */
        .question-container {
            text-align: center;
            margin-top: 60px;
            padding: 10px; /* Add padding for better appearance */
            font-family: 'Segoe UI';
            font-size: 25px;
            font-weight: 590;
        }

        /* Additional styles for the h3 element (optional) */
        .question-container p {
            margin-top: 120px;
        }

        /* Styles for the slider */
        .slider-container {
            margin-top: 20px; /* Adjust the margin as needed */
            padding: 20px; /* Add padding for better appearance */
            /* Add additional styles for the slider container */
        }

        /* Styles for the answer boxes */


        /* Styles for selected answer box */
        .selected-answer {
            background-color: #e5e7eb;
        }
        
        /* Style for input box */
        input[type="text"] {
            height: 40px;
            width: 280px; /* Adjust width as needed */
            font-size: 14px;
            border-radius: 10px;
            border: 1px solid #e5e7eb;
            margin-bottom: 10px;
            transition: border-color 0.3s;
            padding-left:10px;
        }
        
        input[type="text"]:focus {
            outline: none;
            border: 2px solid black;
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
        <p id="question">What's your current role or title?</p>
    </div>

    <!-- Answer boxes -->
   
        <!-- Input field as an answer box -->
    <div style="display: flex; justify-content: center;">
        <input type="text" id="inputField" placeholder="e.g. Software Engineer">
    </div>


    <!-- Button container -->
    <div class="button-container">
        <button class="button"><a href='/work-history'>Next</a>  </button>
    </div>

    <script>
        function saveToLocalStorage() {
            // Get the question
            var question = document.getElementById('question').textContent.trim();
            // Get the input value
            var inputValue = document.getElementById('inputField').value.trim();
            // Store in local storage
            localStorage.setItem(question, inputValue);
        }

        // Check if there is a stored answer for the question and set the input field value
        window.onload = function() {
            var question = document.getElementById('question').textContent.trim();
            var storedAnswer = localStorage.getItem(question);
            if (storedAnswer) {
                document.getElementById('inputField').value = storedAnswer;
            }
        };
    </script>

</body>
</html>
