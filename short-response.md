# Short Response Questions

Answer each question below in your own words. Aim for 3–5 sentences per answer. Be specific — use the exact terms and concepts from the lesson.

Your responses will each be evaluated out of 6 points. You can earn 3 points for writing quality and 3 points for the accuracy and precision of the technical content per question.

---

## Question 1:

Why is it unsafe to make requests to a third-party API (like Giphy) directly from frontend JavaScript code? What specific risk does this create, and how can a malicious user exploit it?

**Your answer here**:

---

Making requests directly from the frontend is unsafe because your API key is visible to anyone who opens the browser's DevTools. They can just steal it and use it as their own. By using a server instead, the API key stays hidden in the
.env file and nobody can see it.

## Question 2:

What is the proxy server strategy? How does it help avoid exposing API Keys in client-side code while still providing access to APIs that require keys?

**Your answer here**:

---

A proxy server is basically a middleman between your frontend and the API. Instead of your frontend talking directly to Giphy, it talks to your own server, and your server talks to Giphy. That way the API key stays on the server and never reaches the browser where someone could steal it.

## Question 3:

What is an environment variable, and why do we store API keys in a .env file instead of directly in source code? What role does .gitignore play in this setup, and what could go wrong if the .env file were accidentally committed to GitHub?

**Your answer here**:

---

An environment variable is a variable that lives outside of your code on your server. We store API keys there so they don't show up in the source code. The .gitignore makes sure the .env file never gets pushed to GitHub. If it did get pushed, anyone could just go to your repo and grab your API key.
