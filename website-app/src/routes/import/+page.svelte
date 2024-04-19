
<!-- In the HTML file of the route with the question -->
<!DOCTYPE html>
<html lang="en">
    <script>
        function updateProgressBar(progressPercentage) {
           var progressBarInner = document.querySelector('.progress-bar-inner');
           progressBarInner.style.width = progressPercentage + '%';
       }

       // Example: Set progress to 50% over 2 seconds
       var targetProgress = 72;
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
<head>
    <!-- Include the common styles -->
 

    <!-- Specific styles for this route -->
    <style>
        /* Styles for the border */
        .border {
            
            border-bottom: 1px solid #e5e7eb; /* Bottom border */
        }

        /* Styles for the question container */
        .question-container {
            text-align: center;
            margin-top:120px;
            padding: 10px; /* Add padding for better appearance */
            font-family:'Segoe UI';
            font-size:23px;
            font-weight:590;
        }

        /* Additional styles for the h3 element (optional) */
        .question-container p {
           margin-top:-20px;
        }

        /* Styles for the slider */
        .slider-container {
            margin-top: 20px; /* Adjust the margin as needed */
            padding: 20px; /* Add padding for better appearance */
            /* Add additional styles for the slider container */
        }
      /* Styles for the answer boxes */
       /* Updated styles for the answer boxes container */
    /* Updated styles for the answer boxes container */
    
    .button-container {
    
    text-align: center;
    margin-top: 60px; /* Adjust the margin as needed */
    margin-bottom:40px;
}


.button1 {
background-color: black;
color: white;
margin-right: 30px;
border: none;
border-radius: 50px;
cursor: pointer;
font-weight: 400;
font-size:15px;
font-family: 'segoe UI';
text-align: center;
height:60px;
width:400px;

}
.button1 a {
color: white;
text-decoration: none; /* Remove underline */

}
.text p {
    text-align: center;
    font-family: 'Segoe UI Symbol';
    line-height:0.5rem;
    font-weight: 200;
}
.text1 p {
    text-align: center;
    font-family: 'Segoe UI';
    font-weight: 600;
    font-size:15px;
}
.text1 p :hover {
    background-color:#e5e7eb;
}
.text1 a {
    text-decoration: None;
    color: black;
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
   
        <!-- Question container -->
       
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
    <div class="question-container">
        <p>Load your background and experience</p>
    </div>
    <div class="text">
        <p>Import your work and education history from Linkedin or enter it manually. We'll use this to custom-</p>
        <p>tailor your experience</p>

    </div>
    <div class="button-container">
        <button class="button1">https://linkedin.com/in/yourusername</button>
    </div>
    <div class="text1">
        <p><a href="/current-roles">No thanks, I'll enter information manually</a></p>

    </div>
    

</body>
</html>
