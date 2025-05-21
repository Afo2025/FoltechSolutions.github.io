#<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0"/>
  <title>AI Chatbot</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #f4f4f4;
      padding: 2rem;
    }
    .chat-container {
      max-width: 600px;
      margin: auto;
      background: white;
      padding: 20px;
      border-radius: 10px;
      box-shadow: 0 0 15px rgba(0,0,0,0.1);
    }
    textarea {
      width: 100%;
      padding: 10px;
      margin-top: 10px;
      font-size: 1rem;
      border-radius: 5px;
      border: 1px solid #ccc;
      resize: none;
    }
    button {
      margin-top: 10px;
      padding: 10px 20px;
      font-size: 1rem;
      background-color: #0078d4;
      color: white;
      border: none;
      border-radius: 5px;
      cursor: pointer;
    }
    #response {
      margin-top: 20px;
      white-space: pre-wrap;
      background-color: #f9f9f9;
      padding: 10px;
      border-left: 4px solid #0078d4;
    }
  </style>
</head>
<body>

  <div class="chat-container">
    <h2>AI Chatbot</h2>
    <textarea id="userInput" rows="4" placeholder="Ask me anything..."></textarea>
    <button onclick="askAI()">Send</button>
    <div id="response"></div>
  </div>

  <script>
    async function askAI() {
      const prompt = document.getElementById("userInput").value;
      const responseDiv = document.getElementById("response");
      responseDiv.textContent = "Thinking...";

      try {
        const res = await fetch("https://afo-chatbot.vercel.app/api/chat", {  // Replace with your real domain
          method: "POST",
          headers: {
            "Content-Type": "application/json"
          },
          body: JSON.stringify({ prompt })
        });

        const data = await res.json();
        responseDiv.textContent = data.response || "No response.";
      } catch (err) {
        console.error(err);
        responseDiv.textContent = "Error connecting to AI.";
      }
    }
  </script>

</body>
</html>
