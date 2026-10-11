Operator Vigilance Monitor v4

Replace index.html, style.css, app.js in your project. Keep models/face_landmarker.task unchanged.
Run python -m http.server 8000 and open http://localhost:8000

NEW: estimated face pitch (camera-relative rotation about X axis), 5-frame smoothing, calibrated baseline. Pitch alerts disabled by default; opt in via Settings.
The estimate is NOT a measured neck flexion angle or validated drowsiness indicator. Test by nodding forward/back, moving your chair, and turning sideways.
Existing v3 browser settings persist.

Version 4.1: Centered calibration countdown and progress overlay, visible on initial camera start and Recalibrate. No changes to detection thresholds.
