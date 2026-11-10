# AQJRO AAS Demo v1.0

**AQJRO Asset Standard — OpenUSD Production Pipeline Demonstration**

**Version:** 1.0  
**Release:** 2026  
**Author:** Sergey Borisovich Nam  
**Project:** AQJRO PROJECT  
**Copyright:** © 2026 Sergey Borisovich Nam. All Rights Reserved.

---

## 1. Overview

AQJRO AAS Demo v1.0 is a technical demonstration of the **AQJRO Asset Standard (AAS)** — a structured, modular asset production and assembly workflow built around Pixar OpenUSD.

The demo presents a production-oriented approach to organizing, composing, and reusing 3D assets within a structured USD environment.

It is based on a real production assembly developed for AQJRO PROJECT and demonstrates how individual components, geometry, materials, references, and assembly structures can work together as a unified scene.

The project is primarily designed for production and rendering with **Autodesk Maya and Arnold**.

Unreal Engine is additionally supported as a tested environment for loading and viewing the USD assembly.

This release is intended for technical evaluation, workflow demonstration, and exploration of the AAS approach.

## 2. Download the Demo

To download the complete AQJRO AAS Demo v1.0, including the actual USD assets, textures, and other Git LFS files, use **GitHub Desktop**.

### Download Instructions

1. Download and install [GitHub Desktop](https://desktop.github.com/).
2. Open the [AQJRO AAS Demo v1.0 repository](https://github.com/aqjro28-collab/AQJRO-AAS-Demo-v1.0).
3. In GitHub Desktop, select **File → Clone Repository**.
4. Open the **URL** tab.
5. Paste the repository URL:

   `https://github.com/aqjro28-collab/AQJRO-AAS-Demo-v1.0.git`

6. Choose a local directory where you want to store the demo.
7. Click Clone and wait until the repository and all Git LFS files have been downloaded.

GitHub Desktop supports Git LFS and retrieves the actual large files referenced by the repository.

After cloning, the complete demo package will be available in the selected local directory.

**Important — Git LFS**

The project uses Git Large File Storage (LFS) for USD assets, textures, and other binary resources.

The automatically generated GitHub **Source code (ZIP)** and **Source code (tar.gz)** archives may contain Git LFS pointer files instead of the actual assets.

For a complete download, use GitHub Desktop as described above.

## 3. Demo Contents

The demonstration includes a static assembly of the AQJRO Experimental Scientific Station and its associated production assets.

The main assembly is located in:

`Experimental_Scientific_Station/`

**Main USD file:**

`AQJRO_Station_Assembly_Demo_v1.0.usd`

The package contains the components and dependencies required by the main assembly, including:

- Modular station components.
- USD geometry and assembly layers.
- USD references and composition structures.
- Materials and texture resources.
- Structured asset organization.
- Reusable elements integrated into the station assembly.

The demo represents a static production assembly. It is not a complete animated project or an interactive game.

## 4. Verified Software Compatibility

The demo has been tested in the following software environments:

| Software | Tested Version | Result |
|---|---|---|
| Autodesk Maya | 2027.2 | Passed |
| Autodesk Maya | 2026.3 | Passed |
| Unreal Engine | 5.8.0 | Passed |

All three environments were tested successfully. The assembly worked as expected, with no errors reported during validation.

These results apply to the tested configurations and do not constitute a guarantee of compatibility with every other software version or configuration.

## 5. Getting Started

Before opening the demo:

1. Make sure the complete repository has been downloaded, including its Git LFS files.
2. Preserve the original directory structure.
3. Navigate to the `Experimental_Scientific_Station` directory.
4. Locate `AQJRO_Station_Assembly_Demo_v1.0.usd`.
5. Load the file as a USD Stage in your application.

**Main assembly path:**

`AQJRO AAS Demo v1.0/Experimental_Scientific_Station/AQJRO_Station_Assembly_Demo_v1.0.usd`

### Important — USD Display Purpose

The assembly uses different USD geometry representations (Purposes).

To display the intended production geometry in the application viewport, make sure the USD Stage is configured to display the **Render** purpose.

Do not use `Proxy` or `Default` as the active display representation when evaluating the intended production appearance of the assembly.

### 5.1 Autodesk Maya

The assembly must be loaded as a USD Stage.

1. Launch Autodesk Maya.
2. Open the USD Stage workflow.
3. Create or open a USD Stage.
4. Load `AQJRO_Station_Assembly_Demo_v1.0.usd` as the Stage's root layer.
5. In the USD Stage display settings, enable the **Render** purpose.
6. Make sure the viewport is not displaying the `Proxy` or `Default` representation.
7. Allow the USD composition, referenced assets, and materials to load.

Do not use the standard geometry import workflow. The assembly is designed to be opened and evaluated as a composed USD Stage.

**Rendering:** Autodesk Maya with Arnold is the primary intended production and rendering environment for this project.

### 5.2 Unreal Engine

Unreal Engine requires its USD-related plugins to be enabled.

1. Launch Unreal Engine 5.8.0.
2. Open the Plugins settings.
3. Enable the USD plugins required for USD Stage functionality.
4. Restart the editor if requested.
5. Open the USD Stage control window.
6. Load `AQJRO_Station_Assembly_Demo_v1.0.usd` as the assembly Stage.
7. In the USD Stage display settings, select the **Render** purpose.
8. Make sure the viewport is not displaying the `Proxy` or `Default` representation.
9. In the rendering settings, select **Unreal** instead of **MaterialX**.
10. Make sure these settings are applied in the USD Stage control window.
11. Allow the Stage and its referenced resources to load.

**Important — Material Display Settings**

For the intended material preview in Unreal Engine, use the **Unreal** rendering mode instead of **MaterialX**.

This setting uses USD Preview Surface materials for viewport visualization in Unreal Engine and provides the intended material preview for this demonstration.

The assembly must be loaded and inspected through the USD Stage workflow rather than imported as ordinary static geometry.

**Note:** Unreal Engine is included as a verified environment for loading and viewing the USD Stage. The primary production rendering environment of AQJRO remains Autodesk Maya with Arnold.

## 6. Rendering and Display

The AQJRO production pipeline is primarily designed around **Arnold Renderer** in Autodesk Maya.

Arnold is the primary rendering environment for evaluating the intended production appearance of the station assembly, including materials, shading, lighting, and final image quality.

The USD assembly also supports viewport inspection in Unreal Engine 5.8.0.

It is important to distinguish between USD geometry representation purposes and the rendering environment:

- **Render Purpose** — the production geometry representation intended for viewing the main assembly.
- **Proxy Purpose** — a simplified representation intended for lightweight scene display and other proxy workflows.
- **Default Purpose** — the default USD representation, which does not necessarily correspond to the intended production display.

For the intended visual result, use the **Render** representation in both Maya and Unreal Engine.

For production rendering, use **Arnold in Autodesk Maya**.

## 7. Working with OpenUSD

The demo uses a modular USD composition approach.

Depending on the asset and assembly level, the project may use:

- USD references for composing reusable assets.
- Separate geometry and look layers.
- Material assignments and shared material resources.
- USD Xforms and hierarchical scene organization.
- Variants and other USD composition features.

The assembly is built around reusable components rather than a single monolithic scene.

When inspecting or modifying the project, preserve the existing USD composition relationships and relative asset paths.

## 8. Portability

Portability is an important principle of the AAS production workflow.

The demo has been validated as a packaged assembly with its required dependencies.

For reliable operation:

- Preserve the original directory structure.
- Keep the relative locations of USD files and referenced resources unchanged.
- Do not rename or move individual dependency directories without updating the corresponding references.
- When transferring the demo to another computer, copy the complete package.
- Avoid replacing relative references with machine-specific absolute paths.

The demo should be treated as a complete, self-contained package rather than a collection of independent USD files.

## 9. Scope and Limitations

AAS Demo v1.0 is a demonstration release, not the complete AAS production standard or a commercial product.

Its purpose is to demonstrate the organization and composition of a real modular OpenUSD production assembly.

The package does not represent the complete AQJRO PROJECT production environment, all internal development tools, or future AAS functionality.

Additional features and documentation may be developed separately.

## 10. License and Usage

This release is provided as a non-commercial demonstration of the AQJRO Asset Standard and its production workflow.

All project-related intellectual property, including AQJRO PROJECT, its name, visual identity, designs, and associated original content, remains the property of its author unless explicitly stated otherwise.

Please refer to the accompanying `LICENSE` file for the applicable terms of use.

Commercial use, licensing, or other permissions must be obtained from the rights holder.

## 11. About AQJRO PROJECT

**AQJRO PROJECT** is an independent cinematic 3D universe and OpenUSD-based production ecosystem.

The project combines original intellectual property, modular 3D production, cinematic development, and proprietary technological infrastructure.

The AQJRO Asset Standard is developed as part of this ecosystem to establish a structured and reusable approach to asset creation, organization, and USD-based production.

---
## Official Project Website

**AQJRO PROJECT** is an independent cinematic 3D universe and OpenUSD-based production ecosystem.

Explore the official project website to learn more about the universe, visual development, original designs, and technological research.

**Website:** https://aqjro28.wixsite.com/aqjro-project

**GitHub:** https://github.com/aqjro28-collab/AQJRO-AAS-Demo-v1.0

**AQJRO PROJECT**  
Independent Cinematic 3D Universe & OpenUSD Production Pipeline

© 2026 Sergey Borisovich Nam. All Rights Reserved.
