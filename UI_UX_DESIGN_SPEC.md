# KolaExplore - UI/UX Design Specification
## For Figma Implementation

### Design System

#### Color Palette
**Primary Colors:**
- Primary: #007AFF (Blue)
- Primary Dark: #0051D5
- Primary Light: #E3F2FD

**Secondary Colors:**
- Secondary: #34C759 (Green)
- Accent: #FF9500 (Orange)
- Error: #FF3B30 (Red)
- Warning: #FFCC00 (Yellow)

**Neutral Colors:**
- Background: #FFFFFF
- Surface: #F5F5F7
- Text Primary: #1D1D1F
- Text Secondary: #6E6E73
- Border: #D2D2D7

#### Typography
**Font Family:**
- Primary: Inter, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif
- Headings: Inter Bold
- Body: Inter Regular

**Type Scale:**
- H1: 32px / 40px (Bold)
- H2: 24px / 32px (Bold)
- H3: 20px / 28px (SemiBold)
- H4: 18px / 24px (SemiBold)
- Body Large: 16px / 24px (Regular)
- Body: 14px / 20px (Regular)
- Body Small: 12px / 16px (Regular)
- Caption: 11px / 14px (Regular)

#### Spacing System
- Base Unit: 4px
- Scale: 4, 8, 12, 16, 24, 32, 48, 64, 96, 128

#### Border Radius
- Small: 4px
- Medium: 8px
- Large: 12px
- XLarge: 16px
- Round: 50%

#### Shadows
- Small: 0 1px 2px rgba(0,0,0,0.05)
- Medium: 0 2px 8px rgba(0,0,0,0.1)
- Large: 0 4px 16px rgba(0,0,0,0.15)

### Components

#### Buttons
**Primary Button:**
- Background: Primary Color
- Text: White
- Padding: 12px 24px
- Border Radius: 8px
- Height: 44px
- States: Default, Hover, Active, Disabled

**Secondary Button:**
- Background: Transparent
- Border: 1px solid Primary Color
- Text: Primary Color
- Padding: 12px 24px
- Border Radius: 8px

**Text Button:**
- Background: Transparent
- Text: Primary Color
- Padding: 8px 16px

#### Input Fields
- Height: 44px
- Padding: 12px 16px
- Border: 1px solid Border Color
- Border Radius: 8px
- Font Size: 16px
- States: Default, Focus, Error, Disabled

#### Cards
- Background: White
- Border Radius: 12px
- Shadow: Medium
- Padding: 24px

#### Navigation
- Height: 64px
- Background: White
- Shadow: Small
- Padding: 0 24px

### Layout Structure

#### Grid System
- Container Max Width: 1200px
- Columns: 12
- Gutter: 24px
- Margin: 0 auto

#### Breakpoints
- Mobile: 320px - 767px
- Tablet: 768px - 1023px
- Desktop: 1024px+

### Page Templates

#### Home Page
- Header with Navigation
- Hero Section
- Feature Cards Grid
- Call-to-Action Section
- Footer

#### Detail Page
- Breadcrumb Navigation
- Main Content Area
- Sidebar (if applicable)
- Related Items Section

#### List/Grid View
- Filter/Search Bar
- Sort Options
- Grid/List Toggle
- Item Cards
- Pagination

### User Flows

#### Primary User Journey
1. Landing Page
2. Search/Browse
3. View Details
4. Action (Book/Add/Share)
5. Confirmation

### Accessibility
- WCAG 2.1 AA Compliance
- Minimum Touch Target: 44x44px
- Color Contrast Ratio: 4.5:1 (text), 3:1 (UI components)
- Keyboard Navigation Support
- Screen Reader Support

### Responsive Design
- Mobile-First Approach
- Touch-Friendly Interactions
- Adaptive Layouts
- Flexible Images

### Animation & Interactions
- Transition Duration: 200-300ms
- Easing: ease-in-out
- Hover States on Interactive Elements
- Loading States
- Error States
- Success Feedback

