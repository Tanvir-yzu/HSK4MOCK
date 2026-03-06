# Chinese Proficiency Test (HSK) Mock Exam Viewer

## Overview

This is a web-based application designed to help users practice for the Chinese Proficiency Test (HSK) by providing a clean and interactive interface for viewing mock exam papers (in PDF format) and listening to accompanying audio files.

The application is built as a single-page interface using modern web technologies, making it fast, responsive, and easy to use locally without any complex setup.

## Features

- **Interactive PDF Viewer**:
  - View HSK mock exam papers directly in the browser.
  - Controls for navigating between pages (Previous/Next).
  - Zoom in and out for better readability.
  - Fallback to a native browser viewer if the custom viewer fails to render a PDF.

- **Integrated Audio Player**:
  - Plays audio files (MP3, WMA) linked to the corresponding exam paper.
  - Standard controls for play/pause.
  - Quick seek buttons (-10s, -5s, +5s, +10s) for easy navigation.
  - Displays current time and total duration.

- **Dynamic File Management**:
  - Pre-loaded list of available mock exam files.
  - **Search**: Instantly filter the file list by name.
  - **Upload**: Add your own PDF files via a button or by dragging and dropping them onto the page.

- **Advanced Timer/Stopwatch Component**:
  - **Countdown (Duration)**: Set a timer for a specific duration (e.g., 1 hour) to simulate exam conditions.
  - **Countdown (Target Date)**: Set a countdown to a specific future date and time.
  - **Stopwatch**: A count-up timer to track elapsed time.
  - **Full Controls**: Start, pause, resume, and reset functionality.
  - **State Persistence**: The timer's state is saved in `localStorage`, so it remains accurate even if the page is reloaded.
  - **Visual Feedback**: The timer pulses and changes color when the countdown finishes.

## How to Use

1.  **Run Locally**:
    - Because the application loads local files, it must be run through a local web server to avoid browser security restrictions (CORS issues).
    - The simplest way is to use Python's built-in HTTP server. Open your terminal in the project directory and run:
      ```bash
      python -m http.server
      ```
    - Then, open your web browser and navigate to `http://localhost:8000`.

2.  **Using the Application**:
    - Click on any PDF from the file list on the left to open it in the viewer on the right.
    - If an audio file is associated with the PDF, it will appear in the audio player section.
    - Use the timer at the top to manage your practice session time.

## Technologies Used

- **HTML5**: The core structure of the application.
- **Tailwind CSS**: For modern, responsive, and utility-first styling.
- **Alpine.js**: For adding interactive and reactive behavior directly within the HTML.
- **PDF.js**: A library by Mozilla for rendering PDF files in the browser.