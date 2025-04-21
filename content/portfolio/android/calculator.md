+++
categories = []
coders = ["sudeepthi59o"]
date = 2025-04-12T23:00:00Z
description = "A user-friendly Android calculator with basic and scientific functions"
image = "https://ik.imagekit.io/ys4gkaixy/calculator-svgrepo-com-2.svg?updatedAt=1744747787618"
title = "Android Calculator App"
type = "androidapp"
url = "/portfolio/android/calculator/"
[[tech]]
logo = "https://res.cloudinary.com/samrobbins/image/upload/v1591793276/logos/logos_hugo_h2xbne.svg"
name = "Hugo"
url = "https://gohugo.io/"
+++

## Android Calculator App

The Android Calculator app is designed to perform basic arithmetic operations while mimicking the functionality of the iPhone's default calculator. It supports both portrait and landscape modes, with landscape mode unlocking advanced trigonometric and logarithmic functions.

## Core Features

- Basic arithmetic operations (addition, subtraction, multiplication, division)
- Trigonometric functions (sin, cos, tan) and logarithmic functions (log10, ln) in landscape mode
- User input persists across device rotations
- Custom app icon and button layout
- Log messages recorded for each button click

## Design and User Interface

The app features a simple and intuitive interface with a standard calculator layout. In landscape mode, the layout adjusts to provide additional scientific functions, while the UI remains clear and easy to navigate. The app dynamically adjusts to changes in orientation, ensuring users can continue their calculations without interruption.

## Challenges and Solutions

One of the challenges was managing the chain of operations to ensure trigonometric and logarithmic functions operate correctly on previous results. By carefully implementing the order of operations, I ensured accurate calculations and results.

## Technologies Used

- **Kotlin** for Android app development
- **Android Studio** as the IDE
- **Android Lifecycle** to preserve user input during rotation

## User Experience Enhancements

The app offers a customizable button layout, allowing users to personalize the interface to their liking.

## Demo

![Calculator App Screenshot](path/to/screenshot.png)

## Project Link

You can view the source code on GitHub: [Android Calculator GitHub](https://github.com/yourusername/your-repo)

## Conclusion

This project helped me refine my skills in building Android applications with a focus on user experience and handling device-specific challenges. Future updates will include a more advanced scientific calculator mode.