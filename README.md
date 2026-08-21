# texttospeech
A simple Python script that converts written text into spoken audio using pyttsx3 or gTTS. This tool allows for easy integration of voice output in scripts, virtual assistants, or accessibility applications
Installation
Install the required library using pip.

For Offline Usage (pyttsx3):

pip install pyttsx3

For Online Usage (gTTS):

pip install gTTS
pip install playsound

Usage Examples
Option 1: Using pyttsx3 (Offline)

import pyttsx3

engine = pyttsx3.init()
engine.say("Hello, world!")
engine.runAndWait()

Option 2: Using gTTS (Online)

from gtts import gTTS
import os

tts = gTTS(text="Hello, world!", lang='en')
tts.save("output.mp3")
os.system("start output.mp3")

Customization
Rate: Adjust speaking speed using engine.setProperty('rate', 150). 
Volume: Set volume between 0.0 and 1.0 using engine.setProperty('volume', 0.8). 
Voice: Select male/female voices via engine.getProperty('voices') and setting the voice property to the desired ID. 
License
