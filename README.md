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
    *   **Animations**: Custom keyframe animations for the floating background orbs and interaction effects.
*   **Vanilla JavaScript**: Lightweight logic for:
    *   Scroll-triggered animations (Intersection Observer).
    *   Dynamic navigation bar transparency.
    *   Reading progress bar.

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