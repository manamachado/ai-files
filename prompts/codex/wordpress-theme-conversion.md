Convert the current website into a fully functional WordPress theme.

Goal:
Transform the existing HTML/CSS/JS website into a clean, modular WordPress theme while preserving the current design and layout exactly as it is.

Requirements:

1. Do not change the design, layout, spacing, typography, or styling.
2. Keep the current UI exactly the same as the existing website.
3. Convert the static structure into proper WordPress theme files.

Theme structure to create:

/theme-name
    style.css
    functions.php
    index.php
    header.php
    footer.php
    front-page.php
    page.php
    single.php
    archive.php
    sidebar.php
    screenshot.png
    /assets
        /css
        /js
        /images
    /template-parts
        hero.php
        sections.php

Tasks:

1. Move all CSS, JS, and images into the /assets folder.
2. Properly enqueue styles and scripts using functions.php.
3. Convert reusable sections into template parts.
4. Make the navigation menu dynamic using WordPress menu functions.
5. Convert content areas into WordPress loops where necessary.
6. Ensure the hero section and layout remain identical to the current design.
7. Make the theme responsive and WordPress standards compliant.

Dynamic features:

- Enable featured images
- Add WordPress navigation menus
- Support custom logo
- Support widgets
- Support Gutenberg blocks

Important:

- Do NOT change the current visual design.
- Do NOT modify spacing, layout, or styling.
- Only refactor the code structure to WordPress theme architecture.

Output:

Generate the full WordPress theme folder structure and provide all necessary theme files.
