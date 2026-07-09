# Can-Thyroid-Cancer-be-Predicted-Using-Machine-Learning-
This was a project I made during my senior year of high school (Nov. 2024-Jan. 2025). This is a machine learning project built on Python and was used
to see if it was possible to predict thyroid cancer.

What is Thyroid Cancer?

According to the Mayo Clinic, thyroid cancer is a growth of cells that start in your thyroid area.
The thyroid is a butterfly shaped area located at the base of the neck that regulates heart rate, blood pressure, and bodyweight.
Thyroid cancer can cause a lot of issues ranging from changes in your voice to difficulty swallowing, to pain in your neck and throat.

Thyroid Cancer Prediction:

There have been a lot of advances in thyroid cancer prediction and scanning however two issues that seems to be common
are that it can often be recurrent if not treated properly and it has been hard to accurately predict if it will show up on a healthy person.
To combat these issues, I decided to research AI and machine learning and discovered the advancements made in training models to make predictions.
With proper data techniques alongside training the model with hundreds of patients' of data, we can make a very accurate AI model that allows us to
use the patients' medical history and lifestyle to see what are the chances they even get that cancer and if they had it once, what are the chances of getting it again.

What was used to build this model:

* Using synthetic patient data was the easiest way to complete this project due to time constraints, however if you gathered real patient data, the results will be more accurate.

* I used Google Colab to host my code. This uses the Python programming language which is what this entire project was coded off of.
* We used a variety of Python libraries such as pandas for data manipulation & analysis, numpy for numerical operations, matplotlib and graphviz for plotting and visualization, and scikit for preprocessing, model training, & plotting decision trees.

    A) For the algorithim, we used the random forest decision model. This combines the output of multiple decision trees and makes a single, accurate result.


Refer to the code blocks for step-by-step instructions on how to perform this. We will now focus on what the results mean, starting from the decision tree:
<img width="1570" height="790" alt="image" src="https://github.com/user-attachments/assets/3db3b7a0-270c-4bf1-8953-b4efa4ad6ae6" />

This is our final decision tree. This is basically saying that if the patient has a low response score, is a certain gender, has a small tumor size and no lymph node involvement and assuming the
arrows continue following the true value all the way to the bottom left, then this would suggest
that 144 patient would fit this exact profile and 0 had the severe condition. The model confidently
predicts this patients' tumor is harmless.
On the true box, if the gender is > 0.5, the model asks further questions about the patient's physical score.
The physical score basically says that, the model has narrowed the patients down to a smaller group of 20 people. These patients had similar or same outcome however the model isn't completely sure so it asks further questions. When the physical score is  > 3.5, the model reaches a final decision and doesn't need to ask anymore questions.
The blue box (leaf node) basically says that the model is extremely certain that every patient in this group has had the same outcome.

<img width="999" height="547" alt="image" src="https://github.com/user-attachments/assets/8879a8d9-f91b-4f9a-84a3-a8ff2f7a245b" />
This bar graph is a feature importance chart. What this means is that it ranks which features were the most important for training, analysis, and prediction. In our case, the most important features were Response, N, & T. N & T are thyroid glands and Response represents the patient's response to initial treatment.

<img width="691" height="547" alt="image" src="https://github.com/user-attachments/assets/5017b297-2503-48bf-8686-19715b4a6a40" />
This ROC (Receiver Operating Characteristic Curve) compares the amount of false positives compared to true positives. The blue line means that the closer the curve was to the upper left corner, the less mistakes the model made with the predictions. The red-dotted line simply represents if it is randomly guessing or not. If the blue line follows this line, then it wouldn't be any better than flipping a coin since it would be completely random. What we also saw was an area under curve (AUC) score of 1.00 meaning it was able to perfectly determine the difference between someone who had recurring cancer and someone who didn't.
