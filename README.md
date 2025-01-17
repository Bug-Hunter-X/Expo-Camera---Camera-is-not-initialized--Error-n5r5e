# Expo Camera Initialization Error

This repository demonstrates a common error encountered when using the Expo Camera API: the 'Camera is not initialized' error. This error occurs when `takePictureAsync` is called before the camera has finished initializing.

The `bug.js` file shows the problematic code, which attempts to take a picture before the camera is ready. The `bugSolution.js` file provides a corrected version that addresses this issue by ensuring proper initialization before image capture.

## How to Reproduce

1. Clone this repository.
2. Navigate to the repository directory.
3. Run `npm install` to install dependencies.
4. Run `expo start` to start the Expo development server.
5. Observe the error in the `bug.js` example. 
6. Compare to the corrected implementation in `bugSolution.js`

## Solution

The solution involves using the camera's `status` property and only calling `takePictureAsync` after the camera has reached the `READY` status.  This ensures the camera is fully initialized and functional before any attempts to take pictures.