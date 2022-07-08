# Export settings

## Background color

To change the background color for chroma key compositing etc., change the `Background color` from the `Environment settings` menu on the left of the screen.

## Export motion data

You can save to a BVH or send to other applications in real time using the VMC protocol.

### Save to BVH files

Click `Start BVH recording` from the `Export settings` menu on the left side of the screen, and select the save destination.  
Press the same button again or press the stop button displayed in the upper right corner of the screen to output the BVH file.

### Export VMC protocol

Enable `Send VMC protocol` in the `Export settings` menu on the left side of the screen.

!!! Info "VMC protocol"
    The VMC protocol is a message format for sending and receiving character bones and facial expression morphs between applications in real time.  
    For details, see [https://protocol.vmc.info/](https://protocol.vmc.info/).

    Note that the [Virtual Motion Capture](https://vmc.info/) application itself is not required to send and receive data using the VMC protocol.

## Video stream output

Spout or NDI® allows you to send MocapForStreamer screens to other applications in real time.

The screen sent contains transparency (Alpha channel).  
You can output the screen with a transparent background by setting zero for `A` in `Background color` in the `Environment settings` menu on the left side of the screen.

Below is a brief comparison of the two.

| Feature | Spout | NDI |
| ------- | ---------------- | ----------- |
| Send to other app |Yes|Yes|
| Send to other PC |No|Yes|
| Frame rate | High | Low |
| Latency | Few frames | Depends on the network |

### Spout output

Enable `Send Spout video stream` in the `Export settings` menu on the left side of the screen.  
Spout video streaming will start with the name `MocapForStreamer`.

!!! Info "Spout"
    Spout uses GPU shared memory to share video between applications.  
    See [https://spout.zeal.co/](https://spout.zeal.co/) for the details.  

!!! Info "OBS-NDI plugin"
    [Plugins for receiving video stream sent by NDI](https://obsproject.com/forum/resources/obs-ndi-newtek-ndi%E2%84%A2-integration-into-obs-studio.528/) is avalilable.

### NDI® output

Enable `Send NDI video stream` in the `Export settings` menu on the left side of the screen.  
NDI video streaming will start with the name `MocapForStreamer`.

NDI allows you to send MocapForStreamer's screen to other devices in your local network in real time.  
For example, it is possible to separate the PC that performs motion capture with MocapForStreamer and the PC that composites the screen with other materials and streams video to the internet.

!!! Info "NDI® is a registered trademark of NewTek, Inc."
    See [http://ndi.tv/](http://ndi.tv/) for the details.  
    You can download "NDI Tools" software suites for various platforms directly from this site. [http://ndi.tv/tools/](http://ndi.tv/tools/)

!!! Info "OBS-NDI plugin"
    [Plugins for receiving video stream sent by NDI](https://obsproject.com/forum/resources/obs-ndi-newtek-ndi%E2%84%A2-integration-into-obs-studio.528/) is avalilable.

!!! Failure "When NDI output fails"
    Communication may be blocked by the firewall.  
    Try disabling the firewall or allow communication on the ports used by NDI.  
    The ports used by NDI are **49152** - **65535** as listed [here](https://support.newtek.com/hc/en-us/articles/218109497-NDI-Video-Data-Flow).