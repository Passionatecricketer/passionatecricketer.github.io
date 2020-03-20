# passionatecricketer.github.io


A simple web application to predict the handwritten digit

Tech Stack :-

Python==3.6.5
Tensorflow==1.5
Tensorflowjs==1.6

Process:-

Step1 :- Creating the model

Create a basic model using tensorflow and keras to predict the digit using mnist dataset

Step2 :- Saving the model

Save the created keras model into a .h5 file

Command Used :-

model.save(‘model.h5’)

Step3 :- Convert the keras model into webmodel

Create a seperate virtual environment and install tensorflowjs

Command Used :-

pip install tensorflowjs

Convert the model

Command Used :-

Tensorflowjs_converter –input_format=keras path\to\.h5 file path\to\target_folder

Two files namely
Group1-shard1 of 1
Model.json
Will be created and will be used

Step4 :- Creating the Frontend

Create a file namely tfjs.html to include all the frontend part and tensorflow converted model and prediction to be made

Command used for loading model into html file – 

tf.loadLayersModel('model/model.json')

Command to make predictions –

window.model.predict([tf.tensor(input).reshape([1, 28, 28, 1])]).array()

Complete frontend code available in tfjs.html

