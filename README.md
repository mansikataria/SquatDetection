I have used MediaPipe to detect key points for human body joints,
which in turn allows us to detect squat pose. 

[Here is the Google Colab Notebook](https://github.com/mansikataria/SquatDetection/blob/main/Squat_Detection.ipynb)


![angle logic](https://user-images.githubusercontent.com/11619444/132310099-d62af5df-133e-4523-89f8-3463bff01fd6.jpg)

Used 4 different angles to detect the squat: 
1. Elbow joint (A), Shoulder joint(B), Hip joint(C) and Knee joint(D). 

2. Apply the three points method to calculate the angle between two lines.

3. See if the value for the angle between Hip join (C) and Knee joint (D) is less than 130 degrees.

4. To determine the correct hand position for squat I’ve set the value of the Elbow joint (A) to greater than 130 degrees, and the value of the Shoulder joint(B) to greater than 30 degrees and less than 120 degrees. 

5. The mean square error is used to train the model.

Some sample outputs:

![image](https://user-images.githubusercontent.com/11619444/132310340-6e38990c-e030-48de-b46c-b0093f864586.png)
![image](https://user-images.githubusercontent.com/11619444/132310419-f8945862-22b7-46a9-a851-94304c2bf771.png)
