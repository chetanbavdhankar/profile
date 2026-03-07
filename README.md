# Chetan Bavdhankar - Portfolio

Welcome to my personal portfolio repository. This website is designed to showcase my projects and skills as a Data Scientist and AI Engineer.

## 🏗️ How It Is Built

This portfolio follows a **single-file static architecture** to ensure maximum performance, simplicity, and ease of deployment. There are no build steps, frameworks, or complex dependencies required.

### 💻 Technology Stack

*   **HTML5**: Semantic structure for accessibility and SEO.
*   **Vanilla CSS3**: 
    *   **Glassmorphism Design**: Usage of semi-transparent backgrounds and blurs for a modern "Deep Tech" aesthetic.
    *   **CSS Variables**: A centralized design system for colors (gradients), spacing, and typography.
    *   **Flexbox & Grid**: Responsive layouts that adapt to any device size.
    *   **Animations**: Custom keyframe animations, typewriter blink cursor, and 3D perspective tilt.
*   **HTML5 Canvas**: Full-viewport animated particle constellation network replacing static gradient orbs.
*   **Vanilla JavaScript**: Zero-dependency logic for:
    *   Animated particle network with mouse-repel physics.
    *   Magnetic dual-ring custom cursor (auto-hidden on touch devices).
    *   Typewriter text cycling through key skills.
    *   Scroll-triggered animated stat counters (Intersection Observer).
    *   3D perspective tilt on project and skill cards via mouse tracking.
    *   Dynamic navigation bar transparency.
    *   Reading progress bar.

## 📝 Recent Changes

### Premium Interaction Layer (2026-03-07)

**Why:** The original static gradient orbs and basic hover effects felt generic. These five features create a distinctive, premium feel that differentiates the portfolio on first impression.

**How:** All five features are implemented in pure vanilla JS—zero external libraries:

| Feature | Mechanism | Graceful Degradation |
|---|---|---|
| Particle Constellation | Canvas 2D, 80 particles, proximity-based edge drawing | N/A (always runs) |
| Magnetic Cursor | Dual-ring with lerp tracking, expands on interactive hover | Hidden on touch via `(hover: none)` media query |
| Typewriter Hero | `setTimeout` loop with type/delete cadence, CSS blinking cursor | Falls back to empty subtitle on no-JS |
| Stat Counters | `IntersectionObserver` at 50% threshold, ease-out cubic tween | Shows `0` until scroll (acceptable) |
| 3D Tilt Cards | `mousemove` → `perspective(800px) rotateY/X`, resets on leave | Disabled on touch devices |

**Impact:**
- **Performance**: Particle loop runs at requestAnimationFrame cadence (~60fps). O(n²) connection check is bounded by `PARTICLE_COUNT = 80` (3,160 comparisons max per frame—negligible).
- **Bundle**: 0 bytes added to dependencies. All code inline.
- **Accessibility**: Custom cursor uses `mix-blend-mode: difference` for visibility. Touch devices get native cursor.

## 🚀 Running Locally

Since the project is a static site, you can run it instantly without installing any dependencies.

**Option 1: Direct Open**
*   Simply double-click `index.html` to view the site in your browser.

**Option 2: Live Development**
*   If using **VS Code**, install the **Live Server** extension.
*   Right-click `index.html` and select **"Open with Live Server"**.
*   This enables hot-reloading whenever you make changes.

## ➕ How to Add New Projects

Because the entire site is contained within `index.html`, adding content is straightforward.

1.  Open `index.html` in your text editor.
2.  Search for the `projects-grid` class: `<div class="projects-grid">`.
3.  Choose the appropriate category section (e.g., `<!-- AI Projects -->` or `<!-- Web Projects -->`).
4.  Copy the template below and paste it into the grid.
5.  Update the **Link**, **Emoji**, **Title**, **Description**, and **Tech Stack**.

### Project Card Template

```html
<!-- START NEW PROJECT -->
<a href="https://github.com/yourusername/project-name" target="_blank" class="project-card">
    <div class="project-image">🚀</div> <!-- Choose a relevant emoji -->
    <div class="project-content">
        <div class="project-category">Category Name</div> <!-- e.g. "AI Agent", "Web App" -->
        <h3 class="project-title">Project Title</h3>
        <p class="project-description">
            A concise description of the project, the problem it solves, and the key features.
        </p>
        <div class="project-tech">
            <span class="tech-badge">Tech 1</span>
            <span class="tech-badge">Tech 2</span>
            <span class="tech-badge">Tech 3</span>
        </div>
    </div>
</a>
<!-- END NEW PROJECT -->
```

## 🎨 Design System

The visual style is controlled by CSS variables in the `:root` section of `index.html`. You can easily customize the theme by adjusting these values:

*   `--primary-gradient`: Main brand colors.
*   `--darker-bg`: Background color.
*   `--accent-*`: Various accent colors for highlights.