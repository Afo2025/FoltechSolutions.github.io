FoltechSolutions.github.io
Foltech solutions deals with detecting software defects called bugs, System and Network challenge to Solutions. 
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>FOLTECH QA SERVICES</title>
  <style>
    body {<div>


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
    <p>Welcome to FOLTECH SOLUTIONS- Here we turn your software Challenges to Solutions</p>
  "Foltech does IT Better" </div>

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
  <h2>Ask the AI</h2>
  <textarea id="userInput" rows="4" cols="50" placeholder="Ask me anything..."></textarea><br>
  <button onclick="askAI()">Send</button>
  <p><strong>AI Response:</strong></p>
  <div id="response"></div>
</div>

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

    .logo {<img src="/assets/img/your-logo.png" alt="Your Website Logo" width="100" height="50">
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
  </sript>
</head>
<body>

</body><script>
  async function askAI() {
    const prompt = document.getElementById("userInput").value;

    const responseDiv = document.getElementById("response");
    responseDiv.innerHTML = "Thinking...";
    const res = await fetch("https://foltech-solutions-github-io.vercel.app/api/chat", /completions", {
      method: "POST",
      headers: {
        "Content-Type": "application/json",
        "Authorization": "Bearer YOUR_OPENAI_API_KEY"
      },
      body: JSON.stringify({
        model: "gpt-3.5-turbo",
        messages: [{ role: "user", content: prompt }]
      })
    });

    const data = await res.json();
    const aiText = data.choices?.[0]?.message?.content;
    responseDiv.innerHTML = aiText || "No response.";
  }
</script>
</html>
    <a class="apply-button" href="webpay.html">Click here to Apply for our program</a>
  </div> ) 
  {
 <('Thank you for your interest! We will review your application.')>;
  
  <footer>
    <p>Email: info@foltech.com | Phone: +234-810-975-0268</p>
    <p>&copy; 2025 FOLTECH SOLUTIONS. All rights reserved.</p>
  </footer>
  
