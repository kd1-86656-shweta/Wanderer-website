<!DOCTYPE html>
<html lang="en">
<head>
    <script>
        function updateProgressBar(progressPercentage) {
            var progressBarInner = document.querySelector('.progress-bar-inner');
            progressBarInner.style.width = progressPercentage + '%';
        }

        // Example: Set progress to 50% over 2 seconds
        var targetProgress = 96;
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

        // Function to handle click on plus sign
        function myFunction() {
            var popup = document.getElementById('popup');
            popup.style.display = 'block';
        }

        // Function to close the popup/modal
        function closePopup() {
            var popup = document.getElementById('popup');
            popup.style.display = 'none';
        }
    </script>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Styled MCQ Example</title>
    <style>
        /* Your CSS styles here */
        body {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
           
            margin: 0;
        }

        .border {
    border-bottom: 1px solid #e5e7eb; /* Top border */
    width: 100%; /* Set border-bottom width to full */
}

        /* Styles for the question container */
        .question-container {
            text-align: center;
            margin-top: 20px;
            padding: 10px; /* Add padding for better appearance */
            font-family: 'Segoe UI';
            font-size: 30px;
            font-weight: 590;
            margin-bottom: 20px;
        }

        /* Styles for the slider */
        .slider-container {
            
           
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
            padding-left: 10px;
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
            border: none;
            border-radius: 5px;
            cursor: pointer;
            font-weight: 400;
            font-size: 15px;
            font-family: 'segoe UI';
            text-align: center;
            height: 45px;
            width: 90px;
            margin-top: 50px;
        }

        .button a {
            color: white;
            text-decoration: none;
            /* Remove underline */
        }

        .slider-container {
         
           margin-top:25px;
            margin-bottom: 25px; /* Add padding for better appearance */
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

        .dashed-box {
            width: 180px;
            height: 110px;
            border: 2px dashed #e5e7eb;
            padding: 20px;
            border-radius: 10px;
            display: flex;
            justify-content: center;
            align-items: center;
            margin: 0 auto; /* Center horizontally */
            cursor: pointer; /* Change cursor to pointer */
        }
        .dashed-box:hover {
            border: 2px dashed #A9A9A9;

        }

        .plus-sign {
            font-size: 15px;
            cursor: pointer;
            color:#A9A9A9;
        }

        .plus-circle {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 25px;
    height: 25px;
    background-color: white; /* Set background color to white */
    border: 2px solid #A9A9A9; /* Set border color and width */
    border-radius: 50%;
    margin: 0 auto;
}


.plus-sign {
    font-size: 20px;
    cursor: pointer;
    color: #A9A9A9;
    font-weight: 900; /* Adjust font weight for a thicker plus sign */
}


        .popup {
            display: none;
            position: fixed;
            z-index: 1;
            left: 0;
            top: 0;
            width: 100%;
            height: 100%;
            overflow: auto;
            background-color: rgba(255, 255, 255, 0.8); /* Background color with transparency for the overlay */
            backdrop-filter: blur(5px); /* Apply blur effect */
        }

        .popup-content {
    background-color: white;
    padding: 20px;
    border: 1px solid #e5e7eb;
    width: 80%;
    max-width: 400px; /* Adjust width as needed */
    height: 390px; /* Set height to auto to fit content */
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translate(-50%, -50%);
    border-radius: 10px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Add a border shadow */
}

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
         /* Style for input box */
         input[type="text"] {
            height: 40px;
            width: 400px; /* Adjust width as needed */
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
        /* Style for label */
        label {
            margin-bottom: 10px;
            display: block;
            font-weight: 500;
            font-family:'segoe UI';
            font-size:15px;
        }
        .demo {
            font-size:20px;
            font-weight:500;
            font-family:'segoe UI';
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
    <p id="question">What's your education experience ?</p>
</div>

<div class="dashed-box" onclick="myFunction()">
    <!-- Plus sign -->
    <div class="plus-circle"><span class="plus-sign">+</span></div>
</div>

<!-- Popup container -->
<!-- Popup container -->
<div id="popup" class="popup" >
    <div class="popup-content">
        <span class="close" onclick="closePopup()">&times;</span>
        <p class="demo" id="demo">Add experience</p>
        <!-- First input box with label -->
        <label for="experience1">Degree or field of study</label>
        <div style="display: flex; margin-bottom:5px;">
            <input type="text" id="experience1" placeholder="Ex B.S Computer Science">
        </div>
        <!-- Second input box with label -->
        <label for="experience2">School</label>
        <div style="display: flex; margin-bottom:5px;">
            <input type="text" id="experience2" placeholder="Ex University of California, Berkeley">
        </div>
        <!-- Third input box with label -->
        <label for="experience3">Duration</label>
        <div style="display: flex; margin-bottom:5px;">
            <input type="text" id="experience3" placeholder="Ex 2 years">
        </div>
        <!-- Button -->
        <div class="button-container" style="text-align: left; margin-top: -50px;">
            <button class="button" onclick=" closePopup()">Add</button>
        </div>
        
        
    </div>
</div>


<!-- Button container -->
<div class="button-container">
    <button class="button"><a href='/canvas'>Next</a></button>
</div>
<script>
    window.onload = function() {
        // Get all input fields
        var inputFields = document.querySelectorAll('input[type="text"]');
        
        // Loop through each input field and add an event listener
        inputFields.forEach(function(inputField) {
            inputField.addEventListener('input', function() {
                saveToLocalStorage();
            });
        });

        // Check if there is a stored answer for the question and set the input field value
        var question = document.getElementById('question').textContent.trim();
        var storedExperience = localStorage.getItem(question);
        if (storedExperience) {
            var experience = JSON.parse(storedExperience);
            document.getElementById('experience1').value = experience.degree;
            document.getElementById('experience2').value = experience.school;
            document.getElementById('experience3').value = experience.duration;
        }
    };

    function saveToLocalStorage() {
        // Get the input values
        var degree = document.getElementById('experience1').value.trim();
        var school = document.getElementById('experience2').value.trim();
        var duration = document.getElementById('experience3').value.trim();

        // Get the question
        var question = document.getElementById('question').textContent.trim();
        
        // Create an object to store all values
        var experience = {
            "degree": degree,
            "school": school,
            "duration": duration
        };

        // Store the object in local storage with the question as the key
        localStorage.setItem(question, JSON.stringify(experience));
    }
</script>



</body>
</html>
