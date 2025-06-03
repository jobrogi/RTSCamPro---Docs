RTSCamPro - Premium RTS Camera System Documentation
RTSCamPro is a modular, high-performance RTS-style camera system designed for Unreal Engine 5. It combines a C++ backend for performance and Blueprint subclasses for easy override and customization. Ideal for RTS, simulation, city builders, and tactical games.

###🚀 Features Overview
| Feature                    | Description                                                          |
| -------------------------- | -------------------------------------------------------------------- |
| Pan / Zoom / Tilt / Rotate | Full camera movement control in 3D space                             |
| GlideCam Movement          | Smoothed interpolation for cinematic camera movement                 |
| Enhanced Input Support     | Fully integrated with UE5's Enhanced Input system                    |
| Edge Scrolling             | Mouse edge scrolling with customizable zone thickness                |
| World Bounds               | Prevent camera from leaving the playable area                        |
| Save + Load System         | Hotkey-based camera position saving (1–7) and restore support        |
| Zoom to Cursor             | Zoom centers on mouse-over world point                               |
| Rotation Clamping          | Prevent excessive rotation or tilting                                |
| Multiplayer Compatible     | Client-side camera control works with replicated games               |
| Blueprint Extendable       | All core classes exposed via Blueprint for customization             |
| Rebindable Inputs          | Input actions are easy to extend or replace                          |
| Settings Asset             | Global camera behavior defined through a central settings data asset |
| FOV Control                | Dynamically adjustable field of view with limits                     |
| Clean Project Structure    | Organized folders, comments, and no unused assets                    |
| Game Ready                 | Drop-in functionality with minimal setup required                    |

### 🧰 Included Files


RTSCamPro/
├── Content/
│   └── RTSCamPro/
│       ├── Blueprints/
│       ├── Input/
│       ├── SaveSystem/
│       ├── UI/
│       └── Demo/
├── Config/
├── Plugins/
│   └── RTSCamPro/
│       ├── Source/
│       │   └── RTSCamPro/
│       │       ├── Public/
│       │       ├── Private/
│       │       └── RTSCamPro.build.cs
│       ├── Resources/
│       └── RTSCamPro.uplugin

###🎮 Setup Instructions
Add the RTSCamPro plugin to your project under /Plugins/RTSCamPro.

Enable the plugin in your project settings.

Open the provided demo map to test functionality.

Set your GameMode to use BP_RTSCamProPlayerController and BP_RTSCamProPawn.

Ensure Enhanced Input is enabled in your project (Project Settings → Input → Default Input System).

