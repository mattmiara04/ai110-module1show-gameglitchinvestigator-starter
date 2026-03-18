# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

- What did the game look like the first time you ran it?
  
The game had a very minimal interface with typical HTML. It includes a title with a box to input your guess along with other buttons to intearct with the system.

- List at least two concrete bugs you noticed at the start
  (for example: "the secret number kept changing" or "the hints were backwards").
  
  My first guess was 13 and the game rutrned to me that my guess was correct eventhough the true secret number was 67
  The New Game button did not reset my game after the app was updated to be in a "win" state. The message "You already won. Start a new game to play again" did not leave my screen.

---

## 2. How did you use AI as a teammate?

- Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?
  
  I used Claude in VS Code for this project
- Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
  
  An AI suggesiton whcih was correct was that the secret value was being converted in a string causing wrong comparisons to be marked correct. I verified this by testing my guesses in the app prior to the bug fix and after. This was said to sometimes happen by the AI but happened to me on the first try,

- Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).

The AI did not initially address the bug I asked for but addressed the bug where the hints were reversed. This is alright because it was a bug I did not even get to notice my first time playing, however it is not what I specifically asked for. This is a minor problem and I had issues elsewhere

---

## 3. Debugging and testing your fixes

- How did you decide whether a bug was really fixed?
  I decided a bug was fixed by testing the game multiple times. After playing it once I tried several cases to ensure the logic in the code was correct. As well as using the developer debug panel to know the expected value.
- Describe at least one test you ran (manual or using pytest) and what it showed you about your code.
  A test which I ran was entering the wrong number and ensuring the game would not mark it as a win. After fixing the bugs this was no longer an issue showing me the code worked.
- Did AI help you design or understand any tests? How?
  I specifically asked AI to find the bug I was having and point me to where it is in the code. From here I asked for it to further explain to me the bug allowing me to figure out what specifically I should be testing for

---

## 4. What did you learn about Streamlit and state?

- In your own words, explain why the secret number kept changing in the original app.
  The secret number change sin the original app because Streamlit reruns the entire script when the user interacts with it, while not updating the session state
- How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?
  Streamlit reruns are like waking up every morning and not remembering anyhting from the day before, session state is your memory, allowing you to not forget everything
- What change did you make that finally gave the game a stable secret number?
  The change which I made was making sure the number is only initialized once and stored in session state and not modified during gameplay

---

## 5. Looking ahead: your developer habits

- What is one habit or strategy from this project that you want to reuse in future labs or projects?
  A habit I would like to reuse form this porject is having the AI point me to where it believes the issue is first and having it explain
  
- What is one thing you would do differently next time you work with AI on a coding task?
  On thing which I owuld do diffectinly is be more criticial of each suggestion provided by the AI instead of instanly trusting it.
- In one or two sentences, describe how this project changed the way you think about AI generated code.
  Considering this app is said to be AI generated, I thought i would be able to produce better outputs. However the use of AI to aud in fixing bugs in code is excellent.
