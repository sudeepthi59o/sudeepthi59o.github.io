+++
categories = ["web-dev"]
coders = []
date = 2025-05-10T23:00:00Z
description = "A lightweight iOS fitness tracker for daily step goals built with SwiftUI and Core Motion"
image = "https://ik.imagekit.io/ys4gkaixy/Skills/ios-svgrepo-com.svg?updatedAt=1747166062691"
title = "StepWise - iOS Fitness Tracker"
type = "post"
[[tech]]
name = "Swift"
url = "https://developer.apple.com/swift/"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/swift-svgrepo-com.svg?updatedAt=1744516638040"
[[tech]]
name = "Xcode"
url = "https://developer.apple.com/xcode/"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Xcode.svg?updatedAt=1744516638307"
+++

A lightweight and user-friendly iOS app designed to track and encourage daily walking goals. **StepWise** leverages the Core Motion framework to access step data and includes features like goal setting, reminders, and history tracking — all implemented using modern SwiftUI patterns.

## **Core Features**

- **Live Step Count Tracking:** Users can manually start and stop tracking; live data is displayed in the app using CMPedometer.
- **Daily Step Goal:** Daily step goals between 1,000–15,000 steps can be set and tracked with visual feedback.
- **Motivational Reminders:** Daily toggleable notifications remind users to stay active.
- **Unit Preferences:** Users can switch between kilometers and miles, with seamless distance conversion and persistence.
- **Historical Logs:** Step counts and goals are stored using Core Data and can be reviewed later as graphs.
- **Clean UI:** Built with modular SwiftUI components using adaptive layouts and icon-based visuals for metrics.

## **Design**

The interface uses a friendly gradient background and intuitive navigation:

- **Home View** shows steps, distance, calories, and goal status.
- **History View** displays the daily, weekly and monthly historical step data as graphs.
- **Settings View** includes goal customization, unit toggle, and notifications.
- Reusability is built into views such as MetricRow and ActionButton.

## **Challenges and Solutions**

- **Avoiding HealthKit:** StepWise tracks activity without relying on HealthKit, ensuring broader usability and simplified permissions.
- **Live Step Updates:** Handled real-time updates using SwiftUI state management and reactive UI bindings.
- **Persistent Settings:** Used @AppStorage, UserDefaults and Core Data for smooth user experience across app launches.

## **Technologies Used**

- **SwiftUI** for building reactive and declarative UI
- **Core Motion** for real-time step tracking
- **UserDefaults** for storing user preferences and app state
- **UserNotifications** for daily reminder alerts
- **Core Data** for keeps records of user step data
- **Xcode** for development and testing

## **Demo**

![Step Counter App Screenshot](/stepwise_app2.gif)

## **Conclusion**

This project provided hands-on experience with real-time sensor data and reactive UI design. It also strengthened my familiarity with persistent local storage and iOS notification handling. Future improvements could include HealthKit integration or an achievements system to motivate users.


> This app was developed as part of academic coursework and is hosted in a private repository. Access is available upon request.
---
