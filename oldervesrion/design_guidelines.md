# BotBridgeOps Design Guidelines

## Design Approach

**Selected Approach:** Hybrid - Modern SaaS Aesthetic with Design System Foundation

Drawing inspiration from successful enterprise SaaS platforms (Linear's precision, Stripe's clarity, Vercel's technical sophistication), combined with Material Design principles for consistency in complex enterprise interfaces.

**Core Philosophy:** Professional yet approachable. Technical credibility without intimidation. Data-driven yet human-centered.

---

## Typography System

**Font Families:**
- Primary: Inter (headers, UI elements, body text)
- Monospace: JetBrains Mono (technical specs, code snippets, metrics)

**Hierarchy:**
- H1 (Hero): 3.5rem (56px), font-weight: 700, line-height: 1.1
- H2 (Section Titles): 2.5rem (40px), font-weight: 700, line-height: 1.2
- H3 (Subsections): 1.875rem (30px), font-weight: 600, line-height: 1.3
- H4 (Card Titles): 1.25rem (20px), font-weight: 600, line-height: 1.4
- Body Large: 1.125rem (18px), font-weight: 400, line-height: 1.6
- Body: 1rem (16px), font-weight: 400, line-height: 1.6
- Small/Caption: 0.875rem (14px), font-weight: 500, line-height: 1.5

---

## Layout System

**Spacing Primitives:** Tailwind units of 2, 4, 8, 12, 16, 20, 24 (e.g., p-4, gap-8, mb-12)

**Container Strategy:**
- Max-width container: max-w-7xl (1280px)
- Content sections: px-6 on mobile, px-8 on tablet, px-12 on desktop
- Section vertical spacing: py-16 (mobile), py-20 (tablet), py-24 to py-32 (desktop)

**Grid Patterns:**
- Feature grids: 1 column (mobile), 2 columns (tablet), 3-4 columns (desktop)
- Stats/metrics: 2x2 grid (mobile), 4 columns (desktop)
- Logo grids: 2 columns (mobile), 4-6 columns (desktop)

---

## Component Library

### Navigation
**Header:** Sticky navigation with backdrop blur effect
- Logo (left), navigation links (center), CTA buttons (right)
- Mobile: Hamburger menu with slide-in drawer
- Height: h-16 (64px)

### Hero Section
**Structure:** Full-width, asymmetric layout
- Left: Headline, subheadline, description, dual CTAs, trust badges
- Right: Dashboard screenshot/mockup with subtle shadow and border
- Background: Gradient overlay from teal to dark navy
- Height: min-h-screen on desktop, natural height on mobile
- Trust badges: Inline metrics with icons, separated by vertical dividers

### Feature Cards
**Design:** Elevated cards with hover states
- Padding: p-8
- Border radius: rounded-2xl
- Shadow: subtle on default, elevated on hover
- Icon: Large (h-12 w-12), positioned top-left with background circle
- Title + description with proper spacing (gap-4)
- Optional: Learn more link with arrow icon

### Stats Display
**Format:** Metric cards in grid layout
- Large number: 3xl font size, bold weight, monospace font
- Label: sm font size, muted text
- Icon: Accent color, positioned above or beside metric
- Background: Subtle gradient or solid with border

### CTA Sections
**Structure:** Full-width sections with centered content
- Headline + supporting text + button group
- Background: Contrasting section (dark if previous was light)
- Padding: py-20 to py-24
- Buttons: Primary + secondary, stacked on mobile, inline on desktop

### Forms
**Demo Request Form:**
- Single column layout, max-w-2xl centered
- Input fields: h-12, rounded-lg, border with focus ring
- Labels: font-medium, mb-2
- Submit button: Full-width on mobile, auto-width on desktop
- Field spacing: gap-6

### Testimonial Section
**Layout:** Cards in horizontal scroll (mobile) or grid (desktop)
- Card: Quote, author name, role, company logo
- Photo: Circular avatar (h-16 w-16)
- Quote styling: Larger text with quotation marks
- Background: Alternating or uniform with borders

### Footer
**Multi-column layout:**
- 4 columns on desktop (Product, Solutions, Company, Resources)
- Stacked on mobile
- Newsletter signup: Inline input + button
- Social icons: Horizontal list
- Bottom bar: Logo, copyright, legal links
- Spacing: py-16 top, py-8 bottom bar

---

## Platform-Specific Components

### Dashboard Mockup
- Modern interface with sidebar navigation
- Data visualizations: Line charts, bar graphs, status indicators
- Realistic but simplified for clarity
- Subtle animations: Data updating, loading states

### Process Timeline
- Vertical on mobile, horizontal on desktop
- Connected nodes with lines
- Phase cards: Number badge, title, description, duration
- Progress indicator showing completion

### Integration Logos
- Grayscale by default, full color on hover
- Consistent sizing: h-12
- Grid layout with equal spacing (gap-8)
- Padding: p-4 per logo container

### Pricing Cards
- Three cards side-by-side on desktop, stacked on mobile
- "Most Popular" badge on middle tier
- Feature list with checkmarks
- Price: Large, bold, with /month subtitle
- CTA button: Full-width within card
- Border highlight on featured tier

---

## Images

### Required Images:

1. **Hero Dashboard Mockup**
   - Modern IT operations dashboard showing health metrics, incident timeline, AI agent activity
   - Placement: Right side of hero section (60% width on desktop)
   - Style: Floating with shadow, slight tilt (3-5 degrees)

2. **Platform Diagram**
   - Visual showing BotBridgeOps connecting multiple tools (ServiceNow, Jira, Slack, etc.)
   - Placement: Solution section, centered
   - Style: Clean, minimalist with connecting lines and icons

3. **Customer Logos**
   - 8-12 recognizable company logos
   - Placement: Social proof section, logo grid
   - Style: Monochrome/grayscale

4. **Team Photos**
   - Professional headshots for About page
   - Placement: Team section, circular avatars
   - Style: Consistent lighting and background

---

## Interactions & Animations

**Principle:** Subtle, purposeful, performance-conscious

- **Scroll Reveals:** Fade-in with slight upward movement for sections (100ms duration)
- **Hover States:** Cards lift with shadow increase (150ms ease-out)
- **Button Interactions:** Scale 0.98 on press, smooth transitions
- **Dashboard Mockup:** Subtle floating animation (3-second loop)
- **Metric Counters:** Count-up animation on scroll into view
- **NO:** Parallax effects, excessive animations, auto-playing videos with sound

---

## Responsive Breakpoints

- Mobile: < 768px (single column, stacked layouts)
- Tablet: 768px - 1024px (2 columns where appropriate)
- Desktop: > 1024px (full multi-column layouts)

**Mobile-First Priorities:**
- Readable typography (minimum 16px body)
- Touch-friendly buttons (minimum h-12)
- Simplified navigation (hamburger menu)
- Optimized images for bandwidth

---

## Accessibility Standards

- WCAG 2.1 AA compliance minimum
- Keyboard navigation for all interactive elements
- Focus indicators: 2px ring with offset
- Semantic HTML structure
- Alt text for all images
- Sufficient contrast ratios (4.5:1 for body text, 3:1 for large text)
- Form labels properly associated with inputs
- Skip-to-content link for screen readers