COMPANY NAME: CODTECH ITSOLUTION
NAME: KASHISH SHEWALE
DOMAIN : PYTHON LANGUAGE
DURATION: 4 WEEK
INTERN ID: CT08QSJ
# TASK3
import nltk
import random
import string
from nltk.chat.util import Chat, reflections

# Download the necessary NLTK data (you only need to run this once)
nltk.download('punkt')

# Define pairs of patterns and responses
pairs = [
    (r"hi|hello|hey", ["Hello! How can I help you today?", "Hi there! How can I assist you?"]),
    (r"what is your name?", ["I am a chatbot created to assist you!", "You can call me Chatbot!"]),
    (r"how are you?", ["I'm doing great, thank you for asking!", "I'm just a bot, but I'm doing well!"]),
    (r"what can you do?", ["I can assist you with various tasks and answer questions.", 
                          "I can answer questions, provide information, and more!"]),
    (r"tell me a joke", ["Why don't programmers like nature? It has too many bugs!",
                         "Why do programmers prefer dark mode? Because light attracts bugs!"]),
    (r"bye|exit", ["Goodbye! Have a nice day!", "See you later!"]),
    (r"(.*)", ["I'm sorry, I didn't quite understand that.", "Could you rephrase your question?"])
]

# Create the chatbot using the defined pairs
chatbot = Chat(pairs, reflections)

# Function to initiate the chat
def start_chat():
    print("Hello! I am your chatbot. Type 'exit' or 'bye' to end the chat.")
    while True:
        user_input = input("You: ")
        if user_input.lower() in ['exit', 'bye']:
            print("Chatbot: Goodbye!")
            break
        response = chatbot.respond(user_input)
        print("Chatbot:", response)

if __name__ == "__main__":
    start_chat()
OUTPUT:
Hello! I am your chatbot. Type 'exit' or 'bye' to end the chat.
You: hi
Chatbot: Hello! How can I help you today?

You: what can you do?
Chatbot: I can answer questions, provide information, and more!

You: tell me a joke
Chatbot: Why don't programmers like nature? It has too many bugs!

You: how are you?
Chatbot: I'm doing great, thank you for asking!

You: exit
Chatbot: Goodbye!
