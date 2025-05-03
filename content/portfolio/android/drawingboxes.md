+++
categories = ["app"]
coders = []
date = 2025-04-12T23:00:00Z
description = "An intuitive Android app for drawing and editing boxes on a canvas."
image = "https://ik.imagekit.io/ys4gkaixy/box-svgrepo-com.svg?updatedAt=1744747788111"
title = "Android Box Drawing App"
type = "androidapp"
url = "/portfolio/android/drawingboxes/"
[[tech]]
name = "Android Studio"
url = "https://developer.android.com/studio?_gl=1*1npx4x9*_up*MQ..&gclid=Cj0KCQjwtpLABhC7ARIsALBOCVoDoW_ZoN1eK0q9eFGMlT4ZE-nIwsUWbH7DDGkIsJX7M7GzzNl1aKsaAnV7EALw_wcB&gclsrc=aw.ds&gbraid=0AAAAAC-IOZmHyIn7c11qpDYFzrptif_wk"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Android_Studio_Logo_2024.svg?updatedAt=1744516638440"
[[tech]]
name = "Kotlin"
url = "https://kotlinlang.org"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Kotlin_Icon.svg?updatedAt=1744516638766"
+++

A simple and interactive Android app that lets users draw boxes by touching the screen. The app supports multiple boxes on the canvas, and each box can be drawn with touch gestures, offering real-time visual feedback

### Core Features

- **Interactive Box Drawing:** Users can draw boxes by tapping and dragging on the screen.
- **Multiple Boxes:** Multiple boxes can be drawn and exist simultaneously on the canvas.
- **Real-Time Update:** The app provides instant visual updates as users interact with the screen.
- **Customizable Appearance:** Each box is drawn with a customizable color and style.
- **Canvas Background:** A soft background color for better visibility and contrast.


### Design

The app features a minimalistic design with a simple canvas as the drawing area. Users can draw boxes by pressing down and dragging their finger across the screen. The app dynamically responds to touch events, allowing for precise control of box size and position.

### Challenges and Solutions

The main challenge was handling touch events for dynamic updates. The app handles touch gestures efficiently, ensuring smooth drawing experience even with multiple boxes. Additionally, maintaining the state of all drawn boxes across different touch events was managed using a mutable list and real-time updates on the canvas.

### Technologies Used

- **Kotlin** for Android app development
- **Android Studio** as the IDE
- **Custom Views**  to handle touch and drawing operations

### Demo

![Box Drawing App Screenshot](/box_drawing.gif)

### Conclusion

This project helped improve my Android development skills, particularly in custom view creation, event handling, and dynamic UI updates. Future improvements may include the ability to modify or delete existing boxes, along with adding color options for each box.

> This app was completed as part of academic coursework and is hosted in a private repository and available upon request.  