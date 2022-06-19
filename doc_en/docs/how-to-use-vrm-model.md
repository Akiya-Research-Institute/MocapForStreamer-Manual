# Load VRM model

## Load file

Drag and drop the .vrm file to MocapForStreamer window to load the file.

## Settings for eye bones

The names of the eye bones vary from model to model. If the bone cannot be detected automatically, the eyes will not move.  
In this case, open the 'Facial expression settings' on the left-hand side of the screen and manually specify the names of the eye bones under 'Eye bone override'.  
Also, if the pupil movement range is not appropriate, adjust the 'Max angle'.

## Settings for facial morph targets (blend shapes)

Different models have different names for Morph Targets. By default, it is assumed that the model has morph targets with the names used by [Perfect Sync](https://hinzka.hatenablog.com/entry/2020/08/15/145040).  
If the model has morph targets with other names, open 'Facial expression settings' on the left-hand side of the screen and enter the appropriate morph target names manually.  
Note that there are presets of morph target names for models created by VRoid Studio. Open 'Load preset...' pull down box to load a preset for the beta or latest version of VRoid model.