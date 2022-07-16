# Smoothing filter settings

## Overview of the process

For body movements, data is processed in the following order:

1. AI estimates the 2D position of each joint of the user in the camera image
1. Apply **smoothing filter** to the 2D position (`Tracking position` settings)
1. Estimates the 3D position of each joint of the user based on disparity
1. Estimates the orientation of each joint of the character based on the 3D position of each joint of the user
1. Apply **1€ filter filter** for each joint orientation of the character (`Bone Rotation` settings)
1. Apply **1€ filter filter** for changes in the character's facial expression and root position (`Others` settings)

!!! Info "1€ filter"
    [1€ filter](http://cristal.univ-lille.fr/~casiez/1euro/) is a low-pass filter whose cutoff frequency increases in proportion to the speed.
    At low speeds, the filter suppresses jitter noise like a normal low-pass filter, and at high speeds, the cutoff frequency increases to follow quick movements.

The smoothing filter in "2" above is based on the 1€ filter, but incorporates coefficients that depend on the "confidence" of AI estimation.  

## How to adjust filter parameters

Adjustable parameters of the filter are as follows:

- Impact of the confidence of AI estimation
- Parameters of 1€ filter
    - Minimum cutoff frequency `f`.
    - Increase rate of the cutoff frequency `β`.
    - Cutoff frequency of the speed `fv`.

### Impact of the confidence of AI estimation

Increasing `Conf. power` value suppresses noise when joints are hidden by other parts of the body or when joints are out of view.

- Head, Shoulders, Elbows: Increase the value so that the noise at the head, shoulder, and elbow positions is sufficiently small when hidden by the hands.
- Wrists: Increase the value so that the noise at the hand position is sufficiently small when the hand is out of view.
- Hips： Since the hips are usually out of view, set a larger value of about "3".

### Parameters of 1€ filter

- Minimum cutoff frequency `f`: Decrease this value until the noise is acceptable at rest.
- Increase rate of the cutoff frequency `β`: Increase this value until the delay to movement is acceptable when the body is moved.
