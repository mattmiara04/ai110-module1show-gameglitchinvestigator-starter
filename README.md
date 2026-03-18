# 🎮 Game Glitch Investigator: The Impossible Guesser

## 🚨 The Situation

You asked an AI to build a simple "Number Guessing Game" using Streamlit.
It wrote the code, ran away, and now the game is unplayable. 

- You can't win.
- The hints lie to you.
- The secret number seems to have commitment issues.

## 🛠️ Setup

1. Install dependencies: `pip install -r requirements.txt`
2. Run the broken app: `python -m streamlit run app.py`

## 🕵️‍♂️ Your Mission

1. **Play the game.** Open the "Developer Debug Info" tab in the app to see the secret number. Try to win.
2. **Find the State Bug.** Why does the secret number change every time you click "Submit"? Ask ChatGPT: *"How do I keep a variable from resetting in Streamlit when I click a button?"*
3. **Fix the Logic.** The hints ("Higher/Lower") are wrong. Fix them.
4. **Refactor & Test.** - Move the logic into `logic_utils.py`.
   - Run `pytest` in your terminal.
   - Keep fixing until all tests pass!

## 📝 Document Your Experience

- The purpose of the game is to have the user guess a randomly generated number between 1-100 with x amount of guesses with x depenfing on the diffculty. After each guess the user gets notified whether their guess hsould be higehr or lower than the number they provided.
- The two main bugs which I found the game sometimes marked incorrect guesses as correct because the secret number was being converted into a string, causing improper comparisons and the New Game button did not fully reset the game because not all session state variables were reinitialized
- I fixed the incorrect win logic by removing the conversion of the secret number to a string, ensuring that guesses are always compared as integers and I also fixed the New Game bug by resetting all relevant session state variables (such as attempts, score, status, and history) so the game properly restarts.

## 📸 Demo

- <img width="2555" height="1310" alt="image" src="https://github.com/user-attachments/assets/cdab9dec-935c-4d2a-b4c1-7e5b8d0c8f44" />


## 🚀 Stretch Features

- [ ] [If you choose to complete Challenge 4, insert a screenshot of your Enhanced Game UI here]
