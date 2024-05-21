<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Password generator</title>
</head>
<body>

    <!-- Header Section -->
    <header class="header">
        <div class="header-container">
            <h1>LOCK-P</h1>
           
             <nav>
                <ul>
                    <li><a href="contact1.html"><h4>Contact</h4></a></li>
                    <li><a href="login.html"><h4>Login</h4></a></li>
                </ul>
            </nav>

        </div>
    </header>





  
    <div class="mmm">***PASSWORD***</div>
    <div class="container">

        <h2>Password Generator</h2>

        <div class="display-content">
            <input readonly placeholder="Password" class="display" data-passwordDisplay>

            <button data-copy>
                <span data-copyMsg></span>
                <img src="copyimage.png" alt="copy" width="23" height="23">
            </button>
        </div>

        <!-- Password Length Section -->
        <div class="input-container">

            <div class="length-container">
                <p>Password Length</p>
                <p data-lengthNumber>0</p>
            </div>

        </div>

        <!-- Slider -->
        <input type="range" min="0" max="20" class="slide" step="1" data-lengthSlider>

        <!-- Check boxes -->
        <!-- Upper CASE -->
        <div>
            <input type="checkbox" id="uppercase">
            <label for="uppercase">Include Uppercase Letters</label>
        </div>

        <!-- Lower CASE -->
        <div>
            <input type="checkbox" id="lowercase">
            <label for="lowercase">Include lowercase Letters</label>
        </div>

        <!-- Numbers -->
        <div>
            <input type="checkbox" id="numbers">
            <label for="Numbers">Include Numbers </label>
        </div>

        <!-- Symbols -->
        <div>
            <input type="checkbox" id="symbols">
            <label for="Symbols">Include Symbols</label>
        </div>

        <!-- Strength Section -->
        <div class="strength-container">
            <p>Strength</p>
            <div data-indicator></div>
        </div>

        <!-- generate password button -->
        <button class="generateButton">Generate Password</button>

    </div>
    <div class="moving-text">***PROTECT----PASSWORD***</div>

    <!-- Footer Section -->
    <footer class="footer">
        <div class="footer-container">
            <div class="about">
                <h3>About Our Website</h3>
                <p>Welcome to LOCK-P, your go-to destination for generating secure passwords. We provide a simple and efficient tool to create strong passwords tailored to your needs. Protect your accounts with confidence using LOCK-P!</p>
            </div>

        </div>
    </footer>

<style>
/* General Styles */
body {
    font-family: Arial, sans-serif;
    background-image: url('bp.webp'); /* Add the path to your background image */
    background-size: cover;
    background-repeat: no-repeat;
    margin: 10px;
    padding: 0;
     
}


.header-container {
    text-shadow: 5px 5px 5px rgba(13, 28, 13, 0.9);
    padding: 10px; /* Add padding to give space between content and border */
    position: relative; /* Ensure the container is positioned relatively */
}

/* Create a fading dot border */
.header-container::before {
    content: '';
    position: absolute;
    top: -6px;
    right: -6px;
    bottom: -6px;
    left: -6px;
    border: 6px dotted #F5DEB3; /* Adjust the border style and color */
    border-radius: 15px; /* Adjust the border radius */
    animation: fadeInBorder 2s infinite alternate; /* Add the fade-in animation */
}

@keyframes fadeInBorder {
    0% {
        opacity: 0;
    }
    100% {
        opacity: 1;
    }
}


.header-container {
    text-shadow: 5px 5px 5px rgb(13, 28, 13, 0.9);/* Add a white border */
    padding: 10px; /* Add padding to give space between content and border */
}

/* Add more CSS styles as needed */

/* Add this CSS to position the locker logo image */
.locker-logo {
    position: fixed;
    top: 50%;
    left: 50%;
    transform: translate(-50%, -50%);
    z-index: 9999; /* Ensure the logo appears above other content */
    opacity: 0.1; /* Optionally adjust the opacity */
}

/* Style for the navigation list */
.header nav ul {
    list-style: none;
    margin: 0;
    padding: 0;
}

/* Style for the list items */
.header nav ul li {
    display: inline-block;
    margin-right: 20px; /* Adjust as needed */
}

/* Style for the anchor tags */
.header nav ul li a {
    text-decoration: none;
    color: #333; /* Adjust as needed */
}

/* Style for the contact and login logos */
.header nav ul li a img {
    width: 30px; /* Adjust width as needed */
    height: 30px; /* Adjust height as needed */
}

/* Example footer styles */
.footer {
    background-color: #f0f0f0; /* Adjust background color as needed */
    padding: 20px;
    text-align: center;
}



.container {
    position: relative;
    max-width: 600px;
    margin: 50px auto;
    padding: 20px;
    /*background-image: url('locker.webp'); /* Replace 'your_image.jpg' with the path to your image */
    background-size: cover;
    background-repeat: no-repeat;

    box-shadow: 10px 10px 10px rgba(168, 104, 16, 1);
    min-height: 600px;

    /* Add the double round solid and dot border with yellow color */
    border: 4px double yellow;
    border-radius: 15px; /* Adjust as needed */
     animation: fadeIn 5s forwards;
    /* Adjust image opacity */
    background-color: #C4A484; 
    opacity: 0.9;/* Adjust the alpha channel (0.0 to 1.0) */
}





.moving-text {
    position: relative;
    text-align: center;
    color: #FFD700; /* Set text color to gold */
    background-color: #8B4513; /* Set background color to brown */
    padding: 10px; /* Add padding for better visibility */
    animation: moveText 1s linear infinite alternate;
    width: 150px; /* Adjust the width as needed */
    margin: 0 auto; /* Center the element horizontally */
}

@keyframes moveText {
    0% {
        transform: translateY(0);
    }

    100% {
        transform: translateY(-20px);
    }
}

.header {
    background-color:#6F4E37; /* Header background color */
    color: #FFD700; /* Text color */
    padding: 10px 0;
    margin-bottom: 20px; /* Add margin-bottom */
}

.header-container {
    max-width: 960px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}

.header h1 {
    margin: 0;
    font-size: 24px;
}

.header nav ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}

.header nav ul li {
    display: inline-block;
    margin-right: 20px;
}

.header nav ul li:last-child {
    margin-right: 0;
}

.header nav ul li a {
    color: #edcece;
    text-decoration: none;
}

.display-content {
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin-bottom: 100px;
}

.display {
    width: 70%;
    padding: 10px;
    border: 1px solid #17c5e8;
    border-radius: 4px;
}

button {
    background-color: #722F37;
    color: #fff;
    border: none;
    padding: 10px;
    border-radius: 4px;
    cursor: pointer;
    transition: background-color 0.3s ease;
}

button:hover {
    background-color: #CC7722;
}

input[type="range"] {
    width: 100%;
    margin-bottom: 20px;
}

/* Styles for the thumb (handle) */
input[type="range"]::-webkit-slider-thumb {
    -webkit-appearance: none; /* Remove default styling */
    appearance: none;
    width: 15px; /* Adjust the width of the thumb */
    height: 15px; /* Adjust the height of the thumb */
    background-color: brown; /* Set the color of the thumb */
    border-radius: 50%; /* Round the thumb */
    cursor: pointer; /* Show pointer cursor */
}

/* Styles for the track */
input[type="range"]::-webkit-slider-runnable-track {
    width: 100%; /* Set the width of the track */
    height: 5px; /* Set the height of the track */
    background-color: brown; /* Set the color of the track */
    border-radius: 5px; /* Round the track */
    cursor: pointer; /* Show pointer cursor */
}

input[type="checkbox"] {
    margin-right: 5px;
}

.strength-container {
    text-align: center;
    margin-bottom: 20px;
}

[data-indicator] {
    width: 100%;
    height: 50px;
    background-color: #fafafa;
    border-radius: 5px;
}

[data-indicator]::after {
    content: '';
    display: block;
    width: 0;
    height: 100%;
    background-color: #2ace27;
    border-radius: 5px;
    transition: width 0.3s ease;
}

/* Footer Styles */
.footer {
    background-color: #333; /* Footer background color */
    color: #fff; /* Text color */
    padding: 20px 0;
}

.footer-container {
    max-width: 960px;
    margin: 0 auto;
    padding: 0 20px;
    display: flex;
    justify-content: space-between;
}

.about,
.welcome {
    flex: 1;
    padding: 0 20px;
}

.about h3,
.welcome h3 {
    margin-top: 0;
}

.about p,
.welcome p {
    margin-bottom: 0;
}

.moving-text {
    position: relative;
    text-align: center;
    color: #FFD700; /* Set text color to gold */
    background-color: #654321; /* Set background color to brown */
    padding: 10px; /* Add padding for better visibility */
    animation: moveText 1s linear infinite alternate;
    width: 150px; /* Adjust the width as needed */
    margin: 0 auto; /* Center the element horizontally */
}

@keyframes moveText {
    0% {
        transform: translateY(0);
    }

    100% {
        transform: translateY(-20px);
    }
}

.mmm {
   position: relative;
    text-align: center;
    color: #1a180a; /* Set text color */
    background-color: #f9cb9f; /* Set background color */
    padding: 10px; /* Add padding for better visibility */
    width: 150px; /* Adjust the width as needed */
    margin: 0 auto; /* Center the element horizontally */
    animation: fadeIn 5s forwards; /* Corrected animation property */
    border: 2px solid #000000;
}

@keyframes fadeIn {
    0% { opacity: 0; }
    100% { opacity: 1; }
}
</style>

    <script>
const inputSlider = document.querySelector("[data-lengthSlider]");
const lengthDisplay = document.querySelector("[data-lengthNumber]");
const passwordDisplay = document.querySelector("[data-passwordDisplay]");
const copyBtn = document.querySelector("[data-copy]");
const copyMsg = document.querySelector("[data-copyMsg]");
const uppercaseCheck = document.querySelector("#uppercase");
const lowercaseCheck = document.querySelector("#lowercase");
const numbersCheck = document.querySelector("#numbers");
const symbolsCheck = document.querySelector("#symbols");
const indicator = document.querySelector("[data-indicator]");
const generateBtn = document.querySelector(".generateButton");
const allCheckBox = document.querySelectorAll("input[type=checkbox]");
const symbols = '~`!@#$%^&*()_-+={[}]|:;"<,>.?/';

let password = "";
let passwordLength = 10;
let checkCount = 0;
handleSlider();

function handleSlider() {
    inputSlider.value = passwordLength;
    lengthDisplay.innerText = passwordLength;
}

function setIndicator(color) {
    indicator.style.backgroundColor = color;
}

function getRanInteger(min, max) {
    return Math.floor(Math.random() * (max - min)) + min;
}

function generateRandomNumber() {
    return getRanInteger(0, 10);
}

function generateLowercase() {
    return String.fromCharCode(getRanInteger(97, 123));
}

function generateUppercase() {
    return String.fromCharCode(getRanInteger(65, 91));
}

function generateSymbols() {
    const randNum = getRanInteger(0, symbols.length);
    return symbols.charAt(randNum);
}

function calcStrength() {
    let hasUpper = false;
    let hasLower = false;
    let hasNum = false;
    let hasSym = false;
    if (uppercaseCheck.checked) hasUpper = true;
    if (lowercaseCheck.checked) hasLower = true;
    if (numbersCheck.checked) hasNum = true;
    if (symbolsCheck.checked) hasSym = true;

    if (hasUpper && hasLower && (hasNum || hasSym) && passwordLength >= 8) {
        setIndicator("#0f0");
    } else if ((hasLower || hasUpper) && (hasNum || hasSym) && passwordLength >= 6) {
        setIndicator("#ff0");
    } else {
        setIndicator("#f00");
    }
}

async function copyContent() {
    try {
        await navigator.clipboard.writeText(passwordDisplay.value);
        copyMsg.innerText = "Copied";
    } catch (e) {
        copyMsg.innerText = "Failed";
    }
    copyMsg.classList.add("active");
    setTimeout(() => {
        copyMsg.classList.remove("active");
        copyBtn.innerText = "Copy"; // Reset copy button text
    }, 2000);

    // Clear password display after copying
    passwordDisplay.value = '';
}

function shufflePassword(array) {
    for (let i = array.length - 1; i > 0; i--) {
        const j = Math.floor(Math.random() * (i + 1));
        const temp = array[i];
        array[i] = array[j];
        array[j] = temp;
    }
    return array.join('');
}

function handleCheckBoxChange() {
    checkCount = 0;
    allCheckBox.forEach((checkbox) => {
        if (checkbox.checked) checkCount++;
    });

    if (passwordLength < checkCount) {
        passwordLength = checkCount;
        handleSlider();
    }
}

allCheckBox.forEach((checkbox) => {
    checkbox.addEventListener('change', handleCheckBoxChange);
});

inputSlider.addEventListener('input', (e) => {
    passwordLength = e.target.value;
    handleSlider();
});

copyBtn.addEventListener('click', () => {
    if (passwordDisplay.value) {
        copyContent();
        // Change copy button text to "Copied" after clicking
        copyBtn.innerText = "Copied";
    }
});

generateBtn.addEventListener('click', () => {
    if (checkCount == 0)
        return;

    if (passwordLength < checkCount) {
        passwordLength = checkCount;
        handleSlider();
    }

    password = "";

    let funcArr = [];

    if (uppercaseCheck.checked)
        funcArr.push(generateUppercase);

    if (lowercaseCheck.checked)
        funcArr.push(generateLowercase);

    if (numbersCheck.checked)
        funcArr.push(generateRandomNumber);

    if (symbolsCheck.checked)
        funcArr.push(generateSymbols);

    for (let i = 0; i < funcArr.length; i++) {
        password += funcArr[i]();
    }

    for (let i = 0; i < passwordLength - funcArr.length; i++) {
        let randIndex = getRanInteger(0, funcArr.length);
        password += funcArr[randIndex]();
    }

    password = shufflePassword(Array.from(password));
    passwordDisplay.value = password;
    calcStrength();
})</script>
</body>
</html>
