# iTeacher
An Educatif Chatbot with Deep Learning, Python and Flask REST API and Html sass and javascript

## Table of Contents

- [Requirements](#requirements)
- [VsCode Setup](#vscode)
- [Execution](#execution)

## Requirements (libraries)
1. TensorFlow
2. Flask
3. nltk
4. Keras
5. python
6. Sass


## VsCode SetUp
2. Create a python virtual environment 
```
# macOS/Linux
# You may need to run sudo apt-get install python3-venv first
python3 -m venv .venv

# Windows
# You can also use py -3 -m venv .venv
python -m venv .venv
```
When you create a new virtual environment, a prompt will be displayed to allow you to select it for the workspace.

3. Activate the virtual environment
```
#linux
source ./venv/bin/activate  # sh, bash, or zsh

#windows
.\venv\Scripts\activate
```
4. Run ```pip install --upgrade tensorflow``` to install ```Tensorflow```
5. Run ```pip install -U nltk``` to install ```nltk```
6. Run ```pip install -U Flask``` to install ```flask```
7. To expose your bot via Ngrok, run ```pip install flask-ngrok``` to install ```flask-ngrok``` Then you'll need to configure your ngrok credentials(login: email + password) Then uncomment this line ```run_with_ngrok(app) ``` and comment the last two lines ```if __name__ == "__main__": app.run() ``` Notice that ngrok is not used by default.
8. To access your bot on localhost, go to ```http://127.0.0.1:5000/ ``` If you're on Ngrok your url will be ```some-text.ngrok.io```

## Architecture

train.py — the code for reading in the natural language data into a training set and using a Keras sequential neural network to create a model
template — countain the code of user interface.
classes.pkl — a list of different types of classes of responses
words.pkl — a list of different words that could be used for pattern recognition
intents.json — abunch of JavaScript objects that lists different tags that correspond to different types of word patterns
chatbot_model.h5 — the actual model created by train_chatbot.py and used by chatgui.py


### Execution
To run this Bot, first run the ```train.py``` file to train the model. This will generate a file named ```chatbot_model.h5```<br>
This is the model which will be used by the Flask REST API to easily give feedback without the need to retrain.<br>
After running ```train.py```, next run the ```app.py``` to initialize and start the bot.<br>
To add more terms and vocabulary to the bot, modify the ```intents.json``` file and add your personalized words and retrain the model again.



[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-c66648af7eb3fe8bc4f294546bfd86ef473780cde1dea487d3c4ff354943c9ae.svg)](https://classroom.github.com/online_ide?assignment_repo_id=8085977&assignment_repo_type=AssignmentRepo)
