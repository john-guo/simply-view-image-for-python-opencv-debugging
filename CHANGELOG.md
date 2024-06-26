# Change Log

All notable changes to the "simply-view-image-for-python-opencv-debugging" extension will be documented in this file.

Check [Keep a Changelog](http://keepachangelog.com/) for recommendations on how to structure this file.

## [0.0.11]
- Fix an issue, use the globalStorageUri.fsPath instead of globalStorageUri.path. 

## [0.0.10]

- Add "onDebugResolve:debugpy" to package.json (activationEvents) 
- Compatibility with registerCodeActionsProvider (use DocumentSelector instead of string)

## [0.0.9]

- Add tf2 tensor support.

## [0.0.8]

- Now the global variables can be view.

## [0.0.7]

- Using a workaround for supporting multithreading.

## [0.0.6]

- Add an option "svifpod.usetmppathtosave" to choose which path (tmp or extenion private storage path) to save, default is tmp path.

## [0.0.5]

- Add a command "View Image(Python OpenCV Debug)".
- Add a keyboard shortcut "ctrl+alt+Q" for quickly image viewing.

## [0.0.4]

- Add ndarray checking to avoid some exceptions.

## [0.0.3]

- Update README.md

## [0.0.2]

- Thanks to [marisancans](https://github.com/marisancans) add support for float np array.

## [0.0.1]

- Initial release
