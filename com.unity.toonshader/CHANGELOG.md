# Changelog
## [0.7.0-preview] - 2022-03-20
### Updated:
* Renamed `Double Shade with Feather` to `Three Color Toon`.
* Renamed `Shading Grade map` to `Three Color Toon with Special Maps`.
* Shader version properties in all the render pipeline shaders.
* Updated installation.md.
* Replaced toggle buttons Off/Active UI to Unity standard toggle.
* Renamed `Basic Shader Settings` to `Shader Setting`.
* Renamed `Point Light High Cut Filter` to `Point Light Hight Light Filter`.
* Replaced some toggle buttons, such as `Emissive UV Coord`, `Specular Mode`, to dropdown menus
* Made everything in the inspector hidden when disabled to be shown but grayed out.
* Folder headers use Unity standard style in the inspector window when SRP core newer than 12 is not installed.
* Folder headers use SRP style in the inspector window when SRP core newer than 12 is installed.
* Renamed `【DX11 Phong Tessellation Settings】` to `Legacy Pipeline: Phong Tessellation Settings` as it works on Mac too.
* Renamed term, `Technique` to `Mode`.
* Renamed term, `Contribution` to `Effectiveness`.
* Renamed foldout name `Light Color Contribution` to `Scene Light Effectiveness Settings`
* Moved `Gi Intensity` and `Scene Light hi cut filter` to under it.
* Renamed `Scene  Hi-cut filter` to  `Light Intensity Limitter` .
* Renamed term, `High Color` to `Highlight`.
* Renamed `Settings for PointLights in ForwardAdd Pass` to `Point Light Settings`.
* Renamed `Stencil No.` to `Stencil Number`.
* Renamed `Unlit Intensity` to `Metaverse Light Intensity and `Buiilt-in light` settings are moved into `Metaverse Settings` folder in the inspector so that users can understand  setting them is not necessary for usual uses.The setting works only when no directional lights are on the scenes like some VRChat scenes.
* Renamed 'Basic Look Dev' to 'Shading Step and Feather Settings'
* `Advanced settings` in Outline folder are always shown.
### Added:
* Legacy: Compatibility with Single Pass Stereo Rendering.
* Legacy: Graphics Test 2022.2.
* Universal RP: Graphics Test 2022.2.
* HDRP: Graphics Test 2022.2.
### Removed:
* removed   `● Additional Settings` in the Inspector.
* Removed Simple UI.
* Removed Japanese and English manual link buttons.
* Removed Game Recommendation window and changed the default values of shader variables.
* Removed 【】in the Inspector window.
* Removed  ● in the Inspector window.
* Removed unnecessary labes in the inspector such as `System Shadows:`

### Fixed:
* Undo/Redo was not working on some items in the inspector window.
* `Point Light High Cut Filter` Side Effects. It just shows or hides the point lights' highlight.

## [0.6.1-preview] - 2022-02-24
### Fixed:
* typo in inspector.
* removed .sample.json under Samples~ folder
* Some unnecessary classes were public.

## [0.6.0-preview] - 2022-02-22
### Updated:
* Replaced test VM to use gtx1080
* Updated README.md
* Added LICENSE.md under the project folder.
* Shader version properties in all the render pipeline shaders.
### Fixed:
* Some unnecessary classes were public.
* URP: a depth output issue later then 10.0.x. (Thanks to riina)
* Typos in README.md
* promotion test issues.
* no .sample.json files under each render-pileline sample folder.

## [0.5.0-preview] - 2022-01-20
### Updated:
* Updated documentation and folder structure in order to make the package structure friendly to Unity official package.
* Tentatively deleted Japanese documentation before making the package ready for Unity standard translation system.
* HDRP: made UTS compatible with HDRP AOV. Capable of outputting Albedo, Normal and so on using AOV Image Sequence Recorder newer than 3.0.
* More effective and strict internal tests.
### Fixed:
* HDRP:reduced shader variants by disabling some debug pragmas.
* URP:UTS materials don't receive shadows when using newer than Unity 2021.1.
* Legacy:Unable to disable Outline.
* AutoRenderQueue is disabled when material inspector is unfocused.


### Known Issues:
* HDRP: When outputting AOV images, UTS Outline is also put into the images. In such cases, please disable OUTLINE in Material Inspectors.

## [0.4.1-preview] - 2021-10-20
### Added
* HDRP:Something similar to HDRP exposure compensation.
### Fixed:
* typo in documents.
* missing mono behaviors in sample scenes.
* HDRP:BoxLightAdjustment script. some flags are not updated properly when some checkboxes are clicked.
* HDRP:Shader compile errors when used with HDRP 12.1


## [0.4.0-preview] - 2021-10-13
### Added
* HDRP: Compatibility with Box Light, a spot light variation, as main lights.
* HDRP: BoxLightAdjustment mono-behavior
### Fixed:
* URP: Unstable SRP Compatibility. Thanks to tangx246.
* URP: Outline pass is not compatible with VR when  Single Pass Instanced rendering is chosen. Thanks to tangx246 again.
* URP: Some warnings.
### Updated:
* Documentation~/en/FeatureModel_en.md. Thanks to riina.
* Platforms in documentation.

## [0.3.2-preview] - 2021-09-28
### Added
* doc: HDRP: description for ray-trace shadow.
### Fixed
* HDRP: fix Gaps between self-shadow and ray-trace shadow.

## [0.3.1-preview] - 2021-09-27
* description is above.

## [0.3.0-preview] - 2021-09-16
* HDRP: Fixed weird steps when more than 3 point lights are in a scene.
* HDRP: Added Toon EV Adjustment per Model.
* HDRP: Compatible with Raytraced Hardshadow when DX12 is chosen as API.
* Legacy: Applied a fix for outline flicker in VR chat..
## [0.2.2-preview] - 2021-08-24
* Modified Toon EV Adjustment Curve inspector.
* Excluded unnecessary files from release zip.
* Improved folder structure in order not to cause long file name errors when included in other packages.
* Added documentation for Toon EV Adjustment Curve.
## [0.2.1-preview] - 2021-08-18
* HDRP: Fixed: Multiple instances of Toon EV adjustment curve can exist in one scene.

## [0.2.0-preview] - 2021-08-17
* HDRP: Toon EV adjustment curve as a Mono-behavior.
* Legacy, Universal and HDRP: Some texture samplers,such as  _MainTex,  _NormalMap, _1st_ShadeMap and  _2nd_ShadeMap, are shared by 1 sampler, sampler_MainTex, in order to avoid sampler number exceeding errors.
* Integrated Textures feature is removed from all the render pipeline versions instead of above.
* HDRP and URP are compatible with SRP Batcher.
* Legacy, Universal and HDRP: Added image comparison tests for Windows Vulkan API.
* HDRP: Added light probe compatibility.
* Added a material converter from Unity-chan Toon Shader newer than 2.0.7  to Unity Toon Shader. (Experimental)

## [0.1.0-preview] - 2021-07-07
* HDRP: Emission started to work.
* HDRP: Improved exposure.
* HDRP: Implemented tessellation to the outline pass.
* deleted ValidationConfig.json.

## [0.0.7-preview] - 2021-06-14
* Made samples installable.

## [0.0.6-preview] - 2021-06-04
* Modified documents

## [0.0.5-preview] - 2021-05-12
* Channel Mask rendering feature put the results into alpha channel.

## [0.0.4-preview] - 2021-05-09
* Universal RP shaders are compatible with SRP 12.

## [0.0.3-preview] - 2021-05-05
* Universal RP and HDRP shaders are compatible with SRP 10.
* HDRP shaders' DepthOnly path is replaced to DepthForwardOnly path.
* Internal tests are compatible with not only 2019.4 but also 2020.x now.

## [0.0.2-preview] - 2021-03-30
* Legacy shaders are integrated into two shaders.
* The number of textures is reduced experimental
* Added Clipping Matte feature for HDRP.
* Removed almost all the warnings when compiling shaders.
* Grafted graphics tests from Scriptable Render Pipelines.
* Reorganized documents.
* Reorganized repository folder structure.
* Added feature model list FeatureModel_en.md

## [0.0.1-preview] - 2021-03-11

* Reorganized Unity-chan/Universal Toon Shader as Unity Toon shader.

