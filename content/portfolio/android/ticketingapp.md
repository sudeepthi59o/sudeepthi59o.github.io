+++
categories = ["app"]
coders = []
date = 2025-04-12T23:00:00Z
description = "A user-friendly Android ticketing tracking app"
image = "https://ik.imagekit.io/ys4gkaixy/ticket-svgrepo-com.svg?updatedAt=1744747787740"
title = "Android Ticketing App"
type = "androidapp"
url = "/portfolio/android/ticketingapp/"
[[tech]]
name = "Android Studio"
url = "https://developer.android.com/studio?_gl=1*1npx4x9*_up*MQ..&gclid=Cj0KCQjwtpLABhC7ARIsALBOCVoDoW_ZoN1eK0q9eFGMlT4ZE-nIwsUWbH7DDGkIsJX7M7GzzNl1aKsaAnV7EALw_wcB&gclsrc=aw.ds&gbraid=0AAAAAC-IOZmHyIn7c11qpDYFzrptif_wk"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Android_Studio_Logo_2024.svg?updatedAt=1744516638440"
[[tech]]
name = "Kotlin"
url = "https://kotlinlang.org"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Kotlin_Icon.svg?updatedAt=1744516638766"
+++

A simple yet effective Android application for managing task or issue tickets. Users can create, update, and view tickets with fields such as title, description, date, assignee, and an optional photo attachment. 

### Core Features

- **Ticket Creation & Editing:** Add or update task-related tickets with essential details.
- **Room Database Integration: Tickets are stored locally with Room, supporting schema migrations and data persistence.
- **Live Data Updates:** Uses Kotlin Flows and StateFlow to observe real-time ticket list updates.
- **Date Picker Dialog:** Pick a due date for a ticket using an intuitive calendar interface.
- **Image Attachment (Planned/Partial):** Schema supports photo file paths for ticket-related images (with potential to expand UI support).
- **Scalable Bitmap Utility:** Efficient image loading with dynamic scaling to reduce memory overhead.

### Design

The app uses a ViewModel-driven architecture to separate UI and business logic, promoting maintainability and testability. A Repository pattern manages data access and abstracts Room operations. Tickets are presented in a list that updates automatically as data changes, creating a responsive experience.

### Challenges and Solutions

The challenge of real-time database updates to the UI was solved by using Kotlin Coroutines, Flow, and StateFlow for lifecycle-aware state management. To handle future schema changes, Room migrations were implemented to ensure smooth database evolution without data loss.

### Technologies Used

- **Kotlin** for Android app development
- **Android Studio** as the IDE
- **Room** for local persistence with custom TypeConverters and schema migrations.
- **Kotlin Coroutines + Flow** for asynchronous data handling.
- **ViewModel + StateFlow** for lifecycle-safe state management.
- **DatePickerDialog** for intuitive date selection.

### Demo

![Ticketing App Screenshot](/ticket_app.gif)


### Conclusion

This project sharpened my skills in Android architecture components, local data storage, and clean app design. Future plans include:

- Implementing full photo capture/display functionality.
- Adding delete and filter/sort options for better ticket management.
- Enhancing UI/UX with animations and accessibility improvements.

> This app was completed as part of academic coursework and is hosted in a private repository and available upon request.  