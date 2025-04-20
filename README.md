# FocusTrack

**FocusTrack** is a real-time backend service that uses your webcam input to detect whether you're focused or distracted.

---

## What It Does

-  Accepts real-time webcam frames via WebSocket
- Detects gaze, eye openness, and head posture using MediaPipe + OpenCV
- Computes a "focus score" from the visual data
- Emits live alerts when the user is distracted
- Stores session events (focused, distracted) in a PostgreSQL database
- Provides an `/analytics` endpoint to view focus performance over time

---

## Tech Stack

| Component       | Tech Used           |
|----------------|---------------------|
| API framework   | FastAPI             |
| Real-time comm  | WebSockets          |
| CV Processing   | OpenCV + MediaPipe  |
| Database        | PostgreSQL + SQLAlchemy |
| Config          | python-dotenv       |
| Deployment      | Docker-ready        |

---

## Quickstart (Local)

### 1. Clone the Repo

```bash
git clone https://github.com/maniic/focustrack.git
cd focustrack
