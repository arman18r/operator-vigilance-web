# Privacy Policy — Operator Vigilance Monitor

**Last updated:** October 11, 2026  
**Application:** [Operator Vigilance Monitor](https://arman18r.github.io/operator-vigilance-web/)  
**Project repository:** [operator-vigilance-web](https://github.com/arman18r/operator-vigilance-web)

## 1. About this application

Operator Vigilance Monitor is an experimental, browser-based application that uses a device camera and facial landmarks to display possible indicators of eye closure, mouth opening, and head movement. It is intended for demonstration, exploratory research, and usability testing. It is **not** a certified fatigue detection system, medical device, or substitute for established workplace safety procedures.

This policy describes the behavior of the **web application version 4.3 as reviewed from its application files**. It does not represent an independent security certification or an audit of third-party hosting infrastructure. If the application changes, this policy should be reviewed and updated.

## 2. Camera access and on-device processing

- The application requests access to your camera only when you choose **Start Monitoring** and your browser grants permission.
- Camera frames are processed in your browser using MediaPipe Face Landmarker. The application derives facial landmarks and estimated eye, mouth, and head indicators from the video stream.
- The reviewed application code does **not intentionally upload camera video, photographs, or facial landmarks to an application-operated server**.
- The application requests video access without microphone audio (`audio: false`). It does not request microphone access.
- Selecting **Stop** stops the camera tracks used by the application. The application also attempts to stop those tracks when the page is closed or reloaded. You can additionally revoke camera permission through your browser or device settings.

Your browser or operating system controls camera permissions and may display a camera-use indicator.

## 3. Information stored in your browser

The application uses browser local storage to remember preferences such as:

- Selected language (English, Persian, or Arabic);
- Selected light or dark theme;
- Monitoring thresholds, calibration-related settings, and sound preferences.

These preferences may remain on your device between visits until you clear the site's stored data. They are not user accounts or identity records.

The event history displayed by the application (for example, warning type, time, and value) is maintained in the active page's memory in the reviewed version. It is not automatically uploaded by the application. If you select **Export CSV**, your browser creates and downloads a local file containing event records. You control how that exported file is stored, shared, or deleted.

## 4. External services and network requests

The website is delivered through **GitHub Pages**. The application also loads MediaPipe JavaScript and WebAssembly resources from **jsDelivr** and loads its face landmark model from the website's own `models/` path. These network requests are required to load and run the application.

When your browser connects to hosting or content-delivery services, those services may receive ordinary connection information such as your IP address, request details, browser information, and timestamps, subject to their own policies. This is separate from the application's local processing of camera frames.

Relevant third-party information:

- [GitHub Privacy Statement](https://docs.github.com/en/site-policy/privacy-policies/github-general-privacy-statement)
- [jsDelivr](https://www.jsdelivr.com/)

The project developer does not claim to control the independent logging or retention practices of these services.

## 5. Sharing and sale of information

The reviewed application code does not implement user accounts, advertising trackers, analytics event uploads, or an application backend for receiving camera images or event histories. The developer does not use the application code to sell camera images or facial landmarks. This statement does not eliminate ordinary data processing performed independently by hosting providers, CDNs, or your browser.

## 6. Your choices

You can:

- Decline camera access (monitoring will not function);
- Stop monitoring at any time;
- Revoke camera permission in your browser settings;
- Clear this website's stored data to remove saved preferences;
- Avoid exporting event history, or delete exported CSV files from your device;
- Close the page to end the active monitoring session.

## 7. Security and limitations

The application is served over HTTPS through GitHub Pages. No internet-connected application or third-party service can be guaranteed completely secure. The absence of upload logic in the reviewed application files is not a guarantee against browser extensions, compromised devices, altered dependencies, or future code changes.

Because this is an experimental prototype, alerts may be inaccurate or delayed. **Do not rely on it as the sole measure of operator fitness, fatigue, or workplace safety.**

## 8. Children and sensitive use

This application is not specifically designed for children. Do not use it to make employment, medical, disciplinary, or other consequential decisions about an individual without an appropriate legal basis, informed safeguards, and independently validated methods.

## 9. Policy changes

This policy may be updated when features, dependencies, hosting, or data practices change. The date at the top identifies the latest revision.

## 10. Contact

For questions about this policy or the application, please use the project's [GitHub Issues page](https://github.com/arman18r/operator-vigilance-web/issues). **Do not post personal information, face images, or sensitive workplace records in public issues.**
