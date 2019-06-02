# PredGAN
Official implementation of  A deep multi-scale video prediction framework for anomaly detection for unlabelled videos.
Our proposed framework is inspired by the paper - https://arxiv.org/abs/1511.05440
Our code is based on Tensorflow Implementation by https://github.com/dyelax

In this paper we propose a multi-scale video prediction framework with adversarial training for detecting anomalies in videos. Anoma- lous events are those which do not conform to normal behavior. Supervised learning framework cannot account for all the unusual activities since a universal definition of anomaly cannot be adopted. To tackle this problem, we propose an unsupervised approach to learn the internal representation of videos and use this learning to accurately predict the future-frames of the videos. We train our network adversarially on videos consisting of only normal activi- ties. When our network encounters unusual or irregular activities the generated frames consists of fuzzy regions where the irregular activities are present. These fuzzy regions consequently lower the peak signal to noise ratio (PSNR) of the generated frames. The PSNR values are normalized to have values between 0 and 1 and is used as a regularity score to tag a frame as anomalous or not-anomalous. We provide quantitative and qualitative evaluation of the proposed framework and also introduce Earth Mover’s Distance as a new evaluation metric to assess the quality of the images generated. We demonstrate our framework on UCSD Pedestrian dataset and show that we achieve comparable results.





To run the code follow these directions -

1) Git clone - https://github.com/dyelax/Adversarial_Video_Generation
2) Download the UCSD anomaly detection dataset - https://www.google.com/search?source=hp&ei=8PfzXJ7OD8eOlwTYyaToBQ&q=ucsd+pedestrian+dataset&oq=ucsd+pedes&gs_l=psy-ab.1.0.0l2j0i22i30.582.3181..3992...0.0..0.500.4264.3-4j5j1......0....1..gws-wiz.....0..0i131j0i3.xG2hYVB_uGg

3)Create a folder called Data in the downloaded code repository and move the downloaded UCSD pedestrian dataset.
4)Now go to folder called Code and go to constants.py, modify the data paths.
5)Play with the learning rate, batch size and other parameters.
6)Start training by running - avg_runner.py
7)In our experiments we found that setting the number of input frames equal to the number of frames allowed the network to generate sharp images.
8) We introduce Earth Mover's Distance (EMD) as one of the novel criteria to assess the quality of the frames generated.
9)After the frames are generated we can assess the quality of the frames that are generated using EMD.
10) pip install pyemd.


