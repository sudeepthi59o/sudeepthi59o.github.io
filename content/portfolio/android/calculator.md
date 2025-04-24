+++
categories = ["app"]
coders = []
date = 2025-04-12T23:00:00Z
description = "A user-friendly Android calculator with basic and scientific functions"
image = "https://ik.imagekit.io/ys4gkaixy/calculator-svgrepo-com-2.svg?updatedAt=1744747787618"
title = "Android Calculator App"
type = "androidapp"
url = "/portfolio/android/calculator/"
[[tech]]
name = "Android Studio"
url = "https://developer.android.com/studio?_gl=1*1npx4x9*_up*MQ..&gclid=Cj0KCQjwtpLABhC7ARIsALBOCVoDoW_ZoN1eK0q9eFGMlT4ZE-nIwsUWbH7DDGkIsJX7M7GzzNl1aKsaAnV7EALw_wcB&gclsrc=aw.ds&gbraid=0AAAAAC-IOZmHyIn7c11qpDYFzrptif_wk"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Android_Studio_Logo_2024.svg?updatedAt=1744516638440"
[[tech]]
name = "Kotlin"
url = "https://kotlinlang.org"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Kotlin_Icon.svg?updatedAt=1744516638766"
+++

The Android Calculator app is designed to perform basic arithmetic operations while mimicking the functionality of the iPhone's default calculator. It supports both portrait and landscape modes, with landscape mode unlocking advanced trigonometric and logarithmic functions.

### Core Features

- Basic arithmetic operations (addition, subtraction, multiplication, division)
- Trigonometric functions (sin, cos, tan) and logarithmic functions (log10, ln) in landscape mode
- User input persists across device rotations
- Custom app icon and button layout
- Log messages recorded for each button click

### Design

The app features a simple and intuitive interface with a standard calculator layout. In landscape mode, the layout adjusts to provide additional scientific functions, while the UI remains clear and easy to navigate. The app dynamically adjusts to changes in orientation, ensuring users can continue their calculations without interruption.

### Challenges and Solutions

Managing chained operations with trigonometric and logarithmic functions required careful ordering of operations. A consistent operator precedence system was implemented to ensure accurate results.

### Technologies Used

- **Kotlin** for Android app development
- **Android Studio** as the IDE
- **Android Lifecycle** to preserve user input during rotation

### Demo

![Calculator App Screenshot](/calculator_demo_2.gif)

### Conclusion

This project strengthened my Android development skills, particularly in managing orientation changes and enhancing user experience. Future improvements may include history tracking and additional scientific features.

> This app was completed as part of academic coursework and is hosted in a private repository and available upon request.  