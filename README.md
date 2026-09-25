# Anubhav — Object Confessional

A small local AI experiment by Anubhav. Upload a photo of an everyday object and let the object describe what it has witnessed in a short, slightly petty first-person confession. The app also turns the confession into playable speech.

## Requirements

- Node.js 18+
- A desktop environment supported by QVAC
- Enough disk space for the local model downloads

## Install

```bash
npm install
```

## Run

```bash
node server.js
```

Open `http://localhost:3000`.

The first run downloads the local QVAC models. Later runs use the cached models.

## QVAC

- `@qvac/sdk` `^0.20.0`
- `loadModel()` for the local vision and speech models
- `completion()` for image understanding and confession generation
- `textToSpeech()` for local audio generation
- `unloadModel()` in the CLI flow

No cloud AI API or API key is used for inference. The uploaded image is processed locally and removed from the temporary upload folder after the request.

## Project

Built and designed by **Anubhav**.

## License

MIT
