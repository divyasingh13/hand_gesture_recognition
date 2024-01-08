Hand Gesture Recognition using MediaPipe Library

MediaPipe Hands utilizes an ML pipeline consisting of multiple models working together: A palm detection model that operates on the full image and returns an oriented hand bounding box. A hand landmark model that operates on the cropped image region defined by the palm detector and returns high-fidelity 3D hand keypoints.

WE NEED A MODEL TO DETECT THE HAND AND THE GESTURES FOR THAT THERE ARE MODEL BUNDLES AVAILABLE THAT CAN BE USED:

The Gesture Recognizer contains two pre-packaged model bundles: a hand landmark model bundle and a gesture classification model bundle.

The landmark model detects the presence of hands and hand geometry, and
The gesture recognition model recognizes gestures based on hand geometry.
Building a basic hand gesture recognizer, which is recognizing 4-5 hand gestures on the basis of change of landmarks for better classification by considering the wrist point as the origin and measuring distances to the finger points from there, which will identify if the finger is closed or open. There are five conditions passed each for one finger and a thumb. The conditions will check if the finger is open or closed which will define a hand gesture , if a particular condition is satisfied,the model will identify it .

![image](https://github.com/divyasingh13/hand_gesture_recognition/assets/43674640/7d96210f-e93b-4d64-bf37-428d679e28e2)
![image](https://github.com/divyasingh13/hand_gesture_recognition/assets/43674640/439f09cb-6431-4f67-9b6d-94768ca866b0)

PALM DETECTION IS TIME CONSUMING THEREFORE IT USES A BOUNDING BOX DEFINED BY THE DETECTED HAND LANDMARKS IN THE CURRENT FRAME TO LOCALIZE THE REGIONS OF THE HAND IN THE NEXT FRAME.

Do these steps to recognize the steps: Step 1:Perform Hands Landmarks Detection Step 2:Build the Fingers Counter Step 3:Visualize the Counted Fingers Step 4:Build the Hand Gesture Recognizer

![image](https://github.com/divyasingh13/hand_gesture_recognition/assets/43674640/cb5b60ee-1d89-4b8e-9ab6-0e0f5dcbc621)
![image](https://github.com/divyasingh13/hand_gesture_recognition/assets/43674640/9e01682d-1644-44f8-9cc9-28fb257e7d03)

Returning the list of “recognized_gesture_list [3, 3, 3, 3, 3, 3, 3, 1, 1, 1, 1, 1, ]”


Note : Hand Gesture Task to be placed in the same directory as main.py Recognizing two hand gestures : victory and rock on:
