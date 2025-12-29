# Shared Design System & Assets - Complete Specification

## Design Philosophy

### Core Principles
1. **Consistency**: Unified design language across all platforms
2. **Accessibility**: WCAG 2.1 AA compliance
3. **Scalability**: Reusable components that scale
4. **Clarity**: Clear visual hierarchy and information architecture
5. **Efficiency**: Streamlined user flows and interactions

## Color System

### Primary Palette

**Primary Colors:**
- `Primary-50`: #E3F2FD (Lightest)
- `Primary-100`: #BBDEFB
- `Primary-200`: #90CAF9
- `Primary-300`: #64B5F6
- `Primary-400`: #42A5F5
- `Primary-500`: #2196F3 (Base Primary)
- `Primary-600`: #1E88E5
- `Primary-700`: #1976D2
- `Primary-800`: #1565C0
- `Primary-900`: #0D47A1 (Darkest)

**Usage:**
- Primary-500: Main CTAs, links, active states
- Primary-700: Hover states, pressed states
- Primary-50: Backgrounds, subtle highlights
- Primary-900: Text on light backgrounds (when needed)

### Secondary Palette

**Secondary Colors:**
- `Secondary-50`: #E8F5E9
- `Secondary-100`: #C8E6C9
- `Secondary-200`: #A5D6A7
- `Secondary-300`: #81C784
- `Secondary-400`: #66BB6A
- `Secondary-500`: #4CAF50 (Base Secondary)
- `Secondary-600`: #43A047
- `Secondary-700`: #388E3C
- `Secondary-800`: #2E7D32
- `Secondary-900`: #1B5E20

**Usage:**
- Success states, confirmations
- Positive actions
- Status indicators

### Accent Colors

**Accent Orange:**
- `Accent-500`: #FF9500
- `Accent-600`: #FF8800
- `Accent-700`: #FF6F00

**Usage:**
- Highlights, special promotions
- Warning states (non-critical)

### Semantic Colors

**Success:**
- `Success-50`: #E8F5E9
- `Success-500`: #4CAF50
- `Success-700`: #388E3C

**Error:**
- `Error-50`: #FFEBEE
- `Error-500`: #F44336
- `Error-700`: #D32F2F

**Warning:**
- `Warning-50`: #FFF3E0
- `Warning-500`: #FF9800
- `Warning-700`: #F57C00

**Info:**
- `Info-50`: #E3F2FD
- `Info-500`: #2196F3
- `Info-700`: #1976D2

### Neutral Colors

**Grays:**
- `Gray-50`: #FAFAFA
- `Gray-100`: #F5F5F5
- `Gray-200`: #EEEEEE
- `Gray-300`: #E0E0E0
- `Gray-400`: #BDBDBD
- `Gray-500`: #9E9E9E
- `Gray-600`: #757575
- `Gray-700`: #616161
- `Gray-800`: #424242
- `Gray-900`: #212121

**Text Colors:**
- `Text-Primary`: #212121 (Gray-900)
- `Text-Secondary`: #757575 (Gray-600)
- `Text-Disabled`: #BDBDBD (Gray-400)
- `Text-On-Primary`: #FFFFFF
- `Text-On-Secondary`: #FFFFFF

**Background Colors:**
- `Background-Primary`: #FFFFFF
- `Background-Secondary`: #FAFAFA (Gray-50)
- `Background-Tertiary`: #F5F5F5 (Gray-100)
- `Background-Overlay`: rgba(0, 0, 0, 0.5)

**Border Colors:**
- `Border-Light`: #E0E0E0 (Gray-300)
- `Border-Medium`: #BDBDBD (Gray-400)
- `Border-Dark`: #757575 (Gray-600)

## Typography System

### Font Family

**Primary Font:**
- **Inter** (Web & Desktop)
  - Weights: 400 (Regular), 500 (Medium), 600 (SemiBold), 700 (Bold)

**Fallback Stack:**
- `-apple-system, BlinkMacSystemFont, 'Segoe UI', 'Roboto', 'Oxygen', 'Ubuntu', 'Cantarell', 'Fira Sans', 'Droid Sans', 'Helvetica Neue', sans-serif`

**Monospace (for code/data):**
- `'SF Mono', 'Monaco', 'Inconsolata', 'Fira Code', 'Droid Sans Mono', 'Courier New', monospace`

### Type Scale

**Desktop/Web:**
- `H1`: 48px / 56px (Bold, -0.5px letter-spacing)
- `H2`: 36px / 44px (Bold, -0.5px letter-spacing)
- `H3`: 28px / 36px (SemiBold, -0.25px letter-spacing)
- `H4`: 24px / 32px (SemiBold, -0.25px letter-spacing)
- `H5`: 20px / 28px (SemiBold)
- `H6`: 18px / 24px (SemiBold)
- `Body-Large`: 18px / 28px (Regular)
- `Body`: 16px / 24px (Regular)
- `Body-Small`: 14px / 20px (Regular)
- `Caption`: 12px / 16px (Regular)
- `Overline`: 10px / 16px (Medium, uppercase, 1.5px letter-spacing)

**Mobile:**
- `H1`: 32px / 40px (Bold)
- `H2`: 28px / 36px (Bold)
- `H3`: 24px / 32px (SemiBold)
- `H4`: 20px / 28px (SemiBold)
- `H5`: 18px / 24px (SemiBold)
- `H6`: 16px / 22px (SemiBold)
- `Body-Large`: 16px / 24px (Regular)
- `Body`: 14px / 20px (Regular)
- `Body-Small`: 12px / 18px (Regular)
- `Caption`: 11px / 16px (Regular)

### Text Styles

**Headings:**
- Use for page titles, section headers
- Maximum 2-3 heading levels per page
- Maintain hierarchy

**Body Text:**
- Primary content text
- Maximum line length: 75 characters (desktop)
- Maximum line length: 50 characters (mobile)

**Labels:**
- Form labels, field labels
- Use Body-Small or Caption
- Medium weight for emphasis

**Links:**
- Color: Primary-500
- Hover: Primary-700, underline
- Visited: Primary-600
- Focus: Outline with Primary-500

## Spacing System

### Base Unit
- **4px** base unit (all spacing multiples of 4)

### Spacing Scale
- `0`: 0px
- `1`: 4px
- `2`: 8px
- `3`: 12px
- `4`: 16px
- `5`: 20px
- `6`: 24px
- `8`: 32px
- `10`: 40px
- `12`: 48px
- `16`: 64px
- `20`: 80px
- `24`: 96px

### Usage Guidelines
- **Component Padding**: 16px (4), 24px (6)
- **Section Spacing**: 32px (8), 48px (12)
- **Page Margins**: 24px (6) mobile, 48px (12) desktop
- **Grid Gutter**: 24px (6)

## Border Radius

- `None`: 0px
- `Small`: 4px
- `Medium`: 8px
- `Large`: 12px
- `XLarge`: 16px
- `Round`: 50% (for circles)

### Usage
- **Buttons**: Medium (8px)
- **Cards**: Large (12px)
- **Inputs**: Medium (8px)
- **Badges**: Round (50%) or Small (4px)
- **Modals**: Large (12px)
- **Images**: Medium (8px) or Large (12px)

## Shadows & Elevation

### Shadow System
- `Elevation-0`: None
- `Elevation-1`: 0 1px 2px rgba(0, 0, 0, 0.05)
- `Elevation-2`: 0 2px 4px rgba(0, 0, 0, 0.08)
- `Elevation-3`: 0 4px 8px rgba(0, 0, 0, 0.12)
- `Elevation-4`: 0 8px 16px rgba(0, 0, 0, 0.15)
- `Elevation-5`: 0 16px 32px rgba(0, 0, 0, 0.2)

### Usage
- **Cards**: Elevation-2
- **Modals**: Elevation-4
- **Dropdowns**: Elevation-3
- **Sticky Headers**: Elevation-1
- **Floating Buttons**: Elevation-3

## Reusable UI Components

### Buttons

**Primary Button:**
- Background: Primary-500
- Text: White
- Padding: 12px 24px
- Height: 44px (mobile), 40px (desktop)
- Border Radius: Medium (8px)
- Font: Body, Medium weight
- States: Default, Hover (Primary-700), Active (Primary-800), Disabled (Gray-300, 50% opacity)

**Secondary Button:**
- Background: Transparent
- Border: 1px solid Primary-500
- Text: Primary-500
- Padding: 12px 24px
- Height: 44px (mobile), 40px (desktop)
- Border Radius: Medium (8px)
- States: Default, Hover (Primary-50 background), Active, Disabled

**Text Button:**
- Background: Transparent
- Text: Primary-500
- Padding: 8px 16px
- Height: Auto
- States: Default, Hover (Primary-50 background), Active, Disabled

**Icon Button:**
- Square: 40px x 40px (desktop), 44px x 44px (mobile)
- Circular or rounded square
- Icon size: 20px
- States: Default, Hover, Active, Disabled

### Input Fields

**Text Input:**
- Height: 44px (mobile), 40px (desktop)
- Padding: 12px 16px
- Border: 1px solid Border-Light
- Border Radius: Medium (8px)
- Background: Background-Primary
- Font: Body
- States:
  - Default: Border-Light
  - Focus: Border Primary-500, 2px outline Primary-500 (offset)
  - Error: Border Error-500
  - Disabled: Background Gray-100, Border Gray-300

**Textarea:**
- Min Height: 120px
- Padding: 12px 16px
- Same border and states as Text Input
- Resizable: Vertical only

**Select/Dropdown:**
- Same styling as Text Input
- Dropdown arrow icon
- Options: Hover state (Primary-50)

**Checkbox:**
- Size: 20px x 20px
- Border: 2px solid Border-Medium
- Border Radius: Small (4px)
- Checked: Primary-500 background, white checkmark
- Indeterminate: Primary-500 background, horizontal line

**Radio Button:**
- Size: 20px diameter
- Border: 2px solid Border-Medium
- Selected: Primary-500 fill, white center dot

**Switch/Toggle:**
- Width: 44px, Height: 24px
- Border Radius: Round
- Off: Gray-300 background
- On: Primary-500 background
- Thumb: 20px circle, white

### Cards

**Standard Card:**
- Background: Background-Primary
- Border Radius: Large (12px)
- Padding: 24px
- Shadow: Elevation-2
- Border: Optional 1px Border-Light

**Interactive Card:**
- Same as Standard Card
- Hover: Elevation-3, transform translateY(-2px)
- Cursor: Pointer
- Transition: 200ms ease

**Compact Card:**
- Padding: 16px
- Border Radius: Medium (8px)

### Badges

**Status Badge:**
- Height: 24px
- Padding: 4px 12px
- Border Radius: Round
- Font: Caption, Medium weight
- Colors:
  - Success: Success-500 background, white text
  - Error: Error-500 background, white text
  - Warning: Warning-500 background, white text
  - Info: Info-500 background, white text
  - Neutral: Gray-500 background, white text

**Count Badge:**
- Size: 20px diameter (min)
- Background: Error-500
- Text: White, Caption, Bold
- Position: Top-right of parent

### Navigation

**Top Navigation:**
- Height: 64px (desktop), 56px (mobile)
- Background: Background-Primary
- Shadow: Elevation-1 (when scrolled)
- Padding: 0 24px

**Sidebar Navigation:**
- Width: 256px (expanded), 64px (collapsed)
- Background: Background-Primary
- Border Right: 1px Border-Light
- Item Height: 48px
- Item Padding: 16px
- Active State: Primary-500 background, Primary-50 text

**Bottom Navigation (Mobile):**
- Height: 64px
- Background: Background-Primary
- Shadow: Elevation-2 (top)
- Item: Icon + Label

### Modals & Overlays

**Modal:**
- Width: 480px (small), 640px (medium), 800px (large)
- Max Width: 90vw
- Border Radius: Large (12px)
- Shadow: Elevation-5
- Background: Background-Primary
- Padding: 24px
- Backdrop: Background-Overlay

**Dialog:**
- Same as Modal
- Confirmation dialogs: 400px width

**Bottom Sheet (Mobile):**
- Full width
- Border Radius: Large (12px) top corners
- Max Height: 90vh
- Drag handle indicator

### Tables

**Table:**
- Border: 1px Border-Light
- Border Radius: Medium (8px)
- Header: Background Gray-50, SemiBold text
- Row Height: 56px
- Row Hover: Background Gray-50
- Padding: 16px
- Alternating rows: Optional (subtle background)

### Loading States

**Spinner:**
- Size: 16px (small), 24px (medium), 32px (large), 40px (xlarge)
- Color: Primary-500
- Animation: Rotate 360deg, 1s linear infinite
- Usage: 
  - Small: Inline with text
  - Medium: Buttons, cards
  - Large: Page sections
  - XLarge: Full-page loading

**Skeleton:**
- Background: Gray-200
- Border Radius: Medium (8px)
- Animation: Pulse (opacity 0.5 to 1, 1.5s ease-in-out infinite)
- Usage: Placeholder for content while loading
- Variants:
  - Text skeleton: Rounded rectangles
  - Image skeleton: Square/rectangle with aspect ratio
  - Card skeleton: Multiple elements combined
  - List skeleton: Multiple row placeholders

**Progress Bar:**
- Height: 4px (thin), 8px (thick)
- Background: Gray-200
- Fill: Primary-500
- Border Radius: Round
- Animation: Smooth fill animation
- Variants:
  - Determinate: Shows percentage complete
  - Indeterminate: Animated fill (pulsing)
  - Buffer: Shows buffered vs loaded content

**Loading Overlay:**
- Background: Background-Overlay (rgba(0, 0, 0, 0.5))
- Content: Centered spinner with message
- Spinner: 48px, Primary-500
- Message: Body text, white
- Usage: Full-screen blocking loader for critical operations

### Tooltips

**Tooltip:**
- Background: Gray-900
- Text: White, Caption
- Padding: 8px 12px
- Border Radius: Medium (8px)
- Max Width: 200px
- Arrow: 4px triangle

### Alerts & Notifications

**Alert:**
- Padding: 16px
- Border Radius: Medium (8px)
- Border Left: 4px solid (semantic color)
- Background: Semantic-50 (e.g., Error-50, Success-50)
- Text: Semantic-700 (e.g., Error-700, Success-700)
- Icon: Semantic-500, 20px, left side
- Dismissible: X button (top-right, optional)
- Variants:
  - Success: Green (Success-500 border, Success-50 background)
  - Error: Red (Error-500 border, Error-50 background)
  - Warning: Orange (Warning-500 border, Warning-50 background)
  - Info: Blue (Info-500 border, Info-50 background)

**Toast Notification:**
- Min Width: 300px
- Max Width: 400px
- Padding: 16px
- Border Radius: Medium (8px)
- Shadow: Elevation-3
- Position: Top-right (desktop), Bottom-center (mobile)
- Auto-dismiss: 3-5 seconds (configurable)
- Animation: Slide in from edge, fade out
- Content:
  - Icon: 20px, left side
  - Message: Body text
  - Action button: Optional, right side
  - Close button: Optional, top-right
- Variants: Success, Error, Warning, Info (same colors as Alerts)
- Stacking: Multiple toasts stack vertically with spacing

## Layout Guidelines

### Grid System

**Desktop:**
- Container Max Width: 1200px
- Columns: 12
- Gutter: 24px
- Margin: 0 auto

**Tablet:**
- Container Max Width: 768px
- Columns: 8
- Gutter: 24px

**Mobile:**
- Full width
- Padding: 16px
- Single column

### Breakpoints
- `xs`: 0px - 575px (Mobile)
- `sm`: 576px - 767px (Large Mobile)
- `md`: 768px - 991px (Tablet)
- `lg`: 992px - 1199px (Desktop)
- `xl`: 1200px - 1439px (Large Desktop)
- `xxl`: 1440px+ (Extra Large Desktop)

### Container Padding
- Mobile: 16px
- Tablet: 24px
- Desktop: 32px

## Interaction Guidelines

### Transitions
- **Duration**: 200ms (fast), 300ms (standard), 400ms (slow)
- **Easing**: ease-in-out (standard), ease-out (entrance), ease-in (exit)

### Hover States
- All interactive elements must have hover states
- Color change: 1 shade darker/lighter
- Elevation increase: +1 level
- Scale: 1.02x (subtle)

### Focus States
- Outline: 2px solid Primary-500
- Offset: 2px from element
- Required for accessibility

### Active/Pressed States
- Color: 1 shade darker than hover
- Scale: 0.98x (subtle press effect)

### Disabled States
- Opacity: 50%
- Cursor: not-allowed
- No interactions

## Accessibility Standards

### WCAG 2.1 AA Compliance

**Color Contrast:**
- Normal text: 4.5:1 minimum
- Large text (18px+): 3:1 minimum
- UI components: 3:1 minimum

**Touch Targets:**
- Minimum: 44px x 44px
- Spacing between targets: 8px minimum

**Keyboard Navigation:**
- All interactive elements keyboard accessible
- Tab order logical
- Focus indicators visible
- Skip links for main content

**Screen Readers:**
- Semantic HTML
- ARIA labels where needed
- Alt text for images
- Form labels associated

## Animation Guidelines

### Micro-interactions
- Button press: 100ms scale
- Card hover: 200ms elevation
- Loading: Continuous until complete
- Success: 300ms scale + fade

### Page Transitions
- Slide: 300ms ease-in-out
- Fade: 200ms ease-in-out
- Modal entrance: 300ms ease-out

### Performance
- Use transform and opacity for animations
- Avoid animating width, height, top, left
- 60fps target (16.67ms per frame)

## Icon System

### Icon Library
- **Style**: Outlined (primary), Filled (selected states)
- **Size**: 16px, 20px, 24px, 32px, 48px
- **Color**: Inherit from parent or use semantic colors
- **Stroke Width**: 1.5px (outlined), 2px (filled)

### Common Icons
- Navigation: Home, Search, Bookings, Profile
- Actions: Add, Edit, Delete, Save, Cancel
- Status: Success, Error, Warning, Info
- Services: Flight, Hotel, Car, Event, Spa
- UI: Chevron, Close, Menu, Filter, Sort

## Image Guidelines

### Aspect Ratios
- **Hero**: 16:9
- **Card**: 4:3 or 16:9
- **Thumbnail**: 1:1 (square)
- **Avatar**: 1:1 (circle)

### Image Sizes
- **Hero**: 1920px width
- **Card**: 800px width
- **Thumbnail**: 400px width
- **Avatar**: 200px width

### Formats
- **WebP** (primary)
- **JPEG** (fallback)
- **PNG** (transparency needed)
- **SVG** (icons, logos)

## Component Naming Convention

### Structure
`[Platform]/[Category]/[Component]/[Variant]/[State]`

**Examples:**
- `Web/Button/Primary/Default`
- `Mobile/Card/Service/Hover`
- `Merchant/Table/Bookings/Empty`
- `Admin/Modal/Confirm/Error`

### Variants
- Size: Small, Medium, Large
- State: Default, Hover, Active, Disabled, Loading, Error
- Type: Primary, Secondary, Tertiary

## Design Tokens

### Organization
- Colors
- Typography
- Spacing
- Border Radius
- Shadows
- Transitions
- Breakpoints

### Implementation
- CSS Variables (Web)
- JSON (Design tools)
- SCSS Variables
- Theme objects (React/Vue)

## Platform-Specific Adaptations

### Web
- Hover states
- Keyboard navigation
- Larger touch targets (optional)
- Desktop-optimized layouts

### Mobile
- Touch-optimized (44px minimum)
- Gesture support
- Bottom navigation
- Swipe actions
- Pull to refresh

### Tablet
- Hybrid approach
- Touch + hover
- Optimized layouts
- Responsive grids

