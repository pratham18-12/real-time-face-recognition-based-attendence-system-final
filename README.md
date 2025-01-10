# Real-Time Face Recognition and Attendance System

This project implements a real-time face recognition and attendance system. It uses the `face_recognition` library for facial encoding and comparison, along with OpenCV for video capturing and display. The system also logs attendance data in a CSV file.

## Features
- **Real-Time Face Recognition**: Identifies faces from live video feed.
- **Attendance Logging**: Logs attendance data with timestamps into a CSV file.
- **Model Evaluation**: Provides accuracy metrics, confusion matrix, and classification report for model performance on test data.
- **Data Augmentation**: Includes optional noise addition for testing robustness.
- **Visualization**: Displays confusion matrix, accuracy, and face distance distributions using `matplotlib` and `seaborn`.

---

## Prerequisites
Ensure you have the following installed:
- Python 3.7 or higher
- OpenCV
- face_recognition
- numpy
- matplotlib
- seaborn
- scikit-learn

To install the dependencies, run:
```bash
pip install opencv-python face_recognition numpy matplotlib seaborn scikit-learn
Folder Structure
The project assumes the following folder structure:

bash
Copy code
.
├── train/
│   ├── Person1/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   ├── Person2/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   └── ...
├── test/
│   ├── Person1/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   ├── Person2/
│   │   ├── image1.jpg
│   │   ├── image2.jpg
│   │   └── ...
│   └── ...
└── attendance.csv
How to Run
Prepare the Data:

Place training images in the train folder, with subfolders named after each person.
Place test images in the test folder, with the same structure.
Train and Evaluate: Run the script to train the model on the train dataset and evaluate it on the test dataset. The script outputs:

Test accuracy
Precision, recall, and F1-score
Confusion matrix and other visualizations
Real-Time Face Recognition: To start the real-time face recognition, ensure a webcam is connected, and run the script. Press q to quit the live feed.
Output Files
Attendance Log: The attendance.csv file contains attendance records in the format:
Name,Timestamp
John Doe,2025-01-09 09:00:00
Jane Smith,2025-01-09 09:15:00
Customization
Image Preprocessing: Modify the img_resize function to adjust the input image resolution.
Training/Testing Limits: Change the limit parameter in the load_encodings function to adjust the number of images used.
Recognition Threshold: Adjust the distance threshold in the real-time recognition section for stricter or more lenient matching.
Example Visualizations
Confusion Matrix
The script generates a confusion matrix to show classification performance:


Histogram of Face Distances
Shows the distribution of face distances between encodings.


Future Improvements
Add GPU support for faster processing.
Implement additional preprocessing methods like histogram equalization.
Integrate with a database for better attendance management.
Acknowledgments
face_recognition library
OpenCV
matplotlib
seaborn
