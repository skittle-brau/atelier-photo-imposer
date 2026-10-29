# atelier-photo-imposer
An imposition tool for ingesting photos, cropping, setting quantities, and imposing

## Usage

Open `index.html` in a browser, then add or drop a batch of photos onto the page. Everything runs locally in the browser; photos are never uploaded. The page loads pdf-lib from cdnjs, so it needs an internet connection.

1. Choose a print size (5 × 7 in by default) and a press sheet (SRA3 by default).
2. Set the number of copies of each photo in the tray on the right.
3. Click any print on the sheet, or a thumbnail in the tray, to adjust its crop.
4. Click **Download PDF**.

## Features

- **Print sizes:** 2.5×3.5, 3.5×5, 4×6, 5×7, 6×8, 8×10, 8×12, 11×14 in, 4×4 and 6×6 in squares, 9×13 to 20×30 cm, A6 to A4, or any custom size in inches or millimetres
- **Automatic orientation:** landscape photos get landscape prints and portrait photos portrait ones; prints are turned 90° on the sheet to fit their slot. You can force portrait or landscape for any photo.
- **Cropping:** prints are centre-cropped to fill by default. Per photo, drag the frame to move the crop, zoom in, rotate the photo in 90° steps, or switch to **Fit** for the whole photo with white borders. The crop editor shows the bleed band and the effective resolution (ppi).
- **Sheets:** A5 to A0, SRA4, SRA3, SRA2, B4, B3, Letter, Tabloid, 12×18 and 13×19 in, or a custom size, in portrait, landscape or best fit
- **Imposition:** automatic best fit, which can mix portrait and landscape slots when that fits more prints on the sheet (still cuttable on a guillotine), or a fixed number of columns × rows. Gutters between columns and rows, and separate top, bottom, left and right margins.
- **Quantities:** copies of each photo, a "set all" for the whole batch, and an option to fill empty slots on the last sheet with extra copies
- **Bleed:** 3 mm by default, taken from the photo itself. With a gutter of at least twice the bleed every print gets full bleed; smaller gutters trim the bleed between neighbours.
- **Marks:** crop marks, mark colour (K or registration) and a slug line
- **Guillotine cut chart:** every cut position measured from the sheet edges
- **High-quality PDF:** JPEGs are embedded byte for byte, with no recompression, and cropped by clipping. EXIF orientation, embedded ICC profiles and CMYK JPEGs are respected. PNGs are embedded losslessly. For very large batches, **Resample** saves each crop at a set resolution (300 ppi by default) for a much smaller file.
- **Resolution warnings** for photos that would print below 200 ppi
- **Saved setups:** stored in the browser

JPEG, PNG and WebP work everywhere. HEIC photos open in Safari; in other browsers, export them as JPEG first.
