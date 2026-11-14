# VoxGuard - Voice-Based Security Assistant

## Status: In Development

## What It Does
VoxGuard is a Python-based voice-controlled assistant focused on security tasks. The idea is to let a user control basic security actions using voice commands, hands-free.

Current features I am building:
- Voice command to lock the system
- Voice command to check system status
- Voice command to open security tools
- Voice alert when a command is recognized

## Tech Used
- Language: Python
- Libraries: SpeechRecognition, pyttsx3, os, datetime
- Platform: Windows / Linux

## How To Run
1. Clone this repo
2. Install requirements:
   ```bash
   pip install SpeechRecognition pyttsx3 PyAudio
   ```
3. Run:
   ```bash
   python voxguard.py
   ```
4. Say "Hey VoxGuard" and give a command like "lock system" or "system status"

## Current Limitations - Honest Note
- Works best in a quiet room, background noise affects accuracy
- Only supports English commands right now
- No real threat detection yet, it is a voice automation prototype
- Needs internet for Google Speech Recognition API

## What I Am Learning From This
- How voice recognition works in Python
- How to handle errors when voice is not recognized
- How to map voice commands to system actions securely

## Future Plan
- Add offline voice recognition
- Add Hindi voice commands
- Add a simple log file for every voice command for audit purpose

## Demo
Demo GIF will be added once the stable version is ready.
