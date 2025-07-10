# Image Organizer

Image Organizer is a desktop application for organizing and managing images into folders. Built with Electron, it provides a simple interface to upload, search, and manage images on your local machine.

## Features

- **Upload Images:** Select and upload multiple images to a named folder.
- **Search Images:** Search for images by folder name and view them in a gallery.
- **Image Management:** Delete and copy images as needed.
- **Configuration:** Save and load application settings.
- **Theme Support:** Switch between themes from the settings panel.

## Project Structure

```
.
├── ImageOrgenaiz.exe
├── resources/
│   └── app/
│       ├── main.js         # Electron main process
│       ├── preload.js      # Preload script for IPC
│       ├── index.html      # Main UI
│       └── styles.css      # Stylesheet
├── locales/
│   ├── en-US.pak           # English (US) locale
│   └── ...                 # Other language packs
├── LICENSE
├── LICENSES.chromium.html
└── ... (Electron/Chromium runtime files)
```

## Usage

1. **Run the Application:**  
   Launch `ImageOrgenaiz.exe`.

2. **Upload Images:**  
   - Enter a folder name in the "Upload" section.
   - Click "Upload Image" and select images to add.

3. **Search Images:**  
   - Enter a folder name in the "Search" section.
   - Click "Search" to view images in that folder.

4. **Settings:**  
   - Click the ⚙️ icon to open the settings panel.
   - Change the theme as desired.

## Technical Details

- **Electron** is used for the desktop shell.
- **IPC** is handled via Electron's `ipcMain` and `ipcRenderer` ([main.js](resources/app/main.js), [preload.js](resources/app/preload.js)).
- **Images** are stored in the user's data directory under an `images` folder.
- **Localization** is supported via `.pak` files in the `locales` directory.

## License

This project includes Chromium and other open-source components. See [LICENSE](LICENSE) and [LICENSES.chromium.html](LICENSES.chromium.html) for details.

---

**Note:**  
This application is for local image organization only. No images are uploaded to the internet.
