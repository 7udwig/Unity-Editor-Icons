# Unity Editor Icons

A fast, searchable browser for the **built-in editor icons of the Unity Editor** (2022.3, 6000.0, 6000.3 - about 2,800 to 3,400 icons each).
Pick a version, search, change the display size of all icons at once, open an icon to compare it at several sizes on a dark,
light or checkerboard background, and copy its name or the C# line that uses it.

* **Version selector** with *NEW* and *GONE IN x* badges and filters for both. Names are the same across 2022 and 6000, so they are compared over all versions.
* **Categories** are the folders inside the editor resources (e.g. *Type icons*, *UI Toolkit*, *Skin images*).
* **One click copies code**: `EditorGUIUtility.IconContent("name")` or `EditorGUIUtility.FindTexture("name")` (only for icons that `FindTexture` finds), plus a tint line for UI Toolkit and IMGUI.
* **Nothing is stored or sent** - no cookies, no local storage, no analytics, no external requests.
* Names without prefix are the light-theme icons (dark artwork), `d_` names the dark-theme icons. In the dark editor `IconContent` returns the `d_` version of a plain name if there is one.

## Where the data comes from

An editor script ran in the Unity Editor of each version (2022.3.62, 6000.0.85, 6000.3.26) and saved every icon that `EditorGUIUtility.IconContent` resolves, in the highest resolution found (`@2x`, `@4x`, `@8x`). 15 names the editor lists but `IconContent` cannot resolve (brush textures, emoji atlases, `PhysicMaterial Icon`) are not included. Release dates are those of the Unity release API.

## License

* The icons are (c) Unity Technologies and are shown only as a developer reference. They are not offered under an open license. If Unity asks for removal, they will be removed. See `LICENSE-UNITY-ICONS.txt`.
* The code of this site (everything else) is MIT licensed, see `LICENSE`.

This is an unofficial project, not affiliated with or endorsed by Unity Technologies. "Unity" is a trademark of Unity Technologies.
