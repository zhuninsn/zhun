# zhun

``` python
from flask import Flask
from flask import render_template
import glob
import os
from datetime import datetime

app = Flask("Elwing")

@app.route("/")
def root():
  ds = glob.glob("articles/*")
  result = []
  for d in ds:
    fs = glob.glob(d + "/*.txt")
    t = (d.split("/")[-1], len(fs))
    result.append(t)
  return render_template("index.html", d = result)
  ```
  
  ## ex
  yee | bang
  ----|----
  iiu | uhiu


![](https://www.google.com/url?sa=i&source=images&cd=&ved=2ahUKEwij-b-zpY7kAhWQHqYKHVViA_4QjRx6BAgBEAQ&url=https%3A%2F%2Fevctw.fandom.com%2Fwiki%2FYee&psig=AOvVaw02zou6sngJxpavQC_8Owd5&ust=1566282032653232
)
