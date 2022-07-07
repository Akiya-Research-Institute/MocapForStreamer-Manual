# Known issue

## Unable to connect to some models of cameras
Not all models of webcams are necessarily supported.

## Previous cameras are not loaded correctly on start-up
Sometimes it fails to wait for the webcam start-up correctly. If this is the case, please reopen the camera manually.

## VRM files with long file path cannot be loaded correctly
Place the VRM file in a directory with a short path (e.g. `C:\temp`) and load it.

## Background transparency is disabled on NDI and Spout outputs when the screen percentage of the rendering is not 100%
When background transparency is required on NDI and Spout outputs, set 100% for the screen percentage in "Performance settings".  
To reduce the rendering load for improved performance, reduce the size of the MocapForStreamer window itself.