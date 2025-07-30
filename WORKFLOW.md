# PixInsight Workflow – Helix Nebula by Phillip Comer

This document outlines the full manual PixInsight processing flow used on my Helix Nebula image. No AI filters or upscaling were used — this is real work, pixel by pixel.

---

## 📌 Original File
- Source: Seestar S50 stacked image
- Format: Native JPEG (exported to TIFF for processing)

---

## 🧰 Step-by-Step Processing

### 1. Background Neutralization
- Tool: `BackgroundNeutralization`
- Targeted uneven lighting and color cast
- Reference patch drawn from clean dark region

---

### 2. Dynamic Background Extraction (DBE)
- Tool: `DynamicBackgroundExtraction`
- Custom sample points
- Correction method: Subtraction
- Sample radius: 15 px
- Tolerance: 0.5

---

### 3. EZ Denoise
- Tool: `EZ Processing Suite > EZ Denoise`
- Mild preset to retain detail
- Noise reduction masked to nebula and background
- Stars preserved with star mask

---

### 4. Histogram Transformation
- Tool: `HistogramTransformation`
- Shadows clipped slightly above black point
- Midtones stretched to reveal nebular gas

---

### 5. Curves Transformation
- Tool: `CurvesTransformation`
- RGB-K: Added contrast S-curve
- Blue and Red channels boosted separately
- Highlight compression to preserve stars

---

### 6. Star Reduction (optional)
- Tool: `MorphologicalTransformation`
- Star mask applied
- Method: Dilation + erosion
- Softened stars without removing them

---

### 7. Final Annotation (Post-process)
- “Captured by Phillip Comer” added manually in Photoshop
- No other artificial edits used

---

## 🧪 Notes

- All edits were performed using PixInsight 1.8 on local hardware
- No AI used to modify or invent image features
- Resolution and framing preserved from original capture

---

© Phillip Comer, 2025  
Crow Hill Observatory – ComerConsults
