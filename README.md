# Software implementation of an algorithm for biometric identification of a person by single sample face image

### Description 

This project is designed to recognize people by a single face image, which is stored in the database.
The problem of Single Sample per Person was solved by augmentation of reference image.

### Example of work application

![](https://github.com/vbrovenk/Face-Identification/blob/master/imgs/run_app.gif)

### Scheme of algorithm

![](https://github.com/vbrovenk/Face-Identification/blob/master/imgs/process_diagramm.png)

The Algorithm includes following methods:
- **Augmentation** for extanding training set; 
- **Histogram of Oriented Gradients** for detection a region of face in image;
- **Normalization** in order to turn an image where eyes are on one y-axis; trained model shape_predictor_5_face_landmarks from Dlib is using to find 5 key landmarks on face image for finding a turning angle;
- **CNN**: trained model dlib_face_recognition_resnet_model_v1 from Dlib is using for extracting 128-d feature vector (embedding) from face image;