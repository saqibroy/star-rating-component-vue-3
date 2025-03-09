# Star Rating Component (Vue 3)

A highly customizable star rating component for Vue 3, optimized for performance, SEO, and accessibility.

## FOCUS
- **Memoization**: Optimized computed properties for better performance.
- **Lazy Loading**: Heavy resources are loaded lazily.
- **SEO Optimized**: Uses semantic HTML tags.
- **Accessibility**: ARIA attributes for better accessibility.

## Features
- Click to set rating
- Hover effect for visual feedback
- Displays numerical rating (e.g., "4/5")
- Fully reusable Vue 3 component
- Optimized for performance & responsiveness

## Approach & Decisions
**1. Tech Stack:**
- Built with **Vue 3** and **Vite** to align with frontend requirements.
- Used **Tachyons CSS** (offline version in `/assets`) for simplicity and zero build setup.
  - *Why Tachyons?* While Tailwind CSS is my go-to choice for professional projects, I opted for Tachyons here to avoid build tool conflicts and focus on core functionality. This saved time for bonus tasks.

**2. Component Design:**
- Created a reusable `StarRating` component with props for category names and two-way binding for ratings.
- Implemented hover/click interactions using Vue’s reactivity system.

**3. Trade-offs:**
- Skipped Tailwind CSS to eliminate PostCSS configuration complexities.
- Used static Tachyons classes instead of dynamic styling for simplicity.

**4. Tasks Completed:**
- Added a **Submit button** that logs all ratings to the console.
- Ensured mobile responsiveness using Tachyons’ utility classes (e.g., `mw6 center` for max-width).

---

## How to Run
**Requirements:**
- Node.js v18.x (LTS version recommended)
- npm v9.x

**Steps:**
1. Clone the repository  
2. Install dependencies:  
   ```bash
   npm install
3. Start development server: 
   ```bash
   npm run dev

### Project Structure
```plaintext
sohail-lumas-task/
├── src/
│   ├── assets/
│   │   └── tachyons.min.css
│   ├── components/
│   │   └── StarRating.vue
│   ├── App.vue
│   ├── main.js
├── index.html
├── package.json
├── vite.config.js
└── README.md
```
