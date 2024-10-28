# Class Attendance System | A Flask App based on Face Recognition

A face recognition-based attendance system that streamlines student attendance tracking using deep learning techniques and facial detection. This Flask-based web app leverages MTCNN for real-time face detection and MongoDB for secure data storage, ensuring an efficient, touch-free attendance process. It utilizes SVM classifier for face matching.

## Demo

🔗[Class Attendance System](https://class-attendance-system-er4s.onrender.com)

test-username : tutor

test-password : tutor

## Features

- User authentication with login functionality.
- Attendance marking based on face recognition.
- View attendance history and edit attendance records.
- Real-time face embedding using FaceNet.
- User-friendly web interface.

## Installation

Clone the repository:

```bash
git clone https://github.com/supratimbanik/Class-Attendance-System.git
```

Create a virtual environment:

```bash
python -m venv .venv
```

**Make sure python 3.11.9 is installed**

**Either make python 3.11.9 your primary version or create a virtual environment with python 3.11.9**

Activate the virtual environment:
On Windows:

```bash
.venv\Scripts\activate
```

On macOS/Linux:

```bash
source .venv/bin/activate
```

Install dependencies:

```bash
   pip install -r requirements.txt
```

Set up environment variables in the .env file:

```bash
SECRET_KEY=<your_secret_key>
MONGODB_URI=<your_mongodb_uri>
```

Database setup:

Create a MongoDB database named **ClassAttendance**.

Create three collections inside it - **user_login, sections, attendance**.

Inside **user_login** isert a document like:

```bash
{
  username: "tutor",
  password: "tutor",
  sections: ["section 1", "section 2", "section 3"]
}
```

You can change username and password as per convenience.

Preprocessing the data:

Look inside the **dataset** directory for the **Train** directory. It contains the dataset rquired for each section.

To preprocess the data of any section use the following syntax:

```bash
python embedder.py "your_sections_folder_name"
```

For example:

```bash
python embedder.py "section 1"
```

To run the app use the following command:

```bash
python app.py
```

You can now visit the app on **localhost:3000**

Use the images in **Test** directory inside **dataset** directory for testing the app.

## Authors

- [@supratimbanik](https://github.com/supratimbanik)

## Tech Stack

![FLASK](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=Flask&logoColor=white)

![TENSORFLOW](https://img.shields.io/badge/-TensorFlow-FF6F00?style=for-the-badge&logo=tensorflow&logoColor=white)

![SCIKIT-LEARN](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikit-learn&logoColor=white)

![KERAS](https://img.shields.io/badge/-Keras-E34F26?style=flat-square&logo=keras)

![NUMPY](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)

![MONGODB](https://img.shields.io/badge/-MongoDB-13aa52?style=for-the-badge&logo=mongodb&logoColor=white)
