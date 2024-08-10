# parking-spot-project
This system detects parking spot availability in real-time. It analyzes video frames to identify free and occupied spots. The system calculates differences between frames and uses a machine learning model for classification. Free spots are marked in green, occupied ones in red. It displays the count of available spots.

Parking Spot Detection System
Description
The Parking Spot Detection System is designed to provide real-time insights into parking spot availability by analyzing video footage. This tool is ideal for managing parking lots and garages, ensuring that users can easily determine whether parking spaces are occupied or free. The system combines video processing techniques with machine learning to deliver accurate and timely information about parking spot status.

Features
Dynamic Spot Detection: The system begins by loading a mask image that represents the parking layout. This mask is used to identify and extract the locations of parking spots within each video frame.
Real-Time Occupancy Analysis: By comparing consecutive video frames, the system detects changes in parking spot occupancy. It calculates differences between frames to determine if a spot has been vacated or occupied.
Visual Indicators: The video feed is overlaid with bounding boxes around each parking spot. These boxes are color-coded: green indicates available spots, while red signals occupied spots. Additionally, the system displays a count of available spots in real-time on the video frame.
Machine Learning Integration: The tool uses a pre-trained machine learning model to classify parking spots as either empty or occupied. This model helps in accurately assessing the spot status based on visual cues in the video.
How It Works
Initialization: The system starts by reading the mask image and video file. It uses connected components analysis to identify parking spots from the mask.
Video Frame Processing: As the video plays, each frame is compared with the previous one to detect changes in spot occupancy. Differences are calculated to assess whether a spot is empty or occupied.
Status Determination: The machine learning model predicts the status of each spot based on the differences between frames.
Visualization and Feedback: Bounding boxes are drawn around parking spots, and their status is indicated by color. The system also provides a count of available spots, offering a clear and immediate overview of parking availability.
Requirements
Python 3.x: Programming language used for the system.
OpenCV: Library for video processing and visualization.
NumPy: For numerical operations.
scikit-image: For image processing tasks.
Pickle: For loading the machine learning model.
