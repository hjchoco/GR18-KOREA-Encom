# GR18-KOREA-Encom
GR18-KOREA-Encom

## Overview
Meraki-for-SmartCity is a management dashboard with a missing child alert feature on top of it. Its goal is to build an additional value on Cisco Meraki product for governments and public organizations to have digitized IT work process. Meraki-for-SmartCity is designed for monitoring Meraki APs, presenting visualized analysis from Meraki API, sending an real-time Webex alert message when the missing child is found around the Meraki APs. The flexibility of web dashboard and scalability of Webex alert message brings Smart City available on our laptop, or even on our phone.

## The Problem to Solve 
Finding a missing child in crowded area such as famous beach, tourist attractions, and shopping center is a complicated problem. It requires human resource, time, and effort. However, most of them already have implemented APs for public Wi-Fi so we can utilize the existing infrastructure to resolve this problem.

## Solution Diagram
![image](https://user-images.githubusercontent.com/73694660/120414373-d8836d00-c394-11eb-980c-275975e79a05.png)

## Software Architecture

## How it works
It displays the webcam video in real time with person’s names tagged on the video.
* Camera.py – Checks webcam and opens a window to display it
* Face_recog.py – Recognizes the faces on webcam frame by comparing face object with the pictures in ‘knowns’ folder
* Live_streaming.py – Send video over network http://{{ip_address}}:5000/. Face recognition can be displayed via web with this code.
### Usage
```
$ python camera.py
$ python face_recog.py
$ python live_streaming.py
```
Put picture with the person’s face in ‘knowns’ directory. Change the file name as the person’s name like ‘john.jpg’. Then run ‘python face_recog.py’ or ‘python live_streaming.py’ to send video over network.
