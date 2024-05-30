# Implementation of Implantation Stagger Measuring Unit

## Overview

The Implantation and Stagger Measuring Unit is designed to automate the measurement of the distance between the overhead electrification (OHE) masts and the railway tracks (implantation) as well as the horizontal displacement of the overhead contact wire from the centerline of the pantograph (stagger). This automation is achieved using a Raspberry Pi equipped with a camera, combined with computer vision techniques.

## Table of Contents

1. Introduction
2. Hardware Setup
3. Software Setup
4. Implementation Details
   - Implantation Measurement
   - Stagger Measurement
5. Usage Instructions
6. Paper Preview

## Introduction

Railway electric traction systems, known as Overhead Equipment (OHE) systems, require precise measurements to ensure the proper placement of masts relative to the railway tracks and the correct alignment of overhead contact wires. Traditionally, these measurements are performed manually. This project aims to automate the process using computer vision with a Raspberry Pi camera, thereby reducing manual labor and increasing accuracy.

## Hardware Setup

1. **Raspberry Pi**: Ensure that the Raspberry Pi is set up with the latest Raspberry Pi OS.
2. **Camera**: Attach a Raspberry Pi camera module to the Raspberry Pi.

### Connection

- Connect the Raspberry Pi camera to the Raspberry Pi.
- Mount the Raspberry Pi on the wooden frame.
- Place the laser pointer on top of the camera.

## Software Setup

1. **Install Raspberry Pi OS**: Follow the official Raspberry Pi documentation to install the latest Raspberry Pi OS.
2. **Python Libraries**: Install the necessary Python libraries using the following command:
3. **Clone the Repository**: Clone the project repository to your Raspberry Pi.

## Implementation Details

### Implantation Measurement

1. **Setup**: Place a 2D object (e.g., a circle) on the mast at the point where the laser pointer falls. Ensure the camera and the object are at the same height.
2. **Image Capture**: The Raspberry Pi camera continuously captures frames.
3. **Distance Calculation**: Using the contour area method in OpenCV, the distance between the camera and the object is calculated based on the area of the detected contour. The relationship between contour area and distance is established through calibration.
4. **Display**: The calculated distance is displayed on the GUI.

### Stagger Measurement

1. **Setup**: Position the camera at the center of the track facing the overhead contact wire.
2. **Image Capture**: The Raspberry Pi camera captures frames of the overhead wire.
3. **Wire Detection**: The endpoints of the contact wire are detected, and a line is drawn indicating the wire's position.
4. **Displacement Calculation**: The midpoint of the detected wire is calculated and its displacement from the center of the frame is determined. This pixel displacement is converted to centimeters.
5. **Display**: The stagger measurement is displayed on the GUI.

## Usage Instructions

1. **Power On**: Power on the Raspberry Pi and ensure it is connected to the camera.
2. **Run the Application**: Execute the main application script.
3. **Measure Implantation**:
   - Align the camera with the mast using the laser pointer.
   - Place the circle on the mast.
   - Click the "Distance" button on the GUI to measure the distance.
4. **Measure Stagger**:
   - Position the camera at the center of the track facing the overhead wire.
   - Click the "Stagger" button on the GUI to measure the stagger.

## Paper Preview

### Title: 
**Implementation of Implantation Stagger Measuring Unit**

### Authors:
Angela Infanta Ramesh, Ashish Dinesh Singh,Battina Babykutty, and Dheeraj Kallakuri

### Link to Full Paper:
[Read the full paper here](https://ijemr.vandanapublications.com/index.php/ijemr/article/view/57/57)

### Citation:
A.I. Ramesh, A. Singh, B. Babykutty and D. Kallakuri, Implementation of Implantation Stagger Measuring Unit. *International Journal of Engineering and Management Research, Volume-11, Issue-3 (June 2021)*,
