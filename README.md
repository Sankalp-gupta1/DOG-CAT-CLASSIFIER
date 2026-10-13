# Dog vs Cat Classifier

A live browser-based image classifier built with **TensorFlow.js** and **MobileNet**.

## Live app

**https://dog-cat-classifier-sankalp.vercel.app/**

## How it works

1. You choose or drag a pet image into the page.
2. MobileNet loads in the browser.
3. The model produces ImageNet labels and probabilities.
4. The app groups common dog-breed and cat labels into two scores.
5. The UI shows the result and the original top ImageNet predictions.

The image stays in the browser. This deployment does not upload the photo to a backend.

## Why this implementation exists

The repository originally contained only documentation and no runnable model or source code.

To make the project honest and deployable, the live version uses a clearly identified pretrained MobileNet model instead of claiming a custom CNN that was not present in the repository.

## Tech stack

- HTML
- CSS
- JavaScript
- TensorFlow.js
- MobileNet
- Vercel

## Run locally

```bash
cd web
python -m http.server 8000
```

Open `http://localhost:8000`.

Internet access is needed the first time because TensorFlow.js and MobileNet are loaded from a CDN.

## Limitations

- This is an ImageNet-based portfolio demo.
- It is not a custom-trained dog/cat binary model.
- Unusual images may return “Not sure”.
- It should not be used for animal health or safety decisions.

## Author

Sankalp Gupta  
GitHub: https://github.com/Sankalp-gupta1
