# Accessibility Presentation

## Intro to Accessibility  

- **1.3 billion** people worldwide have a disability.  
- By **2030**, **2 billion** people will need at least one assistive product.  
- **25 countries** have web accessibility laws and policies.  
- **20%** of web traffic could come from a person with a disability.  
  - Includes **situational disabilities** (e.g., temporary hearing loss, broken arm).  

## WCAG  

- **"WhaCAG"?**  
- **WCAG 2.2, AA is the target**  
  - **Success Criterion:**  
    - **POUR** – Perceivable, Operable, Understandable, Robust.  
  - **Levels:**  
    - **A** – Basic  
    - **AA (Target)** – Desirable (many organizations aim for this level).  
    - **AAA** – Comprehensive.  

## Building Accessibility into Mapping Apps  

### High Contrast  

- Visual presentation should have **contrast of 4.5:1** (AA, 1.4.3).  
- High contrast in components:  
  - `calcite-meter`, `calcite-button`, `calcite-link`.  
- **Windows High Contrast Mode** – Can be turned on, but also possible to code a high contrast mode.  
- **Checking Contrast?**  

### Live Regions & Map Descriptions  

- **ARIA Descriptions (`aria-describedby`)**  
  - All **non-text content** needs a **text alternative**.  
  - Links elements to additional descriptive text for screen readers.  
  - Helps visually impaired users understand maps.  
  - Works well with long descriptions but should be **ephemeral, not four paragraphs**.  
- **ARIA Live Regions**  
  - **Accessible Rich Internet Applications (ARIA)** – can be tricky.  
  - **Bad ARIA is worse than no ARIA** – needs to be implemented correctly.  
  - Used for **content updates without user focus** (e.g., notifications, chat messages).  
  - **ARIA Attributes:**  
    - `aria-live: "polite"` – Announce updates when idle (recommended).  
    - `aria-live: "assertive"` – Interrupt all other speech.  
    - `aria-live: "off"` – Default, no announcement.  
  - **CSS for screen reader instructions** – Hide them from visual display.  

### Focus Trapping (WCAG 2.1.2)  

- Ensures **keyboard users don't get stuck** in an interface.  
- Benefits users with **visual & cognitive impairments**.  
- When closing elements like popups, **reset focus** properly.  

### Handling Animations (WCAG 2.2.2, 2.3.3)  

- **If content moves, blinks, or scrolls for more than 5 seconds,** provide a way to pause/stop/hide.  
- **Flashing/Blinking** must meet **2.3.1 & 2.3.2** criteria.  
- Motion animation can be disabled *unless essential* (e.g., **ESRI bookmarks**).  
- **GoTo Method** respects user preference for reduced motion.  
- Detect user preferences via:  
  - **CSS:** `@media (prefers-reduced-motion: reduce)`  
  - **JS:** `window.matchMedia("(prefers-reduced-motion)")`  

### Consistent Focus  

- **2.4.3 – Focus Order**  
- **2.1.1 – Keyboard Navigation**  

## Testing, Tools & Resources  

### Testing Methods  

- **User Acceptance Testing** – Real-world performance (**most important**).  
- **Manual Testing** – Using screen readers (JAWS, NVDA, VoiceOver).  
- **Automated Testing** – Browser extensions.  
  - **Limitations:**  
    - Cannot guarantee full accessibility.  
    - Only catches **20-30%** of accessibility issues.  
  - **Developer tools:**  
    - Chrome/Firefox DevTools → Inspect Accessibility Properties.  
  - **False Positives & Bugs:**  
    - `calcite-inputs-clearable` – X button on a search isn't keyboard-accessible.  
    - Incorrect/missing language settings.  

### Accessibility Tools  

- **Color Ramps by ESRI**  
- **Contrast Grid by Eightshapes**  
- **Browser Extensions:**  
  - **Colorblindly**  
  - **Axe by Deque**  
  - **WAVE by WebAIM**  
  - **Accessibility Insights by Microsoft**  
  - **Accessibility Checker by Silktide**  

## The Road Ahead  

- **AI in Accessibility**  
- **24px for touchpoint sizes?**  
