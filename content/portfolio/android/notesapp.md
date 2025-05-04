+++
categories = ["app"]
coders = []
date = 2025-04-12T23:00:00Z
description = "A Firebase-powered personal note manager"
image = "https://ik.imagekit.io/ys4gkaixy/notes-note-svgrepo-com.svg?updatedAt=1744747787683"
title = "Android Notes App"
type = "androidapp"
url = "/portfolio/android/notesapp/"
[[tech]]
name = "Android Studio"
url = "https://developer.android.com/studio?_gl=1*1npx4x9*_up*MQ..&gclid=Cj0KCQjwtpLABhC7ARIsALBOCVoDoW_ZoN1eK0q9eFGMlT4ZE-nIwsUWbH7DDGkIsJX7M7GzzNl1aKsaAnV7EALw_wcB&gclsrc=aw.ds&gbraid=0AAAAAC-IOZmHyIn7c11qpDYFzrptif_wk"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Android_Studio_Logo_2024.svg?updatedAt=1744516638440"
[[tech]]
name = "Kotlin"
url = "https://kotlinlang.org"
logo = "https://ik.imagekit.io/ys4gkaixy/Skills/Kotlin_Icon.svg?updatedAt=1744516638766"
+++

A user-friendly Android app for creating, editing, and managing notes. The app provides a clean, responsive interface to add, update, and delete text notes—making it ideal for quick reminders, to-do lists, or jotting down ideas.

### Core Features

- **User Authentication:** Login screen to ensure notes are accessed only by the intended user.
- **Create Notes:** Add new notes with a title and content.
- **Edit Notes:** Modify existing notes with ease.
- **Delete Notes:** Remove unwanted notes with a long press.
- **Persistent Storage:** Notes are stored locally using Room Database and persist across sessions.
- **RecyclerView UI:** Scrollable and responsive list of saved notes.

### Design

The app uses a minimalistic design to keep the focus on content. Notes are displayed in a vertically scrolling list, with each item showing the title and preview of the note body. A floating action button (FAB) allows users to quickly create a new note. A simple form is used for editing and creating notes, ensuring a seamless and distraction-free user experience.

### Challenges and Solutions

A key challenge was implementing real-time updates to the notes list. This was addressed using StateFlow from the ViewModel to observe changes in the Room database. Properly defining entity classes, DAO interfaces, and ViewModel logic ensured smooth data persistence and retrieval through Room and consistent UI updates.

### Technologies Used

- **Kotlin** for Android app development
- **Android Studio** as the IDE
- **Room Database** for local storage of notes
- **ViewModel** and **StateFlow** for managing UI state and reactive updates
- **RecyclerView** for displaying the list of notes
- **Firebase Authentication** for secure user login functionality


### Demo

![Notes App Screenshot](/notes_app_demo.gif)

### Conclusion

This project strengthened my skills in Android app development, particularly in integrating Firebase Authentication and implementing reactive UI updates. Future improvements could include adding user-specific note storage and support for rich text editing.

> This app was completed as part of academic coursework and is hosted in a private repository and available upon request.  