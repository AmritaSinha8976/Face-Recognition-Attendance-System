# Face Recognition Based Attendance System

## Overview

This project implements a Face Recognition Based Attendance System designed to streamline attendance tracking using facial recognition technology. The system captures and identifies faces in real-time, automatically recording attendance. It also provides an intuitive web interface for managing users and viewing attendance records.

## Features

- **Real-Time Face Detection and Recognition:** Utilizes OpenCV to detect and recognize faces in real-time using a trained K-Nearest Neighbors (KNN) model.
- **Automated Attendance Logging:** Automatically logs the recognized faces with the corresponding timestamp into a CSV file.
- **User Management:** Allows administrators to easily add new users by capturing and storing their face data.
- **Interactive Web Interface:** Built with Flask, HTML, CSS, and Bootstrap, the web interface provides easy navigation and interaction.
- **Voice Feedback:** Provides audio confirmation after successful attendance logging using the Windows SAPI.

## Technologies Used

- **Frontend:**
  - HTML, CSS, Bootstrap for responsive UI design.
  - JavaScript for interactive elements.
- **Backend:**
  - Flask for web application framework.
  - Python for implementing face detection and recognition using OpenCV.
- **Machine Learning:**
  - K-Nearest Neighbors (KNN) for face recognition.
- **Database:**
  - CSV files to store attendance records.
- **Additional Libraries:**
  - `joblib` for model serialization.
  - `pandas` for data manipulation.
  - `win32com.client` for speech synthesis.

## Setup Instructions

### Prerequisites

Make sure you have the following installed:

- Python 3.x
- Flask
- OpenCV
- Required Python libraries (`joblib`, `pandas`, etc.)

### Installation

1. **Clone the Repository:**

    ```bash
    git clone https://github.com/your-username/face-recognition-attendance-system.git
    cd face-recognition-attendance-system
    ```

2. **Install Required Packages:**

    ```bash
    pip install -r requirements.txt
    ```

3. **Run the Application:**

    ```bash
    python app.py
    ```

4. **Access the Application:**

    Open your web browser and navigate to `http://localhost:5000`.

### Project Structure

```plaintext
face-recognition-attendance-system/
│
├── static/
│   ├── faces/           # Stores user face images
│   ├── css/             # Contains custom CSS files
│   └── js/              # Contains custom JavaScript files
│
├── templates/
│   ├── home.html        # Main template file for the home page
│
├── Attendance/          # Stores attendance CSV files
│
├── app.py               # Main application file
├── requirements.txt     # List of dependencies
└── README.md            # Project documentation
```

## Usage

### 1. Homepage (`/`)

- Displays the total number of registered users.
- Shows the list of users who have marked their attendance today.

### 2. Take Attendance (`/start`)

- Opens the webcam and starts capturing video.
- Recognizes faces using the trained KNN model.
- Logs attendance when the 'O' key is pressed.

### 3. Add New User (`/add`)

- Allows you to add a new user by capturing their face images.
- The new user's data is stored, and the model is retrained.

## Contributing

We welcome contributions! If you have ideas for new features or improvements, feel free to create a pull request or open an issue.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.

---

Feel free to update any placeholders like repository links with the correct information relevant to your project.
