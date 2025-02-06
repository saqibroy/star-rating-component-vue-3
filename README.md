# Star Rating Component (Vue 3)

## Project Overview
This is a reusable Star Rating component built in Vue 3 that allows users to rate artworks in three categories.

## Features
- Click to set rating  
- Hover effect for visual feedback  
- Displays numerical rating (e.g., "4/5")  
- Fully reusable Vue 3 component  
- Optimized for performance & responsiveness  

## Project Structure
- `StarRating.vue` → Handles star rating logic  
- `App.vue` → Uses `StarRating` for different categories  
- `styles.css` → Basic styles using Tailwind  
- `store.js` → (Optional) Used if global state is needed  

## 🛠️ Installation & Running Locally
```sh
npm install
npm run dev

#### Approach & Decisions
**1. Tech Stack:**  
- Built with **Vue 3** (Composition API) to align with LUMAS's frontend requirements.  
- Used **Tachyons CSS** (offline version in `/assets`) for simplicity and zero build setup.  
  - *Why Tachyons?* While Tailwind CSS is my go-to choice for professional projects, I opted for Tachyons here to avoid build tool conflicts and focus on core functionality. This saved time for bonus tasks.  

**2. Component Design:**  
- Created a reusable `StarRating` component with props for category names and two-way binding for ratings.  
- Implemented hover/click interactions using Vue’s reactivity system.  

**3. Trade-offs:**  
- Skipped Tailwind CSS to eliminate PostCSS configuration complexities.  
- Used static Tachyons classes instead of dynamic styling for simplicity.  

**4. Bonus Tasks Completed:**  
- Added a **Submit button** that logs all ratings to the console.  
- Ensured mobile responsiveness using Tachyons’ utility classes (e.g., `mw6 center` for max-width).  
- Included **offline Tachyons CSS** (`tachyons.min.css` in `/assets`) to avoid CDN dependency.  

**5. Assumptions:**  
- Ratings are independent across categories.  
- Offline Tachyons file was manually downloaded for reliability.  

---

### How to Run
1. Clone the repository.  
2. Run `npm install && npm run dev`.  

---

### Project Structure