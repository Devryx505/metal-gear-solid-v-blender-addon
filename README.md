# Metal Gear Solid V FMDL Import - export still wip

<p align="center">
  <img src="https://img.shields.io/badge/Blender-Community_Addon-F5792A?style=for-the-badge&logo=blender&logoColor=white" alt="Blender Version Compatibility"/>
  <img src="https://img.shields.io/badge/Addon_Version-v1.0.0_WIP-inactive?style=for-the-badge" alt="Addon Version"/>
</p>

---

### Overview
This Blender add-on provides a robust pipeline for importing Fox Engine FMDL model assets directly into your workspace. It handles all necessary spatial matrix recalculations and coordinate systems automatically, bridging the data differences between Fox Engine layout rules and standard Blender environments.

* **Import Status:** Production Ready
* **Export Status:** Experimental / Under Development

---

## Compatibility and System Matrix

| Attribute | Specification |
| :--- | :--- |
| **Supported Game Assets** | Metal Gear Solid V: The Phantom Pain / Ground Zeroes (`.fmdl`) |
| **Blender Version Target** | Blender 2.80 through Blender 4.0.0+ |
| **Data Preserved** | Polygonal Meshes, Armature Rigging, Custom Normals, UV Channels |

---

## Core Feature Set

<details>
<summary>Skeletal Rigging and Hierarchy Ingestion</summary>

* Rebuilds complete Fox Engine bone structures natively within a Blender Armature object.
* Restores naming conventions and relational links between parent and child transform segments.
* Optional boundary parsing enables automatic generation of bone-driven bounding volume matrices.
</details>

<details>
<summary>Geometric Mesh Processing</summary>

* Reads absolute vertex positions and maps spatial data points dynamically.
* Automatically processes the horizontal/vertical axis conversion required to flip coordinates out of the engine space.
* Preserves specialized custom vertex normal loops to maintain high-fidelity in-game shading profiles.
</details>

<details>
<summary>Channel and UV Mapping</summary>

* Reconstructs multiple concurrent UV map channels per mesh object layer.
* Maintains vertex weight associations across multi-influence vertex assignments.
</details>

---

## Installation Pipeline

1. Download the latest asset package from the Releases page as a compressed `.zip` file.
2. Launch Blender and navigate to Edit, then select Preferences.
3. Choose the Add-ons division and click the Install button situated along the top header.
4. Select the downloaded archive file and check the configuration box to initialize the module.

---

## Operation Instructions

1. Active the 3D Viewport sidebar panel by pressing the N key on your keyboard.
2. Locate the dedicated Import navigation menu tab.
3. Click the Import FMDL action item to open the local file explorer system.
4. Select your compiled `.fmdl` target file to initiate data processing into your scene context.

---

## Credits and Heritage
This utility was built on top of extensive community reverse-engineering data layers. Special recognition goes out to BobDoleOwndU for structural architecture reference points derived from the original development of the Unity model interpretation plugin.
