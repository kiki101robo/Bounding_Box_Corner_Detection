# Bounding_Box_Corner_Detection

## Overview
This project involves analyzing video frames to detect changes in image quality and extract useful features. The main tasks include frame extraction, edge detection, corner detection, and drawing bounding boxes based on detected features.

## Setup Instructions
1. **Video Preparation:**
   - Upload the video to your working environment.
   - Rename the video file as necessary to match the filename in the script (`proj2_v2.mp4`).

2. **Environment Setup:**
   - Ensure Python is installed along with the necessary libraries: OpenCV for image processing, os for directory management, and numpy for mathematical operations.

3. **Running the Program:**
   - Execute the script in an environment that supports Python and OpenCV. Adjustments may be needed for paths and file names based on your system configuration.

## Pipeline Details

### Block 1: Importing Libraries
- **Libraries Used:** `cv2`, `os`, `numpy`
- **Purpose:** Set up the environment with necessary Python libraries for image manipulation and matrix operations.

### Block 2: Video and Output Setup
- **Variables Defined:** `video_path`, `output_directory`
- **Operations:** Set the path to the input video and prepare a directory for storing output frames.

### Block 3: Output Video Parameters
- **Configuration:** Define output video path, frame rate, and codec using `cv2.VideoWriter_fourcc`.

### Block 4: Video Capture and Frame Information
- **Operations:** Initialize video capture and retrieve properties like FPS and total frame count using `cv2.VideoCapture`.

### Block 5: Image Processing Parameters
- **Parameters Configured:** Thresholds and settings for edge and corner detection algorithms (e.g., Laplacian threshold, Hough Transform parameters).

### Block 6: Laplacian Kernel and Floodfill Parameters
- **Setup:** Define the Laplacian kernel for edge detection and parameters for flood fill operations.

### Block 7: Video Writer Setup
- **Initialization:** Configure `cv2.VideoWriter` to output processed frames into a video file.

### Block 8: Main Loop for Processing Frames
- **Process:** Each frame is processed to detect edges and corners. Features like the variance of the Laplacian output are used to determine the quality of frames. Custom functions are utilized for connected component analysis.

### Block 9: Release Video Capture and Writer
- **Finalization:** Properly release resources and save the output video, providing confirmation of successful execution.

## Output
- The processed video will be saved with the specified configurations, showcasing detected features and analysis results.

## Additional Notes
- Ensure the video file is correctly placed and accessible from the script.
- Modify the `video_path` and `output_video_path` as needed to match your directory structure.
- Adjust image processing thresholds based on specific requirements or video characteristics.

