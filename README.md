# SilentVoice

### Submission for HackPrinceton 2021

## Inspiration
While spending the past school year taking purely virtual classes because of COVID-19 restrictions, I often referred back to recordings of online lectures when reviewing concepts learned in class. I would tend to open up clsoed captions on these recordings whenever the content shown on screen got a bit too messy or if I wanted to confirm the technical terms the lecturer was using. However, the closed captions were often unreliable and I realized that many would find it challenging to learn from these videos. Additionally, deaf people or those with challeneged hearing would have to exclusively rely on these unreliable ways of conveying the information in lectures. Thus, I set out to increase the accessibility of video lectures by creating an app that dubs videos in American sign language while providing a transcript and text summary of the contents of the video.  

## What it does
SilentVoice aims to eliminates the language barrier in education. It lets users dub lectures in sign language using cutting-edge deep learning technology. To use it, users first have to log in using **Firebase Authentication**. Then, they can paste the YouTube link of their desired lecture and our web app will provide users with a video featuring the ASL translation of the contents of the initial video. 

## How I built it
I used many libraries to create this, including but not limited to: **Google Cloud (Cloud Storage and Cloud Functions), Google OAuth, and Google Cloud Speech-to-Text API, Google Translate API, and Google Cloud Artificial Intelligence Platform**. I used Flask, Pytorch, Scikit-Learn, and OpenCV for the machine learning back-end and Tailwind CSS, React JS, and Chakra UI for the dashboard and landing page frontend. I also used OpenAI to generate summaries of video transcripts.

Here is the workflow for our web application:
1. Download the YouTube video onto Google Cloud Storage
2. Next, the Google Cloud Speech-to-Text API is used to convert the original video into English text.
3. Then the text is interpreted and corresponding ASL videos are stitched together to create the sign language translation video
4. OpenAI is used to create a text summary of the transcript
Users can also add notes for each of their videos (Definitions, Summaries, Misc.).  

## Challenges I ran into
My greatest challenge was learning how to utilize the various Google Cloud APIs implemented in this project. I didn't have a lot of experience working with these Google Cloud APIs for Natural Language Processing so it took some time before I could properly implement them. I also had a bit of trouble thinking of how to translate the transcript text into sign language.  
## Accomplishments that we're proud of
I'm particularly proud of the ingenuity of my idea and how our app helps deal with an issue that plagues students in the modern, diverse world. This idea has never been implemented before, and I'm proud that I'm taking the first steps to creating a more equitable digital education landscape.

## What I learned
I learned a lot about how I could integrate **Google Cloud Platform** services in my web application and how it can quickly enhance my application's performance and provide a myriad of new features for users.

## What's next for SilentVoice
Some future improvements could be developing a more refined front-end and adding the ability to translate the generated transcripts and sign language into other languages/sign languages. Additionally, I could use Google Cloud App Engine to completely deploy my application so that more people can use it.  

