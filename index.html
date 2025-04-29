<!DOCTYPE html>
<!-- Author: Angelina -->
<!-- Purpose: Endocrine System Activity -->
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Endocrine Hangman!</title>
    <style>
        /* CSS remains identical to the previous version */
        @import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600;700&display=swap');
        @import url('https://fonts.googleapis.com/css2?family=Caveat:wght@700&display=swap');

        :root {
            --primary-color: #00796b;  /* Teal */
            --secondary-color: #00acc1; /* Lighter Cyan/Teal */
            --accent-color: #ffc107;   /* Amber */
            --error-color: #d32f2f;    /* Red */
            --correct-color: #388e3c;   /* Green */
            --light-bg: #e0f2f1;       /* Very Light Teal */
            --dark-text: #212121;
            --light-text: #fff;
            --hangman-color: #424242; /* Grey for Hangman */
            --shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
            --border-radius: 12px;
            --ai-loading-color: #757575; /* Grey for loading text */
            --ai-fact-color: #004d40; /* Darker Teal for facts */
        }

        * { box-sizing: border-box; margin: 0; padding: 0; }

        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
            display: flex;
            justify-content: center;
            align-items: flex-start;
            min-height: 100vh;
            color: var(--dark-text);
            padding: 20px;
            overflow-y: auto;
        }

        #game-container {
            background-color: var(--light-bg);
            padding: 30px 40px;
            border-radius: var(--border-radius);
            box-shadow: var(--shadow);
            width: 90%;
            max-width: 700px;
            text-align: center;
            position: relative;
            transition: transform 0.5s ease-in-out, opacity 0.5s ease-in-out;
            margin-top: 20px;
            margin-bottom: 20px;
        }

        .screen { display: none; animation: fadeIn 0.5s ease-in-out forwards; }
        .screen.active { display: block; }
        @keyframes fadeIn { from { opacity: 0; transform: translateY(20px); } to { opacity: 1; transform: translateY(0); } }

        #start-screen h1 { color: var(--primary-color); margin-bottom: 15px; font-size: 2.5em; font-family: 'Caveat', cursive; }
        #start-screen p { margin-bottom: 25px; font-size: 1.1em; color: var(--secondary-color); line-height: 1.6; }
        #start-screen .ai-notice { font-size: 0.9em; color: var(--primary-color); margin-top: -10px; margin-bottom: 20px; }

        #quiz-screen {
            display: grid;
            grid-template-areas:
                "header header"
                "hangman question"
                "hangman answers"
                "hangman feedback"
                "hangman ai"
                "hangman controls";
            grid-template-columns: 1fr 2fr;
            gap: 10px 25px;
            align-items: start;
        }
        @media (max-width: 600px) {
             #quiz-screen { grid-template-areas: "header" "hangman" "question" "answers" "feedback" "ai" "controls"; grid-template-columns: 1fr; gap: 15px; }
             #hangman-drawing { margin: 10px auto; } #ai-content-area { margin-top: 0; } #quiz-controls { margin-top: 10px; }
        }

        #quiz-header { grid-area: header; display: flex; justify-content: space-between; align-items: center; margin-bottom: 10px; padding-bottom: 10px; border-bottom: 2px solid var(--secondary-color); width: 100%; }
        #mistakes-counter { font-size: 1.1em; font-weight: 600; color: var(--error-color); background-color: #ffebee; padding: 5px 10px; border-radius: 5px; }
        #question-counter-hm { font-size: 1.1em; font-weight: 600; color: var(--primary-color); }
        #timer-hm { font-size: 1.3em; font-weight: 700; color: var(--light-text); background-color: var(--primary-color); padding: 5px 15px; border-radius: 20px; min-width: 70px; text-align: center; transition: background-color 0.3s ease; }
        #timer-hm.warning { background-color: var(--error-color); animation: pulse 1s infinite; }
        @keyframes pulse { 0% { transform: scale(1); } 50% { transform: scale(1.1); } 100% { transform: scale(1); } }

        #hangman-drawing { grid-area: hangman; width: 150px; height: 200px; margin-top: 10px; position: sticky; top: 20px; }
        @media (max-width: 600px) { #hangman-drawing { position: static; margin: 10px auto; } }
        #hangman-drawing svg { width: 100%; height: 100%; }
        .hg-part { stroke: var(--hangman-color); stroke-width: 4; fill: none; stroke-linecap: round; opacity: 0; transition: opacity 0.5s ease-in-out; }
        .hg-part.visible { opacity: 1; }

        #question-area { grid-area: question; }
        #answer-buttons-hm { grid-area: answers; display: grid; grid-template-columns: 1fr; gap: 10px; }
        #feedback-hm { grid-area: feedback; margin-top: 5px; font-size: 1.0em; font-weight: 600; min-height: 25px; text-align: left; transition: color 0.3s ease; }
        #question-text-hm { font-size: 1.3em; font-weight: 600; color: var(--primary-color); margin-bottom: 15px; min-height: 50px; line-height: 1.4; text-align: left; }

        .btn-hm { font-family: 'Poppins', sans-serif; background-color: var(--secondary-color); color: var(--light-text); border: none; padding: 12px 15px; border-radius: var(--border-radius); cursor: pointer; font-size: 0.95em; font-weight: 600; transition: background-color 0.3s ease, transform 0.1s ease, box-shadow 0.2s ease; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15); text-align: left; }
        .btn-hm:hover:not(:disabled) { background-color: var(--primary-color); transform: translateY(-2px); box-shadow: var(--shadow); }
        .btn-hm:active:not(:disabled) { transform: translateY(0px); box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1); }
        .btn-hm:disabled { cursor: not-allowed; opacity: 0.7; }
        .btn-hm.correct { background-color: var(--correct-color); animation: correctPulse 0.5s ease; }
        .btn-hm.incorrect { background-color: var(--error-color); animation: shake 0.5s ease; }
        @keyframes correctPulse { 0% { transform: scale(1); } 50% { transform: scale(1.02); } 100% { transform: scale(1); } }
        @keyframes shake { 0%, 100% { transform: translateX(0); } 20%, 60% { transform: translateX(-4px); } 40%, 80% { transform: translateX(4px); } }

        .feedback-correct { color: var(--correct-color); }
        .feedback-incorrect { color: var(--error-color); }
        .feedback-loading { color: var(--ai-loading-color); font-style: italic; }

        #ai-content-area { grid-area: ai; margin-top: 10px; min-height: 60px; display: flex; justify-content: center; align-items: center; text-align: center; padding: 10px; border-radius: 8px; background-color: rgba(255, 255, 255, 0.3); }
        #ai-content-area .ai-fact-text { color: var(--ai-fact-color); font-weight: 600; font-size: 1.05em; line-height: 1.5; }
        #ai-content-area .ai-loading-text { color: var(--ai-loading-color); font-style: italic; }
        #ai-content-area .ai-error-text { color: var(--error-color); font-weight: bold; /* Witty remarks will use this style too */ }

        #quiz-controls { grid-area: controls; margin-top: 15px; text-align: right; }
        @media (max-width: 600px) { #quiz-controls { text-align: center; } }

        #end-screen h2 { color: var(--primary-color); margin-bottom: 15px; font-size: 2.2em; font-family: 'Caveat', cursive; }
        #final-result-hm { font-size: 1.8em; font-weight: 700; margin-bottom: 20px; }
        #final-result-hm.win { color: var(--correct-color); } #final-result-hm.lose { color: var(--error-color); }
        #end-message-hm { font-size: 1.1em; margin-bottom: 30px; line-height: 1.6; color: var(--dark-text); }

        .control-btn { background-color: var(--accent-color); color: var(--primary-color); padding: 12px 25px; font-size: 1.1em; margin-top: 10px; box-shadow: 0 2px 4px rgba(0, 0, 0, 0.15); font-weight: 700; border: none; border-radius: var(--border-radius); cursor: pointer; transition: background-color 0.3s ease, transform 0.1s ease, box-shadow 0.2s ease; }
        .control-btn:hover:not(:disabled) { background-color: #ffb300; transform: translateY(-2px); box-shadow: var(--shadow); }
        .control-btn:active:not(:disabled) { transform: translateY(0px); box-shadow: 0 1px 2px rgba(0, 0, 0, 0.1); }
        .control-btn:disabled { cursor: not-allowed; opacity: 0.6; }

    </style>
</head>
<body>
    <div id="game-container">
        <!-- Start Screen -->
        <div id="start-screen" class="screen active">
            <h1>Endocrine Hangman!</h1>
            <p>Test your endocrine knowledge! Correct answers yield intriguing clinical facts, incorrect answers... well, expect some professional critique. Click "Next" to proceed.</p> <!-- Updated instructions -->
            <p class="ai-notice">(AI features use Pollinations.ai - generation might take a few seconds)</p>
            <button id="start-btn-hm" class="control-btn">Start Game!</button>
        </div>

        <!-- Quiz Screen -->
        <div id="quiz-screen" class="screen">
            <div id="quiz-header">
                <div id="mistakes-counter">Mistakes: 0 / 6</div>
                <div id="question-counter-hm">Q: 1 / X</div>
                <div id="timer-hm">12s</div>
            </div>

            <div id="hangman-drawing">
                 <svg viewBox="0 0 150 200">
                    {/* SVG content remains the same */}
                    <line class="hg-part gallows visible" id="hg-gallows-1" x1="10" y1="190" x2="90" y2="190" /> <line class="hg-part gallows visible" id="hg-gallows-2" x1="50" y1="190" x2="50" y2="10" /> <line class="hg-part gallows visible" id="hg-gallows-3" x1="50" y1="10" x2="110" y2="10" /> <line class="hg-part gallows visible" id="hg-gallows-4" x1="110" y1="10" x2="110" y2="40" /> <circle class="hg-part body" id="hg-head" cx="110" cy="60" r="20" /> <line class="hg-part body" id="hg-body" x1="110" y1="80" x2="110" y2="140" /> <line class="hg-part body" id="hg-arm-l" x1="110" y1="100" x2="80" y2="120" /> <line class="hg-part body" id="hg-arm-r" x1="110" y1="100" x2="140" y2="120" /> <line class="hg-part body" id="hg-leg-l" x1="110" y1="140" x2="85" y2="170" /> <line class="hg-part body" id="hg-leg-r" x1="110" y1="140" x2="135" y2="170" />
                </svg>
            </div>

             <div id="question-area"> <p id="question-text-hm">Question text goes here...</p> </div>
             <div id="answer-buttons-hm"> {/* Buttons generated by JS */} </div>
             <div id="feedback-area"> <p id="feedback-hm"></p> </div>
             <div id="ai-content-area"> {/* AI Fact or feedback */} </div>
             <div id="quiz-controls"> <button id="next-question-btn" class="control-btn" style="display: none;">Next Question</button> </div>

        </div>

        <!-- End Screen -->
        <div id="end-screen" class="screen">
            <h2 id="end-title">Game Over!</h2>
            <p id="final-result-hm" class="">You Lost!</p>
            <p id="end-message-hm">The correct answer was...</p>
            <button id="play-again-btn-hm" class="control-btn">Play Again?</button>
        </div>
    </div>

    <script>
        const questionsHm = [ // Questions remain the same
             { question: "Which gland is often called the 'master gland' because it controls many other endocrine glands?", options: ["Thyroid", "Adrenal", "Pituitary", "Pancreas"], correctAnswer: "Pituitary" },
             { question: "What hormone does the pancreas produce to lower blood sugar levels?", options: ["Glucagon", "Insulin", "Cortisol", "Thyroxine"], correctAnswer: "Insulin" },
             { question: "Which glands are located on top of the kidneys and release adrenaline?", options: ["Thyroid", "Parathyroid", "Adrenal", "Pineal"], correctAnswer: "Adrenal" },
             { question: "Thyroxine, a hormone regulating metabolism, is produced by which gland?", options: ["Pituitary", "Thyroid", "Adrenal", "Ovaries"], correctAnswer: "Thyroid" },
             { question: "Which hormone is primarily responsible for the 'fight or flight' response?", options: ["Insulin", "Growth Hormone", "Adrenaline (Epinephrine)", "Estrogen"], correctAnswer: "Adrenaline (Epinephrine)" },
             { question: "What is the main function of parathyroid hormone (PTH)?", options: ["Lower blood calcium", "Raise blood calcium", "Regulate sleep", "Control metabolism"], correctAnswer: "Raise blood calcium" },
             { question: "Which gland, located in the brain, produces melatonin to regulate sleep cycles?", options: ["Pituitary", "Hypothalamus", "Pineal", "Thyroid"], correctAnswer: "Pineal" },
             { question: "Insulin and Glucagon work together to regulate:", options: ["Heart rate", "Body temperature", "Blood sugar levels", "Growth"], correctAnswer: "Blood sugar levels" },
             { question: "Which endocrine gland produces testosterone in males?", options: ["Adrenal", "Pituitary", "Testes", "Thyroid"], correctAnswer: "Testes" },
             { question: "Growth Hormone (GH) is primarily produced by which gland?", options: ["Thyroid", "Adrenal", "Pancreas", "Pituitary"], correctAnswer: "Pituitary" }
        ];

        // DOM Elements (references remain the same)
        const gameContainerHm = document.getElementById('game-container');
        const startScreenHm = document.getElementById('start-screen');
        const quizScreenHm = document.getElementById('quiz-screen');
        const endScreenHm = document.getElementById('end-screen');
        const startBtnHm = document.getElementById('start-btn-hm');
        const playAgainBtnHm = document.getElementById('play-again-btn-hm');
        const mistakesCounterDisplay = document.getElementById('mistakes-counter');
        const questionCounterDisplayHm = document.getElementById('question-counter-hm');
        const timerDisplayHm = document.getElementById('timer-hm');
        const hangmanDrawing = document.getElementById('hangman-drawing');
        const hangmanParts = document.querySelectorAll('#hangman-drawing .hg-part.body');
        const questionTextHm = document.getElementById('question-text-hm');
        const answerButtonsContainerHm = document.getElementById('answer-buttons-hm');
        const feedbackDisplayHm = document.getElementById('feedback-hm');
        const aiContentArea = document.getElementById('ai-content-area');
        const nextQuestionBtn = document.getElementById('next-question-btn');
        const endTitle = document.getElementById('end-title');
        const finalResultDisplayHm = document.getElementById('final-result-hm');
        const endMessageDisplayHm = document.getElementById('end-message-hm');

        // Game State (remains the same)
        let currentQuestionIndexHm;
        let mistakesHm;
        let timerIntervalHm;
        let timeLeftHm;
        let questionInProgress = false;
        const TIME_PER_QUESTION_HM = 12;
        const MAX_MISTAKES = hangmanParts.length;

        // API Constants (remains the same)
        const POLLINATIONS_TEXT_API = "https://text.pollinations.ai/";

        // Event Listeners (remain the same)
        startBtnHm.addEventListener('click', startGameHm);
        playAgainBtnHm.addEventListener('click', startGameHm);
        nextQuestionBtn.addEventListener('click', handleNextClick);

        // --- Core Game Logic (functions remain structurally similar) ---

        function setActiveScreenHm(screenElement) { /* ... */ }
        function startGameHm() { /* ... */ }
        function hideHangmanParts() { /* ... */ }
        function shuffleArrayHm(array) { /* ... */ }
        function loadQuestionHm() { /* ... */ }
        function resetStateHm() { /* ... */ }
        function startTimerHm() { /* ... */ }
        async function timeUpHm() { /* ... */ }
        async function selectAnswerHm(e) { /* ... */ }
        async function handleIncorrectAnswer(initialFeedbackMsg, isTimeUp = false, selectedAnswer = null) { /* ... */ }
        function showNextButton() { /* ... */ }
        function handleNextClick() { /* ... */ }
        function disableButtonsHm() { /* ... */ }
        function nextQuestionHm() { /* ... */ }
        function endGameHm(isWin) { /* ... */ }


        // --- REIMPLEMENTATION of Functions (with updated logic/prompts) ---

        function setActiveScreenHm(screenElement) {
            document.querySelectorAll('.screen').forEach(screen => screen.classList.remove('active'));
            screenElement.classList.add('active');
        }

        function startGameHm() {
            mistakesHm = 0;
            currentQuestionIndexHm = 0;
            questionInProgress = false;
            mistakesCounterDisplay.textContent = `Mistakes: ${mistakesHm} / ${MAX_MISTAKES}`;
            shuffleArrayHm(questionsHm);
            questionCounterDisplayHm.textContent = `Q: 1 / ${questionsHm.length}`;
            hideHangmanParts();
            nextQuestionBtn.style.display = 'none';
            setActiveScreenHm(quizScreenHm);
            loadQuestionHm();
        }

         function hideHangmanParts() {
             hangmanParts.forEach(part => part.classList.remove('visible'));
         }

         function shuffleArrayHm(array) {
             for (let i = array.length - 1; i > 0; i--) {
                 const j = Math.floor(Math.random() * (i + 1));
                 [array[i], array[j]] = [array[j], array[i]];
             }
         }

        function loadQuestionHm() {
            questionInProgress = true;
            resetStateHm();

            if (currentQuestionIndexHm >= questionsHm.length) {
                endGameHm(true); questionInProgress = false; return;
            }
            if (mistakesHm >= MAX_MISTAKES) {
                 endGameHm(false); questionInProgress = false; return;
            }

            const currentQuestion = questionsHm[currentQuestionIndexHm];
            questionTextHm.textContent = currentQuestion.question;
            questionCounterDisplayHm.textContent = `Q: ${currentQuestionIndexHm + 1} / ${questionsHm.length}`;

            while (answerButtonsContainerHm.firstChild) { answerButtonsContainerHm.removeChild(answerButtonsContainerHm.firstChild); }

            currentQuestion.options.forEach(option => {
                const button = document.createElement('button');
                button.textContent = option;
                button.classList.add('btn-hm');
                button.addEventListener('click', selectAnswerHm);
                answerButtonsContainerHm.appendChild(button);
            });

            startTimerHm();
        }

        function resetStateHm() {
            clearTimeout(timerIntervalHm);
            feedbackDisplayHm.textContent = '';
            feedbackDisplayHm.className = '';
            aiContentArea.innerHTML = ''; // Clear AI area
            timerDisplayHm.classList.remove('warning');
            nextQuestionBtn.style.display = 'none'; // Hide next button
            nextQuestionBtn.disabled = false;
        }

        function startTimerHm() {
            timeLeftHm = TIME_PER_QUESTION_HM;
            timerDisplayHm.textContent = `${timeLeftHm}s`;
            timerDisplayHm.classList.remove('warning');
            clearInterval(timerIntervalHm);

            timerIntervalHm = setInterval(() => {
                if (!questionInProgress) { clearInterval(timerIntervalHm); return; }
                timeLeftHm--;
                timerDisplayHm.textContent = `${timeLeftHm}s`;
                if (timeLeftHm <= 4 && timeLeftHm > 0) { timerDisplayHm.classList.add('warning'); }
                if (timeLeftHm <= 0) {
                    clearInterval(timerIntervalHm);
                    if (questionInProgress) { timeUpHm(); }
                }
            }, 1000);
        }

        async function timeUpHm() {
             if (!questionInProgress) return;
             questionInProgress = false;
             const correctAnswer = questionsHm[currentQuestionIndexHm].correctAnswer;
             disableButtonsHm();
             await handleIncorrectAnswer(`Time's Up! The answer was: ${correctAnswer}`, true);
        }

        async function selectAnswerHm(e) {
            if (!questionInProgress) return;
            questionInProgress = false;
            clearInterval(timerIntervalHm);

            const selectedButton = e.target;
            const correctAnswer = questionsHm[currentQuestionIndexHm].correctAnswer;
            const isCorrect = selectedButton.textContent === correctAnswer;

            disableButtonsHm();

            if (isCorrect) {
                selectedButton.classList.add('correct');
                feedbackDisplayHm.textContent = "Correct! Check below for a clinical pearl..."; // Update feedback text
                feedbackDisplayHm.className = 'feedback-correct';
                await generateAiFact(correctAnswer); // Generate fact
                showNextButton();
            } else {
                selectedButton.classList.add('incorrect');
                // Display initial feedback, then call AI for witty remark
                feedbackDisplayHm.textContent = `Incorrect. The answer was: ${correctAnswer}...`;
                feedbackDisplayHm.className = 'feedback-incorrect';
                await handleIncorrectAnswer(`Incorrect! The answer was: ${correctAnswer}`, false, selectedButton.textContent); // Pass original msg for context if needed, but AI will overwrite display
            }
        }

        // Handles incorrect answers OR serves as a wrapper for AI feedback display
        async function handleIncorrectAnswer(initialFeedbackMsg, isTimeUp = false, selectedAnswer = null) {
            // This function now primarily triggers the AI feedback generation
            // The basic feedback ("Incorrect...") is set directly in selectAnswerHm or timeUpHm

            if(!isTimeUp) { // Only count mistakes if it wasn't a time-up event
                mistakesHm++;
                mistakesCounterDisplay.textContent = `Mistakes: ${mistakesHm} / ${MAX_MISTAKES}`;
            }

            // Draw hangman part if applicable
            if (mistakesHm > 0 && mistakesHm <= hangmanParts.length) {
                 const partToShow = hangmanParts[mistakesHm - 1];
                 if (partToShow) partToShow.classList.add('visible');
            }

            // Highlight correct answer if it wasn't time up
            const correctAnswer = questionsHm[currentQuestionIndexHm].correctAnswer;
            if (!isTimeUp) {
                Array.from(answerButtonsContainerHm.children).forEach(button => {
                     if (button.textContent === correctAnswer) { button.classList.add('correct'); }
                 });
            }

            // Generate the witty AI feedback
            await generateAiFeedback(correctAnswer, selectedAnswer, isTimeUp);

            // Show the next button AFTER AI attempt
            showNextButton();
        }

        function showNextButton() {
             if (quizScreenHm.classList.contains('active')) {
                 nextQuestionBtn.style.display = 'inline-block';
             }
        }

        function handleNextClick() {
            nextQuestionBtn.style.display = 'none';
            nextQuestionBtn.disabled = true;

            if (mistakesHm >= MAX_MISTAKES) {
                endGameHm(false);
            } else {
                nextQuestionHm();
            }
        }

        // --- AI Generation Functions (with UPDATED prompts) ---

        async function generateAiFact(topic) {
            aiContentArea.innerHTML = `<p class="ai-loading-text">🔬 Consulting the literature for a pearl on ${topic}...</p>`;

            // *** UPDATED PROMPT for formal/witty fact ***
            const prompt = encodeURIComponent(`Generate a concise, intriguing medical or scientific fun fact about ${topic} (1-2 sentences). Aim for a detail that a doctor or medical student might find amusing or surprising. Use a slightly formal but witty tone.`);
            const textUrl = `${POLLINATIONS_TEXT_API}${prompt}`;

            try {
                const response = await fetch(textUrl);
                if (!response.ok) throw new Error(`API Error: ${response.status}`);
                const aiText = await response.text();
                if (quizScreenHm.classList.contains('active')) {
                    aiContentArea.innerHTML = `<p class="ai-fact-text">💡 Pearl: ${aiText.trim()}</p>`;
                    console.log("AI Fact received:", aiText);
                }
            } catch (error) {
                 console.error("AI Fact generation error:", error);
                 if (quizScreenHm.classList.contains('active')) {
                     aiContentArea.innerHTML = `<p class="ai-error-text">😥 Couldn't retrieve a clinical pearl about ${topic}.</p>`;
                 }
            }
        }

         async function generateAiFeedback(correctAnswer, selectedAnswer, isTimeUp) {
            aiContentArea.innerHTML = `<p class="ai-loading-text">🤔 Pondering the differential...</p>`; // Updated loading text

            let userContext = "";
            if (isTimeUp) {
                userContext = "The user's response time exceeded acceptable limits.";
            } else if (selectedAnswer) {
                userContext = `The user incorrectly diagnosed the answer as "${selectedAnswer}".`; // More clinical framing
            }

            // *** UPDATED PROMPT for formal/witty feedback ***
            const prompt = encodeURIComponent(`Context: Endocrine hangman quiz for a medical audience. ${userContext} Correct answer: "${correctAnswer}". Respond with a concise (1-2 sentence) remark exhibiting dry wit or a humorous clinical perspective on the mistake. Avoid being overly harsh.`);
            const textUrl = `${POLLINATIONS_TEXT_API}${prompt}`;

            try {
                const response = await fetch(textUrl);
                if (!response.ok) throw new Error(`API Error: ${response.status}`);
                const aiText = await response.text();
                if (quizScreenHm.classList.contains('active')) {
                    // Display witty feedback using error style for visual distinction
                    aiContentArea.innerHTML = `<p class="ai-error-text">💬 ${aiText.trim()}</p>`;
                    console.log("AI Feedback received:", aiText);
                }
            } catch (error) {
                 console.error("AI Feedback generation error:", error);
                 if (quizScreenHm.classList.contains('active')) {
                     aiContentArea.innerHTML = `<p class="ai-error-text">😥 AI consultation unavailable. Proceed with caution.</p>`; // Witty error fallback
                 }
            }
        }

        // --- Utility and End Game Functions (Implementations) ---

        function disableButtonsHm() {
             Array.from(answerButtonsContainerHm.children).forEach(button => {
                button.disabled = true; button.style.pointerEvents = 'none';
            });
        }

        function nextQuestionHm() {
             if (quizScreenHm.classList.contains('active')) {
                 currentQuestionIndexHm++;
                 loadQuestionHm();
             }
        }

        function endGameHm(isWin) {
            questionInProgress = false;
            clearTimeout(timerIntervalHm);
            setActiveScreenHm(endScreenHm);
            aiContentArea.innerHTML = '';
            nextQuestionBtn.style.display = 'none';

            if (isWin) {
                 endTitle.textContent = "Consult Complete!"; // Updated Title
                 finalResultDisplayHm.textContent = "Diagnosis: Success!";
                 finalResultDisplayHm.className = 'final-result-hm win';
                 endMessageDisplayHm.textContent = `You navigated the endocrine system with only ${mistakesHm} misstep(s). Excellent clinical acumen!`; // Updated message
            } else {
                 endTitle.textContent = "Case Closed"; // Updated Title
                 finalResultDisplayHm.textContent = "Diagnosis: Failure";
                 finalResultDisplayHm.className = 'final-result-hm lose';
                 hangmanParts.forEach(part => part.classList.add('visible'));
                 const lastQuestion = questionsHm[currentQuestionIndexHm] || questionsHm[questionsHm.length - 1];
                 endMessageDisplayHm.textContent = `Further review required. The critical finding was: ${lastQuestion.correctAnswer}. Consider consulting a specialist (or the textbook).`; // Updated message
            }
        }

    </script>
</body>
</html>
