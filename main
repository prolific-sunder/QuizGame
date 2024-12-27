##############
#Program Start
##############

import random

def get_question_answer_words(possible_questions):
    question = random.choice(list(possible_questions.keys()))
    answer = possible_questions[question]
    return question, answer

def get_question_answer_math():
    variable1 = random.randint(1, 20)
    variable2 = random.randint(1, 20)
    operation = random.choice(['+', "-", "*"])
    question = f"What is {variable1} {operation} {variable2}?"
    if operation == '+':
        answer = str(variable1 + variable2)
    elif operation == "-":
        answer = str(variable1 - variable2)
    elif operation == "*":
        answer = str(variable1 * variable2)
    return question, answer

def main():
    status = True

    print("\nWelcome to trivia!\nEach correct trivia answer will give you +3 points. Each correct math answer will give you +1 point.\n")
    start = input("Press enter when you are ready to start!")

    while status == True:
        possible_questions = {
            'How many bones are in the human body?': ['206', '206 bones', '206 Bones'],
            'What vitamin is most important for vision?': ['A', 'Vitamin A', 'vitamin A', 'vitamin a', 'a'],
            'Do birds or dogs live longer?': ['Birds', 'birds'],
            'How many years are in a century?': ['100', 'A hundred', '100 years'],
            'When did World War 2 start?': ['September 1, 1939', '1939', 'On September 1, 1939', 'september 1, 1939'],
            'What data type holds characters in python?': ['str', 'string', 'Str', 'String', 'strings', 'Strings'],
            'What is 3 PM in Military Time?': ['1500', '15:00', 'Fifteen hundred'],
            'Who is the author of The Great Gatsby?': ['F. Scott Fitzgerald', 'Fitzgerald', 'Scott Fitzgerald', 'fitzgerald'],
            'What ballet is famously associated with Christmas?': ['Nutcracker', 'The Nutcracker', 'nutcracker', 'the nutcracker', 'the Nutcracker'],
            'What do you add to a recipe that tastes flat?': ['Acid', 'acid', 'lemon', 'Lemon', 'acidity', 'Acidity', 'lemon juice', 'Lemon Juice'],
            'What composer is considered to have composed the most difficult violin pieces? ': ['Paganini', 'paganini', 'Niccolo Paganini'],
            "What does the phrase 'comme ci, comme ca' mean? ": ['so-so', 'so so', 'neither good or bad', 'tolerable', 'mediocre', 'So-so'],
            'What animal produces silk? ': ['Silkworms', 'Silk Worms', 'silkworms', 'silk worms'],
            'How many times was King Henry VIII married?': ['6', 'six', 'Six', 'six times', 'Six times']
        }
        answer_key = []
        points = 0
        correct = 0
        count = 0
        while count < 10:
            question_type = random.choice(["Math", "Word"])
            if question_type == "Math":
                question, answer = get_question_answer_math()
                response = input(f"{count+1}. {question} ")
                answer_key.append(answer)
                if response == answer:
                    points += 1
                    correct += 1
                    print("Correct")
                else:
                    print("Incorrect")
            else:
                question, answer = get_question_answer_words(possible_questions)
                response = input(f"{count+1}. {question} ")
                if response in answer:
                    print("Correct")
                    points += 3
                    correct += 1
                else:
                    print("Incorrect")
                answer_key.append(answer)
                del possible_questions[question]
                
            count += 1
        
        print(f"\nYou got {correct} answers correct! \nYour score is: {points}")
        answers = input(f"Would you like to see the correct answers? (y/n) ")
        if answers == 'y':
            count = 1
            for item in answer_key:
                if isinstance(item, list):
                    print(f"{count}. {item[0]}")
                else:
                    print(f"{count}. {item}")
                count += 1

        again = input("\nWould you like to play again (y/n)? ")
        if again != "yes" or again != "y":
            status = False


        

if __name__ == "__main__":
    main()
