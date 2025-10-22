# YouTube Clone

A complete YouTube-like video sharing platform consisting of:
- **Web App** - React front-end with a Node.js / Express backend.
- **Android App** - Native client (MVVM + Room) for mobile users.
- **C++ Server** - Recommendation microservice that provides personalized video suggestions.

This repository serves as the central documentation hub, linking all three components and providing setup instructions, usage guides, and screenshots.

---

## Repositories
| Component | Description | Repository |
|------------|--------------|-------------|
| Web + Node.js Server | React + Express app for video streaming, upload, comments, and profiles | [YouTube](https://github.com/nogagur/YouTube) |
| Android App | Mobile client with authentication, uploads, and comment management | [YouTubeAndroid](https://github.com/nogagur/YouTubeAndroid) |
| C++ Recommendations Server | Provides video recommendations using user and video data | [cppServer](https://github.com/nogagur/cppServer) |

---

## Getting Started
Follow the [Setting Up the Project](docs/Setting_up.md) guide to install dependencies and run all three components locally.  
You’ll need:
- Node.js  
- MongoDB  
- Android Studio  
- Git LFS  

Once set up:
- Run the Node.js server (`npm start`)
- Build and run the C++ server (`make && ./server_app`)
- Launch the Android app via Android Studio

Default ports:
- Node.js server → `8081`  
- C++ recommender → `55555`  
- MongoDB → `27017`

---

## Documentation
All detailed documentation can be found here:

- [Setting Up the Project](docs/Setting_up.md)
- [Web App Overview](docs/Web_App.md)
- [Android App Overview](docs/Android_App.md)

Each section includes explanations, feature lists, screenshots, and demo credentials.

---

## Architecture Overview

The system consists of three connected components:

- **Node.js / Express backend** – the main API that manages authentication, videos, comments, and profiles, and communicates with the recommendation service.  
- **C++ recommendation server** – a separate microservice that analyzes user and video data to generate personalized recommendations.  
- **Clients:** a React web app and an Android app that both interact with the same API.  

All data is stored in MongoDB, and both clients receive recommended videos through the Node.js API.
