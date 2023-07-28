## Happy-Sad-Angry Model

This model is used to predict people's emotions based on their face. It is trained on an imagenet Resnet-18 model using transfer learning. A.I models that can recognize emotions can be used in a variety of fields, like healthcare, marketing, customer service, and car safety. 

## The Algorithm
The algorithm uses a 2GB Jetson Nano, and so it uses a preflashed SD card flashed from the NVIDIA web page. Because the Jetson Nano can't support a live video, I've opted to use images. It uses a facenet to find a person's face in the image, then it crops the image to just hold the face. It then sends the face to the transfer learning model. The transfer model then predicts your emotion. It will try to guess your emotion to the best of its abilities. Then it will print out the emotion if it is confident. It is up to the user to interpret the information.
Note: I ran this model on a relatively low epoch with information that was askew. The pretrained model is quite inaccurate. 

## Running this project
1. Connect to your Jetson Nano via VSCODE. 
2. Ensure that you have the proper things installed. The Renet18.onnx and all others like that - the ones that say resnet18.onnx and the train.py. Also, esure that you have the labels.txt file.
3. Run the docker container and train and export the model.
4. Exit the docker container and run the model. 

[View a video explanation here](video link)
