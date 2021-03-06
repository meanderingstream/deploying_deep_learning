---
title: Deploying Deep Learning
theme: moon
revealOptions:
    transition: 'fade'
---
## Intro

Scott Mueller

###### smueller.tampa.ai@gmail.com

Zach Mueller
###### muellerzr@gmail.com

---
## Tampa.ai

Looking for Presenters

---
# Deploying Deep Learning Models
---
* "Brilliant" Deep Learning Idea
* Built initial Model
> Minimum Viable Product
* What could go wrong
* Deployment Alternatives
* Choices
* Example Project

---
## We'll Focus on smaller scale project

* Websites
* Low-volume Services

> Higher-scale --> Resources to solve that challenge
---
## Normal Father-Son Activities
<img src="./images/NormalFatherSon.JPG"  height="500">

---
## Data Science Father-Son
<img src="./images/FatherSon.jpg"  width="500">
---
## Fast.ai v3
<img src="./images/bears.png"  width="500">
---

## Applying Fast.ai

### Is it Venemous?

---
## Good Friends
<img src="./images/zach_zane.jpg"  width="500">
---
## Is it Venemous?

<img src="./images/RingNeck.jpg"  width="500">
---
## Google Colab
<img src="./images/ColabNotebook.png"  width="500">
---
## Gathering and Sorting Data
<img src="./images/making_folders.png"  width="500">
---
## Learning
<img src="./images/ReLearn.png"  width="500">
---
## Incorrectly Classified
<img src="./images/confusion_matrix.png"  width="500">
---
## Clean up Data
<img src="./images/most_confuse_pred.png"  width="500">
---
## Fast.ai Lessons

* Need an expert to help verify what you are doing is correct
* Google Colab wipes workspace after 12 hours
* Google Colab does not support plugins
* For a free service still works exceptionally well

---
## Let's Build a Website
<img src="./images/file_uploader.png"  width="800">
---
## What could go wrong?

* Misidentification
* Linked to Bank Account
* Obtain some business value
* Security of application
---
## Model is just a function
<img src="./images/WebsiteWModel.png"  width="400">

> Inputs, Processing, Result
---
## Inference
<img src="./images/Inference.png"  width="400">
---
## Example Inference Code

```python
pred_class,pred_idx,outputs = learn.predict(img)
pred_class
```

```python
'black'
```
---
## Architectures for Function Calls

* Remote Procedure Calls
* SOAP requests
* JSON Service
* Web Socket Communication
* Serverless
---
## Why Distributed?

* Deep Neural Nets use lots of Memory
* Lots of simple math function calls
* Slows down your web server when scaling model calls
---
## To GPU or not to GPU?

* Latency impact on business
* Sustained concurrent usage

---
## Remote Function Calls
---
## Serverless

<img src="./images/zeit_now.png"  width="500">

https://zeit.co/
---
<img src="./images/zeit_guide.png"  width="700">
---
## Flask Server

* Simple Python Server

<img src="./images/flask_server.png"  width="700">

http://flask.pocoo.org/]
---
Productionizing Flask

<img src="./images/gunicorn.png"  width="700">

https://vsupalov.com/flask-web-server-in-production/

---
## Remote communication via JSON

* Security
* Denial of Service Attack Robustness
* Direct Service Access by 3rd Party 
---
## Calling between languages
```elixir
  @doc """
  Call python function using MFA format
  """
  def call_python(pid, module, function, arguments \\ []) do
    pid
    |>:python.call(module, function, arguments)

  end
```
* Elixir calling Python
---
## Example Applications

https://github.com/nikhilno1/healthy-or-not/blob/master/heroku-deploy.md

https://github.com/dzlab/deepprojects/tree/master/emotion-classifier

https://hackernoon.com/anothernothotdog-280ee5b86fb3

https://github.com/keyurparalkar/ASL-live-predictor

---

https://medium.com/@lankinen/fastai-model-to-production-this-is-how-you-make-web-app-that-use-your-model-57d8999450cf

https://github.com/etown/dl1/blob/master/face/README.md

https://github.com/EdwardJRoss/whatcar

https://medium.com/datadriveninvestor/building-a-cold-or-canker-sores-classifier-app-using-deep-learning-242b8c80fbe5

https://github.com/tamlyn/treeid


---
## Optimization

* Latency vs Accuracy
* Cost vs Accuracy at medium scale
---
## Distillation

- Train accurate, complex model

- Train a simpler model from complex model
---
<img src="./images/knowledge_distillation_medium_com_neural_machines.png"  width="600">

https://medium.com/neural-machines/knowledge-distillation-dc241d7c2322

---
Questions?
---
## Study Group

https://ai-tampa-study-group.github.io/meetings/

---

[MomsSafetyNet.com](https://www.momssafetynet.com/team.html)

Looking for Founder Engineers

Elixir, Functional Programming, Rails, Experience

Web presentation skills