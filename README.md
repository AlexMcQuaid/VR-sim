
# Functional Vision Simulator — Meta Quest 3

An interactive WebXR training prototype designed to help intervenors explore how different functional vision characteristics can affect everyday activities, environmental awareness, and object interaction.

Developed for training purposes at Sensity.

**Current live version:** v6  
**In development:** v7 — Mixed Reality (MR) feasibility testing

> This simulator is an educational approximation of functional vision, not a medical reconstruction of an individual's subjective visual experience.

## Project Goals

Develop a functional vision training tool with two complementary modes:

### 1. Virtual Reality (VR)

Intervenors explore a simulated environment with adjustable vision characteristics.

Training activities will eventually include:
- Locating and identifying objects.
- Exploring how distance affects visual access.
- Recognizing people and movement.
- Understanding the effects of glare and contrast.
- Practising scanning and environmental awareness.
- Exploring sighted-guide and Methods & Techniques scenarios.

### 2. Mixed Reality (MR)

Intervenors see their actual surroundings through Meta Quest 3 passthrough while experiencing simulated vision restrictions.

The goal is to allow intervenors to complete real-world tasks using their own hands and physical objects.

Potential activities include:
- Locating objects on a table.
- Sorting and identifying materials.
- Reading labels or identifying visual information.
- Completing everyday tasks with restricted vision.
- Comparing task performance with and without simulated restrictions.

**MR development is experimental.** The current browser-based prototype has not yet demonstrated working passthrough with the vision simulation applied.

## Current Features — v6

### Adjustable Vision Simulation

- **Useful viewing distance**
  - Adjustable from 0.3 m to 2.0 m.
  - Virtual objects progressively lose visibility beyond the selected distance.
  - Default distance: 0.5 m.

- **Peripheral vision restriction**
  - Adjustable from 20% to 100%.
  - Creates a restricted central viewing area with darkened peripheral regions.
  - Designed to remain aligned with the user's view during head movement.
  - Adjustable using desktop controls or the in-VR settings panel.

- **Blind-spot overlays**
  - Camera-relative visual obstructions.
  - Approximate areas of missing or reduced visual information.

- **Glare simulation**
  - Optional visual overlay demonstrating the potential effects of glare.

- **Normal/simulated comparison**
  - Switch between unrestricted and simulated viewing conditions.

These effects are training approximations rather than clinically calibrated representations of visual impairment.

### Interactive VR Environment

The current environment is a simple, low-detail room containing:

- A table.
- A virtual coffee mug.
- A communication card.
- A movable yellow cube.
- A moving person surrogate.
- A bright window.
- An interactive sound-button panel.

The environment is intentionally basic at this stage. More realistic room assets are planned.

### Hand Tracking and Interaction

The simulator supports Meta Quest hand tracking.

Current interactions include:
- Detecting tracked hands.
- Touching virtual buttons with an index fingertip.
- Pinching to pick up and move the virtual cube.
- Pinching to pick up and move the virtual mug.
- Adjusting simulation settings without leaving VR.

### In-VR Settings

The settings panel allows users to adjust:

- Useful viewing distance.
- Peripheral field restriction.
- Glare.
- Moving-person animation.
- Normal/simulated vision comparison.

The settings are synchronized with the browser-based controls.

## Mixed Reality Development — v7

Version 7 introduces an initial attempt to support mixed reality through WebXR.

The proposed implementation includes:
- An Enter AR option alongside Enter VR.
- Passthrough mode for viewing the real environment.
- Hiding the virtual room when entering MR.
- Retaining the vision overlays and settings.
- Preserving the existing VR functionality.

**Status:** Code prepared, but deployment has not been confirmed successful. MR functionality has not yet been verified on Meta Quest 3.

### Technical Challenges

Standard WebXR passthrough does not necessarily provide direct access to the camera image for processing.

This affects our ability to simulate:
- Adjustable blur and reduced visual acuity.
- Reduced contrast sensitivity.
- Realistic glare and light sensitivity.
- Distance-dependent visual limitations in the real environment.

Camera-image processing or a different application architecture may be required for advanced MR effects.

The immediate goal is to establish whether the existing browser-based simulator can display passthrough with a functioning peripheral-field restriction.

## Technology

- A-Frame 1.7.1
- WebXR
- JavaScript
- HTML/CSS
- Three.js (through A-Frame)
- GitHub Pages
- Meta Quest 3

The project is browser-based and does not currently require Unity or a native Quest application.

## Running the Simulator

### Meta Quest 3

1. Open the hosted GitHub Pages URL in Meta Quest Browser.
2. Select **Enter VR**.
3. Allow or enable hand tracking as required.
4. Locate the settings panel on the left.
5. Adjust the viewing distance and peripheral field.
6. Use your index fingertip to activate buttons.
7. Pinch near the virtual cube or mug to pick it up.
8. Compare simulated and normal viewing conditions.

Begin seated in a clear area.

### Desktop Browser

Open the hosted URL in a compatible desktop browser.

- Use the mouse to look around.
- Use WASD for movement.
- Adjust settings through the on-screen controls.

Desktop testing is useful for checking the interface and basic functionality.

Hand tracking, immersive rendering, and mixed reality must be tested on the headset.

### Hosting

The simulator runs from `index.html` and requires HTTPS for immersive WebXR functionality.

Current hosting:

**GitHub Pages — deployed from the `main` branch, root directory.**

No custom build process is required.

## Development Roadmap

### Completed or Working in v6

- [x] Browser-based VR prototype.
- [x] Adjustable useful viewing distance.
- [x] Blind-spot overlays.
- [x] Optional glare.
- [x] Moving person surrogate.
- [x] Normal/simulated comparison.
- [x] Quest hand tracking.
- [x] Interactive sound-button panel.
- [x] Pinch-to-grab virtual objects.
- [x] In-VR settings panel.
- [x] Adjustable peripheral field restriction.
- [x] Peripheral field controls available inside VR.

### Current Priority — Mixed Reality Feasibility

- [x] Prepare initial VR/MR mode implementation.
- [ ] Successfully deploy v7.
- [ ] Confirm Enter AR availability in Quest Browser.
- [ ] Confirm real-world passthrough displays correctly.
- [ ] Test peripheral field restriction over passthrough.
- [ ] Confirm overlay stability during head movement.
- [ ] Test a simple physical-object interaction.
- [ ] Confirm reliable return to normal vision.

### Planned Vision Features

- [ ] Adjustable blur and reduced visual acuity.
- [ ] Adjustable contrast sensitivity.
- [ ] More advanced glare and lighting effects.
- [ ] Configurable central vision loss and blind spots.
- [ ] Save and load functional vision profiles.
- [ ] Quick-select training presets.
- [ ] Explore separate left/right eye settings.
- [ ] Investigate real-world depth-dependent effects in MR.

### Planned Training Features

- [ ] More realistic VR environments.
- [ ] Everyday task-based training scenarios.
- [ ] Object-location and identification exercises.
- [ ] Scanning and environmental awareness activities.
- [ ] Sighted-guide training scenarios.
- [ ] Methods & Techniques training scenarios.
- [ ] Trainer-controlled simulation profiles.
- [ ] Task prompts and structured debrief questions.
- [ ] Opportunities to capture training feedback.

## Training and Safety Considerations

The simulator is intended to support understanding of functional vision and its impact on everyday tasks.

It does not reproduce the exact visual experience of a particular person and should not be treated as a diagnostic or clinical assessment tool.

Visual impairments are highly individualized. The same diagnosis may produce different functional consequences for different people.

When testing restricted vision:
- Begin seated in a controlled environment.
- Keep the surrounding area free of hazards.
- Avoid hot liquids, sharp objects, and unsafe physical tasks.
- Provide a reliable way to return to unrestricted viewing.
- Supervise activities where appropriate.

The goal is to develop practical understanding of visual access, environmental barriers, and effective support strategies.

## Development Approach

Development follows an incremental process:

1. Implement one manageable change.
2. Test the change in a desktop browser.
3. Test the change on Meta Quest 3.
4. Confirm existing features still work.
5. Document results and limitations.
6. Proceed to the next milestone.

Features are not considered complete until they have been tested successfully.

## Project Status

**v6:** Current working VR prototype.

**v7:** Initial mixed-reality implementation prepared; deployment and headset testing pending.

**Next milestone:** Confirm mixed-reality passthrough and peripheral-field simulation on Meta Quest 3.
