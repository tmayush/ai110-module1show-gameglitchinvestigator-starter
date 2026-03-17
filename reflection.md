# 💭 Reflection: Game Glitch Investigator

Answer each question in 3 to 5 sentences. Be specific and honest about what actually happened while you worked. This is about your process, not trying to sound perfect.

## 1. What was broken when you started?

### What did the game look like the first time you ran it?

It ran perfectly! But I did notice a few bugs as I was (using the app)/(playing the game). A bit buggy when I open the developer info panel, and try to guess a number. Each time i click "guess", it has to push the number onto the list, and then I have to click again so it takes my input.

### List at least two concrete bugs you noticed at the start  
  > (for example: "the secret number kept changing" or "the hints were backwards").

Bugs I noticed in chronological order:

1. The hints (Go Lower/Higher) are wrong or rather opposite to what they're supposed to be. Ex: If secret = 99, and guess = 88; "Go Lower" is the hint that is shown, even though it should be "Go Higher", since the value of secret is higher than the value of guess.

*At this point I looked at the "[Getting Started](https://www.loom.com/share/f5f84df907c7447dacb723f959bb812a)" video in case I missed anything, and I got to know another bug:*

2. The parameters/attributes in the difficulty level are partially incorrect:

    **Easy**:
    - Range: **Good**.
    - Attempts Allowed: **Needs Correction**. It is lower than Normal, when it should be higher.

    **Normal**:
    - Range: **Fine**. One aspect could be improved, which will be discussed down below.
    - Attempts Allowed: **Good**.

    **Hard**:
    - Range: **Needs Correction**. It is easier than "normal" and harder than "easy", so has to be corrected. Possible solutions are discussed below.
    - Attempts Allowed: **Good**.

    <br />

    **Possible Solutions**

    - **Fix for Easy's Attempts Allowed**
      - We can simply adjust the value to something like 10 since the value is 8 for medium and 5 for hard.

    - **Fix for Hard's Range**
      - Since the range for "Hard" difficulty is wrong, we can adjust the medium's range to something like "1 to 50" and keep the hard's range as "1 to 100".

      - The alternative would be to adjust the range to 1 to 200.

      Both solutions are valid, I'll be moving forward with the former.

3. The secret number for hard doesn't respect the provided range

4. New game button doesn't work:
    - Banners (like "Game Over") do not close.
    - Secret changes, so that's a good sign, but history is not cleared, so even if you click New Game button, it will not restart the game, maybe because history is full (equal to the number of max attempts allowed)?
    - The actual attempts you can try is one lower than the actual number of attempts you are given (the number from the sidebar)

5. When you start a new game, the "attempts left" in the blue banner is one number lower than the allowed attempts on the sidebar.

6. When you hit submit guess, the counter (attempts left) in blue banner does not decrease the first time, and starts decreasing from the second guess, but the game still ends when the number of attempts left are 1. Ex:

    Actual attempts supposed to be given to the user: 8

    (Blue Banner) Attempts left: 7 (one lower than actual)

    If secret is 10.

    I guess:
    - x (change) [number on screen]
    - 5 (no change) [7]
    - 6 (-1) [7]
    - 7 (-1) [6]
    - 8 (-1) [5]
    - 9 (-1) [4]
    - 10 (-1) [3]
    - 11 (-1) [2]
    - 12 (-1) [1]

    Game end banner shown, and attempts left should be 0, but shows as 1 because of its drift since 1st guess. If it did decrease since 1st guess, it would be showing 0. It would be wrong either way, since the number of attempts should actually be 8

---

## 2. How did you use AI as a teammate?

### Which AI tools did you use on this project (for example: ChatGPT, Gemini, Copilot)?

I used Claude Code to help me with this assignment.


### Give one example of an AI suggestion that was correct (including what the AI suggested and how you verified the result).
![alt text](./readme_images/image.png)
### Give one example of an AI suggestion that was incorrect or misleading (including what the AI suggested and how you verified the result).
>i committed reflections.md, commit the newly modified code, also you can add .calude fodler to gitignore
The .claude/ folder and CLAUDE.md are now properly ignored going forward.

![alt text](./readme_images/image-2.png)
![alt text](./readme_images/image-1.png)
---

## 3. Debugging and testing your fixes

### How did you decide whether a bug was really fixed?
### Describe at least one test you ran (manual or using pytest) and what it showed you about your code.
### Did AI help you design or understand any tests? How?

---

## 4. What did you learn about Streamlit and state?

### In your own words, explain why the secret number kept changing in the original app.

The secret number didn't keep changing unless I clicked the "New Game" button. However, everything other than the secret number remained the same.

### How would you explain Streamlit "reruns" and session state to a friend who has never used Streamlit?

reruns, assuming referring to Streamlit rerun in 

### What change did you make that finally gave the game a stable secret number?

---

## 5. Looking ahead: your developer habits

### What is one habit or strategy from this project that you want to reuse in future labs or projects?
  > This could be a testing habit, a prompting strategy, or a way you used Git.
### What is one thing you would do differently next time you work with AI on a coding task?
### In one or two sentences, describe how this project changed the way you think about AI generated code.
