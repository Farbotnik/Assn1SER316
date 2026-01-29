Author:Neil Farbotnik
README
=========
dev
documentation: README.md
feature1: play again
feature2: max attempts
feature3: hint system
hotfix:randomInt
main

=========
\* ab7cd7b (hotfix) Fix randomInt to properly include max value in range
| \* 1f23d1c (feature3) done
| \* 3631e47 had to fix
| \* c070288 got it done
| \* f1097b6 started hint
|/
| \* e367776 (HEAD, feature2) Implement max attempts logic and game over condition
| \* 45aa640 Add maxAttempts constant and game over state
| \* 5f95961 (dev) Add encouraging message for players
|/
| \* f48cf81 (feature1) Add version comment documenting quit feature
| \* 9df380f Improve user feedback messages for guesses
| \* f8dfe81 Add play-again loop functionality
| \* 3bbc201 Add ability to quit game with negative number input
|/
\* 45767c4 (main) Initial Number guessing game
=========
d5fe07a (HEAD -> dev) Cherry-pick hotfix and merge main to dev
283d18a (main) Fix randomInt to properly include max value in range
6a1e192 (feature2) Resolving conflicts for merging dev into feature2
941de75 (feature3) Add hint system to show proximity after 3 attempts and rebase
fa05240 step 4 gradlew commit (stash didnt work)
e4d9f11 Implement max attempts, game over condition, and rebase dev
4207b41 fixed merge conflict with userQuit and gameOver Logic
3d6e0cb Merge branch 'dev' into feature1
f48cf81 Add version comment documenting quit feature
9df380f Improve user feedback messages for guesses
f8dfe81 Add play-again loop functionality
3bbc201 Add ability to quit game with negative number input
5f95961 Add encouraging message for players
45767c4 Initial Number guessing game
=========
1) Differences between:
- merge: combines 2 branches together and keeps all the history, makes a merge commit so you can see where stuff came from
- rebase: takes your commits and rewrites them on top of another branch so it looks clean and linear, but you lose track of all the where everything came from, lacking context.
- squash: combines a bunch of little commits into one commit so your history isn't as cluttered
- cherry-pick: extracts a specific commit from another branch without bringing along all the other ones and applies it
2) Observed in git history between feature1, 2, 3: feature1 you can see the merge commit and branching structure in the history, before it was deleted. feature2 and feature3 commits are both stacked linearly on dev, it looks way cleaner but there is some lost context that they were separate branches originally.
3) When would each strategy be used in a real project:
- merge: on shared branches like dev/main where you want to preserve history. Safe for team collaboration.
- rebase: on your personal feature branches before merging to keep history clean and linear. Not on a shared branch, may screw over the teammates.
- squash: when merging a feature branch that has tons of small commits, as it condenses messy work.
- cherry-pick: when you need one specific bug fix from another branch without pulling in all the other unfinished work.
=========
*   d5fe07a (dev) Cherry-pick hotfix and merge main to dev
|\
| * 283d18a (main) Fix randomInt to properly include max value in range
* |   6a1e192 (feature2) Resolving conflicts for merging dev into feature2
|\ \
| * | 941de75 (feature3) Add hint system to show proximity after 3 attempts and rebase
* | | fa05240 step 4 gradlew commit (stash didnt work)
* | | e4d9f11 Implement max attempts, game over condition, and rebase dev
* | | 4207b41 fixed merge conflict with userQuit and gameOver Logic
|/ /
* |   3d6e0cb Merge branch 'dev' into feature1
|\ \
| * | 5f95961 Add encouraging message for players
| |/
* | f48cf81 Add version comment documenting quit feature
* | 9df380f Improve user feedback messages for guesses
* | f8dfe81 Add play-again loop functionality
* | 3bbc201 Add ability to quit game with negative number input
|/
* 45767c4 Initial Number guessing game