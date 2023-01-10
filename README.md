from flask import Flask
from datetime import datetime

app = Flask (__name__)

@app.route('/')
def hello():
    return"""<html><body>
    <h1><Hello, world!</h1>
    the time {0}.</body></html>""".format(
        str (datetime.now()))

# Launch the flask dev server
app.run(host="localhost", debug=True)
