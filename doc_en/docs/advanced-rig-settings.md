# Rig settings

Use the "Rig Settings" menu on the left side of the screen to set how the movement will be applied to the character.  

## Upper body twist

Turn off "Enable Upper Body Twist" to make the upper body always faces forward.

## Pelvis position

Turn on "Lock pelvis position at" to fix the position of the hip to the specified position.  
Adjust the above position according to the relative positions between the real body and the camera.

!!! Warning "Turn off "Enable Upper Body Twist" when shoulder positions are incorrect"
    When "Enable Upper Body Twist" and "Lock pelvis position" are both turned on, the shoulder bones' orientations tend to be in unintended directions.    
    In that case, try one of the followings:

    - Adjust "Coordinate tweak > Offset for each joint > Shoulders"
    - Turn off "Enable Upper Body Twist"

## Face to head offset

The AI estimates the position of the face based on the positions of the eyes, nose, and mouth of the person in the webcam image.  
Specify the offset from the estimated face position to the position of the character's Head bone at "Face to head offset".

## Hand tracking

Select whether to perform hand tracking with the stereo camera or a single camera with "Use stereo cameras for hand tracking".  

- Turned on (Use stereo camera): Accurate tracking, but vulnerable to waving motion
- Turned off (Use single camera)： Stable and robust tracking. Use less CPU/GPU.

## Adjustment of finger rotation

You can adjust the direction of finger rotation by "Secondary axis for finger rotation".  
This specifies the axis of rotaion for each finger.  
For example, by default, the index finger is set to rotate around the Y axis.  

![](images/fingerAxis.png){ loading=lazy }