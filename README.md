# RTSCamPro - Premium RTS Camera System

**RTSCamPro** is a modular, high-performance RTS-style camera system designed for Unreal Engine 5. It combines a C++ backend for performance and Blueprint subclasses for easy override and customization. Ideal for RTS, simulation, city builders, and tactical games.

---

## 🚀 Features Overview

| Feature                           | Description                                                                 |
|-----------------------------------|-----------------------------------------------------------------------------|
| Pan / Zoom / Tilt / Rotate       | Full camera movement control in 3D space                                    |
| GlideCam Movement                | Smoothed interpolation for cinematic camera movement                        |
| Enhanced Input Support           | Fully integrated with UE5's Enhanced Input system                           |
| Edge Scrolling                   | Mouse edge scrolling with customizable zone thickness                       |
| World Bounds                     | Prevent camera from leaving the playable area                               |
| Save + Load System               | Hotkey-based camera position saving (1–7) and restore support               |
| Zoom to Cursor                   | Zoom centers on mouse-over world point                                      |
| Rotation Clamping                | Prevent excessive rotation or tilting                                       |
| Multiplayer Compatible           | Client-side camera control works with replicated games                      |
| Blueprint Extendable             | All core classes exposed via Blueprint for customization                    |
| Rebindable Inputs                | Input actions are easy to extend or replace                                 |
| Settings Asset                   | Global camera behavior defined through a central settings data asset        |
| FOV Control                      | Dynamically adjustable field of view with limits                            |
| Clean Project Structure          | Organized folders, comments, and no unused assets                           |
| Game Ready                       | Drop-in functionality with minimal setup required                           |

---

## 🧰 Included Files
RTSCamPro/
├── Content/
│ └── RTSCamPro/
│ ├── Blueprints/
│ ├── Input/
│ ├── SaveSystem/
│ ├── UI/
│ └── Demo/
├── Config/
├── Plugins/
│ └── RTSCamPro/
│ ├── Source/
│ │ └── RTSCamPro/
│ │ ├── Public/
│ │ ├── Private/
│ │ └── RTSCamPro.build.cs
│ ├── Resources/
│ └── RTSCamPro.uplugin

---

## 🎮 Setup Instructions

1. Add the `RTSCamPro` plugin to your project under `/Plugins/RTSCamPro`.
2. Enable the plugin in your project settings.
3. Open the provided demo map to test functionality.
4. Set your GameMode to use `BP_RTSCamProPlayerController` and `BP_RTSCamProPawn`.
5. Ensure Enhanced Input is enabled in your project (`Project Settings → Input → Default Input System`).

---

## 🔧 Settings Overview

All major behaviors are controlled via `RTSCamProSettings` asset or exposed variables.

| Setting Name              | Description                                            |
|---------------------------|--------------------------------------------------------|
| `PanSpeed`                | Base speed of camera panning                           |
| `ZoomSpeed`               | Speed of zoom in/out motion                            |
| `TiltSpeed`               | Speed of pitch adjustments                             |
| `RotationSpeed`           | Yaw rotation speed                                     |
| `GlideSmoothing`          | Dampening factor for motion smoothing                  |
| `MinFOV` / `MaxFOV`       | Limits for zoom FOV                                    |
| `UseEdgeScrolling`        | Toggle for mouse-edge scroll movement                  |
| `EdgeScrollZoneSize`      | Pixels from screen edge that activate edge scrolling   |
| `UseWorldBounds`          | Enables movement limits based on world bounds          |
| `WorldBoundsMin/Max`      | Vector bounds for limiting movement                    |
| `EnableCameraSaves`       | Enables hotkey save/load of camera transforms          |
| `ShiftDownPanMultiplier`  | Multiplies pan speed when Shift is held                |

---

## 📘 Blueprint Classes

- `BP_RTSCamProPawn`: The camera actor with Spring Arm & Camera.
- `BP_RTSCamProPlayerController`: Handles input and movement logic.
- `RTSCamProSettings`: Centralized settings asset for designers.
- `BP_RTSCameraSaveSubsystem`: Blueprint-only save/load logic.

---

## ⚙️ C++ Classes

- `URTSCameraMovementLibrary`: Static Blueprint-callable function library for movement logic.
- `ARTSCamProPawn`: Native camera pawn with modular component layout.
- `ARTSCamProPlayerController`: Handles Enhanced Input binding and logic routing.

---

## 🔄 Input Actions (Enhanced Input)

| Action Name       | Description                        |
|-------------------|------------------------------------|
| `IA_Horizontal`   | Handles left/right panning         |
| `IA_Vertical`     | Handles forward/backward panning   |
| `IA_Zoom`         | Scroll zoom in/out                 |
| `IA_Tilt`         | Adjust pitch                       |
| `IA_Rotate`       | Adjust yaw                         |
| `IA_SavePosition` | Save current camera transform      |
| `IA_LoadPosition` | Load saved transform to active cam |

---

## 🧾 License

This product is sold under the Epic Games Fab EULA and includes no third-party content or dependencies.

---

## ❓ Support

For setup help, bug reports, or feature requests, please contact:

- **Email**: `Jobrogi@gmail.com`
- **Community Discord**: [[Ghillie Studios Discord]](https://discord.gg/6xmYHNKk)

---


