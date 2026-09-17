<!DOCTYPE html>

<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>AI Workplace Assistant</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

```
body {
  background: #f4f6f8;
  color: #222;
}

header {
  background: #1f4e79;
  color: white;
  padding: 30px;
  text-align: center;
}

header h1 {
  margin-bottom: 10px;
}

header p {
  font-size: 16px;
}

.container {
  max-width: 1100px;
  margin: 30px auto;
  padding: 20px;
}

.tools {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
}

.card {
  background: white;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
}

.card h2 {
  color: #1f4e79;
  margin-bottom: 10px;
}

.card p {
  margin-bottom: 15px;
  line-height: 1.5;
}

textarea, input, select {
  width: 100%;
  padding: 12px;
  margin: 8px 0;
  border: 1px solid #ccc;
  border-radius: 6px;
}

textarea {
  min-height: 100px;
  resize: vertical;
}

button {
  background: #1f4e79;
  color: white;
  border: none;
  padding: 12px 18px;
  border-radius: 6px;
  cursor: pointer;
  margin-top: 8px;
}

button:hover {
  background: #163a5a;
}

.result {
  margin-top: 15px;
  padding: 15px;
  background: #eef4f8;
  border-radius: 6px;
  min-height: 50px;
  white-space: pre-wrap;
}

.about {
  background: white;
  margin-top: 30px;
  padding: 25px;
  border-radius: 12px;
  box-shadow: 0 3px 10px rgba(0,0,0,0.1);
}

.about h2 {
  color: #1f4e79;
  margin-bottom: 10px;
}

footer {
  text-align: center;
  padding: 25px;
  margin-top: 30px;
  background: #1f4e79;
  color: white;
}
```

  </style>
</head>

<body>

<header>
  <h1>AI Workplace Assistant</h1>
  <p>AI-powered tools for everyday workplace tasks</p>
</header>

<div class="container">

  <div class="tools">

```
<div class="card">
  <h2>📧 Email Generation</h2>
  <p>Create a professional workplace email.</p>

  <input id="emailTopic" placeholder="What is the email about?">

  <select id="emailTone">
    <option>Professional</option>
    <option>Friendly</option>
    <option>Formal</option>
  </select>

  <button onclick="generateEmail()">Generate Email</button>

  <div class="result" id="emailResult"></div>
</div>

<div class="card">
  <h2>📝 Meeting Summarization</h2>
  <p>Turn meeting notes into a short summary.</p>

  <textarea id="meetingNotes" placeholder="Paste your meeting notes here..."></textarea>

  <button onclick="summarizeMeeting()">Summarize Meeting</button>

  <div class="result" id="meetingResult"></div>
</div>

<div class="card">
  <h2>📋 Task Planning</h2>
  <p>Break a goal into smaller tasks.</p>

  <input id="taskGoal" placeholder="Enter your goal">

  <button onclick="planTasks()">Create Task Plan</button>

  <div class="result" id="taskResult"></div>
</div>

<div class="card">
  <h2>🔎 Research Assistance</h2>
  <p>Get an organised explanation of a topic.</p>

  <input id="researchTopic" placeholder="Enter a research topic">

  <button onclick="researchTopic()">Research</button>

  <div class="result" id="researchResult"></div>
</div>

<div class="card">
  <h2>💬 AI Chatbot</h2>
  <p>Ask the workplace assistant a question.</p>

  <input id="chatQuestion" placeholder="Ask a question...">

  <button onclick="chatbot()">Send</button>

  <div class="result" id="chatResult"></div>
</div>
```

  </div>

  <div class="about">
    <h2>About This Project</h2>

```
<p>
  My AI Workplace Assistant is an AI-powered solution designed to help
  automate common workplace tasks such as email generation, meeting
  summarization, task planning, research assistance, and chatbot interaction.
</p>

<br>

<p>
  This project demonstrates the use of AI tools such as ChatGPT,
  Google Gemini, and Notion AI, as well as prompt engineering and
  responsible and ethical AI use.
</p>

<br>

<h3>Responsible AI Use</h3>

<p>
  AI-generated information should be checked for accuracy. Users should
  avoid entering confidential or sensitive information into AI tools.
  Human oversight is important when using AI for important decisions.
</p>
```

  </div>

</div>

<footer>
  AI Workplace Assistant | Built as an AI Skills Project | Responsible AI Use
</footer>

<script>

function generateEmail() {
  const topic = document.getElementById("emailTopic").value;
  const tone = document.getElementById("emailTone").value;

  if (!topic) {
    document.getElementById("emailResult").innerText =
      "Please enter what the email is about.";
    return;
  }

  document.getElementById("emailResult").innerText =
`Subject: ${topic}

Dear Manager,

I am writing regarding ${topic}.

I would like to provide you with the necessary information and kindly ask for your consideration.

Thank you for your time.

Kind regards,
Precious

Tone: ${tone}`;
}

function summarizeMeeting() {
  const notes = document.getElementById("meetingNotes").value;

  if (!notes) {
    document.getElementById("meetingResult").innerText =
      "Please enter your meeting notes.";
    return;
  }

  document.getElementById("meetingResult").innerText =
`Meeting Summary:

• Main discussion:
${notes}

• Key action:
Review the information discussed and complete the required tasks.

• Follow-up:
Check progress and communicate any updates with the team.`;
}

function planTasks() {
  const goal = document.getElementById("taskGoal").value;

  if (!goal) {
    document.getElementById("taskResult").innerText =
      "Please enter a goal.";
    return;
  }

  document.getElementById("taskResult").innerText =
`Task Plan for: ${goal}

1. Define the main objective.
2. Break the objective into smaller tasks.
3. Complete the most important task first.
4. Review your progress.
5. Complete and check the final result.`;
}

function researchTopic() {
  const topic = document.getElementById("researchTopic").value;

  if (!topic) {
    document.getElementById("researchResult").innerText =
      "Please enter a research topic.";
    return;
  }

  document.getElementById("researchResult").innerText =
`Research Topic: ${topic}

Key Points:

• Understand the meaning and purpose of the topic.
• Identify the main facts and important information.
• Organise the information into clear points.
• Compare information from reliable sources.

Important: Always verify important information using reliable sources.`;
}

function chatbot() {
  const question = document.getElementById("chatQuestion").value;

  if (!question) {
    document.getElementById("chatResult").innerText =
      "Please enter a question.";
    return;
  }

  document.getElementById("chatResult").innerText =
`AI Workplace Assistant:

Thank you for your question.

"${question}"

I can help you organise your work, create plans, draft workplace communication, summarise information, and explain workplace topics.

Please remember to review AI-generated information before using it.`;
}

</script>

</body>
</html>
