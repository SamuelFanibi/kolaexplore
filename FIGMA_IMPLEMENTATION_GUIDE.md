# Figma Implementation Guide - Complete Setup

## Figma File Structure

### Main File Organization

```
KolaExplore Design System
├── 🎨 Design System
│   ├── Colors
│   ├── Typography
│   ├── Spacing
│   ├── Shadows
│   ├── Icons
│   └── Components
│
├── 🌐 Web Platform
│   ├── Home & Discovery
│   ├── Flight Booking
│   ├── Hotel Booking
│   ├── Rides Booking
│   ├── Events Booking
│   ├── Spa & Wellness Booking
│   ├── Cart & Checkout
│   ├── Booking Management
│   └── User Profile
│
├── 📱 Mobile App
│   ├── Onboarding
│   ├── Home & Discovery
│   ├── Flight Booking Flow
│   ├── Hotel Booking Flow
│   ├── Rides Booking Flow
│   ├── Events Booking Flow
│   ├── Spa Booking Flow
│   ├── Cart & Checkout
│   ├── Booking Management
│   └── Profile & Settings
│
├── 🏪 Merchant Dashboard
│   ├── Dashboard Overview
│   ├── Service Management
│   ├── Booking Management
│   ├── Availability Calendar
│   ├── Customer Management
│   ├── Analytics
│   └── Settings
│
├── 👨‍💼 Admin Dashboard
│   ├── Platform Overview
│   ├── User Management
│   ├── Merchant Management
│   ├── Booking Oversight
│   ├── Service Moderation
│   ├── Content Management
│   ├── Financial Management
│   └── System Settings
│
└── 📐 Prototypes
    ├── Web User Flows
    ├── Mobile User Flows
    ├── Merchant Flows
    └── Admin Flows
```

## Step-by-Step Implementation

### Phase 1: Design System Setup

#### 1. Create Color Styles

**In Figma:**
1. Create a "Design System" page
2. Create color swatches for all colors in the palette
3. Select each color → Right-click → "Add as style"
4. Name styles using convention: `Color/Primary/500`, `Color/Error/500`, etc.

**Color Style Names:**
- `Color/Primary/50` through `Color/Primary/900`
- `Color/Secondary/50` through `Color/Secondary/900`
- `Color/Success/50`, `Color/Success/500`, `Color/Success/700`
- `Color/Error/50`, `Color/Error/500`, `Color/Error/700`
- `Color/Warning/50`, `Color/Warning/500`, `Color/Warning/700`
- `Color/Info/50`, `Color/Info/500`, `Color/Info/700`
- `Color/Gray/50` through `Color/Gray/900`
- `Color/Text/Primary`, `Color/Text/Secondary`, `Color/Text/Disabled`
- `Color/Background/Primary`, `Color/Background/Secondary`
- `Color/Border/Light`, `Color/Border/Medium`, `Color/Border/Dark`

#### 2. Create Text Styles

**For each typography variant:**
1. Create text layers with sample text
2. Apply font family, size, weight, line height
3. Select text → Right-click → "Add as style"

**Text Style Names:**
- `Text/H1/Desktop`, `Text/H1/Mobile`
- `Text/H2/Desktop`, `Text/H2/Mobile`
- `Text/H3/Desktop`, `Text/H3/Mobile`
- `Text/H4/Desktop`, `Text/H4/Mobile`
- `Text/H5/Desktop`, `Text/H5/Mobile`
- `Text/H6/Desktop`, `Text/H6/Mobile`
- `Text/Body/Large`, `Text/Body/Regular`, `Text/Body/Small`
- `Text/Caption`, `Text/Overline`
- `Text/Button/Primary`, `Text/Button/Secondary`
- `Text/Label`, `Text/Helper`

#### 3. Create Effect Styles (Shadows)

**For each elevation:**
1. Create a rectangle
2. Apply shadow effect
3. Select → Right-click → "Add as style"

**Effect Style Names:**
- `Shadow/Elevation-1`
- `Shadow/Elevation-2`
- `Shadow/Elevation-3`
- `Shadow/Elevation-4`
- `Shadow/Elevation-5`

### Phase 2: Component Library

#### 1. Create Base Components

**Button Components:**
1. Create button frame (use Auto Layout)
2. Apply color, typography, spacing
3. Create variants for:
   - Type: Primary, Secondary, Text, Icon
   - Size: Small, Medium, Large
   - State: Default, Hover, Active, Disabled, Loading
4. Convert to component: `Button/Primary/Medium/Default`

**Component Structure:**
```
Components/
├── Button/
│   ├── Primary/
│   │   ├── Small/Default
│   │   ├── Small/Hover
│   │   ├── Medium/Default
│   │   ├── Medium/Hover
│   │   └── Large/Default
│   ├── Secondary/
│   └── Text/
├── Input/
│   ├── Text/Default
│   ├── Text/Error
│   ├── Text/Disabled
│   ├── Textarea/Default
│   └── Select/Default
├── Card/
│   ├── Standard/Default
│   ├── Standard/Hover
│   └── Compact/Default
├── Badge/
│   ├── Status/Success
│   ├── Status/Error
│   └── Count/Default
└── [Continue for all components]
```

#### 2. Component Variants Setup

**Using Figma Variants:**
1. Create base component
2. Select component → "Add variant" in right panel
3. Set up variant properties:
   - `Type`: Primary, Secondary, Text
   - `Size`: Small, Medium, Large
   - `State`: Default, Hover, Active, Disabled

**Example Variant Properties:**
```
Button Component
├── Type: Primary | Secondary | Text | Icon
├── Size: Small | Medium | Large
└── State: Default | Hover | Active | Disabled | Loading
```

#### 3. Create Composite Components

**Form Components:**
- Input with Label
- Input with Error Message
- Form Field Group
- Form Section

**Navigation Components:**
- Top Navigation Bar
- Sidebar Navigation Item
- Bottom Navigation Bar
- Breadcrumb

**Card Components:**
- Service Card
- Booking Card
- Product Card

### Phase 3: Web Platform Designs

#### 1. Home Page

**Layout:**
- Frame: 1440px width (desktop)
- Header: 64px height, sticky
- Hero Section: Full width
- Content: 1200px max-width container
- Footer: Full width

**Components to Use:**
- Navigation component
- Search bar component
- Service category cards
- Featured deals carousel
- Service cards grid
- Footer component

**Breakpoints:**
- Create frames for: Desktop (1440px), Tablet (768px), Mobile (375px)

#### 2. Booking Flow Pages

**For each service type (Flights, Hotels, etc.):**
1. Create page in "Web Platform" section
2. Design each screen in the flow
3. Use consistent components
4. Link screens in prototype mode

**Flight Booking Flow:**
- Flight Search Page
- Flight Results Page
- Flight Details Page
- Passenger Information Page
- Seat Selection Page
- Add-ons Page
- Review Page
- Payment Page
- Confirmation Page

#### 3. Responsive Design

**Create Responsive Variants:**
1. Design desktop version first
2. Duplicate frame for tablet
3. Adjust layout using constraints
4. Duplicate frame for mobile
5. Redesign for mobile (simplified)

**Use Auto Layout:**
- Enable Auto Layout on containers
- Set constraints properly
- Use "Fill container" for flexible elements
- Use "Fixed" for fixed-size elements

### Phase 4: Mobile App Designs

#### 1. Mobile Frame Setup

**Frame Sizes:**
- iPhone 14 Pro: 393 x 852px
- iPhone SE: 375 x 667px
- Android: 360 x 640px

**Use Standard Frame:**
- Create frame: 375px width (standard mobile)
- Height: 812px (iPhone standard)

#### 2. Mobile Components

**Create Mobile-Specific Components:**
- Bottom Navigation Bar
- Mobile Card (full width)
- Mobile Input (larger touch targets)
- Bottom Sheet
- Swipe Actions

#### 3. Mobile User Flows

**Design Complete Flows:**
- Home → Search → Results → Details → Booking → Payment → Confirmation
- Use prototype mode to link screens
- Add interactions and transitions

### Phase 5: Merchant Dashboard

#### 1. Dashboard Layout

**Layout Structure:**
- Sidebar: 256px width (expanded), 64px (collapsed)
- Main Content: Flexible width
- Header: 64px height

**Create:**
- Sidebar navigation component
- Dashboard header component
- Data table component
- Metric card component

#### 2. Service Management Screens

**Design:**
- Service list page
- Service creation form
- Service edit page
- Service detail view

**Use:**
- Form components
- Table components
- Modal components
- Status badges

#### 3. Booking Management

**Design:**
- Bookings list
- Booking details
- Calendar view
- Availability management

### Phase 6: Admin Dashboard

#### 1. Admin Layout

**Similar to Merchant but:**
- More navigation items
- More data tables
- More analytics components
- Advanced filters

#### 2. Management Screens

**Design:**
- User management
- Merchant management
- Booking oversight
- Service moderation
- Content management
- Financial management

### Phase 7: Prototypes

#### 1. Set Up Prototypes

**For each user flow:**
1. Select starting frame
2. Click "Prototype" tab
3. Connect frames with interactions
4. Set interaction details:
   - Trigger: On Click, On Drag, etc.
   - Action: Navigate to, Open Overlay, etc.
   - Animation: Instant, Smart Animate, etc.
   - Easing: Ease In, Ease Out, etc.

#### 2. Prototype Interactions

**Common Interactions:**
- Button click → Navigate to next screen
- Card tap → Open detail modal
- Form submit → Show success state
- Swipe → Navigate or dismiss
- Drag → Open bottom sheet

#### 3. Prototype Scenarios

**Create Complete Flows:**
1. Customer: Flight booking end-to-end
2. Customer: Multi-service cart checkout
3. Merchant: Service creation
4. Merchant: Booking management
5. Admin: Merchant approval
6. Admin: Booking oversight

## Component Organization Best Practices

### Naming Convention

**Format:** `[Platform]/[Category]/[Component]/[Variant]/[State]`

**Examples:**
- `Web/Button/Primary/Medium/Default`
- `Mobile/Card/Service/Hover`
- `Merchant/Table/Bookings/Empty`
- `Admin/Modal/Confirm/Error`

### Component Structure

**Organize by:**
1. Platform (Web, Mobile, Merchant, Admin)
2. Category (Button, Input, Card, etc.)
3. Component name
4. Variants
5. States

### Component Properties

**Use Component Properties for:**
- Text content (text layers)
- Boolean properties (show/hide layers)
- Instance swap (icon variants)
- Variant selection

**Example:**
```
Button Component Properties:
├── Label: "Button Text" (text)
├── Icon: Swap instance (icon component)
├── Show Icon: true/false (boolean)
└── Variant: Primary/Secondary/Text (variant)
```

## Auto Layout Guidelines

### When to Use Auto Layout

**Use for:**
- Buttons (padding, spacing)
- Cards (content spacing)
- Forms (field spacing)
- Navigation (item spacing)
- Lists (item spacing)

### Auto Layout Settings

**Direction:**
- Horizontal: For rows
- Vertical: For columns

**Spacing:**
- Use spacing tokens (4px, 8px, 16px, 24px)

**Padding:**
- Consistent padding values
- Use spacing scale

**Constraints:**
- Set "Fill container" for flexible elements
- Set "Fixed" for fixed-size elements

## Design Tokens in Figma

### Create Tokens File

**Structure:**
1. Create "Tokens" page
2. Organize by category:
   - Colors
   - Typography
   - Spacing
   - Border Radius
   - Shadows

**Documentation:**
- Add descriptions to each token
- Show usage examples
- Include code values (CSS, JSON)

## Responsive Design

### Breakpoint Frames

**Create frames for:**
- Mobile: 375px
- Tablet: 768px
- Desktop: 1440px

### Responsive Components

**Use Constraints:**
- Left/Right: For horizontal positioning
- Top/Bottom: For vertical positioning
- Left & Right: For horizontal stretching
- Top & Bottom: For vertical stretching
- Scale: For proportional scaling

### Responsive Variants

**Create component variants:**
- `Button/Mobile/Medium/Default`
- `Button/Desktop/Medium/Default`

## Collaboration Features

### Comments

**Use for:**
- Design feedback
- Questions
- Change requests
- Approval status

### Version History

**Best Practices:**
- Save versions at milestones
- Name versions descriptively
- Add version notes

### Sharing

**Share Settings:**
- View-only for stakeholders
- Edit access for team
- Developer handoff enabled

## Developer Handoff

### Prepare for Handoff

**1. Organize Layers:**
- Use clear naming
- Group related elements
- Remove unused layers

**2. Add Specifications:**
- Use "Inspect" panel
- Add notes for developers
- Specify interactions

**3. Export Assets:**
- Mark exportable layers
- Set export settings (1x, 2x, 3x)
- Use SVG for icons
- Use PNG/JPG for images

**4. Generate Code:**
- Use Figma's code generation
- Export CSS variables
- Export component code snippets

### Design Specs

**Include:**
- Spacing values
- Color codes
- Typography specs
- Border radius
- Shadow values
- Animation details

## Testing & Iteration

### Design Reviews

**Checklist:**
- [ ] All components use design system
- [ ] Colors match design system
- [ ] Typography is consistent
- [ ] Spacing follows scale
- [ ] All states are designed
- [ ] Responsive designs work
- [ ] Prototypes function correctly
- [ ] Accessibility considered

### User Testing

**Prototype Testing:**
- Share prototype links
- Gather feedback
- Iterate on designs
- Update components

## Final Checklist

### Before Handoff

- [ ] All pages designed
- [ ] All components created
- [ ] All variants defined
- [ ] All prototypes linked
- [ ] Design system complete
- [ ] Responsive designs complete
- [ ] All states designed
- [ ] Error states designed
- [ ] Empty states designed
- [ ] Loading states designed
- [ ] Documentation complete
- [ ] Assets exported
- [ ] Code specs ready
- [ ] Team access granted
- [ ] Version saved

## File Organization Tips

### Page Naming

**Use clear, descriptive names:**
- ✅ "Flight Booking Flow"
- ❌ "Page 1"

### Frame Naming

**Include context:**
- ✅ "Flight Search - Desktop"
- ❌ "Frame 123"

### Layer Naming

**Be specific:**
- ✅ "Button Primary Medium"
- ❌ "Rectangle 2"

### Group Organization

**Group logically:**
- Header
- Content
- Footer
- Sidebar

## Advanced Techniques

### Component Overrides

**Use for:**
- Text content changes
- Color variations
- Icon swaps
- Visibility toggles

### Smart Animate

**Use for:**
- Page transitions
- Modal animations
- State changes
- Micro-interactions

### Interactive Components

**Create for:**
- Toggle switches
- Tabs
- Dropdowns
- Accordions

## Maintenance

### Regular Updates

**Keep updated:**
- Design system
- Component library
- Documentation
- Prototypes

### Version Control

**Track changes:**
- Use version history
- Document major changes
- Communicate updates

### Team Sync

**Regular:**
- Design reviews
- Component updates
- System improvements
- Feedback integration

