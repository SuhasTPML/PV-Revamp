# PV Website Navigation & UI Components
## Feature Document - UI Behavior & User Interactions

**Version**: 1.0  
**Date**: July 31, 2025  
**Audience**: Product Managers, QA Engineers, Developers

#### User Story 1.5: Desktop Mega-Menu Navigation
**As a** desktop user exploring category submenus  
**I want** subcategory links to navigate to specific content areas  
**So that** I can quickly access targeted content without multiple clicks

**Acceptance Criteria:**
- [ ] Mega-menu panel displays when main category is clicked (first click)
- [ ] Subcategory links in mega-menu navigate to L2 placeholder pages
- [ ] Hover effects provide visual feedback on interactive elements
- [ ] Menu remains open while user explores subcategory options
- [ ] Clicking outside menu or ESC key closes mega-menu
- [ ] Navigation maintains context of parent category

---

## 1. MAIN HEADER COMPONENT

### Epic: Primary Site Navigation and Branding

#### User Story 1.1: Header Layout and Branding
**As a** user visiting the website  
**I want** to see consistent branding and navigation options  
**So that** I can easily identify the site and access key functions

**Acceptance Criteria:**
- [ ] Logo (SVG) is prominently displayed on the left side
- [ ] Logo scales appropriately across different screen sizes
- [ ] Logo is clickable and links to homepage
- [ ] Desktop shows horizontal navigation menu with primary categories
- [ ] Mobile/tablet hides desktop navigation and shows hamburger menu
- [ ] Header height adapts responsively across devices

#### User Story 1.2: Header Action Buttons
**As a** user  
**I want** quick access to key site functions  
**So that** I can efficiently navigate to important areas

**Acceptance Criteria:**
- [ ] Search icon button visible on desktop/tablet (hidden on mobile)
- [ ] Login button displays "Login" text with consistent styling
- [ ] ePaper button shows newspaper icon + "Read ePaper" text
- [ ] Hamburger menu button (bars icon) positioned on far right
- [ ] All buttons have hover states with color transition
- [ ] Mobile buttons are appropriately sized for touch interaction

#### User Story 1.3: Responsive Header Behavior
**As a** user on different devices  
**I want** the header to adapt to my screen size  
**So that** all functions remain accessible and usable

**Acceptance Criteria:**
- [ ] Desktop (≥992px): Full navigation + all action buttons visible
- [ ] Tablet (768-991px): Condensed navigation + all action buttons
- [ ] Mobile (≤767px): Logo + essential buttons only (no search icon)
- [ ] Container padding adjusts appropriately for each screen size
- [ ] Text sizes scale appropriately for touch targets

#### User Story 1.4: Enhanced Desktop Navigation Click Behavior
**As a** desktop user  
**I want** intuitive navigation behavior for menu items with submenus  
**So that** I can either explore subcategories or navigate directly to main sections

**Acceptance Criteria:**
- [ ] First click on navigation item with submenus shows dropdown with subcategories
- [ ] Second click on same navigation item navigates to main section page
- [ ] Click tracking resets when clicking other menu items or pressing ESC
- [ ] Items without submenus navigate directly on first click
- [ ] Menu item maintains visual active state during interaction
- [ ] Click behavior works consistently across all navigation items
**As a** user on different devices  
**I want** the header to adapt to my screen size  
**So that** all functions remain accessible and usable

**Acceptance Criteria:**
- [ ] Desktop (≥992px): Full navigation + all action buttons visible
- [ ] Tablet (768-991px): Condensed navigation + all action buttons
- [ ] Mobile (≤767px): Logo + essential buttons only (no search icon)
- [ ] Container padding adjusts appropriately for each screen size
- [ ] Text sizes scale appropriately for touch targets

---

## 2. STICKY HEADER BEHAVIOR

### Epic: Persistent Navigation Access

#### User Story 2.1: Desktop Sticky Header
**As a** desktop user  
**I want** the main header to remain visible while scrolling  
**So that** I always have access to navigation and key functions

**Acceptance Criteria:**
- [ ] Header sticks to top of viewport on desktop and tablet
- [ ] Positioned with appropriate stacking order above content
- [ ] Subtle box shadow appears for visual separation
- [ ] No animation or transitions on desktop sticky behavior
- [ ] Header remains visible regardless of scroll direction

#### User Story 2.2: Mobile Header Behavior
**As a** mobile user  
**I want** the header to behave appropriately for mobile consumption  
**So that** I have maximum screen real estate for content

**Acceptance Criteria:**
- [ ] Main header is **not sticky** on mobile (`position: static`)
- [ ] Header scrolls out of view naturally when scrolling down
- [ ] No box shadow on mobile header
- [ ] Mobile menu bar becomes the sticky navigation element instead

---

## 3. FEATURED BAR COMPONENT

### Epic: Promoted Content Discovery

#### User Story 3.1: Desktop Featured Bar
**As a** desktop user  
**I want** to see featured content prominently below the main header  
**So that** I can quickly access highlighted topics and premium content

**Acceptance Criteria:**
- [ ] Positioned directly below main header with sticky behavior
- [ ] Bullhorn icon (fas fa-bullhorn) on left as visual indicator
- [ ] Horizontal list of featured items as styled chips/buttons
- [ ] "Premium" item highlighted with red background
- [ ] Other items have light gray background with hover effect
- [ ] Sticky positioning below header with appropriate stacking order

#### User Story 3.2: Featured Bar Scroll Behavior (Desktop)
**As a** desktop user scrolling content  
**I want** the featured bar to intelligently hide/show  
**So that** I get more screen space when reading but can easily access it

**Acceptance Criteria:**
- [ ] Hides when scrolling down past threshold with transform animation
- [ ] Shows when scrolling up with transform animation
- [ ] Smooth transition animation for hide/show behavior
- [ ] Uses vertical translation to hide completely
- [ ] Scroll direction detection prevents jittery behavior

#### User Story 3.3: Mobile Featured Bar Integration
**As a** mobile user  
**I want** access to featured content within the hamburger menu  
**So that** I can discover highlighted topics without cluttering the main interface

**Acceptance Criteria:**
- [ ] Featured bar appears inside hamburger menu overlay on mobile
- [ ] Positioned below the overlay header but above main navigation
- [ ] Same visual styling as desktop version (bullhorn icon + chips)
- [ ] No sticky behavior - scrolls with menu content
- [ ] Border styling: top and bottom borders for visual separation

---

## 4. HAMBURGER MENU (OVERLAY) COMPONENT

### Epic: Comprehensive Mobile Navigation

#### User Story 4.1: Menu Activation and Overlay
**As a** user  
**I want** to open a comprehensive navigation menu  
**So that** I can access all site sections and features

**Acceptance Criteria:**
- [ ] Triggered by hamburger icon in main header OR bottom nav menu button
- [ ] Full-screen overlay covering entire viewport
- [ ] Solid background with high stacking priority
- [ ] Open animation with opacity and visibility transitions
- [ ] Body scroll locked when menu is open
- [ ] ESC key closes the menu

#### User Story 4.2: Overlay Header Bar
**As a** user with the overlay menu open  
**I want** familiar branding and actions in the menu header  
**So that** I maintain context and can perform key actions

**Acceptance Criteria:**
- [ ] Same logo and layout as main header
- [ ] Desktop/tablet: Shows inline search input with appropriate width
- [ ] Mobile: Shows search icon that reveals search input when tapped
- [ ] Login and ePaper buttons maintain same styling
- [ ] Close button (X icon) positioned on far right
- [ ] Close button hover state: red color + light background

#### User Story 4.3: Two-Level Navigation Structure
**As a** user  
**I want** to navigate through main categories and their subcategories  
**So that** I can find specific content areas efficiently

**Acceptance Criteria:**
- [ ] Level 1: Main categories displayed as card-like tiles
- [ ] Each L1 item shows: Title (uppercase) + descriptive tagline
- [ ] L1 items arranged in responsive grid: 3 columns (desktop), 2 (tablet), 1 (mobile)
- [ ] Chevron down icon indicates expandable items
- [ ] Clicking L1 item expands to show L2 subcategories below the row
- [ ] L2 content: Full-width area with light background tint
- [ ] L2 items arranged in columns with category links
- [ ] L2 links navigate to dedicated L2 placeholder pages

#### User Story 4.4: Menu Animation Behavior
**As a** user  
**I want** smooth, professional animations when navigating the menu  
**So that** the experience feels polished and responsive

**Acceptance Criteria:**
- [ ] Desktop/tablet: Menu body slides down from top
- [ ] Mobile: Menu body slides in from right
- [ ] L1 expansion: Chevron rotates 180° with smooth timing
- [ ] L2 content expansion: Height animation with opacity fade
- [ ] L1 active state: Red border highlight + light background tint
- [ ] All transitions use consistent, smooth timing

#### User Story 4.5: Social Media Integration
**As a** user  
**I want** to access social media links from the menu  
**So that** I can follow the publication on various platforms

**Acceptance Criteria:**
- [ ] "Follow Us" section at bottom of menu
- [ ] Circular icon buttons for: Facebook, Twitter, Instagram, YouTube, Telegram, WhatsApp
- [ ] Icons arranged horizontally with consistent spacing
- [ ] Hover effect: red background + white icons
- [ ] Section separated with top border and appropriate spacing

#### User Story 4.6: Menu Search Functionality
**As a** mobile user  
**I want** to search within the overlay menu  
**So that** I can quickly find content without leaving the navigation context

**Acceptance Criteria:**
- [ ] Mobile: Search icon reveals full-width search input area
- [ ] Search input slides in from top with smooth animation
- [ ] Input placeholder: "ಪ್ರಜಾವಾಣಿಯಲ್ಲಿ ಹುಡುಕಿ..." (Kannada) or "Search Prajavani..." (English)
- [ ] Search button with magnifying glass icon
- [ ] Input styling: rounded left corners, button with rounded right corners

---

## 5. MOBILE MENU BAR COMPONENT

### Epic: Mobile Category Navigation

#### User Story 5.1: Mobile Category Strip
**As a** mobile user  
**I want** quick access to main content categories  
**So that** I can navigate between sections without opening the full menu

**Acceptance Criteria:**
- [ ] Horizontal scrollable strip below main header on mobile only
- [ ] Shows filtered categories marked with `showInMobileBar: true`
- [ ] Items distributed evenly across available width
- [ ] Active item highlighted with red text + red bottom border
- [ ] Smooth horizontal scrolling with hidden scrollbars
- [ ] Appropriately sized font with semibold weight
- [ ] Links navigate to corresponding L1 section pages

#### User Story 5.2: Mobile Menu Bar Sticky Behavior
**As a** mobile user scrolling content  
**I want** the category navigation to remain accessible  
**So that** I can switch between sections while reading

**Acceptance Criteria:**
- [ ] Sticky positioning at top of viewport
- [ ] Hides when scrolling down past threshold
- [ ] Shows when scrolling up
- [ ] Smooth transition animation
- [ ] Box shadow when sticky for visual separation
- [ ] Only affects mobile viewport (≤767px)

---

## 6. MOBILE BOTTOM NAVIGATION

### Epic: Mobile Primary Actions

#### User Story 6.1: Bottom Navigation Bar
**As a** mobile user  
**I want** persistent access to key site functions  
**So that** I can quickly navigate without scrolling back to top

**Acceptance Criteria:**
- [ ] Fixed bottom position (`position: fixed`) on mobile only
- [ ] Four equal-width items: Home, Podcasts, ePaper, Menu
- [ ] Each item: Icon (top) + label (bottom) in vertical layout
- [ ] Icons: home, podcast, newspaper, bars (Font Awesome)
- [ ] Hover/tap effect: red color transition
- [ ] Menu button opens hamburger overlay
- [ ] Background: white with top border + subtle shadow

#### User Story 6.2: Bottom Nav Scroll Behavior
**As a** mobile user scrolling content  
**I want** the bottom navigation to appear when I need it  
**So that** it doesn't interfere with content consumption but remains accessible

**Acceptance Criteria:**
- [ ] Hidden by default when main header is visible
- [ ] Shows when main header has scrolled out of view
- [ ] Hides when scrolling down, shows when scrolling up
- [ ] Smooth transition animation
- [ ] Slides below viewport when hidden
- [ ] Scroll direction logic includes threshold to prevent jitter

---

## 7. MOBILE BOTTOM AD SLOT

### Epic: Mobile Advertising Integration

#### User Story 7.1: Ad Container Positioning
**As a** mobile user  
**I want** ads to be clearly marked and positioned appropriately  
**So that** I understand they are advertisements and they don't disrupt navigation

**Acceptance Criteria:**
- [ ] Fixed position above bottom navigation bar
- [ ] "Advertisement" label with gray background and small text
- [ ] Ad content area: standard mobile banner size with centered alignment
- [ ] Placeholder shows dimensions when no ad content loaded
- [ ] Dashed border styling for empty ad container
- [ ] Only visible on mobile viewport (≤767px)

#### User Story 7.2: Ad Positioning Logic
**As a** mobile user  
**I want** the ad position to coordinate with bottom navigation  
**So that** both elements work together without overlap

**Acceptance Criteria:**
- [ ] Default: Positioned above bottom nav with appropriate spacing
- [ ] When bottom nav hidden: Repositions closer to bottom edge
- [ ] Position changes use CSS class toggles: `nav-hidden`
- [ ] Smooth position transitions for bottom value changes
- [ ] Ad visibility tied to header scroll position (same logic as bottom nav)

#### User Story 7.3: Ad Scroll Interaction
**As a** mobile user scrolling content  
**I want** ads to behave predictably with navigation elements  
**So that** the interface feels cohesive and professional

**Acceptance Criteria:**
- [ ] Hidden when main header is still visible
- [ ] Shows when main header scrolled out of view  
- [ ] Always visible once header is gone (doesn't hide on scroll down like nav)
- [ ] Coordinates with bottom nav: adjusts position when nav hides/shows
- [ ] Uses same scroll detection logic as other mobile elements

---

## 9. NAVIGATION & PLACEHOLDER PAGES

### Epic: Comprehensive Site Navigation Structure

#### User Story 9.1: L1 Section Pages (Main Categories)
**As a** user clicking on main navigation categories  
**I want** to be taken to dedicated section pages  
**So that** I can explore all content within that category

**Acceptance Criteria:**
- [ ] Desktop navigation: Second click on main category navigates to L1 page
- [ ] Mobile navigation: Direct click on category navigates to L1 page
- [ ] URL structure uses section parameter: `l1-placeholder.html?section={sectionId}`
- [ ] Page displays section title, description, and tagline
- [ ] Grid layout shows all subcategories as clickable cards
- [ ] Each subcategory card links to corresponding L2 page
- [ ] Page title updates to reflect current section
- [ ] Back to home navigation link provided

#### User Story 9.2: L2 Subsection Pages (Subcategories)
**As a** user clicking on subcategory links  
**I want** to be taken to specific subsection pages  
**So that** I can access targeted content areas

**Acceptance Criteria:**
- [ ] Accessible from L1 pages, desktop mega-menus, and mobile hamburger submenus
- [ ] URL structure uses section parameter: `l2-placeholder.html?section={subsectionId}`
- [ ] Page displays subsection title and parent section context
- [ ] Breadcrumb navigation: Home > Parent Section > Current Subsection
- [ ] Links to navigate back to parent L1 section
- [ ] Page title updates to include both L2 and L1 section names
- [ ] Content placeholder explains this is a subsection area

#### User Story 9.3: Dynamic Menu Highlighting
**As a** user on section or subsection pages  
**I want** the relevant navigation items to be visually highlighted  
**So that** I understand my current location in the site structure

**Acceptance Criteria:**
- [ ] L1 pages highlight corresponding desktop and mobile navigation items
- [ ] L2 pages highlight the parent L1 navigation items
- [ ] Highlighting removes default "News" highlighting when on other sections
- [ ] Visual highlighting uses red color and bottom border treatment
- [ ] Highlighting applies to both desktop and mobile navigation simultaneously
- [ ] State management resets highlighting when navigating between pages

#### User Story 9.4: Breadcrumb Navigation System  
**As a** user navigating deeper into the site structure  
**I want** clear breadcrumb navigation  
**So that** I can understand my location and navigate back efficiently

**Acceptance Criteria:**
- [ ] L1 pages show: Home > [Current Section]
- [ ] L2 pages show: Home > [Parent Section] > [Current Subsection]
- [ ] Each breadcrumb element is clickable and navigates to appropriate page
- [ ] Visual separator (›) between breadcrumb elements
- [ ] Current page element not clickable and styled differently
- [ ] Breadcrumbs positioned above main page content
- [ ] Responsive design maintains usability on mobile devices

#### User Story 9.5: Placeholder Content Management
**As a** user visiting incomplete sections  
**I want** clear communication about content availability  
**So that** I understand the site's development status and know when to return

**Acceptance Criteria:**
- [ ] Clear messaging that content is placeholder/coming soon
- [ ] Professional styling maintains brand consistency
- [ ] Informative content about what the section will contain
- [ ] Multiple navigation options to other areas of the site
- [ ] Error handling for invalid section parameters
- [ ] Graceful fallback to home page when sections not found
- [ ] Maintains full header/footer navigation functionality

---

### Epic: Intelligent UI Element Management

#### User Story 8.1: Mobile Scroll Direction Detection
**As a** mobile user  
**I want** UI elements to intelligently appear/disappear based on my scrolling  
**So that** I get maximum content space when reading but easy access when needed

**Acceptance Criteria:**
- [ ] Scroll direction detected with threshold to prevent premature hiding
- [ ] Small delay on direction change to prevent jittery behavior
- [ ] Throttled for smooth performance
- [ ] Only active on mobile viewport (≤767px)
- [ ] Elements affected: mobile menu bar, bottom nav, bottom ad

#### User Story 8.2: Desktop Featured Bar Scroll
**As a** desktop user  
**I want** the featured bar to hide when I'm focused on reading  
**So that** I get more screen space but can easily bring it back

**Acceptance Criteria:**
- [ ] Only active on desktop viewport (≥992px)
- [ ] Same scroll threshold and direction detection logic
- [ ] Uses vertical transform for smooth hiding
- [ ] Smooth transition animation
- [ ] Independent of other scroll behaviors

#### User Story 8.3: Responsive Behavior Reset
**As a** user resizing my browser or rotating my device  
**I want** scroll behaviors to reset appropriately  
**So that** UI elements display correctly for the new viewport

**Acceptance Criteria:**
- [ ] Window resize event (debounced) resets all scroll classes
- [ ] Mobile-specific classes removed when switching to desktop/tablet
- [ ] Desktop-specific classes removed when switching to mobile/tablet
- [ ] All elements return to default visible state after resize
- [ ] Scroll position tracking resets to current position

---

*This document focuses on user interactions and behaviors. Specific design measurements, timing values, and technical implementation details should be determined during the design and development phases based on platform standards and user testing results.*