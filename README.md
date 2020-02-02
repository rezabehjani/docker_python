# docker_python
# image python on ubutu 


*  stap 1
make file name test

* stap 2
open notpad write
```
from flask import Flask
app = Flask(__name__)
@app.route("/")
def hello():
    return "Hello World!"
if __name__ == "__main__":
    app.run(host="0.0.0.0", port=int("5000"), debug=True)
```
save name index.py
*  stap 3
open notpad and write
```
FROM python:3.7
COPY . /app
WORKDIR /app
RUN pip install -r requirements.txt
EXPOSE 5000
CMD python ./index.py

```
save file whit name Dockerfile

*  stap 4
open notpad write
```
flask
```
save name requirements.txt

* stap 5
open terminal in file
```
docker build --tag my-python-app .
```
whait to complet command excute 

* stap 6
```
docker run --name python-app -p 5000:5000 my-python-app
```
