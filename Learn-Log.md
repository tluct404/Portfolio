# Frontend Development Study Notes
**Date:** June 28, 2026

---

## 1. CSS Cascade & Specificity

The Cascade is the engine that determines which CSS rules apply when multiple styles conflict. When multiple rules target the same HTML element, **specificity** acts as a scoring system to determine the winner.

### The Specificity Hierarchy
1. **IDs (`#id`):** Highest priority. Targets a single unique element.
2. **Classes (`.class`):** Medium priority. Targets groups of elements.
3. **Tags / Elements (`div`, `p`):** Lowest priority. Targets all instances of an HTML tag.

$$\text{ID (\#id)} > \text{Class (.)} > \text{Tag Selectors}$$

---

## 2. The Box Model

Every HTML element is treated as a rectangular box. The box model dictates how the dimensions and spacing of these elements are calculated.



### Core Components
* **Content:** The actual text, image, or child elements inside the box.
* **Padding:** The transparent space *inside* the HTML element, surrounding the content.
* **Border:** A defined line that wraps around both the content and the padding.
* **Margin:** The transparent space *outside* the HTML element, used to separate it from neighboring elements.

### The Box-Sizing Reset
By default, padding and borders expand the total size of an element beyond its defined width and height. To make layouts predictable and easier to control, use the universal `border-box` reset. This forces the padding and border to be absorbed *inside* the declared width.

```css
*,
*::before,
*::after {
  box-sizing: border-box;
}
