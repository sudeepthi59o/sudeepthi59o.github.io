+++
categories = ["app"]
coders = []
date = 2025-04-12T23:00:00Z
description = "A responsive Android app that fetches and displays real-time social posts with Firebase integration."
image = "https://ik.imagekit.io/ys4gkaixy/comment-balloon-part-3-svgrepo-com.svg?updatedAt=1744747787673"
title = "Android Posts App"
type = "androidapp"
url = "/portfolio/android/postsapp/"
[[tech]]
name = "Android Studio"
url = "https://developer.android.com/studio?_gl=1*1npx4x9*_up*MQ..&gclid=Cj0KCQjwtpLABhC7ARIsALBOCVoDoW_ZoN1eK0q9eFGMlT4ZE-nIwsUWbH7DDGkIsJX7M7GzzNl1aKsaAnV7EALw_wcB&gclsrc=aw.ds&gbraid=0AAAAAC-IOZmHyIn7c11qpDYFzrptif_wk"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Android_Studio_Logo_2024.svg?updatedAt=1744516638440"
[[tech]]
name = "Kotlin"
url = "https://kotlinlang.org"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Kotlin_Icon.svg?updatedAt=1744516638766"
+++

The Android Posts app displays real-time posts submitted by users, including usernames, image uploads, and descriptions. The feed mimics core social platform functionality and includes authentication, live data updates, and dynamic UI rendering.

### Core Features

- Displays a real-time feed of posts from Firebase Firestore
- Each post includes a username, description, image (optional), and relative timestamp
- Supports user authentication and logout using Firebase Auth
- Navigation to post creation via a floating action button (FAB)
- Uses Coil library for smooth and efficient image loading

### Design

The app follows the Model-View-ViewModel (MVVM) architecture to maintain clean separation of concerns. Posts are observed using Kotlin StateFlow for real-time UI updates. A RecyclerView is used to display a scrollable list of posts with a custom layout per item. Relative timestamps (e.g., “2 hours ago”) are calculated using DateUtils. For development convenience, post images are hosted on GitHub and dynamically loaded using the Coil image loading library.

### Challenges and Solutions

Handling null or invalid image URLs required implementing exception-safe image loading with fallback placeholders using Coil. Firebase Firestore queries were optimized with ordering and limiting to fetch the most recent 30 posts.

### Technologies Used

- **Kotlin** for Android development
- **Firebase Firestore** for cloud-based data storage
- **Firebase Authentication** for secure user login
- **StateFlow** and **ViewModel** for reactive data handling
- **RecyclerView** for efficient list rendering
- **Coil** for efficient image loading from remote URLs (images hosted on GitHub)

### Screenshots


| ![Login](/Login_Screen.png) | ![Posts View](/Posts_Screen.png) | ![Add Post](/Add_Post.png) |
|------------------------|------------------------|------------------------|

### Conclusion

This project enhanced my skills in cloud data integration, real-time UI updates, and mobile UI/UX design. It represents a foundational component of social apps and is extensible with features like likes, comments, and pagination.

> This app was completed as part of academic coursework and is hosted in a private repository and available upon request.  