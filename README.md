# CodeQuest

A gamified quiz platform that helps programming students practise through points, levels, streaks, badges, lives and timers. Built as a prototype for a project on gamified learning platforms.

## Features

- **7 topics:** Python, C, DSA, Java, Web (HTML, CSS, JavaScript), SQL, AI/ML (5 questions each)
- **XP and levels:** every correct answer earns XP, and each 100 XP is one level
- **Daily streak:** finish a quiz on consecutive days to grow your streak
- **Badges:** First win, Perfect 5, Hot run, Level 2, 3-day streak, Speed demon, Brave
- **Lives:** 3 per quiz; a wrong or timed-out answer costs one
- **Timer:** a countdown bar on every question
- **Difficulty levels:** Easy, Medium, Hard (Hard unlocks at level 3)
- **Mistake review:** missed questions are listed with the answer and an explanation
- **Dashboard and leaderboard:** XP, level, streak, quizzes played, badges and rank
- **Demo sign-in:** name only, saved in the browser (no password, no server)
- Works on phone and desktop, with light and dark themes

## How to run

1. Double-click `index.html` to open it in any modern browser.

No installation, build step or internet connection is needed. If you are offline, the page uses your system fonts instead of the Google Fonts it normally loads.

## How to play

1. Enter your name (or continue as guest).
2. Choose a difficulty and a topic.
3. Answer 5 timed questions. You have 3 lives.
4. See your score, XP, level-up and new badges, then review your mistakes.
5. Open the **Dashboard** tab to see your stats, badges and leaderboard rank.

## Scoring rules

| Difficulty | Time per question | XP multiplier | Unlock |
|---|---|---|---|
| Easy | 20 seconds | 1x | Level 1 |
| Medium | 12 seconds | 1.5x | Level 1 |
| Hard | 8 seconds | 2x | Level 3 |

Quiz XP = (20 per correct answer + 5 per fast answer + 20 bonus for a perfect score) x difficulty multiplier.
A fast answer is one given with more than half the time left. Level = 1 + (total XP / 100, rounded down).

## Demo tips

On the **Dashboard**:
- **Demo tool: add 100 XP** helps you reach level 3 quickly to show the Hard unlock.
- **Demo tool: pretend it is a new day** lets the next quiz count as a new day, so you can show the streak growing.
- **Reset progress** clears XP, badges and streak (your name is kept).
- **Log out** returns to the sign-in screen.

## Project structure

```
CodeQuest/
  index.html   The whole app (HTML, CSS and JavaScript in one file)
  README.md    This file
```

## How it works

- Plain JavaScript functions, with comments in the code and no frameworks.
- Questions are stored in one `Q` object, so adding a question or topic means adding entries to it.
- Progress (name, XP, streak, badges, quizzes played) is saved in the browser's local storage.

## Adding your own questions

In `index.html`, find the `Q` object and add an entry to a topic:

```js
{q:'Your question?', o:['Option A','Option B','Option C','Option D'], a:1, e:'Short explanation.'}
```

`a` is the index of the correct option (0 for the first option). To add a new topic, also add its name to the `ICONS` and `INFO` objects.

## Limitations

- 5 questions per topic; difficulty changes time and XP, not the questions
- The leaderboard uses sample players, and progress is stored in one browser only
- The sign-in is a demo with no real authentication

## Future scope

Adaptive difficulty, AI-generated hints and explanations, larger question banks with separate Easy/Medium/Hard questions, real accounts and a shared leaderboard, a teacher dashboard, and daily challenges.

## Author

Maithilee Sachin Kadam, B.Tech Computer Science & Engineering, Sharad Institute of Technology, College of Engineering
