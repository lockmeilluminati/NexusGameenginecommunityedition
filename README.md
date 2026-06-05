# The Nexus Game Engine - Community Edition

**Developed by DoctorGraphene | A Section 9 Initiative**

The Nexus is a custom, lightweight 3D game engine and scene editor built from the ground up in C++ using Raylib. It features a native `.glb` and `.gltf` asset pipeline, a custom material mapping system, integrated AI pathfinding logic, and a dynamic animation state machine.

## Core Features
* **Master Asset Importer:** Drag-and-drop or browse to ingest `.glb` and `.gltf` files.
* **Smart Texture Extraction:** Automatically runs a Python script to extract and rescue textures embedded in binary GLB files.
* **Custom `.nxmat` Format:** Saves and resolves persistent material overrides using dynamic relative paths so assets can be shared across computers without breaking.
* **Animator & Timeline:** Sequence animations, create montages, and drive skeletal animations using a built-in state machine.
* **AI Pathfinding:** Interactive viewport tools to plot, snap, and loop navigational waypoints for characters.
* **Asset Browser & Prefabs:** Generates live thumbnails and saves configured characters as `.nxchar` prefabs.

---

## Prerequisites

To compile and run The Nexus on Windows, ensure you have the following installed and configured in your system `PATH`:

1. **C++ Compiler:** MinGW-w64 (GCC).
2. **Raylib:** The engine core framework.
3. **ImGui / rlImGui:** Included in the project for immediate-mode UI rendering.
4. **Python 3:** Required for the `nexus_smart_extractor.py` utility to run in the background during asset ingestion.

---

## How to Compile

Open your terminal (PowerShell or Command Prompt) in the root directory of the project. To compile the engine into a standalone executable, use the following exact build command to ensure all translation units, Windows dialogues, and C++17 standards are correctly linked:

```powershell
g++ main.cpp file_dialog.cpp nexus_3dviewportcontrols.cpp nexus_environment.cpp nexus_character.cpp nexus_texture_extractor.cpp nexus_timeline.cpp nexus_project.cpp nexus_asset_browser.cpp nexus_win32.cpp nexus_asset_scanner.cpp nexus_anim_selector.cpp nexus_waypoint.cpp nexus_prefab.cpp nexus_animator.cpp nexus_publisher.cpp nexus_player.cpp nexus_combat.cpp nexus_character_creator.cpp nexus_scene_manager.cpp nexus_manual_importer.cpp rlImGui.cpp imgui.cpp imgui_draw.cpp imgui_tables.cpp imgui_widgets.cpp -o nexus3d.exe -O2 -Wall -Wno-unused-variable -Wno-sign-compare -std=c++17 -I include -L lib -lraylib -lopengl32 -lgdi32 -lwinmm -lcomdlg32
