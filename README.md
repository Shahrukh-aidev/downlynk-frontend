<div align="center">

# 🚀 Downlynk

### Universal Media Downloader • Fast • Modern • AI-Inspired UI

Download videos and audio from hundreds of supported platforms through a clean, modern interface powered by a custom Railway backend.

<br>

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Railway](https://img.shields.io/badge/Railway-Backend-0B0D0E?style=for-the-badge&logo=railway&logoColor=white)
![REST API](https://img.shields.io/badge/REST-API-00C853?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-success?style=for-the-badge)

</div>

---

# 🎥 Demo

<p align="center">

<img src="demo.gif" width="100%">

</p>

---

# 🌟 Overview

Most online downloaders suffer from the same problems.

- Pop-up advertisements
- Fake download buttons
- Slow servers
- Malware redirects
- Poor user experience
- Limited platform support

**Downlynk** was built to solve those problems.

It provides a modern web application that communicates with a dedicated backend to analyze media URLs, retrieve metadata, and securely download audio or video files without exposing users to intrusive advertisements or confusing interfaces.

Instead of feeling like an outdated utility website, Downlynk delivers a premium application experience with responsive design, live download telemetry, real-time progress tracking, and elegant animations.

---

# ✨ Features

| Feature | Description |
|----------|-------------|
| 🎥 Universal Downloader | Download videos from hundreds of supported websites |
| 🎵 Audio Extraction | Convert supported media directly into MP3 |
| 📺 Multiple Video Qualities | Select available resolutions before downloading |
| ⚡ Metadata Preview | Instantly retrieve title, thumbnail and uploader information |
| 📊 Live Progress Tracking | Real-time download percentage, speed and ETA |
| 🚀 Fast Backend | Dedicated Railway-powered extraction server |
| 🔄 Smart URL Analysis | Automatic media detection after pasting a link |
| 🎨 Modern Interface | Responsive glassmorphism-inspired UI |
| 🛡 Error Handling | Graceful handling of unsupported or invalid URLs |
| 📱 Responsive Design | Optimized for desktop and mobile browsers |

---

# 📸 Screenshots

## Home Page

<p align="center">

<img src="DOWNLYNK PIC/Download.jpeg" width="100%">

</p>

---

## Media Preview

<p align="center">

<img src="DOWNLYNK PIC/Download.jpeg" width="100%">

</p>

Once a URL is pasted, Downlynk automatically analyzes the content and displays

- Thumbnail
- Title
- Uploader
- Duration
- Available qualities
- Supported formats

before the download even begins.

---

## Download Progress

<p align="center">

<img src="DOWNLYNK PIC/Download1.jpeg" width="100%">

</p>

Unlike many browser downloaders, Downlynk provides real-time download telemetry including

- Progress Percentage
- Current Download Speed
- Estimated Remaining Time
- Download Status
- Completion Indicator

---

# 💡 Why Downlynk?

Most download websites are designed around advertisements instead of user experience.

Downlynk focuses on delivering

- Speed
- Simplicity
- Reliability
- Clean Design
- Secure Downloads
- Modern UX

The frontend remains lightweight while the backend handles extraction, processing, and media delivery.

---

# ⚙️ Download Workflow

```text
             User Pastes URL
                    │
                    ▼
        Automatic URL Validation
                    │
                    ▼
         Metadata Request (/info)
                    │
                    ▼
      Thumbnail + Video Information
                    │
                    ▼
     User Selects Quality & Format
                    │
                    ▼
        Download Request (/download)
                    │
                    ▼
      Backend Starts Media Extraction
                    │
                    ▼
      Progress Polling (/progress)
                    │
                    ▼
        Browser Receives File Blob
                    │
                    ▼
          Secure File Download
```

---

# 🧠 What Makes It Different?

Unlike traditional download websites, Downlynk separates responsibilities into two independent systems.

## Frontend

Responsible for

- User Interface
- URL Validation
- Progress Display
- Animations
- File Delivery
- User Interaction

---

## Backend

Responsible for

- Media Extraction
- Platform Compatibility
- Download Processing
- Stream Buffering
- Quality Detection
- File Generation

This architecture keeps the frontend lightweight while allowing the backend to evolve independently as supported platforms change.

---

# 📈 Performance Highlights

✅ Lightweight Frontend

✅ Vanilla JavaScript

✅ Responsive UI

✅ Blob-based Downloads

✅ Live Download Telemetry

✅ REST API Architecture

✅ Railway Cloud Deployment

✅ Mobile Friendly

---

# 🖼 User Experience

The interface was designed around clarity and responsiveness.

Design highlights include

- Frosted Glass Navigation
- Smooth Animations
- Responsive Layout
- Neon Accent Colors
- Interactive Buttons
- Elegant Progress Indicators
- Dynamic Status Updates

Rather than overwhelming users with dozens of options, Downlynk presents only the controls needed at each step of the download process.

---
# 🏗️ System Architecture

Downlynk follows a client-server architecture where the frontend is responsible for user interaction while the backend performs all heavy media extraction.

```text
                         USER
                           │
                           ▼
               Paste Media URL
                           │
                           ▼
        ┌────────────────────────────┐
        │      Frontend (Browser)    │
        │                            │
        │ HTML • CSS • JavaScript    │
        │                            │
        └──────────────┬─────────────┘
                       │
             POST /info│
                       ▼
        ┌────────────────────────────┐
        │     Railway Backend        │
        │                            │
        │ URL Validation             │
        │ Metadata Extraction        │
        │ Resolution Detection       │
        │ Thumbnail Generation       │
        └──────────────┬─────────────┘
                       │
             Response  │
                       ▼
             Display Metadata
                       │
                       ▼
              User Chooses Quality
                       │
                       ▼
           POST /download Request
                       │
                       ▼
        ┌────────────────────────────┐
        │     Extraction Engine      │
        │                            │
        │ Stream Processing          │
        │ Audio Conversion           │
        │ Video Extraction           │
        │ File Buffering             │
        └──────────────┬─────────────┘
                       │
            GET /progress
                       │
                       ▼
             Live Progress Updates
                       │
                       ▼
            Browser Downloads Blob
```

---

# ⚡ Technology Stack

| Layer | Technology | Purpose |
|--------|------------|----------|
| Frontend | HTML5 | Structure |
| Styling | CSS3 | Responsive UI |
| Programming | Vanilla JavaScript | Application Logic |
| Backend | Railway | Cloud Deployment |
| API | REST | Communication |
| Downloader | yt-dlp Backend | Media Extraction |
| Browser APIs | Blob API | Secure Downloads |
| Async | Fetch API | HTTP Communication |

---

# 📂 Project Structure

```text
Downlynk/

│
├── assets/
│   ├── images/
│   ├── icons/
│   ├── fonts/
│   └── animations/
│
├── css/
│   ├── style.css
│   ├── responsive.css
│   └── variables.css
│
├── js/
│   ├── app.js
│   ├── api.js
│   ├── downloader.js
│   ├── progress.js
│   ├── animations.js
│   └── utilities.js
│
├── screenshots/
│
├── index.html
│
├── README.md
│
└── LICENSE
```

---

# 🌐 REST API

The frontend communicates with the backend using three REST endpoints.

---

## POST `/info`

Retrieves media metadata before downloading.

### Request

```json
{
  "url":"https://youtube.com/watch?v=..."
}
```

### Response

```json
{
  "title":"Video Title",
  "thumbnail":"...",
  "duration":"12:41",
  "qualities":[
      "360p",
      "720p",
      "1080p"
  ]
}
```

Purpose:

- Validate URL
- Fetch metadata
- Retrieve thumbnail
- Detect supported resolutions
- Populate UI

---

## POST `/download`

Starts the extraction process.

### Request

```json
{
    "url":"...",
    "quality":"1080p",
    "format":"video"
}
```

Backend returns a downloadable file Blob after extraction completes.

---

## GET `/progress/{id}`

Returns download progress.

Example response

```json
{
    "progress":72,
    "speed":"3.8 MB/s",
    "eta":"12 sec"
}
```

Used by the frontend to display

- Download Percentage
- Speed
- ETA
- Current Status

---

# 🔄 Frontend Workflow

```text
Paste URL

      │

      ▼

Validate Input

      │

      ▼

Wait 800ms (Debounce)

      │

      ▼

Send Metadata Request

      │

      ▼

Receive Thumbnail

      │

      ▼

Display Video Information

      │

      ▼

Select Format

      │

      ▼

Select Resolution

      │

      ▼

Click Download

      │

      ▼

Receive Progress Updates

      │

      ▼

Generate Blob

      │

      ▼

Automatic Browser Download
```

---

# 🔥 Backend Workflow

```text
Receive URL

      │

      ▼

Validate Link

      │

      ▼

Detect Platform

      │

      ▼

Fetch Metadata

      │

      ▼

Locate Streams

      │

      ▼

Extract Audio/Video

      │

      ▼

Buffer Output

      │

      ▼

Generate Blob

      │

      ▼

Return File
```

---

# 🛡 Error Handling

Downlynk gracefully handles common failure scenarios.

| Scenario | Response |
|----------|----------|
| Invalid URL | Validation Error |
| Unsupported Website | Informative Error Message |
| Backend Offline | Connection Warning |
| Extraction Failure | Retry Option |
| Network Timeout | Request Cancellation |
| Missing Quality | Automatic Fallback |

---

# 🚀 Performance Optimizations

Several optimizations were implemented to keep the application responsive.

### Smart Debouncing

Instead of sending a request every keystroke, URL analysis begins only after the user stops typing for approximately **800 milliseconds**.

---

### Progress Polling

Progress updates are retrieved periodically rather than continuously, reducing unnecessary API traffic while maintaining a smooth user experience.

---

### Blob Downloads

Downloaded files are created entirely in browser memory using

```javascript
window.URL.createObjectURL(blob)
```

This avoids exposing direct media URLs and enables secure file delivery.

---

### Lightweight Frontend

No frontend frameworks are required.

Advantages include

- Faster loading
- Minimal bundle size
- Lower memory usage
- Simpler deployment
- Better browser compatibility

---

# 🎨 UI Philosophy

Rather than copying the appearance of traditional download websites, Downlynk focuses on creating an interface that feels like a modern desktop application.

Design principles include:

- Clean typography
- Frosted glass effects
- Responsive layouts
- Neon accent colors
- Smooth transitions
- Minimal distractions
- Consistent spacing
- Fast interactions

The result is a streamlined experience that prioritizes usability over clutter.

---
# 🚀 Getting Started

Follow these steps to run Downlynk locally.

---

## 1. Clone the Repository

```bash
git clone https://github.com/Shahrukh-aidev/downlynk-frontend.git
```

Move into the project directory.

```bash
cd downlynk-frontend
```

---

## 2. Run the Frontend

Since Downlynk is built using native web technologies, no compilation or bundling is required.

Simply open

```text
index.html
```

inside your preferred browser.

Alternatively, serve the project using a lightweight local server.

Using VS Code Live Server

```
Right Click → Open with Live Server
```

or

```bash
npx serve .
```

---

## 3. Backend

The frontend is already configured to communicate with the deployed Railway backend.

If you are running your own backend, update the API base URL inside the JavaScript configuration.

Example

```javascript
const API_BASE = "https://your-backend-url";
```

---

# ⚙ Configuration

The application communicates with three backend endpoints.

| Endpoint | Purpose |
|-----------|----------|
| POST `/info` | Retrieve media information |
| POST `/download` | Start extraction |
| GET `/progress/{id}` | Live progress updates |

These endpoints can be replaced with your own backend implementation if desired.

---

# 📦 Browser Compatibility

Downlynk supports all modern browsers.

| Browser | Supported |
|----------|-----------|
| Chrome | ✅ |
| Edge | ✅ |
| Firefox | ✅ |
| Brave | ✅ |
| Opera | ✅ |
| Safari | ✅ |

---

# 📈 Performance

The application was designed with responsiveness in mind.

### Optimizations

- Smart request debouncing
- Lightweight frontend
- Blob-based downloads
- Responsive UI rendering
- Efficient API polling
- Optimized CSS animations
- Lazy metadata loading

These optimizations help minimize unnecessary network requests while maintaining a smooth user experience.

---

# 🔒 Security Considerations

Downlynk follows several security-focused practices.

- Client never exposes direct media URLs
- Files are delivered using browser Blob objects
- URL validation before requests
- Graceful handling of failed API responses
- Safe asynchronous requests using Fetch API

Although the frontend remains lightweight, sensitive extraction logic stays on the backend.

---

# 🧪 Error Handling

Common scenarios are handled gracefully.

| Situation | Behavior |
|-----------|----------|
| Invalid URL | Displays validation error |
| Unsupported website | Shows informative message |
| Backend unavailable | Connection warning |
| Extraction timeout | Retry option |
| Network interruption | Request cancelled safely |
| Unsupported quality | Automatic fallback |

---

# 🛣 Roadmap

Future improvements planned for Downlynk include

- Desktop application using Tauri
- Browser extension
- Playlist downloading
- Batch downloads
- Download history
- User accounts
- Favorite downloads
- Download queue
- Resume interrupted downloads
- Cloud synchronization
- Theme customization
- Keyboard shortcuts
- Localization
- Mobile-first interface
- Progressive Web App (PWA)

---

# 🤝 Contributing

Contributions are welcome.

If you would like to improve Downlynk:

1. Fork the repository.

2. Create a feature branch.

```bash
git checkout -b feature/amazing-feature
```

3. Commit your changes.

```bash
git commit -m "Add amazing feature"
```

4. Push your branch.

```bash
git push origin feature/amazing-feature
```

5. Open a Pull Request.

Please ensure your code follows the existing style and includes appropriate documentation where necessary.

---

# 💡 Lessons Learned

Developing Downlynk provided valuable experience in

- REST API integration
- Asynchronous JavaScript
- Browser Blob APIs
- Responsive interface design
- State management
- Download telemetry
- Frontend architecture
- Error handling
- User experience design
- Cloud deployment using Railway

---

# 📚 Acknowledgements

Special thanks to the open-source community and the technologies that made this project possible.

- HTML5
- CSS3
- JavaScript
- Railway
- Fetch API
- Browser Blob API
- yt-dlp ecosystem

---

# 📄 License

This project is licensed under the **MIT License**.

You are free to use, modify, and distribute this software in accordance with the license terms.

---

# ⚠ Disclaimer

Downlynk is provided for **educational and personal use**.

Users are responsible for ensuring they have the appropriate rights or permissions before downloading content from third-party platforms. Please respect copyright laws and the terms of service of the websites you access.

---

<div align="center">

## ⭐ If you found this project helpful, consider giving it a star!

Your support helps others discover the project and encourages future development.

<br>

### Built with ❤️ using HTML, CSS, JavaScript, REST APIs, and Railway.

</div>
