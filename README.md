import random

# Predefined responses for simple keywords
responses = {
    "hello": ["Hi!", "Hello there!", "Hey!"],
    "how are you": ["I'm doing great!", "All good here!", "I'm fine, thanks!"],
    "what is your name": ["I'm a simple chatbot.", "You can call me ChatBot."],
    "bye": ["See you later!", "Goodbye!", "Take care!"]
}

def chatbot():
    print("Welcome to the chatbot!")
    print("Type 'quit' anytime to exit.\n")

    while True:
        user_input = input("You: ").strip().lower()

        if user_input == "quit":
            print("Chatbot: Bye! Have a great day!")
            break

        matched = False
        for keyword, reply_list in responses.items():
            if keyword in user_input:
                print("Chatbot:", random.choice(reply_list))
                matched = True
                break

        if not matched:
            print("Chatbot: Hmm... I didn't quite get that.")

# Run the chatbot
chatbot()
