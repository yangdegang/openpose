OpenPose Library - Release Notes
====================================



## OpenPose 1.0.0rc1
1. Initial version, main functionality:
    1. Body keypoint detection and rendering on Ubuntu 14 and 16.
    2. It can read an image directory, video or webcam.
    3. It can display the results or storing them on disk.



## OpenPose 1.0.0rc2
1. Main improvements:
    1. Rendering max resolution from 720p to >32k images.
    2. Highly improved documentation.
2. Functions or paremeters renamed:
    1. Demo renamed from rtpose to openpose.
3. Main bugs fixed:
    1. Demo uses exec instead of start, so it works with more OpenCV custom compiled versions.



## OpenPose 1.0.0rc3
1. Main improvements:
    1. Added face keypoint detection.
    2. Added Windows 10 compatibily.
    3. Auto-detection of the number of GPUs.
    4. MPI visualization more similar to COCO one.
    5. Rendering max resolution from 720p to >32k images.
    6. GUI info adder working when the worker TDatum has more than 1 Datum.
    7. It prints out the error description before throwing the exception (so that it is writen on the Windows cmd).
    8. Highly improved documentation.
2. Functions or paremeters renamed:
    1. Flag `write_pose` renamed as `write_keypoint` and it also applies to face and/or hands.
    2. Flag `write_pose_json` renamed as `write_keypoint_json` and it also applies to face and/or hands.
    3. Flag `write_pose_format` renamed as `write_keypoint_format` and it also applies to face and/or hands.
    4. PoseSaver and its JSON variant renamed as KeypointSaver.
    5. PoseJsonCocoSaver renamed as CocoJsonSaver.
3. Main bugs fixed:
    1. All visualization functions moved to same thread, so it works with most OpenCV custom compiled versions.
    2. Fixed error on debug mode: `Too many resources requested for launch`.
    3. Bug in Array::getConstCvMat() if mVolume=0, now returning empty cv::Mat.
    4. Bug: `--process_real_time` threw error with webcam.
