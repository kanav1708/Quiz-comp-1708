# Define the quiz questions and answers
quiz = [
    {
        "question": "What is 5 + 2?",
        "options": ["A. 3", "B. 7", "C. 5", "D. 6"],
        "answer": "B"
    },
    {
        "question": "Who wrote 'To Kill a Mockingbird'?",
        "options": ["A. Harper Lee", "B. J.K. Rowling", "C. Ernest Hemingway", "D. Mark Twain"],
        "answer": "A"
    },
    {
        "question": "What is the chemical symbol for water?",
        "options": ["A. CO2", "B. H2O", "C. O2", "D. N2"],
        "answer": "B"
    },
]

# Function to conduct the quiz
def conduct_quiz(quiz):
    score = 0
    for i, item in enumerate(quiz):
        print(f"Question {i+1}: {item['question']}")
        for option in item["options"]:
            print(option)
        answer = input("Your answer (A/B/C/D): ").strip().upper()
        if answer == item["answer"]:
            score += 1
        print()  # Newline for better readability

    print(f"You got {score} out of {len(quiz)} questions correct!")

# Start the quiz
conduct_quiz(quiz)
