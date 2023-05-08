# my_camera_AR
Camera calibration and camera pose estimation w\chessboard using OpenCV


* Camera calibration
  * [CameraCalibration.py](https://github.com/yubin0727/my_camera_AR/blob/main/CameraCalibration.py)
  * Get camera matrix and distortion coefficient using the selected images
  * Select images  
    <img src = "https://user-images.githubusercontent.com/101437398/236874464-6d79f7a8-a3c6-4358-baaf-720f576a4b54.png" width="70%" height="70%">
     <img src = "https://user-images.githubusercontent.com/101437398/236874523-5e9851d6-a482-45e8-bf80-59c31610b097.png" width="70%" height="70%">
  * Results  
    ![K, dist_coef](https://user-images.githubusercontent.com/101437398/236871424-a8c352a2-429d-409c-8d86-58f1d1b3b00a.png)

* Camera pose estimation
  * [CameraAR.py](https://github.com/yubin0727/my_camera_AR/blob/main/CameraAR.py)
  * Using the result of the camera calibration(K, dist_coef)
  * cv.solvePnP() -> cv.projectPoints()
  * __cv.solvePnP()__ : return rotation vector & translation vector (3D world coordinate -> 3D camera coordinate)
  * __cv.projectPoints()__ : 3D points -> image plane
  * Results  
    <img src = "https://user-images.githubusercontent.com/101437398/236874871-b9ebe5f7-d6a6-42d6-a9f8-93318f29f5a5.png" width="70%" height="70%">
    <img src = "https://user-images.githubusercontent.com/101437398/236874880-fec8b126-ba7b-44fe-abfe-a522904d4aad.png" width="70%" height="70%">
    <img src = "https://user-images.githubusercontent.com/101437398/236875876-8b38f3f2-2f08-493b-b8a8-b0f4ecfdd532.gif" width="70%" height="70%">
