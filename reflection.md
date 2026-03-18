# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
- List at least two concrete bugs you noticed at the start  
  (for example: "the hints were backwards").
When I first ran the game, it worked visually but behaved incorrectly during gameplay. One major bug was that the hints were backwards—for example, when my guess was too high, it told me to go higher instead of lower. Another issue was that the game behaved inconsistently because the secret number was sometimes treated as a string instead of an integer. I also noticed that the displayed range did not match the selected difficulty, which was confusing. Additionally, the game accepted invalid inputs like numbers outside the allowed range.
---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
I used ChatGPT as my main AI tool to help debug and understand the code. One correct suggestion it gave was identifying that the hint logic in the check_guess function was reversed. I applied the fix and verified it by running the game and confirming that the hints now matched the correct direction. One misleading aspect was that AI did not initially point out the issue where the secret number was sometimes converted into a string, which caused inconsistent behavior. I had to manually inspect the code and test multiple cases to find and fix that issue.
---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
- Describe at least one test you ran (manual or using pytest)  
  and what it showed you about your code.
- Did AI help you design or understand any tests? How?
I determined whether a bug was fixed by running the game multiple times and testing different types of inputs, including edge cases. For example, I tested guesses that were too high, too low, and correct to confirm the hint logic worked properly. I also created pytest tests for the check_guess function to verify that it returned the correct outcomes for different inputs. The tests showed that the function behaved correctly after my fixes. AI helped me understand how to structure these tests and how to properly check return values.
---

## 4. What did you learn about Streamlit and state?

- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
I learned that Streamlit reruns the entire script every time the user interacts with the app, such as clicking a button or entering input. Session state is used to store values like the secret number, score, and attempts so they don’t reset every time the app reruns. Without session state, the game would restart on every interaction. I would explain it as Streamlit rebuilding the app each time, but using session state to remember important data between runs.
---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  - This could be a testing habit, a prompting strategy, or a way you used Git.
- What is one thing you would do differently next time you work with AI on a coding task?
- In one or two sentences, describe how this project changed the way you think about AI generated code.
One habit I want to reuse is testing edge cases and not just normal inputs, because that helped me find important bugs like out-of-range values. Next time I work with AI, I would double-check its suggestions more carefully instead of assuming everything it says is correct. This project showed me that AI-generated code can look correct but still contain subtle logic errors. It changed the way I think about AI by showing that it is a helpful tool, but it still requires human judgment and careful testing.