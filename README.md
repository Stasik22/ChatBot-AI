# 🤖 Simple AI Chatbot with TensorFlow & NLTK

This is a simple AI chatbot built with Python, TensorFlow, and Natural Language Toolkit (NLTK). It uses a basic intent classification model trained on predefined conversation intents (e.g., greetings, FAQs) to simulate natural interactions.

## 📦 Features

- Intent classification using a neural network (TensorFlow)
- Natural language processing (tokenization, lemmatization)
- Easy customization through a JSON file of intents
- Persistent trained model using `.h5` format
- Fully terminal-based chat interface
- Learns from user-defined patterns and responds accordingly

## 🧠 How It Works

1. **Data Preparation**: The chatbot reads a `intents.json` file that contains various tags (intents), each with example phrases and responses.
2. **Model Training** (`Training.py`):
   - Text preprocessing (tokenizing and lemmatizing user input)
   - Bag-of-words encoding
   - Training a feedforward neural network for intent classification
3. **Chat Runtime** (`Chatbot.py`):
   - Loads the trained model and vocabulary
   - Predicts user intent
   - Responds with a random predefined message from the predicted intent

## 🚀 Getting Started

### Requirements

- Python 3.8+
- `nltk`
- `tensorflow`
- `numpy`
- `pickle`

Install dependencies:
```bash
pip install nltk tensorflow numpy
```


This will generate:
- `chatbotmodel.h5`
- `words.pkl`
- `classes.pkl`

## 📝 Customize

Edit `intents.json` to add your own tags, patterns, and responses.

```json
{
  "tag": "greeting",
  "patterns": ["hello", "hi", "hey"],
  "responses": ["Hello!", "Hi there!", "Greetings!"]
}
```

## 📁 Project Structure

```
├── Chatbot.py           # Main chat interface
├── Training.py          # Model training script
├── intents.json         # Predefined intents, patterns, and responses
├── chatbotmodel.h5      # Trained model (generated)
├── words.pkl            # Vocabulary data (generated)
├── classes.pkl          # Intent labels (generated)
```

## 🙋‍♂️ Credits

Based on a simple intent classification chatbot architecture using NLTK and TensorFlow. Inspired by educational content from [NeuralNine](https://www.youtube.com/c/NeuralNine) and extended for personal use.

## ⚡️ Future Improvements

- Add GUI interface with Tkinter or PyQt
- Connect to Telegram or Discord
- Add speech input/output
- Integrate with APIs (e.g. weather, time)
- Add support for contextual conversations
