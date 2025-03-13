# AthliTech ST-AIOT-Craft-Project

<img width="1512" alt="image" src="https://github.com/user-attachments/assets/6b1851c4-c777-4d51-99b0-0dd6ed72f26c" />
<img width="1512" alt="image" src="https://github.com/user-attachments/assets/2f84e063-61ea-4e00-8f2c-c73b76c994a5" />
 

This project consists of a collection of interactive sensor-based visualizers developed using Flask for the backend and p5.js for the frontend. The games utilize sensor data from a Bluetooth Low Energy (BLE) device (SensorTile Box Pro) and make use of the MLC model generated by ST AIOT Craft Platform to create engaging experiences.

## Table of Contents

- [Features](#features)
- [Technologies Used](#technologies-used)
- [Documentation](#documentation)
- [Poster](#poster)
- [Installation](#installation)
  - [Prerequisites](#prerequisites)
  - [Backend Setup](#backend-setup)
  - [Frontend Setup](#frontend-setup)
- [Dataset](#dataset)
- [File Structure](#file-structure)
- [Usage](#usage)
- [Videos](#videos)
- [Game Descriptions](#game-descriptions)
- [Decision Tree Model MLC Configuration Files](#decision-tree-model-mlc-configuration-files)
- [App Configuration Files](#app-configuration-files)

## Features

- Real-time sensor data visualization.
- Multiple games including Bicep Curls, Squats, Shoulder Press, Push-Ups, Hammer Curls, Plank, Tricep Extension.
- Responsive design with a focus on user experience.
- Cross-Origin Resource Sharing (CORS) enabled for frontend-backend communication.

## Technologies Used

- **Backend**: Flask, Flask-CORS
- **Frontend**: p5.js, HTML, CSS
- **Bluetooth Communication**: Bleak (Python library for BLE)
- **Data Processing**: NumPy (for numerical computations)

## Documentation
 [Documentation](https://docs.google.com/document/d/1_3aOXfcF3SWF6_m7hnmZ2VtqVYfztu8QkoeiiyES2nA/edit?usp=sharing)
 
 [Documentation in PDF Format](https://drive.google.com/file/d/1G0scxTKr364dTLCZbykRRmJVuXC4UFcF/view)

## Installation

### Prerequisites

- Python 3.x
- Node.js (if using npm for JavaScript dependencies)

### Backend Setup

1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd <repository-folder>
   ```

2. Create a virtual environment (optional but recommended):
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. Install Python dependencies:
   ```bash
   pip install -r requirements.txt
   ```

### Frontend Setup

1. Navigate to the static folder:
   ```bash
   cd static
   ```

2. To install JavaScript dependencies, run:
   ```bash
   npm install
   ```
## Poster
[Poster Link](https://docs.google.com/presentation/d/1QCpSiHZgukI_dEbPChZpWSlbRlAN4g-A/edit?usp=sharing&ouid=104706167263291189947&rtpof=true&sd=true)


## Dataset
[Dataset Link](https://drive.google.com/drive/folders/1EbXt3ofgRYc1gK2JeSINofctKB1eFOX6?usp=sharing)

## File Structure

```
/AthliTech
│
├── conn_flask.py          # Main Flask application for handling routes and BLE communication.
│
├── static/
│   ├── bicep_game.js      # JavaScript for the Bicep Curls game, handling game logic and sensor data.
│   ├── bicep_curls.html   # HTML for the Bicep Curls game interface.
│   ├── hammer_game.js      # JavaScript for the Hammer Curl game, handling game logic and sensor data.
│   ├── hammer_curl.html    # HTML for the Hammer Curl game interface.
│   ├── shoulder_game.js    # JavaScript for the Shoulder Press game, handling game logic and sensor data.
│   ├── shoulder_press.html  # HTML for the Shoulder Press game interface.
│   ├── squat_game.js       # JavaScript for the Squat Counter game, handling game logic and sensor data.
│   ├── squat.html          # HTML for the Squat Counter game interface.
│   ├── pushup_game.js      # JavaScript for the Pushup game, handling game logic and sensor data.
│   ├── pushup.html         # HTML for the Pushup game interface.
│   ├── plank_game.js       # JavaScript for the Plank game, handling game logic and sensor data.
│   ├── plank.html          # HTML for the Plank game interface.
│   ├── tricep_overhead_game.js # JavaScript for the Tricep Overhead game, handling game logic and sensor data.
│   └── tricep_overhead.html # HTML for the Tricep Overhead game interface.
│
├── uuid_reader.py          # Python script for reading UUIDs from the BLE device.
└── list_characteristics.py  # Python script for listing characteristics of the BLE device.
 
```

## Usage

1. Start the Flask server:
   ```bash
   python conn_flask.py
   ```

2. Open your web browser and navigate to `http://127.0.0.1:9000` to access the games.

3. Follow the on-screen instructions for each game.

## Videos

[Video Link](https://drive.google.com/drive/folders/1amoFOjHWOWiVsIEGAE2MIUrZG-c_hRs5?usp=sharing)

## Game Descriptions

- **Bicep Curls**: Move the ball by curling your arms. The MLC provides predictions to indicate whether your form is good, standby, or bad.
- **Squat Counter**: Perform squats to increase the counter. The MLC predicts your position to help you maintain proper form.
- **Shoulder Press**: Press your arms up and down to move the ball. The MLC gives feedback on your form during the exercise.
- **Pushups**: Perform pushups to control the ball's movement. The MLC predicts your form to ensure you are doing the exercise correctly.
- **Plank**: Maintain a plank position to keep the ball steady. The MLC provides predictions to help you stay in the correct position.
- **Tricep Overhead**: Extend your arms overhead to move the ball. The MLC gives predictions to indicate your form during the exercise.

## Decision Tree Model MLC Configuration Files

The MLC configuration files are generated by the AIOT Craft app and website, keeping the firmware as **Datalog 3.00**.These configurations are essential for the proper functioning of the MLC predictions.
Link:
[MLC MODEL JSON FILES](https://drive.google.com/drive/folders/1_wgwswTOXAq2rNmJBQEob5R-7LxufqeY?usp=sharing)

### App Configuration Files
The app configuration file is generated in the BLE sensor app after changing the firmware to **Entry/Expert 1.21**. These configurations are essential for the proper functioning of the MLC predictions in the games.
They are required to flash the app inside the Ssensortile Box so that it can run locally.

Link:
[APP FILES](https://drive.google.com/drive/folders/1ifW7kHJNRtXa6Z1mGRVws9v32Ss82mlK?usp=sharing)

 
Configuration file generated after changing the firmware to Entry/Expert 1.21, containing updated settings for the MLC.

