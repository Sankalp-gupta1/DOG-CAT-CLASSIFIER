# Dog vs Cat Classifier

A browser-based image-classification demo that predicts whether an uploaded image is more likely to contain a **dog** or a **cat**.

## Live app

**https://dog-cat-classifier-lac.vercel.app/**

## What changed

The repository originally contained no source code, model, dataset configuration, or runnable demo.

It now contains a complete hosted browser application that:

- loads TensorFlow.js
- loads a pretrained MobileNet image model
- accepts image uploads or drag-and-drop
- runs inference in the browser
- maps ImageNet labels into dog/cat groups
- shows a confidence bar
- displays the top raw model predictions

No backend, database, API key, or image upload server is required.

## How it works

```text
Uploaded image
   -> MobileNet inference in browser
   -> Top ImageNet labels
   -> Dog-label score vs cat-label score
   -> Final demo prediction
```

The model can recognize many individual dog breeds and several common cat labels. The app combines those probabilities into a simpler two-class result.

## Run locally

Because the page loads JavaScript model packages from a CDN, use a small local web server:

```bash
cd web
python -m http.server 8000
```

Then open:

```text
http://localhost:8000
```

## Project structure

```text
DOG-CAT-CLASSIFIER/
├── web/
│   └── index.html
└── README.md
```

## Tech stack

- HTML
- CSS
- JavaScript
- TensorFlow.js
- MobileNet
- Vercel

## Limitations

This is a portfolio/learning classifier built on a general ImageNet model rather than a custom dog-vs-cat training dataset. Images outside those classes may be marked uncertain.

It is not a veterinary or scientific diagnostic system.

## Author

**Sankalp Gupta**

GitHub: https://github.com/Sankalp-gupta1
