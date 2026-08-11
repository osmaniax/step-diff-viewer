## [Beta Release] STEP DIFF VIEW: Lightweight 3D CAD Inspection Tool for Android

### What is STEP DIFF VIEW?
STEP DIFF VIEW is a lightweight Android application designed to quickly load and compare two 3D CAD models (STEP format) right in the palm of your hand.
This tool is not built to replace heavy PC-based CAD software. 
Instead, it is crafted for those moments when you think:"I don't need to boot up my heavy desktop CAD software, but I want to quickly inspect geometric changes on-site."

### Key Features
The core functionality is deliberately kept simple and focused on a 3-mode workflow.

#### Before: 
![Image](./img/Screenshot_20260811-212334.png)

Displays the original reference STEP model (e.g., blank or raw material).

#### Diff Overlay:
![Image](./img/Screenshot_20260811-212336.png)

Superimposes both STEP models with color-coding (Red: Base/Before model, Blue: Finished/After model) to visually inspect geometric variations.

Note: Rather than computing exact, heavy boolean solid subtraction on-device, it overlays both geometries in a unified coordinate system to provide instant, intuitive visual verification.

#### After: 
![Image](./img/Screenshot_20260811-212339.png)

Displays the final processed STEP model independently.The UI follows a natural timeline sequence: 
Before ➔ Diff Overlay ➔ After. 
You inspect the initial state, verify the differences, and examine the final result without a steep learning curve.

#### Split X Axis

![Image](./img/Screenshot_20260811-212354.png)


### Strict Alignment & Coordinate
IntegrityA critical design choice in STEP DIFF VIEW is how model coordinates are handled.
Many 3D viewers automatically re-center or auto-scale loaded models for aesthetic purposes. 
However, doing so ruins the relative position when comparing two manufacturing models. 

STEP DIFF VIEW strictly preserves the original CAD coordinate system and origin $(0,0,0)$, prioritizing engineering consistency over visual fluff.

### Beta Release & Feedback Request

This project is currently in early Beta. The main objective of this release is to test real-world STEP files directly in field environments.A built-in demo model is included, so you can test the 3D rendering and Diff Overlay functionality immediately upon installation without uploading your own files.

Target OS: Android 16 (Tested on Pixel 10 Pro Fold)  
Supported Formats: STEP (.step / .stp)  
Price: Free (Beta)   

If you test your own STEP models and have any feedback—such as file compatibility, rendering speed, or feature suggestions for field use—we would love to hear your thoughts on GitHub Issues!

### Disclaimer
STEP DIFF VIEW is a beta tool designed solely for visual verification of 3D data. 
It does not guarantee full accuracy or geometric precision. For critical manufacturing, machining, or engineering decisions, please always verify using certified CAD/CAM software and proper physical measurement tools. 
The developer assumes no liability for any losses resulting from the use of this software.