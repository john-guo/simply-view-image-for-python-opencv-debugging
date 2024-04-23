# simply-view-image-for-python-opencv-debugging README

## Features

This simple extension can and **only** can let you view the image of a variable when you are debugging **python** codes with **opencv**.

Currently, It's only support python with opencv module *(opencv-python)* debugging.

There is a limition that's your python codes must import opencv as cv2 and import numpy as np.

For example:

    import cv2
    import numpy as np

## Requirements

Python debugger extension for vscode (vscode Microsoft official python extension recommend)

Python module of OpenCV support **imwrite** function installed (official module *opencv-python* recommend)

## How to use

Due to vscode do not allow extension customizes hover when you are debugging so that this extension use the code action command to open a new editor to view the image.

Since 0.0.5 add a command "View Image(Python OpenCV Debug)" and a keybord shortcut "ctrl+alt+q" to open the image.

### Step

1. Open a python file which has "import cv2".

2. Start Debug

3. Break on a certain line

4. Click a variable that contains image data and waiting for the code action icon (a little yellow light bubble) popup.

5. Click the icon or press ctrl+. to popup a menu then click the menu to view image.

![How to use](usage.gif)

## Extension Settings

No settings, the initail version is hardcode.

## Limitations

The initail version is hardcode so there are some limitations:

1. Only work on python debugging with opencv module.

2. The python opencv module **must** support imwrite("filename to save", image_variable) function.

3. The python file **must** import opencv module as cv2 such as "import cv2" and import numpy as np such as "import numpy as np";

4. The extension use imwrite to save the temporary image file.

5. The temporary directory is hardcode.

6. The temporary image file type is png.

7. The temporary image files are removed on extension activation not deactivation.

8. Unsupport variable tracking while debugging so the image cannot be refreshed automatically. You must click the variable again to refresh.

## Release Notes

### 0.0.11
Fix an issue, use the globalStorageUri.fsPath instead of globalStorageUri.path. 

### 0.0.10
Due to a change in the Python debugger type name from 'python' to 'debugpy' after a Visual Studio Code update, this extension became incompatible. This update addresses the issue, ensuring compatibility with the latest VSCode version 1.86.1. Thanks to [aslampr07](https://github.com/aslampr07) (https://github.com/john-guo/simply-view-image-for-python-opencv-debugging/issues/24)

### 0.0.9

Support TF2 tensor(Eager Execution must be enabled) or any other object that has a "numpy()" function which can convert it to a numpy array. Thanks to [saeedizadi](https://github.com/saeedizadi) (https://github.com/john-guo/simply-view-image-for-python-opencv-debugging/issues/13)

### 0.0.8

Now the global variables can be view, but still cannot know which thread or stack frame current within so that if many variables with the same name in different threads or different stack frames the result will be confused.

### 0.0.7

Using a workaround for supporting multithreading. Thanks to [zhfkt](https://github.com/zhfkt) (https://github.com/john-guo/simply-view-image-for-python-opencv-debugging/issues/6)

### 0.0.6

Add an option "svifpod.usetmppathtosave" to choose which path (tmp or extenion private storage path) to save, default is tmp path.

### 0.0.5

Add a command "View Image(Python OpenCV Debug)".

Add a keyboard shortcut "ctrl+alt+Q" for quickly image viewing.

### 0.0.4

Add ndarray checking to avoid some exceptions.

### 0.0.3

Update README.md

### 0.0.2

Add support for float np array. Notice it's a hardcode workaround. Because of this fixing the python file must import numpy as np also. Thanks to [marisancans](https://github.com/marisancans) (https://github.com/john-guo/simply-view-image-for-python-opencv-debugging/issues/1)

### 0.0.1

Initial release

**Enjoy!**
