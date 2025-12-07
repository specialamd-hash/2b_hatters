# Design Guidelines: Personal Landing Page

## Design Approach
**Reference-Based Approach**: Inspired by modern link-in-bio pages (Linktree, Beacons) with elevated visual treatment. This is a visual-first, personality-driven landing page where aesthetic impact is paramount.

**Core Principles**:
- Bold, unapologetic use of color and animation
- Playful, youthful energy with professional polish
- Maximum impact in minimal space
- Mobile-first design (primary viewing context)

---

## Layout System

**Spacing**: Use Tailwind units of 3, 4, 6, and 8 consistently (p-4, gap-6, mb-8, etc.)

**Page Structure** (Single scrollable page):
1. **Hero Section** (Full viewport height on mobile, 80-90vh on desktop)
   - Centered content layout with animated gradient background
   - Profile avatar/illustration positioned prominently
   - Name/title display as main focal point
   - Brief tagline or description
   
2. **Social Links Section** (Natural height, scrollable)
   - Grid of social media buttons
   - Stacked vertically on mobile, 2-column grid on tablet+
   - Generous spacing between buttons (gap-4 to gap-6)
   - Donation button as final, emphasized element

**Container**: Max width of 480px (max-w-md) for optimal mobile experience, centered on larger screens

---

## Typography

**Fonts**: 
- Primary: **Poppins** (Bold 700, SemiBold 600, Medium 500)
- Secondary: **Inter** (Regular 400, Medium 500)

**Hierarchy**:
- Name/Title: 3xl to 4xl (36-48px), font-bold, tight tracking
- Tagline: base to lg (16-18px), font-medium, relaxed leading
- Button Text: base to lg (16-18px), font-semibold
- Footer Text: sm (14px), font-regular

---

## Component Library

### Profile Section
- **Avatar/Illustration**: Circular frame (128-160px diameter), positioned above name
- **Name Display**: Bold, large typography with optional gradient text effect
- **Tagline**: 1-2 line description, lighter weight, subtle opacity

### Social Media Buttons
Each button includes:
- Platform icon (left-aligned, 24x24px from Heroicons or Font Awesome)
- Platform name (centered text)
- Clean, rounded rectangle (rounded-2xl)
- Subtle shadow and hover lift effect
- Uniform height (56-64px)
- Full width on mobile, constrained on desktop

Button variations:
- Standard social links: White/light background with subtle border
- Donation/CTA button: Gradient background (purple to pink), bold treatment

### Background Elements
- **Animated Gradient**: Purple (#8B5CF6) to pink (#EC4899) diagonal gradient
- **Sparkle/Particle Effects**: Floating, subtle animated shapes or stars scattered across background
- **Overlay**: Semi-transparent layer to ensure text readability

---

## Visual Design Elements

**Color Strategy** (Will be refined in implementation):
- Gradient backgrounds for hero and featured buttons
- Clean white/light containers for social buttons
- High contrast text for readability

**Shadows & Depth**:
- Button shadows: shadow-lg for resting state, shadow-xl on hover
- Avatar: shadow-2xl for prominence
- Layered depth through overlapping elements and shadows

**Border Radius**:
- Buttons: rounded-2xl (16px)
- Avatar: rounded-full
- Container cards: rounded-3xl (24px) if used

---

## Images

**Profile Avatar/Illustration**:
- Description: Stylized character illustration or professional headshot
- Placement: Top center of hero section, above name
- Treatment: Circular crop with gradient border ring
- Size: 128-160px diameter
- Purpose: Personal branding and visual anchor

**Background Treatment**:
- No hero image - animated gradient with particle effects creates the visual impact
- Background is fully code-generated with CSS gradients and animations

---

## Animations

**Strategic Animation Points**:
- **Background Gradient**: Slow, continuous color shift (20-30s loop)
- **Sparkles/Particles**: Gentle floating motion, subtle scale pulse
- **Button Hover**: Smooth lift (translateY -2px) with shadow expansion
- **Page Load**: Gentle fade-in of content elements, staggered timing
- **Avatar**: Optional subtle floating animation on desktop

Keep all animations subtle and performant - this page must feel smooth on mobile devices.

---

## Interaction Patterns

**Social Buttons**:
- Click/tap opens link in new tab
- Clear hover state (lift + shadow)
- Active state: slight press effect (scale 0.98)

**Donation Button**:
- Visually distinct with gradient background
- Slightly larger or emphasized positioning
- Same interaction pattern as social buttons

**Mobile Considerations**:
- Minimum touch target size: 48px height
- Adequate spacing between interactive elements (gap-4 minimum)
- No hover-dependent interactions

---

## Accessibility

- All buttons have proper contrast ratios against backgrounds
- Icon + text labels for all social links (no icon-only buttons)
- Semantic HTML structure (main, section, nav where appropriate)
- Alt text for avatar image
- Focus states visible with ring treatment
- Skip to content link (visually hidden but screen reader accessible)

---

## Responsive Behavior

**Mobile (Default)**:
- Single column layout
- Full-width social buttons
- Larger touch targets
- Avatar 128px

**Tablet (md: 768px+)**:
- 2-column grid for social buttons
- Avatar 144px
- Increased spacing

**Desktop (lg: 1024px+)**:
- Maintain 2-column grid (don't expand to 3+)
- Avatar 160px
- Max container width enforced
- Enhanced animation effects

---

## Content Structure

1. **Hero Content**:
   - Avatar/Profile Image
   - Name (e.g., "Alex Johnson")
   - Tagline (e.g., "Content Creator & Streamer")

2. **Social Links** (Customizable set, typically 6-10):
   - Telegram
   - Instagram
   - Twitch
   - TikTok
   - YouTube
   - Twitter/X
   - Discord
   - GitHub (if applicable)
   - Portfolio/Website

3. **Special Button**:
   - Donation/Support button (visually emphasized)

4. **Footer** (Optional):
   - Copyright or minimal text
   - "Made with ❤️" type statement