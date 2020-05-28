## Bert-Toxic-Text-Detector
A flask web app that demonstrates a method to use the Bert language model as an Ai microservice.

The demo app is now offline.<br>
Demo App: http://toxic.test.woza.work/

<br>

<img src="http://toxic.test.woza.work/assets/app_pic1.png" width="350"></img>

<br>

My goal for this project was learn how to build and deploy a production-grade toxic text detection model. Users are able to send text to the model, via an API, and get back predictions. I'm not a frontend or backend expert. I tried to learn enough to get things working.

One way to commercialize a powerful language model like Bert is to deploy it as a microservice. This means that the model lives on a cloud server. Websites can send text to this server. The server responds by sending back a toxicity prediction for each piece of text. The system can also be set up to allow a user to send a file containing rows of text. The model will process this file and the server will return a new file with a prediction for each row.

A tool like this could automatically monitor large volumes of online dialogue. It could help improve the quality of online conversations, protect children from online bullying and protect a companies brand image - but it could also be used for mass surveillance.

Model AUC score: 0.88

The process used to build and train the model is described in this Kaggle kernel:<br>
https://www.kaggle.com/vbookshelf/bert-as-a-microservice-flask-app

The model was fine tuned using data made available during the Kaggle Jigsaw Multilingual Toxic Comment Classification compeition. The data is licenced for any use.<br>
https://www.kaggle.com/c/jigsaw-multilingual-toxic-comment-classification


### Server Deployment

All the frontend and backend code is available in this repo. The model is not included because it was too large to upload. It can be downloaded by following the Kaggle notebook link above. Please put the model inside the subfolder called 'flask' before uploading the entire Toxic Comment Detector folder to your server.

The code is set up to be run as a Docker container. It's based on this video tutorial:

Julian Nash docker and flask video tutorial<br>
https://www.youtube.com/watch?v=dVEjSmKFUVI

The .dockerignore file may not be visible. Please create this file if you don't see it. I suggest that you deploy on a Linux server running Ubuntu 16.04. In this repo I've included a pdf that explains the steps for installing Docker and Docker Compose on a Linux server. 
