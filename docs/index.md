# Welcome to Cloud Computing module

CC repository can be found here [CC@GitHub](https://github.com/warestack/cc).

## Example of a simple Flask documentation page

<!-- termynal -->

```
$ warestack init
---> 100%
Warestack is cool!
```

### Codeblocks

Here is a simple `Flask` test docs.

#### Code for a specific language

Let's see how to import `Flask` in your script:

``` py
from flask import Flask
```

#### Hello World Flask!

``` py title="app.py"
from flask import Flask
app = Flask(__name__)
@app.route('/')
def index():
    return 'Hello, this is the version `1.0.0` of your flask app'
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)

```

#### Flask app with line numbers

``` py linenums="1"
from flask import Flask
app = Flask(__name__)
@app.route('/')
def index():
    return 'Hello, this is the version `1.0.0` of your flask app'
if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)

```

#### Dockerfile Flask (Highlighting lines 1, 15 and 17)

``` py hl_lines="1 15 17"
FROM ubuntu

# Create app directory
WORKDIR /app

# Install app dependencies
RUN apt update
RUN apt install python3-pip -y
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

COPY . .

# OPTIONAL as the `-p` flag is used while running the container
EXPOSE 8000

CMD ["python3", "-m", "flask", "run", "--host=0.0.0.0"]

```
> To run use the following command:
> `python app.py`

## Warestack on Social media

:fontawesome-brands-twitter:{ .twitter }
