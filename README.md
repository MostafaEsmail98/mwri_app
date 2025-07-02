# 🗺️ mwri_google App

## 📌 Overview
The **Land Mapping App** is a mobile application built with **Flutter** that allows users to visualize land boundaries by displaying transparent images over a real-world map and interact with the map by adding notes at specific locations.

The app is designed to assist farmers, surveyors, or landowners in managing their land visually and interactively by overlaying boundary images and saving geolocation-based notes.

---

## 🌟 Key Features

- 🖼️ **Image Overlay on Map**  
  Display transparent images (e.g., scanned land boundaries) aligned accurately over a map using geographic coordinates (top-left and bottom-right points).

- 📝 **Add Notes on Map**  
  Users can **tap on any location on the map** to add a note, which is then **saved to Firebase** along with the latitude and longitude of the tapped point.

- 📍 **Accurate Geolocation Placement**  
  Supports precise coordinate input to position overlays and notes accurately on the map.

- 🔐 **Firebase Integration**  
  Notes with coordinates are securely stored and retrieved from **Firebase Firestore**.

- 🧭 **Interactive Map**  
  Users can zoom, pan, and explore the map to interact with overlays and add custom notes easily.

- 📱 **Responsive Design**  
  Works smoothly across various Android screen sizes.

---

## 🛠️ Tech Stack

| Technology        | Description                                                        |
|------------------|--------------------------------------------------------------------|
| 💙 Flutter        | Main UI framework                                                  |
| 🎯 Dart           | Programming language                                               |
| 🧠 Bloc (Cubit)   | Lightweight state management for note/map control                 |
| ☁️ Firebase       | Cloud Firestore used to store notes and their coordinates         |
| 🧩 Native Android SDK | Used to render image overlays and handle map taps natively      |

---

## ❗ Why Native Android Code Was Used

While Flutter provides several map packages, they **lack fine control** for:

- Displaying **Ground Overlays** using accurate geocoordinates.
- Handling `LatLngBounds` for images with precision.
- Managing real-time taps and custom gesture handling for overlays.

To overcome these limitations, **Native Android SDK** (Kotlin) was integrated with Flutter using **Platform Channels**, enabling:

- `GroundOverlay` support to position images using GPS coordinates.
- Full control over image opacity, scale, and map alignment.
- Handling map click events natively and passing them to Flutter for note creation.

> ✅ This hybrid approach allows the best of both worlds: Flutter for fast UI, Native for deep map control.

---

## 📸 Screenshots 

![1](https://github.com/user-attachments/assets/4290ba10-3a8b-429a-9faf-72f3ef3bac71)
![2](https://github.com/user-attachments/assets/22c3aafb-00f6-45bd-ba5f-588011cf04ef)
![3](https://github.com/user-attachments/assets/d0dca1cc-9447-4c7c-8aae-dec9c92ffd74)
![5](https://github.com/user-attachments/assets/1675bfa6-ac9f-446a-83ea-a4c605f94e15)
![6](https://github.com/user-attachments/assets/c1aea439-2fc1-42ff-991b-5e780eae42c3)





