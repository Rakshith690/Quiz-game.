# Quiz-game.
This is a simple and interactive quiz application developed in Visual Studio Code. Language: Python C:\Users\rr175\OneDrive\Desktop\pyscript\pyscript\demo.py
"C:\Users\rr175\OneDrive\Desktop\rakshitha7 - Copy.pdf"
#python​ #tutorial​ #course
questions = ("who developed python programming language?: ",
                       "Python is Known as?: ",
                       "Which of these data types does python not natively support?: ",
                       "Which of the following is a mutable data type in python?: ",
                       "What data type would you use to store a whole number in python?: ",
                       "Which function is used to read input from the console in Python?:",
                       "which version of Python removed the print statement?:",
                       "Which of the following is an immutable dat type?:",
                       "which of the following is the correct extension of the python file?:",
                       "All keywords in python are in")

                      
options = (("A. wick van Rossum", "B. Rasmus lerdorf", "C. Guido van Rossum", "D. Niene Stom"),
                   ("A. A compiled language", "B. An interpreted language", "C. A machine language", "D. An assembly language"),
                   ("A. Lists", "B. Tuples", "C. Arrays", "D. Dictionaries "),
                   ("A. String", "B. Tuple", "C. List", "D. Integer"),
                   ("A. int", "B. float", "C. str", "D. bool"),
                   ("A. input()","B. read()","C. scan()","D. getinput()"),
                   ("A. python 1.x","B. python 2.x","C. python 3.x","D. python 4.x"),
                   ("A. Lists","B. Dictionaries","C. Tuples","D. sets"),
                   ("A. .python","B. .pl","C. .p","D. .py"),
                   ("A. Capitalized","B. lower case","C. UPPER CASE","D. None of the above"))

answers = ("C", "B", "C", "C", "A","A","C","C","D","D")
guesses = []
score = 0
question_num = 0

for question in questions:
    print("----------------------")
    print(question)
    for option in options[question_num]:
        print(option)

    guess = input("Enter (A, B, C, D): ").upper()
    guesses.append(guess)
    if guess == answers[question_num]:
        score += 1
        print("CORRECT!")
    else:
        print("INCORRECT!")
        print(f"{answers[question_num]} is the correct answer")
    question_num += 1

print("----------------------")
print("       RESULTS        ")
print("----------------------")

print("answers: ", end="")
for answer in answers:
    print(answer, end=" ")
print()

print("guesses: ", end="")
for guess in guesses:
    print(guess, end=" ")
print()

score = int(score / len(questions) * 100)
print(f"Your score is: {score}%")
