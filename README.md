# Frever URP Shader Library
Welcome to the Frever URP Shader Library! Frever is a mobile avatar and content creation platform designed for expressive storytelling through custom 3D characters. Videos created with Frever were shared externally and accumulated over **10+ billion views** across platforms.

This open-source release contains a Unity project/package structured to provide a collection of **shaders** adapted for Unity's Universal Render Pipeline (URP). These shaders were intended for use within systems like the **Frever App** to render environments and effects.

The project/package includes various shaders, potentially both **Shader Graph-based and hand-coded HLSL shaders**.

**Please Note:** This open-source release represents only a fraction of the shaders utilized within the complete Frever application. Many shaders developed for Frever could not be included in this open-source version due to licensing restrictions, third-party dependencies, or other proprietary considerations.

Examples of these shaders in use and materials utilizing them can be found in the example scene repositories:
- Party Room Scene: [https://github.com/FriendFactory/frever-open-setlocation-party-room](https://github.com/FriendFactory/frever-open-setlocation-party-room)
- Laboratory Scene: [https://github.com/FriendFactory/frever-open-setlocation-laboratory](https://github.com/FriendFactory/frever-open-setlocation-laboratory)
- Preppy Bedroom Scene: [https://github.com/FriendFactory/frever-open-setlocation-preppy-bedroom](https://github.com/FriendFactory/frever-open-setlocation-preppy-bedroom)
- Bohemian Bedroom Scene: [https://github.com/FriendFactory/frever-open-setlocation-bohemian-bedroom](https://github.com/FriendFactory/frever-open-setlocation-bohemian-bedroom)

These released shaders were primarily used to establish visual styles, material properties, special effects, and optimized rendering for character-driven content and storytelling on mobile devices.
---
### Dependencies
This shader library is designed to work with Unity's Universal Render Pipeline (URP). **Many of the shaders are standard URP shaders or variations thereof, so it is crucial to have the Universal Render Pipeline (URP) package installed in your project to ensure scenes render correctly and to avoid issues like materials appearing pink.**

### Unity Packages (Required)
The following Unity packages are required for this shader library to function correctly. Ensure they are included in your `manifest.json` or installed via the Unity Package Manager.

| Package Name (Unity ID)                 | Recommended Version (or later) |
|--------------------------------------|------------------------------------|
| com.unity.render-pipelines.universal | 14.0.9                             |
| com.unity.shadergraph                | 14.0.9                             |
| `[com.unity.visualeffectgraph]`      | `[Version]`                        | <!-- Add if VFX Graph shaders are specifically included in *this* library -->
| `[com.unity.modules.particlesystem]` | `[Version]`                        | <!-- Add if particle shaders are specifically included in *this* library -->

*(Note: Ensure your Unity version is compatible with the listed package versions, typically Unity 2022.3.x for URP/ShaderGraph 14.x dependencies.)*

### Optional Dependencies on Other Frever Packages
If this shader library builds upon or includes files from other Frever packages (e.g., a core URP package with basic includes), list them here. This is especially relevant if this package is *not* `com.friendfactory.urp` itself but depends on it.

| Package Name (Unity ID)               | Version | Source |
|---------------------------------------|---------|--------|
| `[com.friendfactory.urp]`             | `[1.0.0]` | GitHub | <!-- Example: if this library needs base URP utilities from another Frever package -->

---
## Instructions for Use

1.  **Clone the Repository (if a standalone project) or Install as a Package:**
    *   **For standalone exploration:**
        ```bash
        git clone [your-repository-url-for-this-shader-library]
        ```
        Then, open the cloned project folder with a compatible Unity Editor version (e.g., Unity 2022.3.x recommended).
    *   **As a package in an existing project (Recommended):**
        Add the package to your `Packages/manifest.json` file:
        ```json
        {
          "dependencies": {
            "[com.friendfactory.shaderlibrary.YOURSHADERLIBNAME]": "https://github.com/FriendFactory/[repository-name-for-this-shader-lib].git#[version_or_branch]",
            // ... other dependencies
          }
        }
        ```
        Replace `[com.friendfactory.shaderlibrary.YOURSHADERLIBNAME]` with the actual package name (e.g., `com.friendfactory.urp`, `com.friendfactory.shaderlibrarynature`) and `[repository-name-for-this-shader-lib]` with its repository name.
        Or install via the Unity Package Manager using "Add package from git URL...".

2.  **Ensure URP is Installed and Configured:** Before opening any scenes or using the shaders, verify that the Universal Render Pipeline (URP) package is installed in your Unity project (via the Package Manager) and that a URP Asset is assigned in your Project Settings (`Project Settings > Graphics > Scriptable Render Pipeline Settings`). This is crucial to avoid materials appearing pink or rendering incorrectly.

3.  **Resolve Package Dependencies:** Unity should attempt to resolve the packages listed in `Packages/manifest.json`. Check the console for any errors related to package resolution.

4.  **Find and Use Shaders:**
    *   Shaders will typically be located within the package's folder structure (e.g., `Packages/[Shader Library Name]/Runtime/Shaders/` or `Assets/[Shader Library Name]/Shaders/` if imported directly into Assets).
    *   Create a new Material in your project (`Right-click in Project window > Create > Material`).
    *   In the Inspector for your new Material, select the desired shader from the Shader dropdown menu. They will likely be found under a category like `Frever/[Shader Category]/[Shader Name]` or simply listed under URP if they don't have a custom menu path.
---
## License
This project is licensed under the [MIT License](LICENSE.md).

Please note that the Software may include references to “Frever” and/or “Ixia” and that such terms may be subject to trademark or other intellectual property rights, why it is recommended to remove any such references before distributing the Software.
---
## Support
This repository is provided as-is, with no active support or maintenance. For inquiries related to the open source project, please contact:

**admin@frever.com**
---
## Contributing
We welcome forks and exploration! While the platform is no longer maintained by the original team, we hope this shader library serves as a useful resource for:
-   Learning about shader development for Unity URP.
-   Understanding shader optimization for mobile applications.
-   A base for creating custom shaders and visual effects.

Please open issues or pull requests on individual repos if you want to share fixes or improvements.
