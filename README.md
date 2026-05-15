# Airwars-geo-image-editor-1.3

A web-based image annotation tool for creating and editing evidence files with rectangles, polygons, labels, and exact location markers.

## Features

- **Upload JPEG Images**: Upload and automatically resize images to 2100px width while maintaining aspect ratio
- **Dual Mode Support**: Satellite and Ground Level image modes with separate annotation layers
- **Rectangle Annotation**: Click and drag to draw rectangles with customizable labels and dash styles
- **Polygon Annotation**: Click to add points and create polygons, double-click to finish
- **Label Annotation**: Place letter labels on images
- **Exact Location Markers**: Add precise location markers with customizable text and glow effects
- **Red Annotations**: All shapes are drawn with 8px red (#ff0000) lines with no fill
- **Undo Polygon Points**: Right-click to remove the last point while drawing a polygon
- **Clear All**: Remove all annotations from the current image
- **Download Image**: Save the annotated image as a JPEG file
- **Download Edit File**: Export complete editable project files (.awe format) containing all annotations and metadata
- **Open File**: Import previously exported .awe files to continue editing

## How to Use

1. Open `index.html` in your web browser
2. Click "Upload Image" and select a JPEG file, or "Open File" to load a previously saved .awe project
3. The image will automatically resize to 2100px width

### Drawing Rectangles
- Click the **Rectangle** button to activate the tool
- Click and drag on the canvas to draw a rectangle
- Release to complete the rectangle
- Edit the label text and position in the edit panel

### Drawing Polygons
- Click the **Polygon** button to activate the tool
- Click on the canvas to add points
- Double-click to finish and save the polygon
- Right-click to undo the last point

### Adding Labels
- Click the **Label** button
- Click on the canvas to place a label
- Edit the letter in the edit panel

### Adding Exact Location Markers
- Click the **Exact Location** button
- Click on the canvas to place a marker
- Edit the text and adjust position in the edit panel
- Toggle glow effect with the **Glow On** button

### Switching Modes
- Use **Satellite Image Mode** and **Ground Level Image Mode** to annotate different views
- Each mode maintains separate annotations

### Saving Work
- **Download Image**: Saves the current view as a JPEG with all visible annotations
- **Download Edit File**: Saves a complete project file (.awe) containing:
  - Original image
  - All annotations for both modes
  - Current settings and preferences
  - Metadata for full reconstruction

### Loading Projects
- Click **Open File** and select a .awe file
- The project will be fully restored with all annotations, settings, and editability preserved

## Files

- `index.html` - Main HTML structure
- `styles.css` - Styling and layout
- `app.js` - Core functionality and canvas interactions

## Technical Details

- **Image Resizing**: Images are resized to 2100px width with automatic height calculation to maintain aspect ratio
- **Annotation Style**: All annotations use 8px stroke width with #ff0000 (red) color
- **No Filling**: Rectangles and polygons are drawn with stroke only, no fill
- **Download Format**: JPEG format with 95% quality for images, ZIP-based .awe format for projects
- **Project Format**: Structured JSON with extensible metadata for future annotation types
- **Dual Mode Storage**: Separate annotation arrays for satellite and ground modes
