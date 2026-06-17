---
name: AuditTile Mini
colors:
  surface: '#f7f9fb'
  surface-dim: '#d8dadc'
  surface-bright: '#f7f9fb'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#f2f4f6'
  surface-container: '#eceef0'
  surface-container-high: '#e6e8ea'
  surface-container-highest: '#e0e3e5'
  on-surface: '#191c1e'
  on-surface-variant: '#434655'
  inverse-surface: '#2d3133'
  inverse-on-surface: '#eff1f3'
  outline: '#737686'
  outline-variant: '#c3c6d7'
  surface-tint: '#0053db'
  primary: '#004ac6'
  on-primary: '#ffffff'
  primary-container: '#2563eb'
  on-primary-container: '#eeefff'
  inverse-primary: '#b4c5ff'
  secondary: '#515f74'
  on-secondary: '#ffffff'
  secondary-container: '#d5e3fc'
  on-secondary-container: '#57657a'
  tertiary: '#943700'
  on-tertiary: '#ffffff'
  tertiary-container: '#bc4800'
  on-tertiary-container: '#ffede6'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dbe1ff'
  primary-fixed-dim: '#b4c5ff'
  on-primary-fixed: '#00174b'
  on-primary-fixed-variant: '#003ea8'
  secondary-fixed: '#d5e3fc'
  secondary-fixed-dim: '#b9c7df'
  on-secondary-fixed: '#0d1c2e'
  on-secondary-fixed-variant: '#3a485b'
  tertiary-fixed: '#ffdbcd'
  tertiary-fixed-dim: '#ffb596'
  on-tertiary-fixed: '#360f00'
  on-tertiary-fixed-variant: '#7d2d00'
  background: '#f7f9fb'
  on-background: '#191c1e'
  surface-variant: '#e0e3e5'
typography:
  headline-lg:
    fontFamily: Inter
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
    letterSpacing: -0.02em
  headline-md:
    fontFamily: Inter
    fontSize: 18px
    fontWeight: '600'
    lineHeight: 24px
    letterSpacing: -0.01em
  body-md:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '400'
    lineHeight: 20px
  body-sm:
    fontFamily: Inter
    fontSize: 13px
    fontWeight: '400'
    lineHeight: 18px
  label-caps:
    fontFamily: Inter
    fontSize: 11px
    fontWeight: '700'
    lineHeight: 16px
    letterSpacing: 0.05em
  data-tabular:
    fontFamily: Inter
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  container-margin: 24px
  gutter: 16px
  cell-padding-v: 8px
  cell-padding-h: 12px
  stack-sm: 4px
  stack-md: 12px
  stack-lg: 24px
---

## Brand & Style

The design system is engineered for high-utility operational environments where information density must coexist with visual "calm." The brand personality is clinical, precise, and objective. It avoids emotional flourish in favor of functional clarity, ensuring that auditors and operators can monitor complex datasets without cognitive fatigue.

The design style is **Corporate / Modern** with a lean toward **Minimalism**. It prioritizes a "content-first" architecture where the UI chrome recedes, using subtle borders and a structured grid to organize information. There are no gradients, shadows are replaced by tonal containment, and motion is restricted to functional transitions (e.g., status changes or data loading).

## Colors

The palette is anchored by a vast range of neutral grays to establish a clear information hierarchy without over-stimulating the user. 

- **Primary Action:** A functional Blue (#2563EB) is used exclusively for interactive elements and primary call-to-actions.
- **Surface Tones:** Backgrounds use a very light cool gray (#F8FAFC) to differentiate from pure white (#FFFFFF) card containers.
- **Semantic Status:** Success Green, Error Red, and Warning Amber are used with high intentionality. These colors should only appear to signal a state change or a metric outlier, never for decorative purposes.
- **Contrast:** High-contrast text (#0F172A) is used for headings, while secondary metadata uses a medium slate (#64748B) to reduce visual noise.

## Typography

This design system utilizes **Inter** for its exceptional legibility and comprehensive OpenType features. 

- **Tabular Figures:** For all metrics, tables, and numeric values, the `tnum` (tabular numbers) and `lnum` (lining numbers) CSS properties must be enabled to ensure columns of figures align perfectly for easy visual scanning.
- **Scale:** The scale is intentionally tight, ranging from 11px to 24px. Larger sizes are avoided to maintain high information density.
- **Hierarchy:** Weight is used more frequently than size to denote importance. Use `Semibold (600)` for section headers and `Medium (500)` for interactive labels or primary data points.

## Layout & Spacing

The layout follows a **Fluid Grid** model with strict 4px increments. While the container expands to fit the browser width, individual "Metric Tiles" and "Data Tables" utilize fixed internal padding to maintain a dense but readable appearance.

- **Grid:** A 12-column grid is used for dashboard layouts. On desktop, sidebars are fixed at 240px, while the main content area remains fluid.
- **Density:** Table rows are compact, utilizing a "Short" height (32px - 36px) to maximize the amount of visible data above the fold.
- **Breakpoints:** 
  - Mobile (< 640px): Single column, full-width tiles.
  - Tablet (640px - 1024px): 2-column tile layout.
  - Desktop (> 1024px): Full 12-column availability.

## Elevation & Depth

This design system avoids heavy drop shadows, opting for **Tonal Layers** and **Low-Contrast Outlines** to define hierarchy.

- **Base Layer:** The application background is #F8FAFC.
- **Surface Layer:** Cards and containers are #FFFFFF with a 1px border (#E2E8F0).
- **Interactive Elevation:** Elements do not "lift" on hover. Instead, they utilize subtle background shifts (e.g., a row highlight shifting to #F1F5F9) or border-color changes to the primary blue.
- **Modals:** Only global overlays (modals) may use a soft, 15% opacity neutral shadow to provide focus and separate the element from the primary data grid.

## Shapes

The shape language is **Soft** but disciplined. 

- **Standard Radius:** All buttons, input fields, and tiles use a 0.25rem (4px) radius. This provides a professional look that is slightly more approachable than sharp corners while maintaining a grid-aligned feel.
- **Selection States:** Checkboxes use a 2px radius. 
- **Tags/Status:** Status indicators (pills) may use a fully rounded radius (100px) to distinguish them from interactive buttons.

## Components

- **Metric Tiles:** Key indicators displayed in white containers with a 1px border. They include a `label-caps` title, a `headline-lg` value with tabular figures, and a small sparkline or percentage change indicator.
- **Data Tables:** The core of the tool. Headers use #F8FAFC background with `label-caps` text. Cell text uses `body-sm` or `data-tabular`. Hover states trigger a light gray background fill.
- **Buttons:** 
  - *Primary:* Solid #2563EB with white text.
  - *Secondary:* White background with #E2E8F0 border and #475569 text.
- **Form Inputs:** Minimalist style. No background fill—only a 1px #E2E8F0 border. On focus, the border changes to #2563EB with a subtle 2px blue "glow" (outline-offset).
- **Status Indicators:** Small dots or text-pills using semantic colors. In "AuditTile Mini," errors are always accompanied by an icon to ensure accessibility (color is not the only indicator).
- **Navigation:** A vertical left-hand sidebar with icons and text, utilizing a subtle active state (blue left-border accent).