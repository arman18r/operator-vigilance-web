<div align="center">

# Operator Vigilance Monitor

**Browser-Based Operator Vigilance and Fatigue Indicator Monitoring**

A multilingual, camera-based prototype for monitoring eye activity, mouth opening, and head posture in real time.

[**Launch Live Demo**](https://arman18r.github.io/operator-vigilance-web/) · [**Report an Issue**](https://github.com/arman18r/operator-vigilance-web/issues)

</div>

---

## Overview

**Operator Vigilance Monitor** is an experimental web application that uses a device camera and facial landmarks to identify *possible* indicators of reduced vigilance. It provides live visual feedback, configurable alert thresholds, audible notifications, and an event history.

The application is intended for demonstrations, research exploration, and usability testing. Its outputs are estimates based on facial geometry and should not be interpreted as a medical diagnosis or a validated assessment of fatigue or fitness for duty.

## Features

- **Eye monitoring:** Eye-opening indicators, closure duration, and blink counts.
- **Mouth monitoring:** Mouth-opening indicators and possible yawning events.
- **Head monitoring:** Relative head tilt, vertical displacement, and estimated face pitch.
- **Real-time alerts:** Visual status indicators and optional sound notifications.
- **Camera calibration:** Guided countdown for establishing a baseline head position.
- **Adjustable settings:** Detection thresholds, delays, smoothing, and alert preferences.
- **Event history:** Timestamped events with CSV export.
- **Languages:** English, Persian (فارسی), and Arabic (العربية), including right-to-left interface support.
- **Appearance:** Light and dark themes.
- **Responsive layout:** Designed for desktop and mobile browsers.

## Try It Online

**Live application:** https://arman18r.github.io/operator-vigilance-web/

1. Open the link in a modern browser on a device with a camera.
2. Select your preferred language and appearance.
3. Choose **Start Monitoring** and allow camera access when prompted.
4. Keep your face visible and your head steady during calibration.
5. Review the live indicators, alerts, and event history.

**First launch:** The browser may need time to download and initialize the MediaPipe runtime, WebAssembly components, and face landmark model. Subsequent launches may be faster depending on browser caching.

## Technology

- HTML, CSS, and JavaScript
- [MediaPipe Tasks Vision](https://ai.google.dev/edge/mediapipe/solutions/vision/face_landmarker/web_js)
- MediaPipe Face Landmarker model (`models/face_landmarker.task`)
- GitHub Pages for static website hosting

## Privacy and Processing

Face landmark processing is designed to run **locally in the browser**. The application does not require users to create an account or upload camera recordings to operate.

**Important:** The website still retrieves application resources (such as JavaScript dependencies and the model) over the network. Users should review browser permissions and the Network panel if they need to verify traffic for their deployment. Do not use this prototype to collect personal or workplace surveillance data without appropriate notice, consent, and safeguards.

## Local Development

Clone or download the repository, then serve it using a local HTTP server. For example, with Python installed:

```bash
python -m http.server 8000
```

Open `http://localhost:8000` in your browser. The `models/face_landmarker.task` file must remain at the expected relative path. Camera access generally requires HTTPS or a secure local context such as `localhost`.

## Project Status and Limitations

> **Experimental prototype — not a certified safety system.**
>
> Eye closure, yawning, and head-pose indicators can be affected by lighting, camera angle, face occlusion, glasses, individual differences, and device performance. False positives and missed detections are possible. The software must not be used as the sole basis for operational, employment, medical, or safety-critical decisions.

This project has not been presented here as clinically or occupationally validated. Any real-world use would require formal evaluation of accuracy, reliability, privacy, and human factors under the intended conditions.

## Repository Notes

This is the **public web deployment repository**. Browser-delivered HTML, CSS, JavaScript, and model assets are accessible to site visitors. Do not commit API keys, credentials, private datasets, or other secrets.

## Developer and Contact

**Project:** Operator Vigilance Monitor  
**GitHub:** [@arman18r](https://github.com/arman18r)  
**Website:** [Live Demo](https://arman18r.github.io/operator-vigilance-web/)

For bugs and suggestions, use the repository's [Issues](https://github.com/arman18r/operator-vigilance-web/issues) section, if enabled.

---

<div align="center"><sub>Developed as an experimental computer-vision monitoring application.</sub></div>
