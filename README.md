# Anubhav — Object Confessional

A small local AI experiment by Anubhav.

Upload a photo of an everyday object and let the object describe what it has witnessed in a short, slightly petty first-person confession. The app can also turn the confession into playable speech.

## Features

- Upload an image of an everyday object
- Local image understanding using Tether QVAC
- Generates a first-person object confession
- Local text-to-speech output
- No cloud AI API or API key required
- Image processing happens locally

## Requirements

- Node.js 18+
- A desktop environment supported by QVAC
- Enough disk space for the local model downloads

## Installation

Install the project dependencies:

```bash
npm install
```

## Run

Start the application:

```bash
npm start
```

Then open:

```text
http://localhost:3000
```

The first run downloads the required local QVAC models. This can take some time. Later runs can use the cached models.

## How It Works

1. Upload an image of an everyday object.
2. QVAC loads the local vision model.
3. The image is analyzed on-device.
4. The AI generates a short first-person confession.
5. The confession can be converted into speech locally.

## QVAC SDK

This project uses Tether QVAC for on-device AI inference.

- SDK: `@qvac/sdk`
- Version: `^0.20.0`
- `loadModel()` — loads the local AI model
- `completion()` — analyzes the image and generates the confession
- `textToSpeech()` — generates local speech
- `unloadModel()` — releases the loaded model

No cloud AI API or API key is used for inference.

## Privacy

The application is designed around local processing. Uploaded images are processed by the local QVAC model and are not sent to a cloud AI API.

## Project

Built and designed by **Anubhav** for the Tether QVAC challenge.

## License

MIT