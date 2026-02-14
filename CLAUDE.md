# Conexion - Life Memories Presentation

## Project Overview
A single-page HTML presentation that showcases personal life memories (failures and successes) tied to geographic locations around the world. The presentation combines three visual elements: a photo slideshow, narrative text, and an animated 3D globe.

## Architecture
- **Single file**: `index.html` — self-contained, no build tools or local dependencies
- **Libraries**: Globe.gl via CDN (unpkg.com) for 3D globe rendering
- **Language**: Vanilla HTML, CSS, and JavaScript only

## Layout
- **Left column (50% screen width)**:
  - Top half: Photo slideshow (one image, crossfade transitions)
  - Bottom half: Text panel (title, location, narrative, failure/success badge)
- **Right column (50% screen width)**:
  - 3D globe (Globe.gl) with smooth travel animation and zoom on slide change
- **Navigation**: Left/Right keyboard arrow keys, slide counter at bottom

## Images
- All images are in the `img/` folder (21 JPGs from personal photos)
- Each image maps to a slide with: title, location (lat/lng), narrative text, and type (success/failure)

## Slide Data Structure
```js
{
  img: "img/filename.jpg",
  title: "Slide Title",
  location: "City, Country",
  lat: Number,
  lng: Number,
  type: "success" | "failure",
  text: "Narrative text..."
}
```

## Key Technical Details
- Globe.gl `pointOfView()` method handles animated globe rotation and zoom
- CSS transitions for photo crossfade and text panel updates
- All slide data defined in a JS array at the top of the script section for easy editing
- Responsive design is not a priority — designed for desktop/laptop screens

## File Structure
```
conexion/
├── CLAUDE.md
├── index.html
└── img/
    └── *.jpg (21 photos)
```
