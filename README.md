import random

responses = {
    "hello": ["Hi!", "Hey!", "Hello!"],
    "how are you": ["I'm good, thanks!", "I'm doing well!"],
    "what's your name": ["I'm a chatbot!", "I don't have a name!"],
    "bye": ["See you later!", "Bye!"],
}

def chatbot():
    print("Welcome to the chatbot!")
    while True:
        user_input = input("You: ").lower()
        if user_input == "quit":
            print("Chatbot: Bye!")
            break
        for keyword in responses:
            if keyword in user_input:
                print("Chatbot:", random.choice(responses[keyword]))
                break
        else:
            print("Chatbot: Sorry, I didn't understand that!")

chatbot()
