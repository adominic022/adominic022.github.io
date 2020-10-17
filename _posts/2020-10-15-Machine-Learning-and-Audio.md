---
layout: post
title: Machine Learning and Audio
excerpt_separator:  <!--more-->
---



Resources:
https://openai.com/blog/musenet/
https://openai.com/blog/jukebox/
https://semiconductor.withgoogle.com/
https://experiments.withgoogle.com/collection/ai

https://magenta.tensorflow.org/
https://ai.googleblog.com/2017/12/tacotron-2-generating-human-like-speech.html
https://arxiv.org/pdf/1711.10958.pdf
https://ai.googleblog.com/2018/09/googles-next-generation-music.html

Deep Learning for Audio Signal Processing
https://arxiv.org/pdf/1905.00078.pdf

Audio Signal Processing for Machine Learning
https://www.youtube.com/watch?v=ZZ9u1vUtcIA&list=PL-wATfeyAMNqIee7cH3q1bh4QJFAaeNv0&index=5


Deep Learning (for Audio) with Python
https://www.youtube.com/watch?v=fMqL5vckiU0&list=PL-wATfeyAMNrtbkCNsLcpoAyBBRJZVlnf


Fields:

1. Audio Classification
The task is essentially to extract features from the audio, and then identify which class the audio belongs to. Many useful applications pertaining to audio classification can be found in the wild – such as genre classification, instrument recognition and artist identification.

A common approach to solve an audio classification task is to pre-process the audio inputs to extract useful features, and then apply a classification algorithm on it. For example, in the case study below we are given a 5 second excerpt of a sound, and the task is to identify which class does it belong to – whether it is a dog barking or a drilling sound. As mentioned in the article, an approach to deal with this is to extract an audio feature called MFCC and then pass it though a neural network to get the appropriate class.



2. Audio Fingerprinting
The aim of audio fingerprinting is to determine the digital “summary” of the audio. This is done to identify the audio from an audio sample. Shazam is an excellent example of an application of audio fingerprinting. It recognises the music on the basis of the first two to five seconds of a song. However, there are still situations where the system fails, especially where there is a high amount of background noise.



http://www.cs.toronto.edu/~dross/ChandrasekharSharifiRoss_ISMIR2011.pdf

3. Automatic Music Tagging
Music Tagging is a more complex version of audio classification. Here, we can have multiple classes that each audio may belong to, aka, a multi-label classification problem. A potential application of this task can be to create metadata for the audio so that it can be searched later on. Deep learning has helped solve this task to a certain extent which can be seen in the case study below.

4. Audio Segmentation
Segmentation literally means dividing a particular object into parts (or segments) based on a defined set of characteristics. Segmentation, especially for audio data analysis, is an important pre-processing step. This is because we can segment a noisy and lengthy audio signal into short homogeneous segments (handy short sequences of audio) which are used for further processing. An application of the task is heart sound segmentation, i.e. to identify sounds specific to the heart.


We can convert this into a supervised learning problem, where each time stamp can be classified on the basis of the segments required. Then we can apply an audio classification approach to solve the problem. In the case study below, the task is to segment the heart sound into two segments (lub and dub), so that we can identify an anomaly in each segment. It can be solved by using audio feature extraction and then deep learning can be applied for classification.

5. Audio Source Separation
Audio Source Separation consists of isolating one or more source signals from a mixture of signals. One of the most common applications of this is identifying the lyrics from the audio for simultaneous translation (karaoke, for instance). This is a classic example shown in Andrew Ng’s machine learning course where he separates the sound of the speaker from the background music.
http://ijcert.org/ems/ijcert_papers/V3I1103.pdf

A typical usage scenario involves:

loading an audio file
computing a time-frequency transform to obtain a spectrogram, and
using some of the source separation algorithm (such as non-negative matrix factorization) to obtain a time-frequency mask
The mask is then multiplied with the spectrogram and the result is converted back to the time domain.
https://github.com/IoSR-Surrey/untwist

6. Beat Tracking
As the name suggests, the goal here is to track the location of each beat in a collection of audio files. Beat tracking can be utilized to automate time-consuming tasks that must be completed in order to synchronize events with music. It is useful in various applications, such as video editing, audio editing, and human-computer improvisation.
https://www.audiolabs-erlangen.de/content/05-fau/professor/00-mueller/01-students/2012_GroschePeter_MusicSignalProcessing_PhD-Thesis.pdf
An approach to solve beat tracking can be to be parse the audio file and use an onset detection algorithm to track the beats. Although the techniques used to for onset detection rely heavily on audio feature engineering and machine learning, deep learning can easily be used here to optimize the results.
https://github.com/adamstark/BTrack

 7. Music Recommendation
Thanks to the internet, we now have millions of songs we can listen to anytime. Ironically, this has made it even harder to discover new music because of the plethora of options out there. Music recommendation systems help deal with this information overload by automatically recommending new music to listeners. Content providers like Spotify and Saavn have developed highly sophisticated music recommendation engines. These models leverage the user’s past listening history among many other features to build customized recommendation lists.
We can tackle the challenge of customizing listening preferences by training a regression/deep learning model. This can be used to predict the latent representations of songs that were obtained from a collaborative filtering model. This way, we could predict the representation of a song in the collaborative filtering space, even if no usage data was available.
https://www.researchgate.net/publication/277714802_A_Survey_of_Music_Recommendation_Systems_and_Future_Perspectives

https://benanne.github.io/2014/08/05/spotify-cnns.html


8. Music Retrieval
One of the most difficult tasks in audio processing, Music Retrieval essentially aims to build a search engine based on audio. Although we can do this by solving sub-tasks like audio fingerprinting, this task encompasses much more that that. For example, we also have to solve different smaller tasks for different types of music retrieval (timbre detection would be great for gender identification). Currently, there is no other system that has been developed to match the industry expected standards.
The task of music retrieval is divided into smaller and simpler steps, which include tonal analysis (e.g. melody and harmony) and rhythm or tempo (e.g. beat tracking). Then, on the basis of these individual analysis, information is extracted which is used for retrieval of similar audio samples.
https://www.nowpublishers.com/article/Details/INR-042


9. Music Transcription
Music Transcription is another challenging audio processing task. It comprises of annotating audio and creating a kind of “sheet” for generating music from it at a later point of time. The manual effort involved in transcribing music from recordings can be vast. It varies enormously depending on the complexity of the music, how good our listening skills are and how detailed we want our transcription to be.
The approach for music transcription is similar to that of speech recognition, where musical notes are transcribed into lyrical excerpts of instruments.


https://www.youtube.com/watch?v=9boJ-Ai6QFM&feature=youtu.be










At a high level, any machine learning problem can be divided into three types of tasks: data tasks (data collection, data cleaning, and feature formation), training (building machine learning models using data features), and evaluation (assessing the model). Features, defined as "individual measurable propert[ies] or characteristic[s] of a phenomenon being observed," [1] are very useful because they help a machine understand the data and classify it into categories or predict a value.

Bishop, Christopher (2006). Pattern recognition and machine learning. Berlin: Springer. ISBN 0-387-31073-8.


What are audio signals?
Audio signals are signals that vibrate in the audible frequency range. When someone talks, it generates air pressure signals; the ear takes in these air pressure differences and communicates with the brain. That's how the brain helps a person recognize that the signal is speech and understand what someone is saying.

Data Features & Transformations
mfcc
gfcc
lpcc
pncc
pncc
entropy
Spectrum
spectral centroid
cepstrum
short-term energy
spectral flux
spectral spread
spectral rolloff
spectogram


Spectrum and cepstrum are two particularly important features in audio processing.
Spectrum & Cepstrum:

Audio Signal (time domain) -> Fourier Transform (sine & cosine) ->
Spectrum (Signal in the freq domain) -> log magnitude (reduce amplitude diff) ->
inverse fourier transform -> cepstrum

Mathematically, a spectrum is the Fourier transform of a signal. A Fourier transform converts a time-domain signal to the frequency domain. In other words, a spectrum is the frequency domain representation of the input audio's time-domain signal.

A cepstrum is formed by taking the log magnitude of the spectrum followed by an inverse Fourier transform. This results in a signal that's neither in the frequency domain (because we took an inverse Fourier transform) nor in the time domain (because we took the log magnitude prior to the inverse Fourier transform). The domain of the resulting signal is called the quefrency.


The reason we care about the signal in the frequency domain relates to the biology of the ear. Many things must happen before we can process and interpret a sound. One happens in the cochlea, a fluid-filled part of the ear with thousands of tiny hairs that are connected to nerves. Some of the hairs are short, and some are relatively longer. The shorter hairs resonate with higher sound frequencies, and the longer hairs resonate with lower sound frequencies. Therefore, the ear is like a natural Fourier transform analyzer!

Another fact about human hearing is that as the sound frequency increases above 1kHz, our ears begin to get less selective to frequencies. This corresponds well with something called the Mel filter bank.

MFCC:
Spectrum -> Mel Scale Filter bank -> log magnitude -> Discrete cosine Transform -> MFCC feature

Passing a spectrum through the Mel filter bank, followed by taking the log magnitude and a discrete cosine transform (DCT) produces the Mel cepstrum. DCT extracts the signal's main information and peaks. It is also widely used in JPEG and MPEG compressions. The peaks are the gist of the audio information. Typically, the first 13 coefficients extracted from the Mel cepstrum are called the MFCCs. These hold very useful information about audio and are often used to train machine learning models.


Another filter inspired by human hearing is the Gammatone filter bank. This filter bank is used as a front-end simulation of the cochlea. Thus, it has many applications in speech processing because it aims to replicate how we hear.

Spectrum -> Gammatone filter bank -> downsample and loudness compression -> discrete cosine transform -> GFCC feature

GFCCs are formed by passing the spectrum through Gammatone filter bank, followed by loudness compression and DCT. The first (approximately) 22 features are called GFCCs. GFCCs have a number of applications in speech processing, such as speaker identification.

Other features useful in audio processing tasks (especially speech) include LPCC, BFCC, PNCC, and spectral features like spectral flux, entropy, roll off, centroid, spread, and energy entropy.

