# Scene-Classification-and-Object-Detection-using-Caffe-and-YOLO
To get the above files runnng,
1) Download the folder and unzip it.
2) Open folder demo and place it in your /caffe/python directory
3) 
cd caffe-master
cd python
cd demo
4) Create the following symbolic link:
ln -s /home/username/caffe-master/python/caffe
4) Ensure that you have models


3) Ensure that your /caffe-master/python/demo directory has a symbolic link to your /caffe-master/python/caffe directory by enter this line in the terminal while you are 
4) Open app.py

Notes:
Line 29 in app.py returns your home directory
Line 29: userhome = os.path.expanduser('~')    
Example: userhome value will be returned as /home/reena-mary

## Changes to be made in app.py
1) Lines 64, 97: Check if your prediction in darknet directory is a predictions.jpg file or a predictions.png file and edit the paths accordingly. This step is important. You need to ensure that the correct file type is present in your path (jpg or png).

2) Most likely, if Darknet is compiled with OpenCV, predictions.jpg will be present or if not,  predictions.png will be present in your darknet directory.

3) The code in app.py is applicable for a darknet folder that is in your Home Directory. If darknet is not in your Home directory, then, in Lines 64, 97 and 265, edit the path by appending your path after /home/username/ that leads to darknet directory in
- Line 64:  yolopred = userhome + "/darknet/predictions.jpg"
- Line 97:  yolopred = userhome + "/darknet/predictions.jpg"
- Line 265: req_path = userhome + "/darknet/"

 Example: yolopred = userhome + "/path between home directory and darknet/darkent/predictions.jpg"

