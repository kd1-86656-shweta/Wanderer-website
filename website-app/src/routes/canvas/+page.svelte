<!DOCTYPE html>
<html lang="en">
<head>
  
  

    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Wanderer Website</title>
   
    <style>
        /* Global Styles */
        body {
            margin: 0;
        }

        /* Header Styles */
        header {
            background-color: #F8FBF8; /* Light gray background */
            border-bottom: 1px solid #ddd; /* Bottom border */
            display: flex;
            justify-content: space-between;
            align-items: center;
            height:50px;
        }

        .logo {
            width: 40px; /* Adjust size as needed */
            height: 40px; /* Adjust size as needed */
            cursor: pointer;
            margin-left:20px;
            margin-right:20px;
        }

        /* Popup Styles */
        .popup {
            display: none;
            position: fixed;
            z-index: 1;
            padding: 20px;
            border: 1px solid #ddd;
            width: 280px; /* Width set to 300px for both popups */
            height: 540px; /* Height set to 100% of viewport height */
            border-radius:10px;
           
        }

        .popup-content {
           margin-top: -10px;
        }

        .answer-popup {
            display: none;
            position: absolute;
            top: 50%;
            left: 170px;
            transform: translate(-50%, -50%);
            width: 230px; /* Width of the answer popups */
            padding: 10px;
            background-color: #fff;
            border-radius: 10px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
            z-index: 9998;
            margin-bottom:30px;
            
           
        }

        .answer-box {
            position: relative;
            height: 35px;
            border: 1px solid #e5e7eb; /* Bottom border */
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-family: 'Segoe UI';
            border-radius: 5px;
            margin-bottom: 5px; /* Add space between boxes */
            font-size: 14px;
            font-weight: 600;
            padding-left: 40px;
            padding-right: 40px;
            background-color: white;
            transition: background-color 0.3s; /* Add smooth transition effect */
        }
        .option-box {
            position: relative;
            height: 32px;
            border: 1px solid #e5e7eb; /* Bottom border */
            display: flex;
            justify-content: center;
            align-items: center;
            cursor: pointer;
            font-family: 'Segoe UI';
            border-radius: 5px;
            margin-bottom: 5px; /* Add space between boxes */
            font-size: 14px;
            font-weight: 600;
            background-color: white;
            transition: background-color 0.3s; /* Add smooth transition effect */
        }


        .answer-box:hover {
            background-color:  #e5e7eb;
        }
        .option-box:hover {
            background-color:  #e5e7eb;
        }

        .close {
            color: #aaa;
            float: right;
            font-size: 28px;
            font-weight: bold;
            cursor: pointer;
        }

        .close:hover,
        .close:focus {
            color: black;
            text-decoration: none;
            cursor: pointer;
        }
        .answer-popup h3 {
            margin-top:8px;
            margin-bottom:8px;
            font-family: 'Segoe UI';
            font-weight:500;
            font-size:18px;
            margin-left:10px;
        }

        /* Highlighted option box */
        .highlighted {
            background-color: #e5e7eb !important;
        }

    </style>
</head>
<script src="./images/wanderer-logo.webp" type="module"></script>

<body>

<header>
    <!-- Left corner logo -->
    
    
    <img src="../src/lib/images/Personalization-1.svg" class="logo" id="toggleLeftPopup">
    <!-- C:\Users\admin\Desktop\website-project\website-app\src\lib\images\Personalization-1.svg-->

    <!-- Right corner logo -->
    <img src="../src/lib/images/Personalization-1.svg" alt="Right Logo" class="logo" id="openRightPopup">
</header>

<!-- Left Popup container -->
<div id="leftPopup" class="popup" style="left: 10px; top: 60px;">
    <div class="popup-content">
        <!-- Left Popup Content -->
        <h3>Settings</h3>
        <p>Customize the information that Wanderer uses to generate your career map.</p>

        <!-- First Content Box -->
        <div class="answer-boxes">
            <h4>Aspirations</h4>
            <div class="answer-box" id="openAnswerPopup1">Goal</div>
            <div class="answer-box" id="openAnswerPopup2">Work life balance</div>
            <div class="answer-box" id="openAnswerPopup3">Income</div>
            <div class="answer-box" id="openAnswerPopup4">Growth</div>
            <div class="answer-box" id="openAnswerPopup5">Known for</div>
        </div>

        <!-- Second Content Box -->
        <div class="answer-boxes">
            <h4>Industries</h4>
            <div class="answer-box" id="openAnswerPopup6">Interested</div>
            <div class="answer-box" id="openAnswerPopup7">Not Interested</div>
        </div>
        <p>Please create a free account or Sign in</p>
    </div>
</div>

<!-- Answer Popup containers -->
<div id="answerPopup1" class="answer-popup" style="top: 390px;">
    <h3>Goal</h3>
   
    <div class="option-box" id="goalOption1">Change career</div>
    <div class="option-box" id="goalOption2">Advance in my current career</div>
    <div class="option-box" id="goalOption3">Explore future career options</div>
    <div class="option-box" id="goalOption4">Just checking things out</div>
</div>
<div id="answerPopup2" class="answer-popup" style="top: 420px; width:500px; left:280px;">
    <h3>Work life balance</h3>
    <div class="option-box" id="balanceOption1">My work provides me with ample personal time to enjoy life</div>
    <div class="option-box" id="balanceOption2">I have balanced lifestyle with equal emphasis on work and personal times</div>
    <div class="option-box" id="balanceOption3">My work is passion and I enjoy devoting a lot of time to it</div>
    <div class="option-box" id="balanceOption4">Not sure</div>
</div>
<!-- Add other answerPopup elements similarly -->

<!-- Right Popup container -->
<div id="rightPopup" class="popup" style="right: 10px; top: 60px;">
    <div class="popup-content">
        <span class="close" id="closeRightPopup">&times;</span>
        <!-- Right Popup Content -->
        <h2>Right Corner Popup</h2>
        <p>This is the content of the right corner popup.</p>
    </div>
</div>

<script>
     
      
  
    
    document.getElementById('toggleLeftPopup').addEventListener('click', function() {
        var leftPopup = document.getElementById('leftPopup');
        if (leftPopup.style.display === 'none' || leftPopup.style.display === '') {
            leftPopup.style.display = 'block';
        } else {
            leftPopup.style.display = 'none';
        }
    });

    document.getElementById('openRightPopup').addEventListener('click', function() {
        var rightPopup = document.getElementById('rightPopup');
        rightPopup.style.display = 'block';
    });

    document.getElementById('closeRightPopup').addEventListener('click', function() {
        var rightPopup = document.getElementById('rightPopup');
        rightPopup.style.display = 'none';
    });

    document.getElementById('openAnswerPopup1').addEventListener('click', function() {
        var answerPopup = document.getElementById('answerPopup1');
        answerPopup.style.display = 'block';
        initializeAnswerPopup('What are you looking to achieve with wanderer?', 'answerPopup1');
    });

    document.getElementById('openAnswerPopup2').addEventListener('click', function() {
        var answerPopup = document.getElementById('answerPopup2');
        answerPopup.style.display = 'block';
        initializeAnswerPopup("Imagine your life 10-20 years from now. How do you see your work fitting into your ideal lifestyle?", 'answerPopup2');
    });

    // Add event listeners for each option box within the answer popups
    document.querySelectorAll('.answer-popup .option-box').forEach(function(optionBox) {
        optionBox.addEventListener('click', function() {
            var answerPopupId = this.parentElement.id;
            var answer = this.innerText;
            storeAnswer(answerPopupId, answer);
        });
    });

    function initializeAnswerPopup(question, answerPopupId) {
    var storedAnswer = localStorage.getItem(question);
    if (storedAnswer) {
        var optionBoxes = document.querySelectorAll('#' + answerPopupId + ' .option-box');
        optionBoxes.forEach(function(optionBox) {
            optionBox.style.backgroundColor = 'white'; // Reset all option boxes to white
            if (optionBox.innerText === storedAnswer) {
                optionBox.style.backgroundColor = '#ccc'; // Gray color for already answered question
            }
        });
    }
}


    function storeAnswer(answerPopupId, answer) {
    var question;
    if (answerPopupId === 'answerPopup1') {
        question = "What are you looking to achieve with wanderer?";
    } else if (answerPopupId === 'answerPopup2') {
        question = "Imagine your life 10-20 years from now. How do you see your work fitting into your ideal lifestyle?";
    }
    localStorage.setItem(question, answer);
    initializeAnswerPopup(question, answerPopupId); // Update color after storing new answer
    closeAnswerPopup(answerPopupId);
}


    function closeAnswerPopup(answerPopupId) {
        var answerPopup = document.getElementById(answerPopupId);
        answerPopup.style.display = 'none';
    }

</script>

</body>
</html>
