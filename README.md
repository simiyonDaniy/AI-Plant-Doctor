# AI Plant Doctor — Android project

This is a native Android WebView wrapper around the AI Plant Doctor web app. It has an app label/icon and a bundled app screen. The image-classification model must still be trained and hosted separately in Teachable Machine, then its model URL entered inside the app.

## Build an APK without a local Android computer

1. Create a GitHub repository and upload the contents of this folder.
2. Open the repository's **Actions** tab and enable workflows.
3. Run **Build AI Plant Doctor APK** (or push a commit to the main branch).
4. Open the completed workflow run and download the `AI-Plant-Doctor-debug-apk` artifact.
5. Extract the artifact ZIP on your Android phone and install the APK. Android may ask you to allow installs from your browser/file manager.

## Model setup

1. Open https://teachablemachine.withgoogle.com/
2. Train an image model with classes such as `Healthy Leaf`, `Damaged Leaf`, and `Not a Leaf`.
3. Export/share it as a hosted model and copy its URL.
4. In the app, paste that URL into **Teachable Machine model URL** and tap **Load AI model**.

## Important limitations

- The hosted model and TensorFlow.js libraries need internet access.
- This is a visual classifier for educational use, not a verified plant disease diagnosis.
- The app has not been compiled or device-tested in this environment; use the GitHub Actions build to compile it and test on your phone before exhibition.
