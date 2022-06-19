# What is MocapForStreamer?

![](images/capsule.png){ loading=lazy }

A Windows application for upper body motion capture using two webcams as stereo cameras.

## Features

You can capture human motion if you have the followings, without the need for special equipments:

- a middle range PC
- 2 webcams of the same model

The captured motion can be exported via the VMC protocol.

## What is the difference with [MocapForAll](https://akiya-research-institute.github.io/MocapForAll-Manual/)?

MocapForStreamer greatly simplifies set-up, such as camera calibration, by limiting the functionality to capturing the upper body only and imposing constraints on the cameras.

| Feature | MocapForStreamer | MocapForAll |
| ------- | ---------------- | ----------- |
| Upper body capture |Yes|Yes|
| Lower body capture |No|Yes|
| Number of cameras |Always 2 | More than 2, no upper limit |
| Camera placement constraints | Must be parallel to each other | No restrictions |
| Camera model constraints | Must be the same model | Not necessarily the same model |
