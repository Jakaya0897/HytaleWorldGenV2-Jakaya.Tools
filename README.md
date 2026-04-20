# 🌍 HytaleWorldGenV2 – Jakaya Tools

A versatile, **non-destructive toolkit** designed to help you build, debug, and refine Hytale worlds.

Built to be **drop-in ready**, these tools can be added to existing worlds with minimal setup no need to rebuild your pipeline.

---

## ✨ Features

- 🔧 Non-destructive – safely layer onto existing worldgen
- ⚡ Quick integration – plug into your current setup
- 🧪 Debug-friendly – visualize and test world data easily
- 🧱 Modular design – use only what you need

---

## 🧰 Current Tools

### 🎨 Colour Heightmap

Visualise terrain height using colour mapping. Perfect for debugging terrain shaping and elevation logic.

![Heightmap Example](images/heightmap.png)

## 🚀 Usage

To use the heightmap tool, add an **Import Material Provider** node to your biome setup.

Set the provider to:

```json
Jakaya_Tools.Heightmap
```
---
## 🗺️ Contour Map (10m)

Visualise terrain using **10 metre contour lines**, making it easy to read elevation, slopes, and terrain structure at a glance.

Every **50 metres** is highlighted with a **thicker line** for improved readability, while the **water level is marked in blue** for quick reference.

### 🧪 Example

![Contour Map Example](images/contour10.png)

### 🚀 Usage

Add an **Import Material Provider** node to your biome setup and set it to:

```json
Jakaya_Tools.Contour10
```
---
## 🌋 Bedrock Foundation

Creates a **layered world foundation** designed to prevent void falls while adding a dramatic, stylised underground appearance.

This tool generates a structured base consisting of **bedrock, lava, and crust layers**, giving your world a strong visual identity beneath the surface.

It operates between **Y=0 and Y=10**, overriding all density maps and other materials within this range.  
Ensure it is placed **at the top of the material stack** so it applies correctly.

### 🧪 Example

![Bedrock Example](images/bedrock.png)

### 🚀 Usage

Add an **Import Material Provider** node to your biome setup and set it to:

```json
Jakaya_Tools.Bedrock
```
---
🏔️ Height Density Optimiser

Provides a fully commented height optimisation setup that creates a stable base for terrain generation.

This tool defines a clean surface cutoff and a height mask, ensuring terrain behaves predictably from deep underground up to near the world height limit.

It is designed to be reusable across projects, giving you a solid foundation to build hills, cliffs, and other terrain features on top of.

🧪 Example

![HeightDensity Example](images/HeightDensityOptimiser.png)

🚀 Usage
Copy and paste into your existing project. All above-ground density fields should be routed through this Mix node—see comments in the file for more details.
---
## 📦 Installation

### 🔽 Download

1. Click the green **`Code`** button at the top of this repository
2. Select **Download ZIP**
3. Extract the contents to a location of your choice



### 📁 Install into Hytale

Copy the **`Server`** folder from this repository into your existing Hytale mod project.

Your final folder structure should look like this:

```json
Your Mod>/Server/HytaleGenerator/Biomes/Jakaya_Tools/
```

