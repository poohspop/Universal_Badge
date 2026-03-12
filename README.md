# Universal Badge Generator

The Universal Badge Generator allows event attendees to create custom social media graphics. It uses chroma key logic to process templates and insert user photos.

---

## Technical Requirements

The system identifies a specific green shade to create transparent windows for headshots. Maintain these color standards in your template design.

| Property | Value |
|----------|-------|
| Hexadecimal (HEX) | `#00b140` |
| Red Green Blue (RGB) | `0, 177, 64` |

---

## Template Graphic Specifications

High-quality output depends on the source file. Follow these constraints for the `template.png` file.

### Dimensions

| Setting | Value |
|---------|-------|
| Minimum | 800 x 800 pixels |
| Recommended | 1080 x 1080 pixels |
| Maximum | 2000 x 2000 pixels |

### File Properties

| Property | Value |
|----------|-------|
| Format | Portable Network Graphics (PNG) |
| Aspect Ratio | 1:1 (Square) |
| Resolution | 72 Dots Per Inch (DPI) |
| File Size | Under 2 Megabytes (MB) |

### Design Guidelines

- Fill photo cutout areas with solid color `#00b140`.
- Disable anti-aliasing on the edges of green shapes to ensure sharp cutouts.
- Do not use chroma key green in logos, text, or border elements.
- Use a flattened image. The code generates transparency during processing.

---

## Project Structure

Place these files in the same web server directory:

- `index.html` — Core application logic and user interface.
- `template.png` — Event-specific graphic.

The application expects these exact file names.

---

## Deployment Instructions

1. Upload `index.html` to your server.
2. Place your prepared `template.png` in the same folder.
3. Navigate to the URL on a mobile device to verify the template loads correctly.

---

## User Workflow

1. Open the event badge URL.
2. Select **Select Headshot** to upload a photo.
3. Adjust the image position using the **Zoom** and **Rotate** sliders.
4. Drag the photo within the preview window for precise alignment.
5. Click **Download Badge**.
6. On mobile, choose **Save Image** from the sharing menu to store the file in the device photo library.

---

## Troubleshooting

| Issue | Solution |
|-------|----------|
| Photo not visible | Confirm the template uses the exact RGB values listed above. |
| Performance lag | Reduce template dimensions if the browser experiences slowness. |
| Loading errors | Check Cross-Origin Resource Sharing (CORS) settings if assets reside on a different domain. |
