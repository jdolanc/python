def new_game():
    # making a empty list  to have the person enter 
    guesses = []
    # setting the guesses to 0 to start the game
    correct_guesses = 0
    # have the question set to 1 for the first question
    question_num = 1
# a for loop to get the questions to pop up
    for key in questions:
        print(key)
# nested for loop to have the first question start at the index of 0
        for i in options[question_num-1]:
            print(i)
            # getting the user's input
        guess = input("Enter (A, B, C, D): ")
        # making the guess upper case
        guess = guess.upper()
        # adds the guess to the empty list
        guesses.append(guess)
# taking the ques for the question and checking if it is correct
        correct_guesses += check_answer(questions.get(key), guess)
        # moving to the next question
        question_num += 1
        # showing the score
    display_score(correct_guesses, guesses)
# checking the answer for the score
def check_answer(answer, guess):
    if answer == guess:
        print("Correct answer")
        return 1
    else :
        print("Incorrect answer")
        return 0
def display_score(correct_guesses, guesses):
    print("Results:")
    # using a for loop to show the correct answers to the questions next to the guesses 
    print("Aswers:", end="")
    for i in questions:
        print(questions.get(i), end=" ")
    print()
    print("Guesses:", end="")
    for i in guesses:
        print(i, end=" ")
    print()

    score = int((correct_guesses/len(questions))*100)
    print("Your score is:"+ str(score)+ "%")


def play_again():
    
    response = input("Do you want to play again? (y/n): ")
    response = response.upper()

    if response == "YES":
        return True
    else: 
        return False
# the questions being asked 
questions = {
    "Who created Python?: ": "A",
    "What year was Python created?": "B",
    "Python is tributed to which comedy group?": "C",
    "Is the Earth flat?": "A"
}
#answers for the questions
options = [["A. Guido van Rossum", "B. Elon Musk", "C. Bill Gates", "D. Mark Zuckerberg"],
        ["A. 1989", "B. 1991", "C. 1990", "D. 2016"],
        ["A. Lonely Island", "B. Smosh", "C. Monty Python", "D. SNL"],
        ["A. True", "B. False", "C. Sometimes","D. What's Earth?"]]


new_game()
# a while loop to ask at the end of the quiz if they want to try and play again
while play_again():
    new_game()
print("Bye!")
