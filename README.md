# Low-Cost Video Monitoring with Tracking and Virtual Fence

This repository contains a **low-cost analytical video monitoring system** developed at the **LSIIM Image Laboratory**. The project uses **computer vision techniques** to perform **people detection, object tracking, and virtual fence monitoring** using conventional cameras.

The system is designed to monitor a predefined area and detect intrusions in real time. When a person enters a delimited polygonal region (virtual fence), the system visually highlights the violation and tracks the individual responsible for breaking the perimeter.

---

## Project Overview

The application processes video streams and applies **background subtraction and object tracking techniques** to identify moving objects, specifically people. A **virtual fence** is defined as a polygonal area of interest within the scene.

- When no intrusion occurs, the fence remains highlighted in **blue**
- When the fence is violated, it changes to **red**
- The person responsible for the intrusion is **outlined and tracked** in real time

The project demonstrates that reliable video surveillance analytics can be achieved using **low-cost hardware and standard video sources**.

---

## Core Features

- Low-cost video monitoring using conventional cameras  
- Background subtraction using OpenCV (`createBackgroundSubtractor`)  
- Noise reduction with morphological operations  
- Contour detection and analysis  
- Virtual fence defined by a polygonal region  
- Real-time intrusion detection  
- Person tracking with visual contour marking  
- Visual feedback through color-coded regions  

---

## Techniques Used

- **Background Subtraction:**  
  Implemented using OpenCV’s `createBackgroundSubtractor` (MOG2 or KNN)

- **Noise Reduction:**  
  Morphological operations combined with contour filling and filtering

- **Virtual Fence:**  
  A polygon representing a restricted area; intrusion is detected when a contour intersects this region

- **Object Tracking:**  
  Contours corresponding to people are tracked and highlighted after fence violation

#### Background subtraction applied with morphological noise reduction operations
<img width="1000" height="541" alt="image" src="https://github.com/user-attachments/assets/a2c21b2c-5adc-4a90-b762-46b567be7b5e" />

---

## Repository Structure

```text
Low-Cost-Video-Monitoring-with-Tracking-and-Virtual-Fence/
├── final.cpp        # Main C++ source code
├── people.mp4       # Video used in the analysis and PDF report
├── highway.mp4      # Additional test video
├── README.md
└── LICENSE
```
---

## How It Works

1. The video stream is loaded and processed frame by frame
2. Background subtraction separates foreground objects from the scene
3. Noise reduction refines detected regions
4. Contours are extracted and analyzed
5. A virtual fence polygon is drawn on the frame
6. If any contour crosses the fence:
    - The fence color changes
    - The person is highlighted and tracked

---

## Technologies Used

- Language: C++
- Library: OpenCV
- Domain: Computer Vision / Video Analytics

--- 

## Results

Using the `people.p4` for example:

<img width="1504" height="788" alt="image" src="https://github.com/user-attachments/assets/8c300a9b-07ac-4b5b-8f84-96aa132fee7a" />
<img width="1527" height="793" alt="image" src="https://github.com/user-attachments/assets/21cb94b9-1e78-4d74-80e7-11f3c4b6b3fe" />

---

## License

This project is licensed under the MIT License. See the LICENSE file for more details.
