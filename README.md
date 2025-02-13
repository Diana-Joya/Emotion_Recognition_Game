# Polar
Polar is a facial expression recognition game that interacts with the user based on the user's emotion predicted from a live camera feed. Polar reacts to Happy, Sad, Angry, and Surprised facial expressions.

## Overview
Polar identifies 5 emotions linked to the user's facial expressions (Neutral, Happy, Sad, Angry, Surprised) but only fully reacts to 4 (excludes Neutral).

Each facial expression reaction provides a different user experience so try them all! 

## Getting Started
### Dependencies:
This project was created using Python 3.6 to avoid conflicts with Keras and TensorFlow.

To have the best experience while running this application, the following libraries need to be installed:

```
- Python 3.6
- pip (latest version)
- Keras 2.2.4 
- tensorflow 1.13.1
- Pillow (any version)
- opencv-python (any version)
- pygame 2.0
```

*Note:* Polar requires specific versions of some of these libraries to prevent the program from crashing. 

### Installing Dependencies:
The easiest way of installing the required dependencies is to clone the repository and run:

``` pip install -r requirements.txt ```

## Polar Game:
To run the Polar game:
1. Make sure you've installed all dependencies required ([instructions here](https://github.com/Diana-Joya/Polar/blob/master/README.md#installing-dependencies))
2. Run:
```python main.py```

### Troubleshooting:
**error: (-215:Assertion failed):** Depending on the camera drives in the host computer, sometimes a OpenCV cv2.error can be encountered if the camera doesn't return any feed. If this happens, exit the application and run again. 

**Facial Expression Accuracy:** Expression recognition accuracy can be affected by the angle at which the camera receives facial input from. For example, if you're having trouble getting an accurate read for 'Sad', slightly tilting your face forward might help. If your camera is too low from a front view of your face, it might have trouble reading 'Surprise', etc... The best way to troubleshoot this issue is by overexaggerating gestures and playing with the camera angles. 

*Note:* I also noticed the application had more trouble predicting my expressions if I had my glasses or any other accesory (hair included) covering part of my face.

## Facial Expression Recognition Training:
The dataset used to train the facial expression recognition model used in Polar, was provided by Kaggle and can be found in the **Challenges in Representation Learning: Facial Expression Recognition Challenge**, for more information on this data set see "[Kaggle Facial Expression Recognition Challenge](https://www.kaggle.com/c/challenges-in-representation-learning-facial-expression-recognition-challenge/data)"

The training model for the facial expression recognition part of the application can be found in the **Facial Expression Recognition** folder. It was inspired by VGG16, a convolutional neural network model proposed by K. Simonyan and A. Zisserman from the University of Oxford. This model was trained using TensorFlow and Keras.  

The trained model and HaarCascade utilities needed to run the facial expression recognition part of the application can be found in the **model** folder. 

The actual facial expression recognition part of the application can be found in the **emotion_classifier.py** file which can be modified to run outside of Polar. 

## Future Work
I'm currently working on adding further emotional reactions to each emotion to add more depth to the game, as well as adding a Fear based reaction.

## Music and Art Credits:
Polar was created and animated by me.

All other music and images are free stock and royalty free. Full credits can be found within the individual reaction folders within the reactions folder.
