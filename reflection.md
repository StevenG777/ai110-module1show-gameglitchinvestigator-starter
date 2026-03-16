# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
ANS: It gives a clean UI, but it cannot defend from edge cases such as number out of range

- List at least two concrete bugs you noticed at the start  
  (for example: "the secret number kept changing" or "the hints were backwards").
ANS:
  - Attemps is not showing despite it was tracked sometimes, but attemp becomes negatives
  - It allows you to enter number outside of range 1-100
  - Once game overs, you cannot restart unless refreshing the page
  - It gives wrong instruction regarding going up or down
  - When you click the toggle to remove hint, it works, but it wouldn't work for opposite case
  - (Not really an error) I don't know what's the point of having difficulties

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
ANS: Claude Code

- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
ANS: AI suggested the program first turn input string with '.' into float and then integer is wrong, because it will allow 
decimal number input. It suggested to call int() on string input. If the input is decimal, then it will throw error

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
ANS: AI suggested that changing to form submission for text input will fix the problem of attempt not updating, however I found out it was wrong through submit the input to check if the attempt numbers went down and it did not.

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
ANS: If the component behaves to my quantifiable expectation, then I believe a bug is really fixed

- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
ANS: I used pytest to run the corrected test provided in test_game_logic.py

- Did AI help you design or understand any tests? How?
ANS: AI helps me to understand the test by summarize the logic and explain expected behavior to me
---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
- What change did you make that finally gave the game a stable secret number?

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
