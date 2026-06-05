The Nexus Game Engine - Community Edition

**Developed by DoctorGraphene | A Section 9 Initiative**

The Nexus is a custom, lightweight 3D game engine and scene editor built from the ground up in C++ using Raylib. It features a native .glb and .gltf asset pipeline, a custom material mapping system, integrated AI pathfinding logic, and a dynamic animation state machine.

## Core Features
* **Master Asset Importer:** Drag-and-drop or browse to ingest .glb and .gltf files into structured directories.
* **Smart Texture Extraction:** Runs automatic Python utility scripts in the background to safely extract embedded assets.
* **Custom .nxmat Format:** Saves and resolves persistent material overrides using dynamic relative paths so assets can move between machines seamlessly.
* **Animator & Timeline:** Sequence tracks, create custom animation montages, and drive skeletal frameworks.
* **AI Pathfinding:** Interactive viewport tools to map, snap, and loop navigational waypoints for characters.

---

## Prerequisites

To compile and run the engine on Windows systems, ensure the following are installed and added to your environmental PATH variables:
1. **C++ Compiler:** MinGW-w64 (GCC)
2. **Raylib Development Libraries:** Ensure you have the core headers/libraries located in your workspace paths.
3. **Python 3:** Required for the background texture processing utilities.

---

## How to Get Started

### 1. Clone the Repository
Open your terminal and run:
\`\`\`powershell
git clone https://github.com/lockmeilluminati/NexusGameenginecommunityedition.git
cd NexusGameenginecommunityedition
\`\`\`

### 2. Compile the Engine
Run the following explicit build command to cleanly stitch all translation units, open Windows common dialog structures, target optimization flags, and link the required system modules together via the C++17 standard:
\`\`\`powershell
g++ main.cpp file_dialog.cpp nexus_3dviewportcontrols.cpp nexus_environment.cpp nexus_character.cpp nexus_texture_extractor.cpp nexus_timeline.cpp nexus_project.cpp nexus_asset_browser.cpp nexus_win32.cpp nexus_asset_scanner.cpp nexus_anim_selector.cpp nexus_waypoint.cpp nexus_prefab.cpp nexus_animator.cpp nexus_publisher.cpp nexus_player.cpp nexus_combat.cpp nexus_character_creator.cpp nexus_scene_manager.cpp nexus_manual_importer.cpp rlImGui.cpp imgui.cpp imgui_draw.cpp imgui_tables.cpp imgui_widgets.cpp -o nexus3d.exe -O2 -Wall -Wno-unused-variable -Wno-sign-compare -std=c++17 -I include -L lib -lraylib -lopengl32 -lgdi32 -lwinmm -lcomdlg32
\`\`\`

### 3. Run the Game Engine
Launch your compiled standalone binary immediately via your interface:
\`\`\`powershell
.\\\nexus3d.exe
\`\`\`

---
*Section 9 Tactical Robotics & Software*" > README.md ; git add README.md ; git commit -m "Initialize formal build documentation for terminal operations" ; git push origin main
