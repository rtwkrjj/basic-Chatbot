# Chatbot with NLP

This repository contains a simple chatbot built using Natural Language Processing (NLP) techniques. The chatbot is designed to answer a set of predefined questions, including topics such as:

- **Plane crash WTC final**
- **Australia vs South Africa cricket matches**
- **Cricketers' knowledge**
- ...and more!

The chatbot uses a basic intent-and-response approach with dictionaries for matching user input and generating appropriate responses. The implementation is straightforward, making it easy to extend with more questions and answers.

## Skills and Features

- Intent detection using simple NLP techniques
- Predefined responses based on recognized intents
- Looping conversation structure to handle multiple user queries
- Easily extensible for new intents and responses

## Programming Language

- **Python**

## Libraries Used

- **NLTK** (Natural Language Toolkit) for basic NLP processing
- **Dictionaries** to map intents and responses

## How it Works

1. **User Input:** The chatbot repeatedly prompts the user for questions.
2. **Intent Matching:** The input is processed using NLP (tokenization, lowercasing, etc.) to match predefined intents.
3. **Response Generation:** The chatbot uses a dictionary to look up and return the appropriate response.
4. **Looping:** The chatbot continues to interact until the user chooses to exit.

## Example Structure

```python
import nltk

# Example intents and responses dictionary
intents = {
    "wtc final": "The World Test Championship final was played between...",
    "aus vs sa": "Australia vs South Africa is a classic cricket rivalry...",
    "cricketer knowledge": "Ask me about famous cricketers and their records...",
    # Add more intents and responses here
}

def get_intent(user_input):
    for key in intents:
        if re.search(key, user_input.lower()):
            return key
    return None

while True:
    user_input = input("You: ")
    if user_input.lower() in ["exit", "quit", "bye"]:
        print("Chatbot: Goodbye!")
        break
    intent = get_intent(user_input)
    if intent:
        print(f"Chatbot: {intents[intent]}")
    else:
        print("Chatbot: Sorry, I don't understand that yet.")
```

## How to Contribute

Feel free to **collaborate**, **suggest improvements**, or **extend the chatbot** with new skills and topics! Contributions are welcome—just open an issue or submit a pull request.

If you have ideas for new features, better NLP techniques, or more comprehensive cricket knowledge, your input is appreciated!

---

**Let's make this chatbot smarter together!**
