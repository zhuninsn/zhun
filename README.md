# zhun

![](https://github.com/zhuninsn/zhun/blob/master/%E6%9C%AA%E5%91%BD%E5%90%8D.png)

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



