# Intelligent-sorting-system
# 🔩 Intelligent Nut & Bolt Sorting System

An automated **computer-vision-based sorting system** designed to identify and sort nuts and bolts based on their visual characteristics.

A smartphone camera captures images of the objects, while a laptop performs image processing and classification. An **ESP8266** handles sensor inputs and controls the sorting mechanism.

---

##  Overview

Sorting nuts and bolts manually can be time-consuming and prone to human error, especially when dealing with large quantities of components.

This project aims to automate the process using:

*  Smartphone-based image acquisition
*  Computer vision using **OpenCV / YOLO**
*  Conveyor-based material transportation
*  IR-based object detection
*  ESP8266-based control
*  Servo-actuated sorting mechanism
*  Multiple collection bins

The system detects an object in a designated detection zone, determines whether it is a **nut or bolt**, and then directs it toward the appropriate collection bin.

---

##  Objectives

* Automate the sorting of nuts and bolts.
* Reduce manual sorting effort.
* Use computer vision for object identification.
* Establish communication between a computer-vision system and an microcontroller.


---

##  How It Works

### 1. Feeding

Nuts and bolts are introduced into the feeding mechanism.

The feeder is designed to guide the components onto the conveyor while minimizing overlap between objects.

### 2. Transportation

A conveyor belt transports the components toward the detection area.

The conveyor provides controlled movement so that objects can be captured and classified consistently.

### 3. Object Detection

An **IR sensor** detects when an object enters the detection region.

The sensor provides a trigger that can be used to synchronize image capture and conveyor movement.

### 4. Image Acquisition

A smartphone camera is positioned above the detection zone.

The camera captures the object against a controlled background and sends the image/video stream to the laptop.

### 5. Computer Vision

The laptop processes the captured image using computer-vision techniques.

The system determines whether the detected component is a **nut or bolt**.

### 6. Communication

The classification result is communicated from the laptop to the ESP.

The ESP does not perform the computationally intensive image processing. Instead, it acts as the **control unit for the physical system**.

### 7. Sorting

Once the ESP receives the classification result and the object reaches the sorting position, it activates the appropriate servo mechanism.

The mechanism redirects the component into its corresponding collection bin.

---

##  Hardware

| Component             | Purpose                       |
| --------------------- | ----------------------------- |
| ESP8266               | Main embedded controller      |
| Smartphone Camera     | Image acquisition             |
| IR Sensor (HW-201)    | Object detection / triggering |
| NEMA 17 Stepper Motor | Conveyor drive                |
| Stepper Motor Driver  | Motor control                 |
| Micro Servo Motor     | Sorting mechanism             |
| Conveyor Belt         | Material transportation       |
| Collection Bins       | Sorted component storage      |
| DC Power Supply       | System power                  |
| Buck Converter(LM2596)| Voltage regulation            |

---


## Mechanical Design

The mechanical system consists of:

* Material feeder
* Conveyor assembly
* Raised conveyor side walls
* Camera mounting structure
* Detection area
* Object stop/gate mechanism
* Sorting mechanism
* Collection bins

The camera mounting structure is designed to maintain a consistent viewpoint and distance from the conveyor.

The conveyor side walls help prevent components from falling off the belt during transportation.

Curtains will be provided at the entrance and exit of detection region to control lighting.

---


##  Performance Metrics

The system can be evaluated using:

### Classification Accuracy

Percentage of objects correctly identified as nuts or bolts.

### Sorting Accuracy

Percentage of objects successfully placed into the correct bin.

### Detection Time

Time required to detect and classify an object.

### Sorting Time

Time between object detection and activation of the sorting mechanism.

### Throughput

Number of components successfully sorted per minute.

### False Detection Rate

Number of incorrect detections relative to the total number of objects processed.

---

##  Future Improvements

Possible future improvements include:

* Classification based on **size and dimensions**
* Detection of different nut and bolt sizes
* Automatic counting of sorted components
* Real-time monitoring dashboard
* Higher-speed conveyor operation
* Improved feeding mechanism
* Industrial-grade camera integration

---
