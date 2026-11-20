
# AroVertexMaker

A browser-based vertex editor for creating 2D and 3D triangle-based shapes, assigning colors, and preparing vertex data for OpenGL projects.

**Live Website:** https://arnob230.github.io/AroVertex/

## Features

- **2D and 3D Modes:** Work with 2D and 3D vertex positions.
- **Interactive Vertex Placement:** Click empty space to add a vertex and click an existing vertex to reuse it in the next triangle.
- **Vertex Editing:** Drag vertices to reposition them.
- **Triangle Selection:** Use `Ctrl` + click to select a triangle.
- **Grid Snapping:** Snap vertices to the grid, with an option to bypass snapping using `Alt`.
- **Shape Tools:** Choose a primitive, edit the index list, and build or clear shapes.
- **Per-Triangle Colors:** Choose colors for new triangles, paint selected triangles, paint all triangles, or generate random pastel colors.
- **Vertex Table:** Inspect vertex coordinates and usage.
- **Import and Export:** Import vertex data and export code arrays for graphics projects.
- **Editing Controls:** Undo, redo, zoom, fit view, and example shape.
- **Copy Generated Code:** Copy generated code directly from the export panel.

## How to Use

1. Open the [AroVertexMaker Website](https://arnob230.github.io/AroVertex/).
2. Choose **2D** or **3D** mode.
3. In the **Build** panel, place vertices on the workspace.
4. Create triangles by adding or reusing vertices.
5. Use the **Colors** panel to set or change triangle colors.
6. Check the **Vertices** panel to review vertex coordinates and usage.
7. Open the **Code** panel to import data or configure export options.
8. Choose the required export format and color/layout options, then select **Copy Code**.

## Mouse and Keyboard Controls

| Action | Control |
|---|---|
| Add a vertex | Click an empty area |
| Reuse a vertex in the next triangle | Click an existing vertex |
| Add a vertex without using it in the next triangle | `Shift` + click |
| Select a triangle | `Ctrl` + click |
| Move a vertex | Drag a vertex |
| Pan the workspace | Drag empty space |
| Zoom | Scroll |
| Delete an item | Right-click or press `Delete` |
| Temporarily skip snapping | Hold `Alt` |

## Color Input

Colors can be entered in these formats:

- Normalized RGB values from `0` to `1`, for example: `0.73, 0.56, 0.79`
- RGB channel values above `1` are interpreted on a `0`–`255` scale.
- Hex color values, for example: `#rrggbb`

## Import and Export Notes

- The import panel supports choosing the number of values per vertex.
- **Import and Replace** replaces the current imported data; **Append** adds data to the existing data.
- Blank lines between groups are preserved during import.
- A second array with the same length can be interpreted as per-vertex colors.
- Indexed export requires **Colors = None**, because one shared vertex may belong to triangles with different colors.

Check the export panel's available options for the exact output format, color mode, layout, component count, and decimal precision supported by the current version.

## Project Structure

```text
AroVertex/
└── index.html    # Application markup, styles, and JavaScript
```

The current repository is a single-page static web application. The interface, styling, and application logic are contained in `index.html`.

## Run Locally

No build step is required.

1. Download or clone this repository.
2. Open `index.html` in a modern web browser.

You can also serve the folder with any simple local static web server if you prefer.

## Deploy with GitHub Pages

This project is hosted using GitHub Pages.

1. Push `index.html` to the repository's `main` branch.
2. Open **Settings → Pages** in the GitHub repository.
3. Under **Build and Deployment**, choose **Deploy from a branch**.
4. Select branch `main` and folder `/(root)`.
5. Save and wait for GitHub Pages to finish publishing.

**Live Website:**

https://arnob230.github.io/AroVertex/

## Technologies

- HTML
- CSS
- JavaScript
- HTML Canvas / Browser APIs

## Repository

https://github.com/arnob230/AroVertex

---

Made as a lightweight browser tool for creating vertex-based shapes and preparing graphics data.
