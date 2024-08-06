# Research Report: Improving Object Tracking with YOLO and COCO

## Overview

During this research, I tried to improve our HW 10 where we worked with KCF and CSRT trackers. There we manually picked what to track. I wanted to extend this with automated objects detection based on a model.

For this case, I have used the YOLO detection system and COCO class labels. I tried YOLO only and checked how it worked. Then I tried two more things:

1. Switch between YOLO, KCF, and CSRT without any optimizations and see how it works.
2. Use YOLO only as a detector and KCF and CSRT as trackers.

## Findings

In general, I still see that CSRT performed better than KCF. It scaled properly and tracked detected objects more accurately. However, it did not remove some of the tracking boxes when objects were out of the viewport. On the other hand, KCF removed objects better, but the tracking was not as accurate.

I also tried to train a model myself for cars using TensorFlow, but I did not manage to do so yet. I will try it in the future to see what I can achieve.

## Implementations

Here you will find three implementations:
- **YOLO only**
- **YOLO/KCF/CSRT**
- **YOLO/KCF/CSRT Optimized** (YOLO used not on every frame)

You can run it yourself and switch between trackers using the letter "T" on the keyboard.

## Attachments

Also attached videos with results showing how everything works. (research_results.mp4)