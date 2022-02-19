# Creating a Flask web-site

# Tutorial Link
https://projects.raspberrypi.org/en/projects/python-web-server-with-flask

# Instructions
1) cd ~   # Go to your home directory
2) mkdir -p ~/Projects/raspberrypiclass/lessons/D-web-server # Make the project directory
3) cd ~/Projects/raspberrypiclass/lessons/D-web-server       # Go to the project directory
4) nano app.py
from flask import Flask

app = Flask(__name__)

@app.route('/')
def index():
  return 'Hello world'

if __name__ == '__main__':
  app.run(debug=True, host='0.0.0.0')

5) Open up a browser on localhost:5000
   You should see the message Hello world

6) Use nano to add lines to the file after the return 'Hello world' line

@app.route('/cakes')
def cakes():
  return 'Yummy cakes'

7) Change the address in the browswer to localhost:5000/cakes
   You should see the message Yummy cakes

8) Try changing the address in the browser back to localhost:5000

9) mkdir templates   # Create a directory for HTML templates

10) cd templates   # Go into the templates directory

11) nano index.html  # Create/Edit a file in the templates directory called index.html

<html>
<body>
<h1>My webiste</h1>
</body>
</html>

12) cd ~/Projects/raspberrypiclass/lessons/D-web-server

13) nano app.py   # Edit the app.py file
On the top line, change:
    from: from flask import Flask
    to:   from flask import Flask, render_template

Change line 7:
    from: return 'Hello world'
    to:   return render_template('index.html')
