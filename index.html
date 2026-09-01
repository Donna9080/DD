<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Boston Roomie Match</title>
  <style>
    * {
      box-sizing: border-box;
      margin: 0;
      padding: 0;
      font-family: Arial, sans-serif;
    }

    body {
      background: linear-gradient(180deg, #0a1f44, #102b5c);
      color: #fff;
      min-height: 100vh;
      display: flex;
      justify-content: center;
      align-items: center;
      padding: 20px;
    }

    .app {
      width: 100%;
      max-width: 420px;
      background: rgba(255, 255, 255, 0.08);
      border: 1px solid rgba(255,255,255,0.12);
      border-radius: 24px;
      padding: 24px;
      box-shadow: 0 20px 50px rgba(0,0,0,0.35);
      backdrop-filter: blur(10px);
    }

    .logo {
      font-size: 28px;
      font-weight: 800;
      margin-bottom: 8px;
    }

    .sub {
      color: #c9d7ff;
      font-size: 14px;
      margin-bottom: 24px;
      line-height: 1.5;
    }

    .screen {
      display: none;
    }

    .screen.active {
      display: block;
    }

    .question-tag {
      display: inline-block;
      background: #1d3d7a;
      color: #dce8ff;
      padding: 6px 12px;
      border-radius: 999px;
      font-size: 12px;
      margin-bottom: 12px;
    }

    .question {
      font-size: 24px;
      font-weight: 700;
      margin-bottom: 18px;
    }

    .answers {
      display: grid;
      gap: 12px;
    }

    .answer-btn, .action-btn, .start-btn, .restart-btn {
      border: none;
      border-radius: 16px;
      padding: 14px 16px;
      font-size: 16px;
      cursor: pointer;
      transition: 0.2s ease;
    }

    .answer-btn {
      background: #ffffff;
      color: #0a1f44;
      text-align: left;
      font-weight: 600;
    }

    .answer-btn:hover {
      transform: translateY(-2px);
      background: #eaf1ff;
    }

    .start-btn, .restart-btn {
      width: 100%;
      background: #7fb3ff;
      color: #08204d;
      font-weight: 800;
      margin-top: 12px;
    }

    .start-btn:hover, .restart-btn:hover {
      background: #a4c8ff;
    }

    .progress {
      margin-top: 18px;
      font-size: 13px;
      color: #c9d7ff;
    }

    .loading {
      text-align: center;
      padding: 30px 0;
    }

    .loading h2 {
      margin-bottom: 10px;
    }

    .card {
      background: #ffffff;
      color: #0a1f44;
      border-radius: 24px;
      padding: 22px;
      box-shadow: 0 15px 35px rgba(0,0,0,0.2);
    }

    .match-label {
      font-size: 13px;
      font-weight: 700;
      color: #476fb8;
      margin-bottom: 10px;
      text-transform: uppercase;
      letter-spacing: 0.08em;
    }

    .match-name {
      font-size: 28px;
      font-weight: 800;
      margin-bottom: 8px;
    }

    .fit-score {
      display: inline-block;
      background: #e8f0ff;
      color: #163d80;
      padding: 8px 12px;
      border-radius: 999px;
      font-weight: 700;
      font-size: 14px;
      margin-bottom: 14px;
    }

    .card p {
      margin-bottom: 10px;
      line-height: 1.5;
    }

    .actions {
      display: grid;
      grid-template-columns: 1fr 1fr 1fr;
      gap: 10px;
      margin-top: 18px;
    }

    .deny { background: #ffe3e3; color: #8a1f1f; }
    .accept { background: #e4f7ea; color: #176537; }
    .request { background: #dce8ff; color: #163d80; }

    .action-btn:hover {
      transform: translateY(-2px);
      opacity: 0.95;
    }

    .small-note {
      margin-top: 14px;
      font-size: 12px;
      color: #c9d7ff;
      text-align: center;
    }

    .result-message {
      text-align: center;
      padding: 20px 0;
    }

    .result-message h2 {
      margin-bottom: 10px;
    }
  </style>
</head>
<body>
  <div class="app">
    <div class="logo">RoomieMatch Boston</div>
    <div class="sub">Fast. Fun. Find your top 3 roommate matches.</div>

    <div id="startScreen" class="screen active">
      <div class="question">Find your Boston roommate vibe ✨</div>
      <div class="sub">Answer 5 quick questions with one tap.</div>
      <button class="start-btn" onclick="startQuiz()">Start Quiz</button>
    </div>

    <div id="quizScreen" class="screen">
      <div class="question-tag" id="questionTag">Question 1</div>
      <div class="question" id="questionText"></div>
      <div class="answers" id="answersBox"></div>
      <div class="progress" id="progressText"></div>
    </div>

    <div id="loadingScreen" class="screen">
      <div class="loading">
        <h2>Finding your top 3 matches...</h2>
        <div class="sub">Checking budget, vibe, habits, and location.</div>
      </div>
    </div>

    <div id="matchScreen" class="screen">
      <div class="card">
        <div class="match-label" id="matchLabel">Top Match</div>
        <div class="match-name" id="matchName"></div>
        <div class="fit-score" id="fitScore"></div>
        <p><strong>Vibe:</strong> <span id="matchVibe"></span></p>
        <p><strong>Why:</strong> <span id="matchWhy"></span></p>
        <p><strong>Area:</strong> <span id="matchArea"></span></p>
        <div class="actions">
          <button class="action-btn deny" onclick="handleAction('Denied')">Deny</button>
          <button class="action-btn accept" onclick="handleAction('Accepted')">Accept</button>
          <button class="action-btn request" onclick="handleAction('Request Sent')">Request</button>
        </div>
      </div>
      <div class="small-note" id="matchCounter"></div>
    </div>

    <div id="endScreen" class="screen">
      <div class="result-message">
        <h2>You reached your top matches 🎉</h2>
        <div class="sub" id="finalMessage">Nice work finding your roommate vibe.</div>
        <button class="restart-btn" onclick="restartApp()">Try Again</button>
      </div>
    </div>
  </div>

  <script>
    const questions = [
      {
        tag: "Budget Check",
        text: "Budget?",
        answers: [
          "1. Under $800",
          "2. $800–$1200",
          "3. $1200–$1600",
          "4. $1600+"
        ]
      },
      {
        tag: "Clean Room Energy",
        text: "Cleanliness?",
        answers: [
          "1. Very neat",
          "2. Pretty tidy",
          "3. Chill",
          "4. Messy is okay"
        ]
      },
      {
        tag: "Sleep Style",
        text: "Your schedule?",
        answers: [
          "1. Early bird",
          "2. Mostly early",
          "3. Night owl",
          "4. Very late nights"
        ]
      },
      {
        tag: "Weekend Vibes",
        text: "Home vibe?",
        answers: [
          "1. Quiet",
          "2. Balanced",
          "3. Social",
          "4. Always active"
        ]
      },
      {
        tag: "Boston Spot",
        text: "Best area?",
        answers: [
          "1. Allston/Brighton",
          "2. Fenway/Brookline",
          "3. Cambridge/Somerville",
          "4. Anywhere easy to commute"
        ]
      }
    ];

    const roommates = [
      {
        name: "Maya",
        vibe: "Calm and focused",
        area: "Fenway / Brookline",
        traits: [2, 1, 1, 1, 2]
      },
      {
        name: "Jordan",
        vibe: "Balanced and easygoing",
        area: "Cambridge / Somerville",
        traits: [3, 2, 2, 2, 3]
      },
      {
        name: "Sofia",
        vibe: "Social but respectful",
        area: "Allston / Brighton",
        traits: [2, 2, 3, 3, 1]
      },
      {
        name: "Ethan",
        vibe: "Quiet and organized",
        area: "Fenway / Longwood",
        traits: [3, 1, 1, 1, 2]
      },
      {
        name: "Nina",
        vibe: "Fun and outgoing",
        area: "Allston",
        traits: [1, 3, 4, 4, 1]
      },
      {
        name: "Leo",
        vibe: "Chill and flexible",
        area: "Anywhere with easy commute",
        traits: [2, 3, 2, 2, 4]
      }
    ];

    let currentQuestion = 0;
    let userAnswers = [];
    let topMatches = [];
    let currentMatch = 0;
    let actionsTaken = [];

    function showScreen(screenId) {
      document.querySelectorAll(".screen").forEach(screen => {
        screen.classList.remove("active");
      });
      document.getElementById(screenId).classList.add("active");
    }

    function startQuiz() {
      currentQuestion = 0;
      userAnswers = [];
      renderQuestion();
      showScreen("quizScreen");
    }

    function renderQuestion() {
      const q = questions[currentQuestion];
      document.getElementById("questionTag").textContent = q.tag;
      document.getElementById("questionText").textContent = q.text;
      document.getElementById("progressText").textContent = `Question ${currentQuestion + 1} of ${questions.length}`;

      const answersBox = document.getElementById("answersBox");
      answersBox.innerHTML = "";

      q.answers.forEach((answer, index) => {
        const btn = document.createElement("button");
        btn.className = "answer-btn";
        btn.textContent = answer;
        btn.onclick = () => selectAnswer(index + 1);
        answersBox.appendChild(btn);
      });
    }

    function selectAnswer(value) {
      userAnswers.push(value);
      currentQuestion++;

      if (currentQuestion < questions.length) {
        renderQuestion();
      } else {
        showScreen("loadingScreen");
        setTimeout(() => {
          generateMatches();
          currentMatch = 0;
          renderMatch();
          showScreen("matchScreen");
        }, 1200);
      }
    }

    function generateMatches() {
      const scored = roommates.map(roommate => {
        let score = 0;
        for (let i = 0; i < userAnswers.length; i++) {
          const diff = Math.abs(userAnswers[i] - roommate.traits[i]);
          score += Math.max(0, 4 - diff);
        }
        return { ...roommate, score };
      });

      scored.sort((a, b) => b.score - a.score);
      topMatches = scored.slice(0, 3);
    }

    function fitLabel(score) {
      if (score >= 17) return "Great Fit";
      if (score >= 14) return "Good Fit";
      return "Possible Fit";
    }

    function whyText(roommate) {
      const reasons = [];

      if (userAnswers[0] === roommate.traits[0]) reasons.push("same budget");
      if (userAnswers[1] === roommate.traits[1]) reasons.push("similar cleanliness style");
      if (userAnswers[2] === roommate.traits[2]) reasons.push("matching schedule");
      if (userAnswers[3] === roommate.traits[3]) reasons.push("shared home vibe");
      if (userAnswers[4] === roommate.traits[4]) reasons.push("preferred Boston area match");

      if (reasons.length === 0) return "You have a few overlapping preferences and could be worth a conversation.";
      if (reasons.length === 1) return `You both have ${reasons[0]}.`;
      if (reasons.length === 2) return `You both have ${reasons[0]} and ${reasons[1]}.`;
      return `You match on ${reasons.slice(0, 3).join(", ")}.`;
    }

    function renderMatch() {
      const match = topMatches[currentMatch];
      document.getElementById("matchLabel").textContent = `Match ${currentMatch + 1} of 3`;
      document.getElementById("matchName").textContent = match.name;
      document.getElementById("fitScore").textContent = `${fitLabel(match.score)} • ${match.score}/20`;
      document.getElementById("matchVibe").textContent = match.vibe;
      document.getElementById("matchWhy").textContent = whyText(match);
      document.getElementById("matchArea").textContent = match.area;
      document.getElementById("matchCounter").textContent = "Swipe style: Deny, Accept, or Send Request";
    }

    function handleAction(action) {
      actionsTaken.push({
        match: topMatches[currentMatch].name,
        action
      });

      currentMatch++;

      if (currentMatch < topMatches.length) {
        renderMatch();
      } else {
        const requested = actionsTaken.filter(a => a.action === "Request Sent").map(a => a.match);
        const accepted = actionsTaken.filter(a => a.action === "Accepted").map(a => a.match);

        let msg = "You reviewed all 3 matches.";
        if (requested.length > 0) {
          msg = `You sent roommate request${requested.length > 1 ? "s" : ""} to ${requested.join(", ")}.`;
        } else if (accepted.length > 0) {
          msg = `You accepted ${accepted.join(", ")} as a strong match.`;
        }

        document.getElementById("finalMessage").textContent = msg;
        showScreen("endScreen");
      }
    }

    function restartApp() {
      currentQuestion = 0;
      userAnswers = [];
      topMatches = [];
      currentMatch = 0;
      actionsTaken = [];
      showScreen("startScreen");
    }
  </script>
</body>
</html>
