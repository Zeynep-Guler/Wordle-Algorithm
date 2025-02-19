Assignment 1: Wordle
In this assignment, you will write a guesser for (a close cousin of) the game Wordle. Wordle is a word-guessing game, where you have 6 attempts to guess a 5-letter word. You can play it here

With each guess, you learn whether you correctly guessed a character (and its position), whether a character appears in the word but in a different position, or does not appear in the word at all.

📝 Task
The Wordle program we give you contains three classes (with pretty self-explanatory names):

game.py runs n games of Wordle coordinating the other two classes and keeps track of the scores. This script creates a new guesser object for every run.
wordle.py implements the game of Wordle, from choosing the word to guess to checking the correctness of a guess.
guesser.py produces a guess word. THIS IS WHAT YOU NEED TO MODIFY TO PRODUCE YOUR SOLUTION. At the moment, `get_guess' just returns a random word from the wordlist.
You also have two wordlists in tsv and yaml format:

train_wordlist (named as wordlist in the folder) contains ca. 4k words along with their frequency in an unnamed corpus, to be used for training. Using the word frequency data (e.g. to compute character n-gram probabilities) is completely optional.
dev_wordlist contains another 500 words for development, matching the size of the test set.
You can run 10 games of Wordle with python game.py --r 10.
When you run this command, the program will output some stats about your success rate.

Please note:

Do NOT modify wordle.py or game.py, or your submission might crash.
Using any variable or function of the World object that gives you a clue is cheating and will be graded 0!
🏅 Assessment
We will evaluate your guesser.py on a secret test set containing 500 words. Your grade will be based on a combination of:

How often your guesser.py correctly guesses the word.
The average number of tries it takes to produce a correct guess.
The time it takes to produce 500 guesses on the test set.
Please note:

Some of the words in the test set will neither be in the training nor the dev set. This is to make sure you don’t overfit your solution words you have access to. You cannot make any assumptions about how words will be selected / sampled from the test set (e.g. with or without replacement).
Your guess can be any 5-letter string. It does not have to be a word. However, the solution will always be drawn from the wordlist (which contains only words).
Our goal is to evaluate how good your guesser.py is at guessing words from a particular list of potential solution words. In the training set, this is wordlist.yaml. For the test set, we will swap this for the testset yaml – therefore, please do not rename wordlist.yaml in your code! This means your guesser.py will always have access to the list of words that the game is played on.
We discourage the use of non-standard Python libraries. We cannot guarantee they will be installed successfully when we run the evaluation script. Fancy packages are not necessary for a good solution!
📥 Submission Instructions
Please upload only your file called guesser.py (using exactly this name) to the BlackBoard Assignment 1 section.


