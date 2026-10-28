# Face Recognizer

A browser-based face-recognition demo built with HTML and JavaScript using [face-api.js](https://github.com/justadudewhohacks/face-api.js). Select an image and the app compares detected faces against the labeled example images included in the repository.

## Preview

[Open the HTMLPreview demo](https://htmlpreview.github.io/?https://github.com/sachin-acharya-projects/Face_Recognizer/blob/docs/improve-readme-preview-links/index.html)

> The app loads model files from `/models` and reference images from `labeled_images/`. If those root-relative paths do not resolve through HTMLPreview, use the local setup below.

## Features

- Select an image from your device.
- Detect faces and facial landmarks.
- Compare face descriptors against labeled reference images.
- Draw a bounding box and predicted identity for each detected face.

## Tech stack

- HTML and CSS
- Vanilla JavaScript
- [face-api.js](https://github.com/justadudewhohacks/face-api.js)

## Run locally

```bash
git clone https://github.com/sachin-acharya-projects/Face_Recognizer.git
cd Face_Recognizer
python -m http.server 8000
```

Open [http://localhost:8000](http://localhost:8000). Wait for the model and labeled-image data to load, then choose an image.

A local HTTP server is recommended because the app fetches model files and images by URL. Opening the HTML file directly may cause path or browser security issues.

## Project structure

- `index.html` — upload control and status message.
- `script.js` — model loading, descriptor matching, and result overlays.
- `style.css` — page styling.
- `face-api.min.js` — bundled face-api.js library.
- `models/` — pre-trained model files.
- `labeled_images/` — labeled reference images used for matching.

## Notes and limitations

- Recognition is limited to the reference identities represented in `labeled_images/`; it is not a general identity lookup service.
- Results depend on image quality, lighting, pose, and the included reference samples.
- Obtain consent before processing identifiable images, and do not treat the result as authoritative identity verification.

## License

No project-specific license is currently documented. Check the repository and dependency licenses before redistributing the code, models, or reference images.
