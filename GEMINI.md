# Technical Execution Plan: Portfolio Modernization

This document outlines the detailed technical steps required to implement the enhancements described in the PM's project plan. The execution is broken down by component, starting with global styles and then addressing individual pages and files.

---

## I. Global Design & UX Enhancements (`style.css`)

**Goal:** Establish a modern, consistent, and maintainable design system for the entire portfolio. All changes in this section will primarily target `style.css`.

### 1.1. CSS Variable Scaffolding

**Action:** Define a centralized color palette and spacing system using CSS variables at the `:root` level for easy management and consistency.

**File:** `style.css`

```css
/* Add at the top of style.css */
:root {
  /* 1. Refined Color Palette */
  --color-background-deep: #0d0d0d; /* For main body background */
  --color-background: #1b1b1b;       /* Original background, for variety */
  --color-surface: #2a2a2a;         /* For cards, sections */
  --color-border: #333;

  --color-text-primary: #e6e6e6;
  --color-text-secondary: #999;

  --color-accent: #00bcd4;
  --color-accent-hover: #00e5ff; /* Lighter for hover states */
  --color-accent-dark: #008c9e;  /* Darker for active/focus states */

  /* 2. Typography */
  --font-primary: 'Poppins', sans-serif;
  --font-secondary: 'Roboto Slab', serif; /* Example secondary font for headings */

  /* 3. Spacing System (Vertical Rhythm) */
  --space-unit: 1rem; /* 16px base */
  --space-xs: calc(0.5 * var(--space-unit));   /* 8px */
  --space-sm: var(--space-unit);             /* 16px */
  --space-md: calc(1.5 * var(--space-unit));   /* 24px */
  --space-lg: calc(2.5 * var(--space-unit));   /* 40px */
  --space-xl: calc(4 * var(--space-unit));     /* 64px */

  /* 4. Transitions */
  --transition-fast: all 0.2s ease-in-out;
}
1.2. Typography Refresh
Action: Import the new heading font and update base element styles to use the new typography system.

File: style.css

Import Font: Add the Google Font import at the top of the CSS file.

CSS

@import url('[https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto+Slab:wght@400;700&display=swap](https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&family=Roboto+Slab:wght@400;700&display=swap)');
Update Base Styles: Modify the body and create new rules for headings.

CSS

body {
  font-family: var(--font-primary);
  background-color: var(--color-background-deep); /* Use new variable */
  color: var(--color-text-primary);
  font-size: 16px; /* Ensure base font size */
  line-height: 1.6;
}

h1, h2, h3, h4, h5, h6 {
  font-family: var(--font-secondary);
  font-weight: 700;
  color: var(--color-text-primary);
  margin-top: var(--space-lg);
  margin-bottom: var(--space-md);
}
1.3. Modern Spacing and Layout
Action: Refactor layout styles to use the new spacing system and create a dedicated, responsive class for iframes.

File: style.css

Update Section Spacing: Replace my-5 in HTML with a class like section and style it.

CSS

.section {
  padding-top: var(--space-xl);
  padding-bottom: var(--space-xl);
}
Iframe Container: Create a class to handle responsive iframes with a 16:9 aspect ratio. Remove all inline styles from <iframe> tags.

CSS

/* Responsive Iframe Container */
.iframe-container {
  position: relative;
  overflow: hidden;
  width: 100%;
  padding-top: 56.25%; /* 16:9 Aspect Ratio */
  margin-top: var(--space-md);
  border: 1px solid var(--color-border);
  border-radius: 8px; /* Consistent border radius */
  background: var(--color-surface);
}

.iframe-container iframe {
  position: absolute;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  width: 100%;
  height: 100%;
  border: none; /* Remove iframe's default border */
}
1.4. Enhanced Interactive Elements
Action: Update styles for buttons and links to have more engaging interactive states using the new color variables and transitions.

File: style.css

CSS

/* Refined Button Styles */
.btn-outline-info {
  border-color: var(--color-accent);
  color: var(--color-accent);
  transition: var(--transition-fast);
}

.btn-outline-info:hover,
.btn-outline-info:focus {
  background-color: var(--color-accent);
  color: var(--color-background-deep);
  transform: translateY(-2px);
  box-shadow: 0 4px 15px rgba(0, 188, 212, 0.3);
}

/* General Link Styles */
a {
  color: var(--color-accent);
  transition: var(--transition-fast);
}

a:hover {
  color: var(--color-accent-hover);
  text-decoration: none;
}
II. Homepage Specific Improvements (index.html)
2.1. Hero Section Reimagining
Action: Update the HTML and CSS for the hero section to add a background image and improve messaging.

File: index.html

Update the text content:

HTML

<section class="hero">
  <div class="container text-center">
    <h1>Transforming Complex Data into Clear, Actionable Insights</h1>
    <p class="lead">Through Interactive Mapping & Machine Learning</p>
  </div>
</section>
File: style.css

Add background styling to the .hero class:

CSS

.hero {
  /* Replace 'path/to/your/image.jpg' with an actual abstract background image */
  background-image: linear-gradient(rgba(13, 13, 13, 0.8), rgba(13, 13, 13, 0.95)), url('path/to/your/image.jpg');
  background-size: cover;
  background-position: center;
  padding: var(--space-xl) 0;
}
2.2. Project Card Standardization & Engagement
Action: Edit index.html to ensure all project cards have consistent links.

File: index.html

CRITICAL FIX: Locate the "Election Forecast Model" card.

Add a "View App/Dashboard" link. Since it doesn't have a live app, the link should go to the details page, but the text should be consistent. Or, if it's truly just a details page, ensure the button text clearly says "Learn More" and is the primary call to action. The PM note suggests it's missing a link, but it seems it's just a "Learn More". Decision: Standardize the button text and ensure it exists. The current HTML shows "Learn More" but no "View" link, which is correct. We will ensure all other cards have both where applicable.

File: style.css

Update .card:hover to use the new system.

CSS

.card {
  /* ... existing styles ... */
  background-color: var(--color-surface);
  border: 1px solid var(--color-border);
  transition: var(--transition-fast);
}

.card:hover {
  transform: translateY(-8px);
  box-shadow: 0 12px 24px rgba(0, 0, 0, 0.5);
  border-color: var(--color-accent);
}
2.3. "Welcome" Section Messaging
Action: Condense the welcome message in index.html.

File: index.html

Replace the two paragraphs inside <section class="welcome"> with a single, concise paragraph as per the PM's plan.

III. Project Detail Page Overhaul (*.html)
3.1. General Content & Structural Refinements
Action: Apply these changes across all project detail pages.

Emphasize "Why": Rewrite the introductory paragraph of each project page to focus on the problem solved or impact created.

Refine "How it was Made": Rewrite this section on each page to explain technology choices and challenges, rather than just listing tools.

Implement Responsive Iframes:

ACTION REQUIRED: Systematically go through CityCouncil.html, DaRaceCounty.html, LaIncome.html, PickleballMapDetails.html, PortlandByAge.html, and CensusAIDetails.html.

Wrap each <iframe> in <div class="iframe-container">.

Remove all inline style attributes from the <iframe> tags.

Change width="1200" (or other fixed widths) to width="100%".

CRITICAL (Accessibility): Ensure every <iframe> has a descriptive title attribute. Example: title="Interactive Map of Portland DA Election Results".

3.2. Data, Table, and Code Cleanup
File: media/election_forecast_detailed.csv

CRITICAL FIX: Open this CSV file. Perform a find-and-replace to remove all occurrences of the `` pattern. The data should be clean numbers and text.

File: ElectionModel.html

CRITICAL FIX: Delete the entire <div class="mb-5"> that contains the "Appendix A" heading and the <pre><code class="language-python">...</code></pre> block.

In its place, add a concise paragraph and a link:

HTML

<h3>A. Code Implementation</h3>
<p>The core methodology was implemented in Python using Pandas, Scikit-learn, and SHAP. For a detailed look at the data preprocessing, model training, and feature analysis, the complete source code is available on GitHub.</p>
<a href="[https://github.com/your-username/your-repo-name](https://github.com/your-username/your-repo-name)" class="btn btn-outline-info" target="_blank">View Code on GitHub</a>
Add a citation above the results table:

HTML

<h3>4.3 Precinct-Level Predictions</h3>
<p>The following table displays the forecasted results. This data is generated by the predictive model and can be found in <code>media/election_forecast_detailed.csv</code>.</p>
File: DaRaceCounty.html

Review the tables. Apply the global table styles from style.css to ensure they are readable.

3.3. Specific Page Fixes Checklist
Action: Go through each file and apply the specified fixes.

[ ] CensusAIDetails.html: Condense the "Key Features" section. Combine points about AI functionality into a single, powerful statement.

[ ] FantasyFootballAppDetails.html: Add a sentence to the introduction clarifying the user benefit (e.g., "enabling data-driven draft decisions and weekly matchup optimizations").

[ ] PickleballMapDetails.html:

Update <title> to "Portland Pickleball Finder: Interactive Courts Map".

Update <h1> to "Portland Pickleball Finder: Interactive Courts Map".

[ ] ElectionModel.html:

Update <h1> to be more specific if needed.

In "Data Sources," add the official source for each dataset (e.g., "Data sourced from Multnomah County Elections Division").

[ ] DaRaceCounty.html:

Update <title> to "Portland DA Race Results: Vasquez vs Schmidt 2024".

Update <h1> to "Portland DA Race Results: Vasquez vs Schmidt 2024".

[ ] LaIncome.html:

CRITICAL FIX: Verify the map's color legend. Correct the descriptive text in the "Income Levels Across Census Tracts" section to accurately reflect whether light or dark shades represent high or low income. The current text is contradictory.

[ ] PortlandByAge.html:

Update <title> to "Portland Age Demographics: Interactive Dashboard".

Update <h1> to "Portland Age Demographics: Interactive Dashboard".

[ ] CityCouncil.html:

Update <title> to "Portland City Council Election Results (2022)".

Update <h1> to "Portland City Council Election Results (2022)".

IV. Portfolio Content - Overall Readme (README.md)
Action: Edit the main README.md file to align with the portfolio's new messaging and structure.

Welcome Message: Rewrite the introductory paragraphs to match the concise, high-impact message from the new index.html.

Project Summaries: Review each project's one-sentence summary. Enhance them to be more value-driven (e.g., add "providing actionable insights for campaigns" to the Election Model summary).

Standardize Links: Ensure every project entry has a consistent link format for "Live Application" and "Project Details Page", making them easy to find and click.