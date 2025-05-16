# speech-based-search-engine

# Speech-Based Search Engine

## Overview

This script provides a **voice-controlled interface** that listens to the user's speech, transcribes it using Google's Speech Recognition API, and performs a **Google search** with the spoken query. It responds via **text-to-speech** using `pyttsx3`.

## Features

* Listens to voice input through the microphone.
* Converts speech to text using Google Speech Recognition.
* Automatically performs a Google search with the spoken query.
* Uses text-to-speech to interact with the user.

## Dependencies

Install the required Python libraries:

```bash
pip install SpeechRecognition pyttsx3 pyaudio
```

> **Note**: `pyaudio` may require additional setup depending on your OS.

## How It Works

### 1. Initialize Text-to-Speech Engine

```python
engine = pyttsx3.init()
```

### 2. Speak Function

Converts text to speech.

```python
def speak(text):
    engine.say(text)
    engine.runAndWait()
```

### 3. Voice Input

Listens via microphone and uses Google’s API to recognize speech.

```python
def take_command():
    ...
    query = r.recognize_google(audio)
```

### 4. Perform Search

Opens a Google search in your default browser.

```python
def search_web(query):
    url = f"https://www.google.com/search?q={query}"
    webbrowser.open(url)
```

### 5. Entry Point

```python
if __name__ == "__main__":
    query = take_command()
    search_web(query)
```

## Usage

Run the script in your terminal or IDE:

```bash
python "speech based search engine.py"
```

Then, speak your search query when prompted.

---
