# ARRWSApp


AR Recycling & Waste Sorting Assistant – Detailed Blueprint
1. Context of Use
    • Residents scan bin labels or packaging.
    • AR displays correct disposal method via animations.
    • Simple drag-and-drop interaction helps reinforce learning.

2. Use Cases
    1. UC1 – Identifying Correct Bin
        ◦ User scans a product label.
        ◦ AR highlights the correct recycling bin in 3D.
    2. UC2 – Learning Waste Types
        ◦ User scans a "Learning Card".
        ◦ AR shows different waste types with interactive sorting practice.
    3. UC3 – Gamified Sorting
        ◦ User drags 3D waste items to correct bins.
        ◦ App shows green/red indicator for correctness.

3. User Stories
    • US1: As a resident, I want to scan packaging so I can know which bin to use.
    • US2: As a child, I want to play a sorting game so I can learn recycling in a fun way.
    • US3: As a community educator, I want a visual guide for waste management campaigns.

4. Requirements
Functional
    • Detect image targets (product label or QR code).
    • Display 3D models of bins and waste items.
    • Allow drag-and-drop interaction.
    • Provide instant feedback (color change, sound).
Non-Functional
    • Load models in <1 second.
    • Maintain 30–60 FPS.
    • Run on mid-range smartphones (Android/iOS).

5. Design & Implementation Constraints
    • Use Unity XR + AR Foundation (cross-platform).
    • Use free 3D bin models (from Unity Asset Store or Sketchfab).
    • Lightweight textures to avoid lag.

6. Storyboard (Text Version)
    1. Launch Screen – "Start Recycling AR".
    2. Camera View – Instruction overlay: "Scan label or bin sticker."
    3. AR View –
        ◦ Correct bin glows green.
        ◦ Waste item appears in 3D.
    4. Interaction Screen – User drags item to bin → sound effect & score display.
    5. Completion Screen – "Great job! You sorted 5/5 items correctly."

7. Free Assets (Unity Asset Store / Sketchfab)
    • Recycling Bin Pack – Free stylized bins.
    • Plastic Bottle, Can, Glass, Paper Models – Low-poly free assets.
    • Audio Feedback – Free button click / success sounds.

8. Development Steps in Unity
    1. Create Unity 3D project, install AR Foundation + XR plugins.
    2. Set up AR Session & AR Session Origin with camera.
    3. Add AR Tracked Image Manager for labels/cards.
    4. Import 3D models (bins, items).
    5. Write C# scripts for:
        ◦ Object spawning when target is detected.
        ◦ Drag-and-drop interaction.
        ◦ Color change & score update.
    6. Build & test on mobile device.
