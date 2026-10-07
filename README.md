# Functional Vision Simulation — Quest Prototype v1

This is a training prototype, not a medical reconstruction of subjective vision.

## What it currently demonstrates
- A simple room-scale scene.
- An adjustable approximate "useful viewing distance" (default 0.5 m).
- Objects progressively becoming less visually useful beyond that distance.
- Irregular blind-spot overlays as a teaching approximation.
- Optional glare.
- A moving person surrogate to demonstrate tracking difficulty.
- Normal/simulated comparison.

## Important limitation
The person's left eye is believed to have severe optic nerve damage with perhaps light perception only.
This first WebXR prototype does NOT yet render a different image to each eye. It instead emphasizes the
functional consequences we can defend from the information available. A later build can use a custom
stereo rendering/shader pipeline for a more literal monocular effect.

## Fastest way to use it on Meta Quest
WebXR production pages need HTTPS.

1. Put `index.html` on any static HTTPS host.
2. Open that HTTPS URL in Meta Quest Browser.
3. Select the VR/Enter VR control in the scene.
4. Start seated or standing in a clear play area.
5. Use the normal/simulation comparison and try approaching the mug/table.

GitHub Pages, Vercel, or another HTTPS static host can serve this one-file prototype.

## Desktop test
Open the hosted page in a desktop browser. You can look around with the mouse and use WASD.
The actual immersive mode must be tested on the headset.

## Next iteration
After confirming this opens correctly on the Quest:
- proper per-eye rendering for left-eye light-perception-only approximation;
- controller-accessible in-VR menu;
- task prompts ("Find the mug", "Who entered?", etc.);
- better room assets;
- contrast and lighting scenarios;
- scoring/debrief prompts.
