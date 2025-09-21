# ComfyUI Manager

**ComfyUI Manager** is a portable Windows application built with PyQt6 to manage ComfyUI installations. It provides a user-friendly interface to:
- Run ComfyUI internally or externally (with CMD console).
- Manage models, folders, and custom nodes.
- Compare dependencies and perform quick pip installs.
- View logs and embed the ComfyUI web interface[](http://127.0.0.1:8188/).

## Features
- **Dark Theme with Green Tabs**: Modern and intuitive design.
- **Portable EXE**: No installation required.
- **Embedded Web View**: Access ComfyUI directly in the app.
- **Customizable**: Edit `config.json` for settings.

## Download
The latest release is available as a portable package (due to GitHub's 25MB limit, hosted externally):
- **Download**: [ComfyUI-Manager-v1.0.0.zip](https://drive.google.com/file/d/16a3iDBwZNBsWbkvLVRe8sMVN3vXBuL7I/view?usp=sharing)
  - Contains `ComfyUIManager.exe`, `config.json`, and `icon.ico`.
  - File size: ~150-200MB.

### How to Use
1. **Download and Extract**:
   - Download the ZIP from the link above.
   - Extract `ComfyUI-Manager-v1.0.0.zip` to a folder (e.g., `C:\ComfyUI-Manager`).

2. **Initial Setup**:
   - Double-click `ComfyUIManager.exe` to launch.
   - Go to the "Settings" tab.
   - Set "ComfyUI base" to your ComfyUI installation (e.g., `G:\ComfyUI_windows_portable`).
   - Set "Python exe for pip" to your Python executable (e.g., `G:\ComfyUI_windows_portable\python_embeded\python.exe`).
   - Save settings (updates `config.json`).

3. **Running ComfyUI**:
   - Switch to the "Run ComfyUI" tab.
   - Uncheck "Open external CMD" for internal run (logs in "Startup Logs" tab).
   - Click "Run ComfyUI" to start.
   - Use "Open UI in browser" or the "ComfyUI Web" tab to access `http://127.0.0.1:8188/`.
   - Click "Stop ComfyUI" to terminate.

4. **Managing Content**:
   - "Models" tab: List and manage models.
   - "Folder Manager" tab: Create or delete folders.
   - "Custom Nodes" tab: Clone, update, or delete nodes (yellow highlight on selection).

5. **Dependencies**:
   - "Check Installed Packages" to list pip packages.
   - "Compare" to find missing dependencies (red highlights).
   - "Quick Install" for missing packages (supports space-separated names).

6. **Logs**:
   - "Manager Logs": App activity.
   - "Startup Logs": ComfyUI output.

### config.json
A default `config.json` is included. Edit it manually if needed:
```json
{
  "COMFY_BASE": "",
  "PYTHON_EMBEDED": "",
  "PORT": 8188,
  "RUN_EXTERNAL_BY_DEFAULT": true
}
