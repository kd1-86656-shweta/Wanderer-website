<script>

    import { image1, image2, image3, image4, image5 } from "$lib";

</script>


<style>
       /* Style for the header container */
.header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    background-color: #ffffff;
    color: black; /* Change text color to black */
    margin-top:-10px;
}

/* Style for the logo and name */
.logo {
    display: flex;
    align-items: center;
    margin-left: 20px; 
}
.logo p {
    margin-left: 10px;
    color: black;
    font-weight: 700;
    font-size: 1.2rem;
    line-height: 1.75rem;
    font-family:  'Segoe UI Emoji'; /* Corrected typo */
}

.logo img {
    width: 25px; /* Adjust the width of the logo as needed */
    height: 25px;
    height: auto;
    border-radius: 50%; /* Make the logo circular */
    overflow: hidden; /* Hide overflow to ensure a perfect circle */
}

/* Style for the button */
.header-button  {
    background-color: black;
    padding: 10px 15px;
    margin-right: 30px;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-weight: 400;
    font-size:15px;
    font-family: 'segoe UI';
   
}

 
.header-button a {
    color: white;
    text-decoration: none; /* Remove underline */

}
.button-container {
    
        text-align: center;
        margin-top: 40px; /* Adjust the margin as needed */
    }

    
.button1 {
    background-color: black;
    color: white;
    padding: 10px 15px;
    margin-right: 30px;
    border: none;
    border-radius: 20px;
    cursor: pointer;
    font-weight: 400;
    font-size:15px;
    font-family: 'segoe UI';
    text-align: center;
   width:250px;
}
.button1 a {
    color: white;
    text-decoration: none; /* Remove underline */

}
/* --font-family: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI',
		Roboto, Helvetica, Arial, sans-serif, 'Apple Color Emoji',
		'Segoe UI Emoji', 'Segoe UI Symbol';

/* Style for the centered h1 */
.centered-h1 {
    text-align: center;
    margin-top: 100px; /* Add margin to create space between the header and h1 */
    font-family: 'Segoe UI Emoji';
    margin-bottom: -20px;
    font-weight: 400;
}

.centered-h1 h1 {
    font-size: 5.5rem; /* Adjust the font size as needed */
}

.centered-p {
    text-align: center;
    font-size: 1.5rem;
    color: #8c8b92; /* Gray color */
    line-height: 0.5rem;
    font-family: 'Segoe UI Emoji'; 
}
/* New styles for the middle container */
.middle-container {
            text-align: center;
            margin-top: 200px;
            position: relative;
            margin-bottom: 250px;
        }

        .middle-container::before {
            content: "";
            display: block;
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 400px; /* Adjust the width of the circular shadow */
            height: 400px; /* Adjust the height of the circular shadow */
            background-color:white; /* Adjust the background color and transparency */
            border-radius: 50%; /* Make it a circle */
            z-index: -1; /* Behind the content */
            border:0 solid #e5e7eb;
            
        }

        .middle-box {
            background-color: white; /* Box background color */
            padding: 10px;
            border-radius: 10px; /* Border radius for the box */
            display: inline-block;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.5); /* Box shadow for a subtle effect */
            position: relative; /* Ensure the box shadow is relative to the container */
            z-index: 1; /* Above the circular shadow */
        }

        .middle img {
            width: 50px; /* Adjust the width of the image as needed */
            height: 50px; /* Adjust the height of the image as needed */
            border-radius: 50%; /* Make the image circular */
            overflow: hidden; /* Hide overflow to ensure a perfect circle */
        }

        .middle-container h1 {
            font-family: 'Segoe UI Emoji';
            font-weight: 700;
            font-size: 35px;
            margin-top: 20px; /* Adjust the margin as needed */
        }

        .middle-container p {
            font-family: 'Segoe UI';
            font-weight: 400;
            font-size: 18px;
            color: #8c8b92;
        }

        .button-container1 {
            margin-top: 40px; /* Adjust the margin as needed */
        }

        .button2 {
            background-color: black;
            color: white;
          
            margin-right: 30px;
            border: none;
            border-radius: 20px;
            cursor: pointer;
            font-weight: 400;
            font-size: 15px;
            font-family: 'segoe UI';
            text-align: center;
            height: 40px;
            width: 160px;
        }

        .button2 a {
            color: white;
            text-decoration: none; /* Remove underline */
        }
        .footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #ffffff;
        color: black;
        padding: 10px;
        bottom: 0;
        width: 100%;
        height: 50px;
    }

        .footer p {
            margin: 0;
            font-size: 14px;
            font-family: 'Segoe UI';
            color:#8c8b92;
        }

        .footer ul {
            list-style: none;
            margin-right: 80px;
          
            display: flex;
        }

        .footer li {
            font-size: 14px;
            font-family: 'Segoe UI';
            font-weight: 500;
            padding: 20px;
        }
       
      
   
    .review h1 {
        font-family: 'Segoe UI Emoji';
        font-weight: 500;
        font-size: 38px;
        text-align: center;
        margin-bottom: 100px;
        margin-top: 200px;
    }

    .review-content {
    display: flex;
    overflow: hidden; /* Add overflow: hidden to hide the overflowing content during animation */
    animation: moveReviewBox 5s linear infinite; /* Adjust the animation duration as needed */
}

@keyframes moveReviewBox {
    0% {
        transform: translateX(10%); /* Start position on the right */
    }
    100% {
        transform: translateX(-10%); /* End position on the left */
    }
}

.review-content:hover {
    animation-play-state: paused;
   
}

.review-box {
    width: 400px;
    margin-bottom: 20px;
    margin-left: 40px;
    height: 600px;
    background-color:white;
    border-radius: 10px;
   
    position: relative; /* Add relative positioning */
}
.review-box:hover {
    background-color:#d9e3ea;
    box-shadow: inset 0 0 1px white;
}


.review-text {
    font-size: 18px;
    margin-bottom: 10px;
    font-family: 'Segoe UI Emoji', Tahoma, Geneva, Verdana, sans-serif;
    padding-left: 15px;
    padding-right: 15px;
    color:black;
    font-weight: 500;
}

.review-box .review-date {
    position: absolute;
    bottom: 10px;
    color: #888;
    font-size: 18px;
    padding-left: 15px;
    padding-right: 15px;
}
.review-box {
    width: 400px;
    margin-bottom: 20px;
    margin-left: 40px;
    height: 300px;
    background-color: white;
    border-radius: 10px;
    position: relative;
}

.review-box .container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
}

.user-name {
    font-weight: 700;
    font-size: 16px;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    color: black;
    margin-left: -140px;
}

.image1 img {
    width: 50px;
    height: 50px;
    border-radius: 50%;
    margin: 0 5px;
}

.image2 img {
    width: 30px;
    height: 30px;
    border-radius: 50%;
    margin: 0 5px;
}



    </style>

<body>

    <!-- Header section -->
    <div class="header-container">
        <!-- Logo and name section -->
        <div class="logo">
            <img src={image5} alt="Logo">
            <p>Wanderer</p>
        </div>

        <!-- Button section -->
        <div class="header-button">
            
            <a href="/started">Get started</a>
         
        
        </div>
       
    </div>

    <!-- Centered h1 -->
    <div class="centered-h1">
        <h1>Map your future</h1>
        </div>
        <div class="centered-p">
        <p>Wanderer is an AI-Powered tool that enables</p>
        <p>students and professionals to find their ideal</p>
        <p>career path.</p>
    </div>
    <div class="button-container">
        <button class="button1"> <a href="/started"> Try Wanderer for free -> </a></button>
       
    </div>
   <!-- ... (previous HTML code) ... -->

   <div class="review">
    <h1>Loved by tens of thousands around the world</h1>
    <div class="review-content">
        <div class="review-box">
            <div class="container">
                <div class="image1"><img src=  { image2 } alt="Profile"></div>
                <p class="user-name">@WILL_HAYESS33</p>
                <div class="image2"><img src=  { image4 } alt="Twitter"></div>
            </div>
            
            <div class="review-details"></div>
            <p class="review-text">
                💫 New year, new life goals?<br>
                
                Want to explore other life paths ahead of you?
                
                Discovered a 😎 tool that proposes alternatives based on interests & priorities.
                
                My results range from becoming an art gallery owner to a VC 🤣 🙃 Intriguing!
                
                </p>
            <p class="review-date">January 30, 2024</p>
        </div>
       
        <!-- Add more review content as needed -->
    
        
        <div class="review-box">
            <div class="container">
                <div class="image1"><img src= { image1 } alt="Profile"></div>
                <p class="user-name">@NATE_RAYCHELL</p>
                <div class="image2"><img src= { image4 } alt="Twitter"></div>
            </div>
            
            <div class="review-details"></div>
            <p class="review-text">What a perfect app to explore setting goals for the new year. The AI is super intutive describing why career paths would be fulfilling for you. </p>
            <p class="review-date">January 30, 2024</p>
        </div>
       
        <!-- Add more review content as needed -->
        
        <div class="review-box">
            <div class="container">
                <div class="image1"><img src= { image3 } alt="Profile"></div>
                <p class="user-name">@DAVIDTSONG</p>
                <div class="image2"><img src= { image4 } alt="Twitter"></div>
            </div>
            
        
            <p class="review-text">Prompted me to start learning something new last night. This is when a product really solves a need..🤩🤩🤩</p>
            <p class="review-date">January 30, 2024</p>
        </div>
    </div>
</div>



    

    <!-- Middle container with image and box -->
    <div class="middle-container">
        <div class="middle-box">
            <div class="middle">
                <img src=  { image5 } alt="Logo">
            </div>

        </div>
        <h1>Try Wanderer now</h1>
        <p>Get Started in minutes</p>
        <div class="button-container1">
            <button class="button2"> <a href="/sign-up"> Try it for free -> </a></button>
        </div>
    </div>
    <div class="footer">
        <p>@2023 Playground Education. All rights reserved</p>
        <ul>
            
            <li>Terms of Services</li>
            <li>Privacy Policy</li>
        </ul>
    </div>

</body>

 