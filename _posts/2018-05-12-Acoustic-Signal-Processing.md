---
layout: post
title: Acoustic Signal Processing
excerpt_separator:  <!--more-->
---

# Acoustic Signal Processing

## Signal Processing: Introduction

Signal processing refers to the acquisition, storage, display, and generation of signals – also to the extraction of information from signals and the re-encoding of information. As such, signal processing in some form is an essential element in the practice of all aspects of acoustics. Signal processing algorithms enable acousticians to separate signals from noise, to perform automatic speech recognition, or to compress information for more efficient storage or transmission. 

### Acoustics? Digital?

Acoustics, or Audio signal processing, is intentional alteration of audio signals, electronically represented as a digital/analog form that can later be processed as signals. Before digital technology came along, analog (read continuous) signals were commonly used, in things like radio broadcasting and such. However, as times changed, and computers/software more affordable, digital signals were preferred. Basic applications include: efficient storage, compression, transmission, enhancement. However, recent introduction of Neural Networks, Statistical Vector Machines, and Other statistical approaches have led to more interesting aspects of application. Areas of music, speech, and environmental sounds have become the hottest topics to date. 

## Applications

Audio classification is a fundamental problem in the field of audio processing. The task is essentially to extract features from the audio, and then identify which class the audio belongs to. Many useful applications pertaining to audio classification can be found in the wild – such as genre classification, instrument recognition and artist identification.

A common approach to solve an audio classification task is to pre-process the audio inputs to extract useful features, and then apply a classification algorithm on it. For example, in the case study below we are given a 5 second excerpt of a sound, and the task is to identify which class does it belong to – whether it is a dog barking or a drilling sound. As mentioned in the article, an approach to deal with this is to extract an audio feature called MFCC and then pass it though a neural network to get the appropriate class.


The aim of audio fingerprinting is to determine the digital “summary” of the audio. This is done to identify the audio from an audio sample. Shazam is an excellent example of an application of audio fingerprinting. It recognises the music on the basis of the first two to five seconds of a song. However, there are still situations where the system fails, especially where there is a high amount of background noise.
To solve this problem, an approach could be to represent the audio in a different manner, so that it is easily deciphered. Then, we can find out the patterns that differentiate the audio from the background noise. In the case study below, the author converts raw audio to spectrograms and then uses peak finding and fingerprint hashing algorithms to define the fingerprints of that audio file.



Music Transcription is another challenging audio processing task. It comprises of annotating audio and creating a kind of “sheet” for generating music from it at a later point of time. The manual effort involved in transcribing music from recordings can be vast. It varies enormously depending on the complexity of the music, how good our listening skills are and how detailed we want our transcription to be.
The approach for music transcription is similar to that of speech recognition, where musical notes are transcribed into lyrical excerpts of instruments.

### References
http://www.antiquark.com/thesis/msc-thesis-derek-ross-v5c.pdf
https://www.coursera.org/learn/audio-signal-processing
http://webhome.csc.uvic.ca/~gtzan/output/
https://www.youtube.com/watch?v=cd2Jfi0PE2Y
https://link.springer.com/article/10.1007%2Fs10462-012-9362-y

1.개념과 정의

2.핵심내용

3.연구분야

4.활용사례

5.과거에서 현재까지의 히스토리

6.앞으로 발전방향

7.관련업무 회사명 리스트(2개)

8.관련특허 링크

9. 참고자료 링크