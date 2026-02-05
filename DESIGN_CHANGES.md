# Memetic Universe - Design Improvements

This document describes the visual design changes made to `index.html` for the webcomic prototype.

## Changes

### 1. Title Header

Added a `<header>` with the comic title "Memetic Universe", an "Issue 1" subtitle, and a horizontal divider. This gives readers immediate context when they land on the page instead of jumping straight into dialogue.

- Uses the **Bangers** display font for the title to evoke a comic book feel.
- Subtitle is italicized and muted for visual hierarchy.

### 2. Typography

Replaced the generic system font stack (`Segoe UI`) with **Comic Neue** from Google Fonts. Comic Neue is a clean, legible comic-style font that matches the hand-drawn art without looking gimmicky. The title uses **Bangers**, a bold display font designed for comic book headers.

- Speech box font size increased from `14px` to `15px`.
- Line height increased from `1.5` to `1.6` for better readability in dense text blocks.

### 3. Background

Changed the flat `#f0f0f0` background to a warmer `#e8e4df` tone with a subtle SVG noise texture overlay. This gives the page a slight paper-like quality that complements the sketched art style without being distracting.

### 4. Variable Panel Spacing (Pacing)

Added two utility classes for controlling vertical rhythm between panels:

- `.pace-tight` (20px margin) - used between panels that flow quickly, e.g. the announcer into MacArthur's introduction.
- `.pace-wide` (55px margin) - used after key story beats to create a dramatic pause, e.g. after MacArthur's long introduction and before the closing panel.

Default spacing is 35px (up from 30px).

### 5. Speech Bubble Tail Fix

Changed the tail CSS selectors from `.speech-box::before` to `.speech-box:first-child::before`. This means only the **first** speech box in a multi-box panel gets a directional tail pointing at the image. Previously, every speech box had a tail, which looked odd when boxes were stacked (like Frame 3 with two speech boxes).

### 6. Footer / Continuation Element

Added a `<footer>` with a divider line and "To Be Continued..." text. This signals to the reader that the story isn't over, rather than the page just ending abruptly after the last panel.

### 7. Responsive Layout

Added a `@media (max-width: 700px)` breakpoint that:

- Stacks panels vertically (image on top, text below) instead of side-by-side.
- Expands images to full width.
- Removes speech bubble tails (not meaningful in a stacked layout).
- Reduces body padding and title font size.
- Adjusts pacing classes for the narrower layout.

Also added `<meta name="viewport">` and `<meta charset="UTF-8">` to the `<head>` for proper mobile rendering.

### 8. Image Styling

Added a subtle `border: 1px solid rgba(0,0,0,0.06)` to panel images and slightly increased the box-shadow. This gives the art a more defined edge against the textured background.

## What Was Not Changed

- **Panel text content** - all dialogue is preserved exactly as written.
- **Image file references** - all `src` paths remain the same.
- **Alternating left/right layout pattern** - the existing layout logic is unchanged.
- **Frame 1** - no title/splash panel was added since `MU-1-1.png` was not referenced in the original and may not exist yet.
