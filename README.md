# Face-Hand-Landmark-Detection
We will use mediapipe python library to detect face and hand landmarks.                                                            
We will use holistic model from mediapipe solutions to detect all the face and hand landmarks.                                               
Mediapipe is a cross-platform library developed by Google that provides amazing ready-to-use solutions for computer vision tasks.                            
OpenCV in python is a computer vision library that is widely used for image analysis, image processing, detection, recognition, etc.                              
                  
Step 1: Import all the necessary libraries                                                                                         
Step 2: Initializing holistic model and drawing utils for detecting landmarks on the image                                             
Parameters for holistic model:                                                                           
a. static_image_mode: It is used to specify whether the input images must be treated as static images or as a video stream. The default value is False.            
b. model_complexity: It is used to specify the complexity of the pose landmark model: 0, 1, or 2. As the model complexity of the model increases the landmark  
   accuracy and latency increase. The default value is 1.                                              
c. smooth_landmarks: This parameter is used to reduce the jitter in the prediction by filtering pose landmarks across different input images. The default value is 
   True.                                                                         
d. min_detection_confidence: It is used to specify the minimum confidence value with which the detection from the person-detection model needs to be considered as    successful. Can specify a value in [0.0,1.0]. The default value is 0.5.                                                   
e. min_tracking_confidence: It is used to specify the minimum confidence value with which the detection from the landmark-tracking model must be considered as  
   successful. Can specify a value in [0.0,1.0]. The default value is 0.5.                                                       
Step 3: Detecting Face and Hand landmarks from the image. Holistic model processes the image and produces landmarks for Face, Left Hand, Right Hand and also detects the pose of the                                                              
        a. Capture the frames continuously from the camera using OpenCV.                                    
        b. Convert the BGR image to an RGB image and make predictions using initialized holistic model.                                     
        c. The predictions made by the holistic model are saved in the results variable from which we can access the landmarks using results.face_landmarks, 
          results.right_hand_landmarks, results.left_hand_landmarks respectively.                                        
        d. Draw the detected landmarks on the image using the draw_landmarks function from drawing utils.                                          
        e. Display the resulting Image.                                                                                                            
The holistic model produces 468 Face landmarks, 21 Left-Hand landmarks, and 21 Right-Hand landmarks. The individual landmarks can be accessed by specifying the index of the required landmark.

