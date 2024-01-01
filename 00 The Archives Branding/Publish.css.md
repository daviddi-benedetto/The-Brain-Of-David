## Publish.css
I use the *Typomagical* theme for obsidian with the custom CSS pasted beneath the :root{}

```css
/* ======================== CUSTOM EDITS BY DAVID START======================== */
/* Removes the footer */
.site-footer a {
  display: none;
}

/* Changes Accent Color */
body{
  --accent-h: 32;
  --accent-s: 60%;
  --accent-l: 65%;
} 

/* Changes Title Variables */
body{
  --site-name-color: var(--text-normal);
  --site-name-color-hover: var(--text-muted);
  --site-name-font: inherit;
  --site-name-size: 30px;
  --site-name-weight: var(--font-semibold);
  --site-menu-icon-color: var(--text-faint);
  --site-menu-icon-color-hover: var(--text-normal);
  --site-menu-icon-size: 24px;
}

/* Applies Title Variables */
.site-body-left-column-site-name {
  display: none; /* Hides it so I can put custom logo */
  color: var(--site-name-color);
  font-size: var(--site-name-size);
  font-weight: var(--site-name-weight);
  z-index: 1;
  cursor: pointer;
  line-height: 0;
  padding: 4px 32px 32px 0;
  text-decoration: none;
}

/* Changes Title Logo - PC */
.site-body-left-column-site-logo img {
  border-radius: var(--logo-radius);
  width: var(--logo-width);
  max-width: var(--logo-max-width);
  height: var(--logo-height);
  max-height: var(--logo-max-height);
  object-fit: contain;
  padding: 4px 32px 4px 0px;
}

/* === Mobile === */
.site-header{
  display: flex;
  justify-content: space-between;
} 

/* Changes Title in the Header */
.site-header-text {
  display: none; /* Hides the Title on mobile */
  color: var(--site-name-color);
  cursor: pointer;
  font-size: var(--site-name-size);
  font-weight: var(--site-name-weight);
  flex: 1 0 0;
  text-decoration: none
}

/* Changes Logo in the Header */
.site-header-logo {
  display: flex; /* Added for flexibility */
  justify-content: center; /* Center the logo */
  width: 100%; /* Full width to allow centering */
}

/* ======================== CUSTOM EDITS BY DAVID END ======================== */
```