<!-- =========================================================================
     IMAGEPEEK PUBLIC WEBSITE
     Design by Tara Design Studio
========================================================================= -->

## 🎹 The Hero Section
![ImagePeek](https://raw.githubusercontent.com/barshasantak/imagepeek/main/ImagePeek_256.png)
<br>


See Beneath the Pixel.
The native, studio-grade image specification analyzer and side-by-side A-B diff comparator engineered exclusively for macOS.
       
     ┌──────────────────────────────────────────────────────────────────────────────────────────────────────┐
     │ 📂 Open Image... │ ⚖️ Compare... │ 💾 Export JSON │ 📋 Copy │ [Report Font: A- 100% A+ ↺] 🔍 Filter │
     ├──────────────────────────────────────────────────────────────────────────────────────────────────────┤
     │ RAW_MASTER.dng (Image A) │ [ ↔ 3 Mismatches ] │ WEB_OPTIMIZED.webp (Image B)                         │
     │ Format: Adobe DNG RAW (45.7 MP) │ Δ: -4240 × -2832 px │ Format: Google WebP (3.1 MP)                 │
     ├───────────────────────────────────────┴─────────────────────────┴────────────────────────────────────┤
     │ [IMAGE GEOMETRY & COLOR PROFILE]                                                                     │
     │ Dimensions 8256 × 5504 px [DIFF] 2048 × 1365 px                                                      │
     │ Megapixels 45.44 MP [DIFF] 2.80 MP (Δ: -42.64 MP)                                                    │
     │ Bit Depth 14-bit per channel [DIFF] 8-bit per channel                                                │
     │ Color Model RGB [MATCH] RGB                                                                          │
     │ ICC Color Profile Adobe RGB (1998) [DIFF] sRGB IEC61966-2.1                                          │
     │ Alpha / Transparency No [MATCH] No                                                                   │
     │ Compression (BPP) 16.20 bits/pixel [DIFF] 1.42 bits/pixel                                            │
     └──────────────────────────────────────────────────────────────────────────────────────────────────────┘


## 📖 The Product Story

### *Why we built ImagePeek*

In modern digital photography, graphic design, print publishing, and web development, managing visual assets is fraught with hidden complexities:

* **Color space stripping:** Did your export retain **Display P3** or **Adobe RGB (1998)** wide-gamuts, or was it silently clipped to generic sRGB?
* **Quantization & bit depth drops:** Did your 16-bit TIFF retain its smooth gradients, or did an automated pipeline compress it down to 8-bit with banding?
* **Metadata & rights leakage:** Are your **IPTC copyright notices**, **EXIF lens parameters**, and **GPS location tags** properly embedded or scrubbed for privacy?
* **Bloated tooling:** Opening Adobe Photoshop, Lightroom, or Bridge just to check an image's DPI, embedded ICC profile, or bits-per-pixel ratio takes 20+ seconds. macOS Preview's Inspector hides structural data, and terminal tools like `exiftool` disrupt your visual workflow.

We asked a simple question: **What if you had a blazing-fast, visually pristine Mac app that reveals the complete DNA of any image file in under 200 milliseconds?**

ImagePeek was created at **Tara Design Studio** to answer that need. Built from the ground up in 100% native Swift and SwiftUI, ImagePeek taps directly into Apple’s low-level `ImageIO`, `CoreGraphics`, and `CryptoKit` frameworks. No web runtimes. No full-bitmap RAM bloat. Just pure, instant visual intelligence.



## ⚡ Key Features

<table width="100%">
  <tr>
    <td width="50%" valign="top">
      <h3>🖼️ Deep Image Stream Demuxing</h3>
      <p>Inspect true dimensions, pixel densities (DPI), Megapixels, bit depths (8/10/12/14/16-bit), color models (RGB, CMYK, Lab, Grayscale), alpha channels, and animation frame counts without loading gigabytes of raw uncompressed bitmap arrays into memory.</p>
    </td>
    <td width="50%" valign="top">
      <h3>⚖️ Side-by-Side A-B Image Comparator</h3>
      <p>Compare two images simultaneously. ImagePeek aligns property keys and instantly highlights dimension scaling, megapixel deltas, color gamut shifts, and missing IPTC copyright tags.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>📐 Precision Dimension & Megapixel Deltas</h3>
      <p>Detect exact pixel scaling (<code>Δ: -4240 × -2832 px</code>) and megapixel differences (down to 0.01 MP) between camera RAW masters and compressed web deliverables.</p>
    </td>
    <td width="50%" valign="top">
      <h3>🎨 ICC Color Space & Profile Introspection</h3>
      <p>Instantly extract embedded ICC Color Profiles (Display P3, Adobe RGB 1998, ProPhoto RGB, Rec. 2020, sRGB) and verify true quantization depth per channel.</p>
    </td>
  </tr>
  <tr>
    <td width="50%" valign="top">
      <h3>📷 Comprehensive EXIF, GPS & IPTC Rights</h3>
      <p>Inspect optical camera data (Aperture, Shutter Speed, ISO, Lens Model, Focal Length), exact GPS coordinates with altitude, and IPTC creator/copyright attribution.</p>
    </td>
    <td width="50%" valign="top">
      <h3>🛡️ Hardware-Accelerated SHA-256</h3>
      <p>Stream massive multi-hundred-megabyte medium format RAW files or uncompressed TIFF archives in 64 KB binary chunks through Apple Silicon’s hardware cryptographic engine.</p>
    </td>
  </tr>
</table>



## 🎯 Universal Image Format Support

ImagePeek parses professional RAW camera masters, vector graphics, print containers, and next-gen web images:

| Category | Supported Formats & Containers |
| :--- | :--- |
| **Professional Camera RAW** | **Adobe DNG** (`.dng`), **Canon RAW** (`.cr2`, `.cr3`), **Nikon Electronic** (`.nef`), **Sony Alpha RAW** (`.arw`), **Generic RAW** (`.raw`) |
| **Next-Gen Web & Modern Formats** | **Apple HEIC / HEIF** (`.heic`, `.heif`), **Google WebP** (`.webp`), **AV1 Image File Format** (`.avif`) |
| **Standard Raster & Vectors** | **JPEG / JFIF** (`.jpg`, `.jpeg`), **PNG / APNG** (`.png`), **Scalable Vector Graphics** (`.svg`), **Windows Bitmap** (`.bmp`) |
| **Print, Prepress & Animation** | **Tagged Image File Format** (`.tiff`, `.tif` in 8/16/32-bit RGB & CMYK), **Graphics Interchange Format** (`.gif` with frame counts) |


## 🏆 Why ImagePeek is Different

Most image inspection utilities are either bloated photo managers or terminal scripts. ImagePeek is built exclusively for macOS:

<div style="overflow-x: auto; margin: 24px 0;">
  <table style="width: 100%; border-collapse: collapse; font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, sans-serif; font-size: 0.9rem; text-align: left; border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden;">
    <thead>
      <tr style="background: rgba(128,128,128,0.1); border-bottom: 2px solid rgba(128,128,128,0.25);">
        <th style="padding: 12px 16px; width: 30%;">Capability / Metric</th>
        <th style="padding: 12px 16px; width: 25%; background: rgba(0, 113, 227, 0.08); color: #0071e3; font-weight: 700;">ImagePeek</th>
        <th style="padding: 12px 16px; width: 25%;">Adobe Bridge / PS</th>
        <th style="padding: 12px 16px; width: 20%;">ExifTool (CLI)</th>
      </tr>
    </thead>
    <tbody>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15);">
        <td style="padding: 10px 16px; font-weight: 600;">Native Architecture</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ 100% Swift / CoreGraphics</td>
        <td style="padding: 10px 16px;">❌ Heavy Suite</td>
        <td style="padding: 10px 16px;">⚠️ Perl Script</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15); background: rgba(128,128,128,0.02);">
        <td style="padding: 10px 16px; font-weight: 600;">Launch Time</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">⚡ &lt; 10 ms (Instant)</td>
        <td style="padding: 10px 16px;">🐢 3,000+ ms</td>
        <td style="padding: 10px 16px;">⚡ Fast</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15);">
        <td style="padding: 10px 16px; font-weight: 600;">Memory Footprint</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">🪶 ~ 22 MB (No Bitmap Buffering)</td>
        <td style="padding: 10px 16px;">🐘 800 MB – 2 GB</td>
        <td style="padding: 10px 16px;">🪶 ~ 25 MB</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15); background: rgba(128,128,128,0.02);">
        <td style="padding: 10px 16px; font-weight: 600;">Visual A-B Diff Mode</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ Built-in Split-Table</td>
        <td style="padding: 10px 16px;">❌ None</td>
        <td style="padding: 10px 16px;">❌ Manual diff</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15);">
        <td style="padding: 10px 16px; font-weight: 600;">Dual-File Drag &amp; Drop</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ Instant Auto-Compare</td>
        <td style="padding: 10px 16px;">❌ Single file</td>
        <td style="padding: 10px 16px;">❌ No GUI</td>
      </tr>
      <tr style="border-bottom: 1px solid rgba(128,128,128,0.15); background: rgba(128,128,128,0.02);">
        <td style="padding: 10px 16px; font-weight: 600;">120Hz ProMotion UI</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ Liquid Smooth</td>
        <td style="padding: 10px 16px;">❌ UI Stutter</td>
        <td style="padding: 10px 16px;">❌ Terminal only</td>
      </tr>
      <tr>
        <td style="padding: 10px 16px; font-weight: 600;">Hardware SHA-256</td>
        <td style="padding: 10px 16px; background: rgba(0, 113, 227, 0.04); font-weight: 600;">✅ CryptoKit NEON Engine</td>
        <td style="padding: 10px 16px;">❌ Not included</td>
        <td style="padding: 10px 16px;">⚠️ Separate tool</td>
      </tr>
    </tbody>
  </table>
</div>


## ✨ User Experience Highlights

### 1. Dual-Drop Compare Mode
Select two image files in Finder (like your 100 MP Hasselblad TIFF master and your optimized web WebP render) and drag them together onto ImagePeek. The window instantly transitions into a **two-column comparative diff table**, highlighting mismatches in bold amber and identical parameters in calm green.

### 2. Zero RAM Bloat on Gigapixel & RAW Files
Thanks to stream-header demuxing via `ImageIO`, dropping a **500 MB 16-bit uncompressed TIFF** takes the exact same fraction of a second as opening a **50 KB thumbnail icon**.

### 3. Native Mac Ergonomics
* Full support for macOS Dark and Light modes.
* Universal keyboard shortcuts (`⌘O` to open, `⌘E` to export, `⌘C` to copy, `⌘+` to scale text, `⇧⌘L` to view logs).
* Multi-column search bar that filters image keys, color profiles, EXIF tags, and copyright data instantly as you type.



## 🚀 Elevate Your Digital Photography & Imaging Workflow

Stop guessing what is inside your image files. Verify color profiles, confirm bit depths, and validate copyright attribution with pixel-perfect precision.



## 💬 Help & Support

### Frequently Asked Questions

<p style="color: #6e6e73; font-size: 0.9rem; margin-bottom: 20px;">
  💡 <em>Click any question below to expand the answer.</em>
</p>

<div style="max-width: 840px; margin: 0 auto; display: flex; flex-direction: column; gap: 12px;">

  <!-- Question 1 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Does ImagePeek alter, strip, or recompress my images?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      No. ImagePeek operates strictly in <strong>read-only mode</strong>. It inspects metadata dictionaries and image stream headers without modifying a single pixel or byte of your files.
    </div>
  </details>

  <!-- Question 2 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Where are diagnostic logs stored?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      ImagePeek maintains rolling daily logs formatted as <code>imagepeek-YYYY-MM-DD.log</code>. You can reveal your log folder directly in Finder anytime by pressing <kbd style="background: rgba(128,128,128,0.15); padding: 2px 6px; border-radius: 4px; font-family: monospace;">⇧ + ⌘ + L</kbd> (or via <strong>Help → Show Logs in Finder</strong>).
    </div>
  </details>

  <!-- Question 3 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>Is ImagePeek private?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      Yes. ImagePeek is <strong>100% secure</strong>. It contains zero analytics, no telemetry, no tracking, and never makes unauthorized network connections.
    </div>
  </details>

  <!-- Question 4 -->
  <details style="border: 1px solid rgba(128,128,128,0.25); border-radius: 8px; overflow: hidden; background: rgba(128,128,128,0.02); transition: all 0.2s ease;">
    <summary style="padding: 14px 18px; font-weight: 600; cursor: pointer; display: flex; justify-content: space-between; align-items: center; user-select: none; font-size: 1rem;">
      <span>How do I report a bug or request a new image format?</span>
      <span style="font-size: 0.75rem; color: #0071e3; font-weight: 600; background: rgba(0,113,227,0.1); padding: 4px 10px; border-radius: 999px; white-space: nowrap; margin-left: 12px;">+ View Answer ▾</span>
    </summary>
    <div style="padding: 14px 18px 18px 18px; border-top: 1px solid rgba(128,128,128,0.15); color: #424245; font-size: 0.95rem; line-height: 1.6; background: rgba(128,128,128,0.01);">
      You can open an issue or start a discussion on our official <a href="https://github.com/santakd/ImagePeek/issues" style="color: #0071e3; text-decoration: underline; font-weight: 500;">GitHub Issues page</a>.
    </div>
  </details>

</div>


### Support

You can report any issues here: [https://github.com/barshasantak/imagepeek/issues](https://github.com/barshasantak/imagepeek/issues){:target="_blank"}

 <br>
 
 <hr>
   <small>© 2026 Santak Das, Tara Design Studio. All rights reserved.</small>
 <br>

