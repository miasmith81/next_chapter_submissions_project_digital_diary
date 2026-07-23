# Gemini Prompt - Correct Exact Image Size

**Date:** July 22, 2026  
**AI tool:** Gemini  
**Intended model:** Gemini 1.5 Flash  
**Status:** Prepared; result pending

## Complete Prompt

Resize the 12 existing images I provided. This is an image-resizing task only.

DO NOT generate replacement artwork.

DO NOT redesign, reinterpret, redraw, or change the images.

### Final Required Size

Every finished image must be exactly:

- Width: 1024 pixels
- Height: 1280 pixels
- Orientation: Portrait
- Aspect ratio: Exactly 4:5
- File format: PNG

The following sizes are not acceptable: 928 x 1152, 1024 x 1024, 1152 x 896, 1280 x 1024, or any size other than exactly 1024 x 1280.

### Required Resizing Method

Each current image is 928 x 1152. To preserve the complete artwork without distortion:

1. Begin with the original 928 x 1152 image.
2. Extend the canvas height to 1160 pixels.
3. Add exactly 4 pixels to the top and 4 pixels to the bottom.
4. Fill added pixels by naturally extending edge colors and artwork.
5. Do not add a visible border, solid strip, or transparent space.
6. Confirm the intermediate canvas is 928 x 1160, exactly 4:5.
7. Resize it to exactly 1024 x 1280.
8. Export as PNG.

Do not stretch 928 x 1152 directly to 1024 x 1280. Correct the canvas ratio first.

### Preserve the Artwork

Preserve subjects, composition, colors, painterly style, lighting, details, and the lower-right AI-generation watermark. The watermark is intentional disclosure.

Do not remove the watermark, add another mark, add text, crop meaningful content, change concepts, add or remove objects, combine images, create a collage, add a frame, or change format.

### Process All 12

1. `frame01.png` - Serenity
2. `frame02.png` - Peace
3. `frame03.png` - Love
4. `frame04.png` - Compassion
5. `frame05.png` - Understanding
6. `frame06.png` - Calm
7. `frame07.png` - Reflection
8. `frame08.png` - Safety
9. `frame09.png` - Hope
10. `frame10.png` - Comfort
11. `frame11.png` - Healing
12. `frame12.png` - Connection

If filenames cannot be assigned, preserve exact order so they can be renamed separately.

### Output and Verification

Return 12 separate downloadable PNGs, not a collage, PDF, contact sheet, description, or unchanged 928 x 1152 files.

Inspect actual downloaded properties and provide a verification table with image, filename, width, height, ratio, format, and result. Mark PASS only when actual properties are 1024 x 1280, 4:5, PNG.

If the platform cannot export the exact size, state:

“NEEDS REVISION: Gemini could not export the required exact 1024 x 1280 dimensions.”

Do not claim success for any other dimensions.
