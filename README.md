# Adversarial Video Generation
This project implements a generative adversarial network to predict future frames of video, as detailed in 
["Deep Multi-Scale Video Prediction Beyond Mean Square Error"](https://arxiv.org/abs/1511.05440) by Mathieu, 
Couprie & LeCun. Their official code (using Torch) can be found 
[here](https://github.com/coupriec/VideoPredictionICLR2016).

Adversarial generation uses two networks – a generator and a discriminator – to improve the sharpness of generated images. Given the past four frames of video, the generator learns to generate accurate predictions for the next frame. Given either a generated or a real-world image, the discriminator learns to correctly classify between generated and real. The two networks "compete," with the generator attempting to fool the discriminator into classifying its output as real. This forces the generator to create frames that are very similar to what real frames in the domain might look like.
