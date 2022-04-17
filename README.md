# DisFluency Detection Using Deep Learning


## Process of the Project

1.  Build a website and connect it to the AWS to save the recorded data which we get live.
2.  Data Analysis and Data Cleaning.
3.  Data Agumentations and Speech Processing tricks for a better output.
4.  Build a Deep Learning Model to Predict the disfluency in speech.



### Website Building and connecting to Github
We have build a simple website using bootstrap and HTML, basic javascript to do some operations in the website. Flask Package is used to deploy the website in Heroku. We have written script in such way that the audio collected is saved in AWS S3 bucket. Then we get to download the data from the bucket for further process. The website consits of  a GUI to record speech data, the person is given a set of questions to explain, and is about speak about 3 mins regarding ques. This is recorded and stored. 
The link of the website is attached below. 


https://myprosody.herokuapp.com/
![image](https://user-images.githubusercontent.com/48018142/163707254-5e810fcd-d281-41db-a81a-6bb1b35e72f7.png)


### Data Analysis Part

1.  The data we get is recorded from various devices and different browser extensions. So sampling rate is set accordingly for proper pre processing.
2.  Human Pitch for Men(100- 120Hz) and Women(300Hz), so low frequency information is necessary and high frequency is discarded. To do this we used a low pass filter.
3.  A window is 10 seconds is sampled so that we can send in limited features to detect disfluencies.
4.  The Mel scale mimics how the human ear works, with research showing humans don't perceive frequencies on a linear scale. Humans are better at detecting differences at lower frequencies than at higher frequencies. So we have used mel spectrograms as an input.



![image](https://user-images.githubusercontent.com/48018142/163707377-24d26e11-ce0a-4934-90fb-4d64911ea4af.JPG)








