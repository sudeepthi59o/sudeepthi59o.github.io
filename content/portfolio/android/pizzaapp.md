+++
categories = ["app"]
coders = []
date = 2025-04-12T23:00:00Z
description = "An interactive Android app to design your perfect pizza with dynamic topping placement and live pricing"
image = "https://ik.imagekit.io/ys4gkaixy/pizza-svgrepo-com.svg?updatedAt=1744747787693"
title = "Android Custom Pizza Builder"
type = "androidapp"
url = "/portfolio/android/pizzaapp/"
[[tech]]
name = "Android Studio"
url = "https://developer.android.com/studio?_gl=1*1npx4x9*_up*MQ..&gclid=Cj0KCQjwtpLABhC7ARIsALBOCVoDoW_ZoN1eK0q9eFGMlT4ZE-nIwsUWbH7DDGkIsJX7M7GzzNl1aKsaAnV7EALw_wcB&gclsrc=aw.ds&gbraid=0AAAAAC-IOZmHyIn7c11qpDYFzrptif_wk"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Android_Studio_Logo_2024.svg?updatedAt=1744516638440"
[[tech]]
name = "Kotlin"
url = "https://kotlinlang.org"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Kotlin_Icon.svg?updatedAt=1744516638766"
+++

A dynamic Android app that allows users to customize a pizza by selecting toppings and their placement—left, right, or across the whole pizza. As toppings are added or removed, the total price updates in real-time based on placement.

### Core Features

- Interactive topping selection with three placement options: Left, Right, or All.
- Real-time price calculation: $0.50 for left/right toppings, $1.00 for full-pizza toppings.
- Modular architecture using Kotlin enum class and Parcelize for efficient state management.
- Maintains state and updates the UI seamlessly using Jetpack Compose.

### Design

The app uses a modern, clean interface styled with Material 3 themes. Users are presented with a base pizza and a topping menu. Each topping has an associated image overlay and label, providing visual feedback as they are placed on the pizza. The UI responds instantly to user input, reflecting topping changes and updated pricing.

### Challenges and Solutions

A major challenge was managing topping placement and ensuring UI consistency while keeping the state immutable. This was addressed by using Kotlin data classes and copy functions to reflect state updates without mutating the original data. Enums were used to cleanly map toppings and placement options with string and drawable resources, ensuring scalability.

### Technologies Used

- **Kotlin** for Android app development
- **Android Studio** as the IDE
- **Jetpack Compose** for declarative UI
- **Material 3** for theming
- **Parcelize** for passing complex data between screens


### Demo

![Pizza Ordering App Screenshot](/pizza_app.gif)


### Conclusion

This project deepened my understanding of state handling and UI composition in Jetpack Compose. It also provided hands-on experience with structured enums, theming, and real-time price logic. Future improvements could include saving past pizza orders, integrating drag-and-drop topping placement, or animating topping overlays.

> This app was completed as part of academic coursework and is hosted in a private repository and available upon request.  