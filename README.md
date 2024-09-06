# The-code-champs-
#Problem statement : Personal Voice Assistant
#by Hetvi Patel
#Janhavhi More
#Shreya Parikh
# code for text to speech
import win32com.client

speaker = win32com.client.Dispatch("SAPI.SpVoice")

while 1:
    print("Enter the word you want to speak it out by computer")
    s = input()
    speaker.Speak(s)

#code for speech to command
import speech_recognition as sr
import webbrowser
sr.Microphone(device_index=1)
r=sr.Recognizer()
r.energy_threshold=20000
with (sr.Microphone()as source):
    print("What you want to search")
    audio = r.listen(source)
    try:
        text=r.recognize_google(audio)
        url = "https://www.youtube.co.in/search?q"
        search_url = url+text
        webbrowser.open(search_url)

    except:
        print("Can't recognize")



import speech_recognition as sr
import webbrowser
sr.Microphone(device_index=1)
r=sr.Recognizer()
r.energy_threshold=20000
with (sr.Microphone()as source):
    print("What you want to search")
    audio = r.listen(source)
    try:
        text=r.recognize_google(audio)

        url= "https://www.amazon.co.in/search?q"


        search_url = url+text
        webbrowser.open(search_url)

    except:
        print("Can't recognize")



import speech_recognition as sr
import webbrowser
sr.Microphone(device_index=1)
r=sr.Recognizer()
r.energy_threshold=20000
with (sr.Microphone()as source):
    print("What you want to search")
    audio = r.listen(source)
    try:
        text=r.recognize_google(audio)

        url= "https://www.google.co.in/search?q"


        search_url = url+text
        webbrowser.open(search_url)

    except:
        print("Can't recognize")




