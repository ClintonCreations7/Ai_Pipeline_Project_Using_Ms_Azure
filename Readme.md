Ai_Pipeline_Project_Using_Ms_Azure


#Overview


In this Project I created pipelines using diffrent machine learning techniques for different tasks using the canvas editor provided by MS Azure so
I didn`t perform any coding to speed up the process. In this project I showed my basic understanding of the differnt machine learning techniques
used.


#Regression TASK


Pipeline model design used for both the pipelines:


![image](https://github.com/user-attachments/assets/de6fc606-1992-4fc0-b3f2-bf746c84a8f4)


Pipeline 1 results:


![image](https://github.com/user-attachments/assets/34b76091-c1ec-43d5-89e1-2cf6a296abf1)


By looking at the result of the first pipeline you can see that I made use of all of the labels.
I did that by including them through the select column in dataset module within the pipeline, 
I made use of 70% of the data for training thorough the Split data module.
Since the purpose of the pipeline is to see the impact of different variables on the weekly sales you can work it out by focusing on the weekly sales that have the highest numeric value, the closer is the value to 1 = high weekly sales.
On the right the scored label section shows the predicted weekly sales for the given store.


Pipeline 2 results:


![image](https://github.com/user-attachments/assets/991f2293-a21b-42a4-bc1d-4696f55773de)


In the second You can notice that there are few variables compared to the first one I did that by excluding further unnecessary variables needed to predict the weekly sales.
Also I split 90% of the data trough the split data module.
On the right you can see the predicted sales for a given store, if you look at both the pipeline Images you can see that they are both slightly different.


#Classification Task


Pipeline model design used for both the pipelines:


![image](https://github.com/user-attachments/assets/1202cbf5-1476-47a2-a8be-51ec65f6ed41)


Pipeline 1 results:


![image](https://github.com/user-attachments/assets/ca237787-399c-4f85-bea7-4baf81cdba52)


In the first pipeline I made use of all of the labels, the data split I entered 0.7 and I normalised all the numeric values by using the normalise data module label values to make them similar between each other to avoid bias.


Pipeline 2 results:


![image](https://github.com/user-attachments/assets/b5bd26ba-d37c-4d41-ab63-09625fc83c40)


In this pipeline I still kept all of the labels, the only thing I changed is the split ratio where I entered 0.6
By looking at the score result of the dataset it is hard to find differences to see that I had to look at the evaluation results of each.

#Clustering Task


Pipeline model design used for pipeline:


![image](https://github.com/user-attachments/assets/1624921e-34c2-4191-85cf-b3549b4c9a16)


Pipeline 1 results:


![image](https://github.com/user-attachments/assets/e0210b95-bca4-45dc-b66d-3e6fc4de43e7)


By looking at the image of the this pipeline above you can see the flowers that are similar to each other, each Distance to cluster centre represents the types of flowers.
For each of the flowers the cluster that they are closer to represents the type of flower they are.
For this pipeline in the select column section I selected all the labels except the species since that what I was trying to predict, then I normalised all of the data within the column to have similar numeric representation to avoid the model to make errors.
For the split ration I entered 0.7 .


#Computer Vision Task


Pipeline model used for the pipeline:


![image](https://github.com/user-attachments/assets/fcf3d44f-6d59-417a-9bf3-d158446bbb9a)


Pipeline 1 results:


![image](https://github.com/user-attachments/assets/8df5d952-ebbd-4a62-af95-97676b441177)


By looking at the pipeline you can see that it classifies each image by showing their probabilities of resemblance for each of the landmarks used during the training.
To know the landmark of each image you just need to look at the scored labels of far right and it also shows the probability for all of the landmarks used during the training.
Other than organising the dataset folder with the images that I wanted to use I also set the split module to 0.9, then for the Train PyTorch model settings I set Epochs to 5, Batch size to 16, Warmup step number to 0, Learning rate 0.001, random seed to 1, Patience to 3 and Print frequency to 10
