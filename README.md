# FoltechSolutions.github.io
Foltech solutions deals with detecting software defects called bugs, System and Network challenge to Solutions. 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>FOLTECH QA SERVICES</title>
  <style>
    body {
      margin: 0;
      font-family: Arial, sans-serif;
      background: #f4f4f4;
    }

    header {
      display: flex;
      justify-content: space-between;
      align-items: center;
      padding: 15px 30px;
      background-color: #222;
      color: white;
    }

    .logo {
      font-size: 1.5em;
      font-weight: bold;
    }

    nav a {
      color: white;
      text-decoration: none;
      margin-left: 20px;
    }

    .scroll-text {
      background: #007acc;
      color: white;
      overflow: hidden;
      white-space: nowrap;
      box-sizing: border-box;
    }

    .scroll-text p {
      display: inline-block;
      padding-left: 100%;
      animation: scroll-left 15s linear infinite;
    }

    @keyframes scroll-left {
      0% {
        transform: translateX(100%);
      }
      100% {
        transform: translateX(-100%);
      }
    }

    .slideshow {
      max-width: 100%;
      position: relative;
      margin: auto;
      overflow: hidden;
    }

    .slides {
      display: flex;
      animation: slide 15s infinite;
      width: 300%;
    }

    .slides img {
      width: 100%;
    }

    @keyframes slide {
      0%   { transform: translateX(0); }
      33%  { transform: translateX(-100%); }
      66%  { transform: translateX(-200%); }
      100% { transform: translateX(0); }
    }

    .content {
      text-align: center;
      padding: 40px 20px;
    }

    .content h1 {
      font-size: 2.5em;
      margin-bottom: 20px;
    }

    .ai-image {
      max-width: 300px;
      margin: 20px auto;
    }

    .apply-button {
      display: inline-block;
      margin-top: 20px;
      padding: 10px 25px;
      font-size: 1em;
      background-color: #007acc;
      color: white;
      text-decoration: none;
      border-radius: 5px;
    }

    footer {
      background-color: #222;
      color: white;
      text-align: center;
      padding: 20px;
    }
  </style>
</head>
<body>

  <header>
    <div class="logo">FOLTECH SOLUTIONS LOGO</div>
    <nav>
      <a href="#">Home</a>
      <a href="#">About Us</a>
      <a href="#">Services</a>
      <a href="#">Events</a>
      <a href="#">Projects</a>
      <a href="#">Contact</a>
    </nav>
  </header>

  <div class="scroll-text">
    <p>Welcome to FOLTECH SOLUTIONS- Turning- Turning your Challenges to Solutions is our Priority</p>
  by changing challenges to solution </div>

  <div class="slideshow">
    <div class="slides">
      <img src="https://via.placeholder.com/1200x400?text=Slide+1" alt="QA Solutions">
      <img src="https://via.placeholder.com/1200x400?text=Slide+2" alt="Network Solutions">
      <img src="https://via.placeholder.com/1200x400?text=Slide+3" alt="System Solutions">
    </div>
  </div>

  <div class="content">
    <h1>Welcome to FOLTECH SOLUTIONS</h1>
    <img class="ai-image" src="https://via.placeholder.com/300x200?text=AI+Computer" alt="AI Computers">
    <br>
    <a class="apply-button" href="webpay.html">Click here to Apply for our program</a>
  </div>
 <script>
  document.querySelector('.apply-button').addEventListener('click', function(event) {
    alert('Thank you for your interest! We will review your application.');
  });
</script>
  <footer>
    <p>Email: info@foltech.com | Phone: +234-810-975-0268</p>
    <p>&copy; 2025 FOLTECH SOLUTIONS. All rights reserved.</p>
  </footer>

</body>
</html>
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
<title>My Web Page</title>
<style>
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 15px 30px;
    background-color: #222;
    color: white;
  }
  .logo {
    font-size: 1.5em;
    font-weight: bold;
  }
  nav a {
    color: white;
    text-decoration: none;
    margin-left: 20px;
  }
  .scroll-text {
    background: #007acc;
    color: white;
    overflow: hidden;
    white-space: nowrap;
    box-sizing: border-box;
    padding: 10px;
  }
  /* Additional styles for form */
  .contact-form {
    max-width: 500px;
    margin: 20px auto;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 8px;
  }
  .contact-form label {
    display: block;
    margin-top: 10px;
  }
  .contact-form input, 
  .contact-form textarea {
    width: 100%;
    padding: 8px;
    margin-top: 4px;
    box-sizing: border-box;
    border-radius: 4px;
    border: 1px solid #ccc;
  }
  .contact-form button {
    margin-top: 15px;
    padding: 10px 20px;
    background-color: #222;
    color: white;
    border: none;
    border-radius: 4px;
    cursor: pointer;
  }
  .error {
    color: red;
    font-size: 0.9em;
  }
</style>
</head>
<body>

<header>
  <div class="logo">MyLogo</div>
  <nav>
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </nav>
</header>

<div class="scroll-text">This is scrolling text for announcements or updates!</div>

<!-- Contact Form -->
<form class="contact-form" id="myForm" novalidate>
  <h2>Contact Us</h2>
  <label for="name">Name:</label>
  <input type="text" id="name" name="name" required />
  <div class="error" id="nameError"></div>

  <label for="email">Email:</label>
  <input type="email" id="email" name="email" required />
  <div class="error" id="emailError"></div>

  <label for="message">Message:</label>
  <textarea id="message" name="message" rows="4" required></textarea>
  <div class="error" id="messageError"></div>

  <button type="submit">Send Message</button>
  <div id="formSuccess" style="color: green; margin-top: 10px;"></div>
</form>

<script>
  document.getElementById('myForm').addEventListener('submit', function(e) {
    e.preventDefault(); // Prevent form from submitting

    // Clear previous errors
    document.getElementById('nameError').textContent = '';
    document.getElementById('emailError').textContent = '';
    document.getElementById('messageError').textContent = '';
    document.getElementById('formSuccess').textContent = '';

    // Get form values
    const name = document.getElementById('name').value.trim();
    const email = document.getElementById('email').value.trim();
    const message = document.getElementById('message').value.trim();

    let valid = true;

    // Validate Name
    if (name === '') {
      document.getElementById('nameError').textContent = 'Please enter your name.';
      valid = false;
    }

    // Validate Email
    const emailPattern = /^[^ ]+@[^ ]+\.[a-z]{2,3}$/;
    if (email === '') {
      document.getElementById('emailError').textContent = 'Please enter your email.';
      valid = false;
    } else if (!email.match(emailPattern)) {
      document.getElementById('emailError').textContent = 'Please enter a valid email.';
      valid = false;
    }

    // Validate Message
    if (message === '') {
      document.getElementById('messageError').textContent = 'Please enter your message.';
      valid = false;
    }

    if (valid) {
      // You can add form submission logic here (like AJAX)
      document.getElementById('formSuccess').textContent = 'Thank you! Your message has been sent.';
      
      // Optionally, reset form after submission
      document.getElementById('myForm').reset();
    }
  });
</script>

</body>
</html>
