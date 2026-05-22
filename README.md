# Snap-Sorter

Snap-Sorter is a modern browser-based image reviewing and sorting tool built with **HTML**, **Tailwind CSS**, and **Vanilla JavaScript**.

It allows users to quickly browse, review, organize, and save images using:

- Keyboard shortcuts
- Drag-and-drop support
- Thumbnail previews
- Fullscreen mode
- Local folder access using the File System Access API

The application is designed to provide a fast and smooth workflow for reviewing large collections of images directly inside the browser.

---

# Features

- Open entire image folders
- Browse images quickly
- Previous / next navigation
- Thumbnail sidebar
- Save selected images
- Auto-next after saving
- Drag & drop support
- Keyboard shortcuts
- Fullscreen mode
- Modern responsive UI
- Local file system access
- Built completely with Vanilla JavaScript
- Lightweight and fast

---

# Technologies Used

## HTML5

Used for the structure and layout of the application.

---

## Tailwind CSS

Used for:

- Responsive design
- Utility-first styling
- Layout management
- Modern UI components
- Hover effects
- Spacing and alignment

CDN Version:

```html
<script src="https://cdn.tailwindcss.com"></script>
```

---

## Vanilla JavaScript

Used for:

- Image loading
- Event handling
- Navigation
- File saving
- Keyboard shortcuts
- DOM manipulation
- Thumbnail rendering
- Fullscreen functionality
- Drag & drop support
- Dynamic UI updates

---

# File System Access API

One of the most advanced features of this project is the use of the **File System Access API**.

This API allows the browser to interact directly with the user's local file system after permission is granted.

## Used For

### Selecting Save Folder

```javascript
saveDirectoryHandle = await window.showDirectoryPicker();
```

Allows the user to choose a local folder.

---

### Creating Files

```javascript
const fileHandle = await saveDirectoryHandle.getFileHandle(
  file.name,
  {
    create: true,
  }
);
```

Creates or accesses a file inside the selected folder.

---

### Writing Files To Disk

```javascript
const writable = await fileHandle.createWritable();

await writable.write(file);
await writable.close();
```

Saves the image directly to the user's computer.

---

# How The Application Works

## 1. Open Image Folder

The user selects a local image folder.

```javascript
imageInput.click();
```

The application reads all selected image files.

---

## 2. Image Filtering

Only valid image files are loaded.

```javascript
file.type.startsWith("image/")
```

---

## 3. Image Viewer

The current image is displayed inside the main viewer.

```javascript
viewer.src = URL.createObjectURL(file);
```

---

## 4. Navigation

Users can move between images using:

- Previous button
- Next button
- Arrow keys

---

## 5. Saving Images

Selected images can be saved directly into a chosen folder.

---

## 6. Thumbnail Sidebar

Every loaded image generates a thumbnail preview for faster navigation.

---

## 7. Drag & Drop

Users can drag image files directly into the application.

---

## 8. Fullscreen Mode

Fullscreen viewing improves image review experience.

```javascript
document.documentElement.requestFullscreen();
```

---

# Keyboard Shortcuts

| Key | Action |
|---|---|
| ← | Previous image |
| → | Next image |
| Space | Save image |
| F | Toggle fullscreen |

---

# Project Structure

```bash
Snap-Sorter/
│
├── index.html
├── README.md
├── screenshots/
└── assets/
```

---

# Browser Support

Best supported browsers:

- Google Chrome
- Microsoft Edge

The File System Access API is currently not fully supported in all browsers.

---

# Performance Improvements

The project includes several optimizations:

- Object URL cleanup
- Efficient image rendering
- Smooth transitions
- Disabled controls when inactive
- Lightweight architecture
- Fast local processing
- No external JavaScript frameworks

---

# Features Breakdown

## Image Loading

Loads multiple images from local folders.

---

## Local File Saving

Saves reviewed images directly to user-selected folders.

---

## Toast Notifications

Displays lightweight feedback messages.

---

## Responsive Design

Works across different screen sizes.

---

## Auto-Next Workflow

Automatically moves to the next image after saving.

---

# Why This Project Is Interesting

This project demonstrates:

- Modern browser APIs
- Real-world workflow tooling
- Advanced JavaScript DOM manipulation
- Local file system interaction
- Responsive UI design
- State management without frameworks
- Practical utility software development

---

# Future Improvements

Possible future upgrades:

- Zoom controls
- Image tagging
- Favorites system
- Delete/reject workflow
- AI image classification
- Electron desktop version
- EXIF metadata viewer
- Batch processing
- Image comparison mode
- Cloud sync support

---

# Running The Project

## Option 1 — Directly Open HTML

Open:

```bash
index.html
```

inside your browser.

---

## Option 2 — VS Code Live Server

Use the VS Code Live Server extension.

---

# GitHub Setup

```bash
git init
git add .
git commit -m "Initial commit"
git branch -M main
git remote add origin https://github.com/WhiruS-X07/Snap-Sorter.git
git push -u origin main
```

---

# Author

Built by **WhiruS**  

GitHub:  
https://github.com/WhiruS-X07

---

# Snap-Sorter

> Sort. Review. Save.
