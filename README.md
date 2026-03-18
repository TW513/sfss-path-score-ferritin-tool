# SFSS Path-Informed Score and Ferritin AUC Calculator

This repository provides simple web-based research calculators for:

- Path-informed CR-SFSS association score
- Ferritin AUC from postoperative day 0 to postoperative day 7 (AUC0–7)

## Purpose

These tools were developed to support reproducible calculation and visualization of exploratory findings from perioperative data in adult living donor liver transplantation.

**Research use only.** These tools are intended to support calculation, visualization, and discussion of exploratory findings. They are not calibrated probability tools and are not intended for clinical decision-making.

## Path-informed CR-SFSS association score

The score is calculated as the weighted linear combination of z-standardized representative variables derived from the mediation-style path framework.

### Formula

Score =

`1.600243 × z(MELD)`
`− 0.657845 × z(Hemoglobin)`
`− 0.599321 × z(Total protein)`
`+ 1.104418 × z(Donor preAST)`
`+ 1.493167 × z(Bleeding mL/kg)`

Where `z(X) = (X − mean) / SD`.

### Standardization parameters

| Variable | Mean | SD |
|---|---:|---:|
| MELD | 15.5977 | 5.6522 |
| Hemoglobin | 9.0302 | 1.7939 |
| Total protein | 5.5884 | 0.7921 |
| Donor preAST | 17.8721 | 4.7917 |
| Bleeding mL/kg | 143.2174 | 152.0901 |

## Ferritin AUC0–7

Ferritin AUC0–7 is calculated using the trapezoidal rule based on ferritin values at:

- Day 0
- POD1
- POD2
- POD3
- POD5
- POD7

Missing intermediate points are linearly interpolated. Missing boundary points are filled using the nearest available value.

## Suggested repository structure

- `index.html` — static web calculator for GitHub Pages
- `README.md` — repository overview and calculation details

## Suggested citation sentence for manuscript or supplement

For reproducibility, web-based calculation tools for the path-informed CR-SFSS association score and ferritin AUC0–7 are provided in the Supplementary Materials.
