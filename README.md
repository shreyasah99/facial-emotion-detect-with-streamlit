# Emotion detection using deep learning

## Introduction

We have  built a deep learning model which detects the real time emotions of students through a webcam so that teachers can understand if students are able to grasp the topic according to students' expressions or emotions and then deploy the model. The model is trained on the FER-2013 dataset .
 
 
This was a group project made by me and my friend Jatin. We decided we both will make a model for emotion detection , and the model which gave better accuracy, the further project would be done on that model.
I made a CNN model from scratch which gave an accuracy of 60. The github link for that model is: https://github.com/shreyasah99/Shreyas-Deep-Learning-Capstone-Face-Emotion-Recognition.git
 
Jatin made a model with the help of transfer learning and it gave an accuracy of 75. Since his accuracy was more than my model we decided to make the further project on his model. The github link for his model is :
https://github.com/jatin090/Jatin-Deep-Learning-Capstone-Face-Emotion-Recognition.git
 
 ## Deploying streamlit model
In this repository we have made a front end using streamlit. Streamlit doesn’t provide the live capture feature itself, instead uses a third party API. We used  streamlit-webrtc which helped to deal with real-time video streams. Image captured from the webcam is sent to  VideoTransformer function to detect the emotion.


Then this model was deployed on heroku platform with the help of buildpack-apt which is necessary to deploy opencv model on heroku. But heroku platform only allows model size as 500 mb. And tensorflow 2.0 itself takes 420 mb so we replaced it with tensorflow-cpu. All the other packages used and their version can be found in requirements.txt .
Our final model was of 380 mb and it was successfully deployed but the live stream itself takes 250-300 mb while loading live-stream or opening the webcam. And hence the webcam was not loading or opening and our model was not giving expected output.

Below is the link of our streamlit model on heroku:
https://jatin-shreyas-emotions.herokuapp.com/
 
 
We tried to deploy the model on azure as well, but same size issue was happening there also. 
Below is the link of our streamlit model on azure :
https://jatin-shreyas-app.azurewebsites.net/

 
Aptfile and setup.sh are only needed while deploying on heroku.

ReleaseLogs_38.zip and deploy.cmd are only needed while deploying on azure.
