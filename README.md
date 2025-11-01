# Test Product Landing Page - Maintenance & Customization Guide

Welcome! This comprehensive guide will help you maintain and customize your Test Product landing page. Whether you're updating text, fixing links, or adding new pages, you'll find clear, step-by-step instructions tailored to your specific HTML structure.

---

## Table of Contents

1. [Quick Start Guide](#quick-start-guide)
2. [Understanding Your Page Structure](#understanding-your-page-structure)
3. [Updating Text and Content](#updating-text-and-content)
4. [Modifying Tailwind CSS Classes](#modifying-tailwind-css-classes)
5. [Fixing and Managing Links](#fixing-and-managing-links)
6. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
7. [Troubleshooting Common Issues](#troubleshooting-common-issues)
8. [Best Practices](#best-practices)

---

## Quick Start Guide

### What You Need to Know

- **Your landing page is written in HTML** - a markup language that structures web content
- **Tailwind CSS** provides styling (colors, spacing, layout) using pre-built class names
- **You don't need to write CSS code** - Tailwind handles all the styling
- **Edit directly in your HTML file** - no special software required (use any text editor)

### How to Edit Your Page

1. Open `index.html` in a text editor (Notepad, VS Code, or any code editor)
2. Find the text or link you want to change
3. Make your edits
4. Save the file (Ctrl+S or Cmd+S)
5. Refresh your browser to see changes

---

## Understanding Your Page Structure

Your landing page consists of these main sections:

```
Header & Navigation (sticky at top)
    ↓
Hero Section (main banner with headline)
    ↓
Features Section (3 feature cards)
    ↓
Benefits Section (4 benefit items)
    ↓
Call-to-Action Section (background image)
    ↓
Testimonials Section (4 customer reviews)
    ↓
About Us Section (company information)
    ↓
Footer (links and company info)
```

Each section has an **ID** (like `id="features"`) that allows navigation links to jump to that section.

---

## Updating Text and Content

### Section 1: Header & Navigation

The header appears at the top of every page and stays visible when scrolling.

#### Changing the Logo Text

**Location:** Lines 28-31

**Current code:**
```html
<a href="#" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition-colors duration-300">
    <i class="fas fa-rocket mr-2"></i>Test Product
</a>
```

**How to change it:**

1. Find the text "Test Product" in the header
2. Replace it with your company name
3. **Example:** Change to "MyCompany" or "Analytics Pro"

```html
<a href="#" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition-colors duration-300">
    <i class="fas fa-rocket mr-2"></i>MyCompany
</a>
```

**Note:** The `<i class="fas fa-rocket mr-2"></i>` displays the rocket icon. See the "Changing Icons" section to modify this.

#### Updating Navigation Menu Items

**Location:** Lines 35-42 (desktop menu)

**Current code:**
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
<a href="#benefits" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Benefits</a>
<a href="#testimonials" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Testimonials</a>
<a href="#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About Us</a>
<a href="mailto:test@example.com" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Contact</a>
```

**How to change navigation text:**

1. Find each menu item text (Features, Benefits, etc.)
2. Replace with your preferred text
3. **Important:** Don't change the `href="#"` part - these link to sections below

**Example - Adding a new menu item:**
```html
<!-- Add this line after the "About Us" link -->
<a href="#pricing" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Pricing</a>
```

**Important:** If you add a new navigation link like `#pricing`, you must create a corresponding section below with `id="pricing"`. See the "Creating New Sections" section for details.

#### Changing the "Get Started" Button Text

**Location:** Line 43

**Current code:**
```html
<a href="https://example.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition-colors duration-300 scale-100 hover:scale-105">Get Started</a>
```

**How to change it:**

1. Find "Get Started" text
2. Replace with your preferred text (e.g., "Sign Up Now", "Try Free", "Book Demo")

```html
<a href="https://example.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition-colors duration-300 scale-100 hover:scale-105">Sign Up Now</a>
```

**Note:** Keep the same `href="https://example.com"` for now. See "Fixing Links" section to update the URL.

---

### Section 2: Hero Section (Main Banner)

The hero section is the large banner with your main headline and call-to-action buttons.

#### Updating the Main Headline

**Location:** Lines 65-68

**Current code:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Unlock Potential: Try Test Product Today!
</h1>
```

**How to change it:**

1. Replace the headline text with your own
2. Keep the HTML tags (`<h1>` and `</h1>`) - they define this as a main heading
3. The `class` attributes control styling - don't remove them

**Example:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight">
    Transform Your Business with Smart Analytics
</h1>
```

**Understanding the text size classes:**
- `text-4xl` = size on small screens (phones)
- `md:text-5xl` = size on medium screens (tablets)
- `lg:text-6xl` = size on large screens (desktops)

#### Updating the Subheadline

**Location:** Lines 70-73

**Current code:**
```html
<p class="text-xl md:text-2xl text-gray-700 leading-relaxed font-light">
    Discover a smarter way to achieve your desired outcome with Test Product. Ready to experience the difference?
</p>
```

**How to change it:**

1. Replace the text between `<p>` and `</p>`
2. Keep all the class names

**Example:**
```html
<p class="text-xl md:text-2xl text-gray-700 leading-relaxed font-light">
    Make data-driven decisions and watch your business grow. Get started in minutes.
</p>
```

#### Updating the Descriptive Paragraph

**Location:** Lines 75-78

**Current code:**
```html
<p class="text-lg text-gray-600 leading-relaxed">
    Transform your workflow with our cutting-edge solution designed for modern businesses. Test Product combines powerful analytics, seamless integration, and personalized insights to help you make better decisions faster.
</p>
```

**How to change it:**

Simply replace the text while keeping the `<p>` tags and class names.

#### Updating Call-to-Action Buttons

**Location:** Lines 80-90

**Button 1 - Primary Action (Blue Button)**

**Current code:**
```html
<a href="https://example.com" class="btn-primary bg-blue-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-blue-700 transition-all duration-300 inline-flex items-center justify-center hover:shadow-lg">
    <i class="fas fa-arrow-right mr-2"></i> Start Your Free Trial
</a>
```

**How to change button text:**

1. Replace "Start Your Free Trial" with your text
2. Keep the `<i class="fas fa-arrow-right mr-2"></i>` for the arrow icon
3. Or change the icon (see "Changing Icons" section)

**Example:**
```html
<a href="https://example.com" class="btn-primary bg-blue-600 text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-blue-700 transition-all duration-300 inline-flex items-center justify-center hover:shadow-lg">
    <i class="fas fa-play mr-2"></i> Start Now
</a>
```

**Button 2 - Secondary Action (White Button)**

**Current code:**
```html
<a href="#features" class="btn-primary border-2 border-blue-600 text-blue-600 px-8 py-4 rounded-lg font-bold text-lg hover:bg-blue-50 transition-all duration-300 inline-flex items-center justify-center">
    <i class="fas fa-play-circle mr-2"></i> Learn More
</a>
```

**How to change it:**

Replace "Learn More" with your preferred text, or change the link destination by modifying `href="#features"`.

#### Updating Statistics

**Location:** Lines 92-102

**Current code:**
```html
<div class="flex items-center space-x-6 pt-8">
    <div class="flex items-center">
        <span class="text-2xl font-bold text-blue-600">10K+</span>
        <span class="text-gray-600 ml-2">Active Users</span>
    </div>
    <div class="flex items-center">
        <span class="text-2xl font-bold text-blue-600">4.9/5</span>
        <span class="text-gray-600 ml-2">Average Rating</span>
    </div>
</div>
```

**How to update statistics:**

1. Change "10K+" to your number (e.g., "5K+", "50K+")
2. Change "Active Users" to your label
3. Change "4.9/5" to your rating
4. Change "Average Rating" to your label

**Example:**
```html
<div class="flex items-center space-x-6 pt-8">
    <div class="flex items-center">
        <span class="text-2xl font-bold text-blue-600">50K+</span>
        <span class="text-gray-600 ml-2">Happy Customers</span>
    </div>
    <div class="flex items-center">
        <span class="text-2xl font-bold text-blue-600">99.9%</span>
        <span class="text-gray-600 ml-2">Uptime</span>
    </div>
</div>
```

---

### Section 3: Features Section

This section displays three main features of your product.

#### Updating the Section Title

**Location:** Lines 114-120

**Current code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Powerful Features Built for Success
</h2>
<p class="text-xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
    Everything you need to streamline your operations and drive meaningful results. Our comprehensive feature set is designed with your success in mind.
</p>
```

**How to change it:**

Replace the heading and description text while keeping the HTML structure.

#### Updating Individual Feature Cards

Each feature card has three parts: **Icon**, **Title**, and **Description**.

**Feature 1: Seamless Integration**

**Location:** Lines 124-144

**Current structure:**
```html
<div class="feature-card bg-white rounded-xl p-8 border-2 border-gray-100 hover:border-blue-300 hover:shadow-xl">
    <!-- Icon -->
    <div class="bg-blue-100 rounded-lg w-16 h-16 flex items-center justify-center mb-6">
        <i class="fas fa-plug text-blue-600 text-2xl"></i>
    </div>
    
    <!-- Title -->
    <h3 class="text-2xl font-bold text-gray-900 mb-3">Seamless Integration</h3>
    
    <!-- Description -->
    <p class="text-gray-600 leading-relaxed mb-4">
        Connect Test Product with your existing tools in minutes...
    </p>
    
    <!-- Feature List -->
    <ul class="space-y-2 text-sm text-gray-700">
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> One-click integration</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Real-time data sync</li>
        <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Zero downtime setup</li>
    </ul>
</div>
```

**How to update Feature 1:**

1. **Change the title:**
   ```html
   <h3 class="text-2xl font-bold text-gray-900 mb-3">Your New Title Here</h3>
   ```

2. **Change the description:**
   ```html
   <p class="text-gray-600 leading-relaxed mb-4">
       Your new description text here...
   </p>
   ```

3. **Change the feature list items:**
   ```html
   <ul class="space-y-2 text-sm text-gray-700">
       <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Your first benefit</li>
       <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Your second benefit</li>
       <li class="flex items-center"><i class="fas fa-check text-green-500 mr-2"></i> Your third benefit</li>
   </ul>
   ```

4. **Change the icon:** See "Changing Icons" section below.

**Feature 2 & 3:** Follow the same pattern for the other two feature cards (Lines 146-166 and 168-188).

#### Changing Icons

Icons come from Font Awesome. To change an icon:

1. Visit [Font Awesome Icons](https://fontawesome.com/icons)
2. Search for your desired icon
3. Note the icon name (e.g., "chart-bar", "cog", "lock")
4. Replace the current icon class

**Current Feature 1 icon:**
```html
<i class="fas fa-plug text-blue-600 text-2xl"></i>
```

**Example - Change to a settings icon:**
```html
<i class="fas fa-cog text-blue-600 text-2xl"></i>
```

**Example - Change to a lock icon:**
```html
<i class="fas fa-lock text-blue-600 text-2xl"></i>
```

**The pattern:** `fas fa-[icon-name]`
- `fas` = Font Awesome Solid (always include this)
- `fa-[icon-name]` = The specific icon

---

### Section 4: Benefits Section

This section highlights business benefits with icons and descriptions.

#### Updating the Section Title

**Location:** Lines 192-198

**Current code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    Transform Your Business with Real Results
</h2>
<p class="text-xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
    See measurable improvements across every aspect of your operations. Our clients report significant gains in efficiency, accuracy, and profitability.
</p>
```

**How to change it:**

Replace the heading and description text.

#### Updating Individual Benefits

**Benefit 1: Save 40% More Time**

**Location:** Lines 202-217

**Current structure:**
```html
<div class="flex gap-6 items-start">
    <!-- Icon -->
    <div class="flex-shrink-0">
        <div class="flex items-center justify-center h-12 w-12 rounded-md bg-blue-600 text-white">
            <i class="fas fa-clock text-xl"></i>
        </div>
    </div>
    
    <!-- Content -->
    <div>
        <h3 class="text-2xl font-bold text-gray-900 mb-2">Save 40% More Time</h3>
        <p class="text-gray-600 leading-relaxed">
            Automate repetitive tasks and streamline your workflow...
        </p>
    </div>
</div>
```

**How to update:**

1. **Change the title:**
   ```html
   <h3 class="text-2xl font-bold text-gray-900 mb-2">Your Benefit Title</h3>
   ```

2. **Change the description:**
   ```html
   <p class="text-gray-600 leading-relaxed">
       Your benefit description here...
   </p>
   ```

3. **Change the icon:**
   ```html
   <i class="fas fa-your-icon-name text-xl"></i>
   ```

**Benefits 2, 3, and 4:** Follow the same pattern for the remaining benefits (Lines 219-234, 236-251, 253-268).

---

### Section 5: Call-to-Action (CTA) Section

This is the section with a background image and large heading.

#### Updating the CTA Headline

**Location:** Lines 274-277

**Current code:**
```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white leading-tight tracking-tight">
    Ready to Transform Your Business?
</h2>
```

**How to change it:**

Replace the text between `<h2>` and `</h2>`.

```html
<h2 class="text-4xl md:text-5xl lg:text-6xl font-bold text-white leading-tight tracking-tight">
    Start Your Free Trial Today
</h2>
```

#### Updating the CTA Description

**Location:** Lines 278-280

**Current code:**
```html
<p class="text-xl md:text-2xl text-gray-100 max-w-2xl mx-auto leading-relaxed">
    Join thousands of successful companies already using Test Product to drive growth and innovation. Start your free trial today with no credit card required.
</p>
```

**How to change it:**

Replace the text while keeping the tags and classes.

#### Updating CTA Buttons

**Location:** Lines 281-291

**Button 1 - Primary (White Button):**
```html
<a href="https://example.com" class="btn-primary bg-white text-blue-600 px-8 py-4 rounded-lg font-bold text-lg hover:bg-gray-100 transition-all duration-300 inline-flex items-center justify-center hover:shadow-xl">
    <i class="fas fa-play-circle mr-2"></i> Start Free Trial
</a>
```

**Button 2 - Secondary (Bordered Button):**
```html
<a href="mailto:test@example.com" class="btn-primary border-2 border-white text-white px-8 py-4 rounded-lg font-bold text-lg hover:bg-white hover:text-blue-600 transition-all duration-300 inline-flex items-center justify-center">
    <i class="fas fa-envelope mr-2"></i> Schedule Demo
</a>
```

**How to update:**

Replace the button text and/or icon. Keep the `href` values for now (see "Fixing Links" section).

---

### Section 6: Testimonials Section

Customer testimonials are displayed in card format.

#### Updating the Section Title

**Location:** Lines 302-308

**Current code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    What Our Customers Say
</h2>
<p class="text-xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
    Hear from real users about how Test Product has transformed their business operations and delivered measurable results.
</p>
```

**How to change it:**

Replace the heading and description.

#### Updating Individual Testimonials

**Testimonial 1: Sarah Mitchell**

**Location:** Lines 312-333

**Current structure:**
```html
<div class="testimonial-card bg-white rounded-xl p-8 border-2 border-gray-100 hover:border-blue-300 hover:shadow-xl">
    <!-- Star Rating -->
    <div class="flex items-center mb-4">
        <div class="flex text-yellow-400">
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
            <i class="fas fa-star"></i>
        </div>
    </div>
    
    <!-- Quote -->
    <p class="text-gray-700 leading-relaxed mb-6 text-lg">
        "Test Product has been a game-changer..."
    </p>
    
    <!-- Author Info -->
    <div class="border-t border-gray-200 pt-4">
        <p class="font-bold text-gray-900">Sarah Mitchell</p>
        <p class="text-gray-600">Operations Manager, TechCorp Solutions</p>
    </div>
</div>
```

**How to update a testimonial:**

1. **Change the quote text:**
   ```html
   <p class="text-gray-700 leading-relaxed mb-6 text-lg">
       "Your customer's testimonial quote here..."
   </p>
   ```

2. **Change the customer name:**
   ```html
   <p class="font-bold text-gray-900">Customer Name</p>
   ```

3. **Change the customer title/company:**
   ```html
   <p class="text-gray-600">Job Title, Company Name</p>
   ```

4. **Change the star rating:** Add or remove `<i class="fas fa-star"></i>` lines
   - 5 stars = 5 lines
   - 4 stars = 4 lines
   - etc.

**Testimonials 2, 3, and 4:** Follow the same pattern (Lines 335-356, 358-379, 381-402).

---

### Section 7: About Us Section

This section contains company information.

#### Updating the Section Title

**Location:** Lines 412-418

**Current code:**
```html
<h2 class="text-4xl md:text-5xl font-bold text-gray-900 mb-4 tracking-tight">
    About Test Product
</h2>
<p class="text-xl text-gray-600 max-w-2xl mx-auto leading-relaxed">
    Learn about our journey, mission, and commitment to excellence in business intelligence.
</p>
```

**How to change it:**

Replace the heading and description.

#### Updating the "Our Story" Section

**Location:** Lines 424-436

**Current code:**
```html
<div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Story</h3>
    <p class="text-gray-700 leading-relaxed text-lg">
        Founded in 2018 by a team of data scientists and business strategists...
    </p>
</div>
```

**How to change it:**

1. **Change the subheading:**
   ```html
   <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Company History</h3>
   ```

2. **Change the story text:**
   ```html
   <p class="text-gray-700 leading-relaxed text-lg">
       Your company story here...
   </p>
   ```

#### Updating the "Our Mission & Values" Section

**Location:** Lines 440-452

**Current code:**
```html
<div>
    <h3 class="text-2xl font-bold text-gray-900 mb-4">Our Mission & Values</h3>
    <p class="text-gray-700 leading-relaxed text-lg">
        Our mission is to empower every organization...
    </p>
</div>
```

**How to change it:**

Follow the same pattern as the "Our Story" section above.

---

### Section 8: Footer

The footer contains company information, links, and social media.

#### Updating Company Info

**Location:** Lines 462-483

**Current code:**
```html
<h3 class="text-xl font-bold text-white mb-6 flex items-center">
    <i class="fas fa-rocket text-blue-400 mr-2"></i> Test Product
</h3>
<p class="text-gray-400 leading-relaxed mb-6">
    Empowering businesses with advanced analytics and intelligent insights since 2018.
</p>
```

**How to update:**

1. **Change company name:**
   ```html
   <h3 class="text-xl font-bold text-white mb-6 flex items-center">
       <i class="fas fa-rocket text-blue-400 mr-2"></i> Your Company Name
   </h3>
   ```

2. **Change company description:**
   ```html
   <p class="text-gray-400 leading-relaxed mb-6">
       Your company description here...
   </p>
   ```

#### Updating Footer Column Headings and Links

**Location:** Lines 485-537

The footer has four columns:
1. **Product** - Links to product pages
2. **Company** - Links to company pages
3. **Legal & Support** - Links to policies and support

**How to update a column:**

**Example - Updating "Product" column:**

**Current code:**
```html
<div>
    <h4 class="text-lg font-bold text-white mb-6">Product</h4>
    <ul class="space-y-3">
        <li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
        <li><a href="#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Pricing</a></li>
        ...
    </ul>
</div>
```

**To change a link:**

1. **Change the link text:**
   ```html
   <li><a href="#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Our Features</a></li>
   ```

2. **Change the link destination:** See "Fixing Links" section below.

3. **Add a new link:**
   ```html
   <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">New Link</a></li>
   ```

#### Updating Social Media Links

**Location:** Lines 474-483

**Current code:**
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
        <i class="fab fa-facebook-f text-lg"></i>
    </a>
    <a href="#" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
        <i class="fab fa-twitter text-lg"></i>
    </a>
    ...
</div>
```

**How to update social links:**

1. **Change the URL:**
   ```html
   <a href="https://facebook.com/yourpage" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
       <i class="fab fa-facebook-f text-lg"></i>
   </a>
   ```

2. **Add a new social link:**
   ```html
   <a href="https://youtube.com/yourchannel" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">
       <i class="fab fa-youtube text-lg"></i>
   </a>
   ```

#### Updating Copyright Year

**Location:** Lines 540-549

**Current code:**
```html
<p class="text-gray-400 text-sm">
    &copy; 2025 Test Product. All rights reserved.
</p>
```

**How to change it:**

Replace "2025" and "Test Product" with your year and company name:

```html
<p class="text-gray-400 text-sm">
    &copy; 2024 MyCompany. All rights reserved.
</p>
```

---

## Modifying Tailwind CSS Classes

### Understanding Tailwind Classes

Tailwind CSS uses class names to apply styles. You don't write CSS code—you just add class names to HTML elements.

**Example:**
```html
<div class="bg-blue-600 text-white px-8 py-4 rounded-lg">
    Content here
</div>
```

This means:
- `bg-blue-600` = Blue background
- `text-white` = White text
- `px-8` = Horizontal padding (left & right)
- `py-4` = Vertical padding (top & bottom)
- `rounded-lg` = Rounded corners

### Common Tailwind Classes Used in Your Page

#### Colors

**Background Colors:**
- `bg-white` = White background
- `bg-blue-600` = Blue background
- `bg-gray-50` = Light gray background
- `bg-gray-900` = Dark gray/black background

**Text Colors:**
- `text-white` = White text
- `text-gray-900` = Dark text
- `text-gray-600` = Medium gray text
- `text-blue-600` = Blue text

**Example - Change a button color:**

**Current (blue button):**
```html
<a href="#" class="bg-blue-600 text-white px-8 py-4 rounded-lg">Button</a>
```

**Change to green:**
```html
<a href="#" class="bg-green-600 text-white px-8 py-4 rounded-lg">Button</a>
```

**Change to red:**
```html
<a href="#" class="bg-red-600 text-white px-8 py-4 rounded-lg">Button</a>
```

#### Spacing (Padding & Margins)

**Padding (space inside):**
- `px-4` = Horizontal padding (small)
- `px-8` = Horizontal padding (large)
- `py-2` = Vertical padding (small)
- `py-4` = Vertical padding (large)

**Margins (space outside):**
- `mb-4` = Margin bottom
- `mt-4` = Margin top
- `ml-2` = Margin left
- `mr-2` = Margin right

#### Size and Spacing Scale

Tailwind uses a scale system:
- `2` = 0.5rem (small)
- `4` = 1rem (medium)
- `6` = 1.5rem
- `8` = 2rem (large)
- `12` = 3rem (extra large)

#### Typography (Text Sizing)

- `text-sm` = Small text (14px)
- `text-base` = Normal text (16px)
- `text-lg` = Large text (18px)
- `text-xl` = Extra large (20px)
- `text-2xl` = 2x large (24px)
- `text-4xl` = 4x large (36px)
- `text-5xl` = 5x large (48px)
- `text-6xl` = 6x large (60px)

**Example - Make a heading smaller:**

**Current:**
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Headline</h1>
```

**Make it smaller:**
```html
<h1 class="text-3xl md:text-4xl lg:text-5xl font-bold">Headline</h1>
```

#### Font Weight

- `font-light` = Thin text
- `font-normal` = Regular text
- `font-semibold` = Semi-bold text
- `font-bold` = Bold text

#### Rounded Corners

- `rounded` = Slightly rounded
- `rounded-lg` = Medium rounded
- `rounded-xl` = More rounded
- `rounded-full` = Completely rounded (circle)

#### Hover Effects

Tailwind classes that start with `hover:` apply when you hover over the element.

**Example:**
```html
<a href="#" class="text-gray-700 hover:text-blue-600">Link</a>
```

This means:
- Normal state: Gray text
- When hovering: Blue text

#### Responsive Design

Tailwind uses prefixes for different screen sizes:
- No prefix = All screen sizes
- `sm:` = Small screens (640px+)
- `md:` = Medium screens (768px+)
- `lg:` = Large screens (1024px+)
- `xl:` = Extra large (1280px+)

**Example:**
```html
<h1 class="text-2xl md:text-4xl lg:text-6xl">
    Responsive Headline
</h1>
```

This means:
- Small screens: 2xl size
- Medium screens: 4xl size
- Large screens: 6xl size

### Common Customizations

#### Changing Button Colors

**Find the button you want to change** and modify the `bg-` class.

**Example - Change primary button from blue to purple:**

**Current:**
```html
<a href="#" class="bg-blue-600 text-white px-8 py-4 rounded-lg hover:bg-blue-700">
    Get Started
</a>
```

**Change to purple:**
```html
<a href="#" class="bg-purple-600 text-white px-8 py-4 rounded-lg hover:bg-purple-700">
    Get Started
</a>
```

**Note:** Change both `bg-blue-600` and `hover:bg-blue-700` to the same color family.

#### Changing Text Colors

**Find the text element** and modify the `text-` class.

**Example - Change headline color from gray to blue:**

**Current:**
```html
<h1 class="text-gray-900">Your Headline</h1>
```

**Change to blue:**
```html
<h1 class="text-blue-900">Your Headline</h1>
```

#### Adjusting Spacing

**Find the element** and modify padding (`p`, `px`, `py`) or margin (`m`, `mx`, `my`) classes.

**Example - Add more spacing around a button:**

**Current:**
```html
<a href="#" class="px-8 py-4">Button</a>
```

**Increase spacing:**
```html
<a href="#" class="px-12 py-6">Button</a>
```

#### Making Text Larger or Smaller

**Find the text** and modify the `text-` class.

**Example - Make feature titles larger:**

**Current:**
```html
<h3 class="text-2xl font-bold">Feature Title</h3>
```

**Make larger:**
```html
<h3 class="text-3xl font-bold">Feature Title</h3>
```

**Make smaller:**
```html
<h3 class="text-xl font-bold">Feature Title</h3>
```

#### Changing Border Colors

**Find the element** and modify the `border-` class.

**Example - Change feature card border:**

**Current:**
```html
<div class="border-2 border-gray-100 hover:border-blue-300">...</div>
```

**Change to red:**
```html
<div class="border-2 border-red-100 hover:border-red-300">...</div>
```

#### Hiding Elements on Certain Screen Sizes

Use `hidden` and responsive prefixes.

**Example - Hide something on mobile, show on desktop:**

```html
<div class="hidden lg:block">
    This only shows on large screens
</div>
```

**Example - Show on mobile, hide on desktop:**

```html
<div class="block lg:hidden">
    This only shows on mobile
</div>
```

### Color Palette Reference

**Blues:** `blue-100`, `blue-300`, `blue-400`, `blue-600`, `blue-700`, `blue-900`

**Grays:** `gray-50`, `gray-100`, `gray-300`, `gray-400`, `gray-600`, `gray-700`, `gray-800`, `gray-900`

**Greens:** `green-100`, `green-500`, `green-600`

**Reds:** `red-100`, `red-300`, `red-600`

**Yellows:** `yellow-400`

**Purples:** `purple-600`, `purple-700`

For a complete list, visit [Tailwind Color Reference](https://tailwindcss.com/docs/customizing-colors).

---

## Fixing and Managing Links

### Understanding Links in Your Page

Links direct users to different pages or sections. Your page has several types of links:

1. **Internal section links** - Jump to sections on the same page (e.g., `#features`)
2. **External links** - Go to other websites (e.g., `https://example.com`)
3. **Email links** - Open email client (e.g., `mailto:test@example.com`)

### Current Links That Need Updating

Here are all the links in your page that likely need to be updated:

| Location | Current Link | Type | Needs Update |
|----------|--------------|------|--------------|
| Header "Get Started" | `https://example.com` | External | ✓ |
| Hero "Start Your Free Trial" | `https://example.com` | External | ✓ |
| Hero "Learn More" | `#features` | Internal | Usually OK |
| CTA "Start Free Trial" | `https://example.com` | External | ✓ |
| CTA "Schedule Demo" | `mailto:test@example.com` | Email | ✓ |
| Footer "Pricing" | `https://example.com` | External | ✓ |
| Footer "Security" | `https://example.com` | External | ✓ |
| Footer "Integrations" | `https://example.com` | External | ✓ |
| Footer "Blog" | `blog.html` | Internal | ✓ |
| Footer "Careers" | `https://example.com` | External | ✓ |
| Footer "Press" | `https://example.com` | External | ✓ |
| Footer "Contact" | `mailto:test@example.com` | Email | ✓ |
| Footer "Privacy Policy" | `privacy.html` | Internal | ✓ |
| Footer "Terms of Service" | `terms.html` | Internal | ✓ |
| Footer "Cookie Policy" | `https://example.com` | External | ✓ |
| Footer "Support Center" | `https://example.com` | External | ✓ |
| Footer "Documentation" | `https://example.com` | External | ✓ |

### Step-by-Step: Update External Links

**Example: Update the "Get Started" button**

1. **Find the link in your HTML:**
   ```html
   <a href="https://example.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition-colors duration-300 scale-100 hover:scale-105">Get Started</a>
   ```

2. **Identify the `href` attribute:**
   - `href="https://example.com"` is what needs changing

3. **Replace with your actual URL:**
   ```html
   <a href="https://yourcompany.com/signup" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition-colors duration-300 scale-100 hover:scale-105">Get Started</a>
   ```

4. **Save the file** (Ctrl+S or Cmd+S)

5. **Test the link** by clicking it in your browser

**Common URLs to update:**

| Link Name | Example URL |
|-----------|------------|
| Get Started / Sign Up | `https://yourcompany.com/signup` |
| Try Free / Free Trial | `https://yourcompany.com/trial` |
| Schedule Demo | `https://yourcompany.com/demo` |
| Pricing | `https://yourcompany.com/pricing` |
| Blog | `https://yourcompany.com/blog` |
| Careers | `https://yourcompany.com/careers` |
| Contact | `https://yourcompany.com/contact` |

### Step-by-Step: Update Email Links

**Example: Update the "Contact" email link**

1. **Find the email link:**
   ```html
   <a href="mailto:test@example.com" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Contact</a>
   ```

2. **Replace with your email:**
   ```html
   <a href="mailto:your-email@yourcompany.com" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Contact</a>
   ```

3. **Test:** Click the link to verify it opens your email client

**All email links to update:**

**Header:**
- Line 41: `mailto:test@example.com` → `mailto:your-email@yourcompany.com`

**CTA Section:**
- Line 289: `mailto:test@example.com` → `mailto:your-email@yourcompany.com`

**Footer:**
- Line 515: `mailto:test@example.com` → `mailto:your-email@yourcompany.com`

### Step-by-Step: Update Internal Links (Same Page)

Internal links use `#` to jump to sections on the same page. These usually don't need changing, but here's how if needed:

**Example: Navigation link to Features section**

**Current:**
```html
<a href="#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
```

This links to the section with `id="features"` (Line 113).

**If you rename the section:**

1. **Find the section ID:**
   ```html
   <section id="features" class="py-24 md:py-32 bg-white">
   ```

2. **Change the ID:**
   ```html
   <section id="our-features" class="py-24 md:py-32 bg-white">
   ```

3. **Update all links pointing to it:**
   ```html
   <a href="#our-features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
   ```

**Important:** Always update both the `id=` and all `href="#"` that reference it.

### Complete Link Update Checklist

Use this checklist to ensure all links are updated:

**Header Navigation (Lines 35-43):**
- [ ] "Features" link → `#features` (usually OK)
- [ ] "Benefits" link → `#benefits` (usually OK)
- [ ] "Testimonials" link → `#testimonials` (usually OK)
- [ ] "About Us" link → `#about` (usually OK)
- [ ] "Contact" link → Update email to `mailto:your-email@yourcompany.com`
- [ ] "Get Started" button → Update to your signup URL

**Mobile Menu (Lines 50-57):**
- [ ] Same as desktop menu above

**Hero Section (Lines 80-90):**
- [ ] "Start Your Free Trial" button → Update to your signup URL
- [ ] "Learn More" button → `#features` (usually OK)

**CTA Section (Lines 281-291):**
- [ ] "Start Free Trial" button → Update to your signup URL
- [ ] "Schedule Demo" button → Update email to `mailto:your-email@yourcompany.com`

**Footer - Product Column (Lines 495-502):**
- [ ] "Features" → `#features` (usually OK)
- [ ] "Benefits" → `#benefits` (usually OK)
- [ ] "Pricing" → Update to your pricing page URL
- [ ] "Security" → Update to your security page URL
- [ ] "Integrations" → Update to your integrations page URL

**Footer - Company Column (Lines 504-511):**
- [ ] "About Us" → `#about` (usually OK)
- [ ] "Blog" → Update to `blog.html` or your blog URL
- [ ] "Careers" → Update to your careers page URL
- [ ] "Press" → Update to your press page URL
- [ ] "Contact" → Update email to `mailto:your-email@yourcompany.com`

**Footer - Legal Column (Lines 513-520):**
- [ ] "Privacy Policy" → Update to `privacy.html` or your privacy page URL
- [ ] "Terms of Service" → Update to `terms.html` or your terms page URL
- [ ] "Cookie Policy" → Update to your cookie policy URL
- [ ] "Support Center" → Update to your support URL
- [ ] "Documentation" → Update to your documentation URL

**Footer - Bottom Links (Lines 543-548):**
- [ ] "Privacy" → Update to `privacy.html` or your privacy page URL
- [ ] "Terms" → Update to `terms.html` or your terms page URL
- [ ] "Blog" → Update to `blog.html` or your blog URL

### Troubleshooting Link Issues

**Problem: Link doesn't work**

1. **Check for typos** in the URL
   - `https://example.com` ✓ Correct
   - `https://example.co` ✗ Wrong (missing 'm')

2. **Ensure external URLs start with `https://`**
   - `example.com` ✗ Won't work
   - `https://example.com` ✓ Correct

3. **For email links, use `mailto:`**
   - `test@example.com` ✗ Won't work
   - `mailto:test@example.com` ✓ Correct

4. **For internal links, check the section ID exists**
   - `href="#features"` requires `<section id="features">`
   - If the ID doesn't exist, the link won't work

**Problem: Email link doesn't open email client**

- Make sure you used `mailto:` prefix
- Correct: `href="mailto:your-email@yourcompany.com"`
- Incorrect: `href="your-email@yourcompany.com"`

**Problem: Internal link jumps to wrong section**

- Verify the section ID matches the link
- Link: `href="#benefits"`
- Section must have: `id="benefits"`

---

## Adding Privacy and Terms Pages

Your landing page currently links to `privacy.html` and `terms.html` in the footer, but these files don't exist yet. This section shows you how to create them.

### Step 1: Create the Privacy Policy Page

1. **Create a new file** named `privacy.html` in the same folder as `index.html`

2. **Copy this template code** into `privacy.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Privacy Policy for Test Product">
    <title>Privacy Policy | Test Product</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <a href="index.html" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition-colors duration-300">
                    <i class="fas fa-rocket mr-2"></i>Test Product
                </a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
                <a href="https://example.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition-colors duration-300">Get Started</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Privacy Policy</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p class="text-gray-600">
                    Last updated: January 2025
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Introduction</h2>
                <p>
                    Test Product ("we," "us," "our," or "Company") is committed to protecting your privacy. This Privacy Policy explains how we collect, use, disclose, and safeguard your information when you visit our website and use our services.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Information We Collect</h2>
                <p>
                    We may collect information about you in a variety of ways. The information we may collect on the Site includes:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li><strong>Personal Data:</strong> Name, email address, phone number, and other contact information you provide voluntarily</li>
                    <li><strong>Device Information:</strong> Browser type, IP address, operating system, and device identifiers</li>
                    <li><strong>Usage Data:</strong> Pages visited, time spent on pages, and interactions with our website</li>
                    <li><strong>Cookies:</strong> Information collected through cookies and similar technologies</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. How We Use Your Information</h2>
                <p>
                    We use the information we collect in the following ways:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>To provide, maintain, and improve our services</li>
                    <li>To process transactions and send related information</li>
                    <li>To send promotional communications (with your consent)</li>
                    <li>To respond to your inquiries and provide customer support</li>
                    <li>To analyze website usage and trends</li>
                    <li>To comply with legal obligations</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Data Security</h2>
                <p>
                    We implement appropriate technical and organizational measures to protect your personal information against unauthorized access, alteration, disclosure, or destruction. However, no method of transmission over the Internet or electronic storage is completely secure.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Your Rights</h2>
                <p>
                    Depending on your location, you may have the following rights:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>The right to access your personal data</li>
                    <li>The right to correct inaccurate data</li>
                    <li>The right to request deletion of your data</li>
                    <li>The right to opt-out of marketing communications</li>
                    <li>The right to data portability</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Third-Party Links</h2>
                <p>
                    Our website may contain links to third-party websites. We are not responsible for the privacy practices of other websites. We encourage you to review their privacy policies before providing any personal information.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Contact Us</h2>
                <p>
                    If you have questions about this Privacy Policy or our privacy practices, please contact us at:
                </p>
                <p>
                    <strong>Email:</strong> privacy@example.com<br>
                    <strong>Address:</strong> Your Company Address<br>
                    <strong>Phone:</strong> Your Phone Number
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Changes to This Policy</h2>
                <p>
                    We may update this Privacy Policy from time to time. We will notify you of any changes by posting the new Privacy Policy on this page and updating the "Last updated" date above.
                </p>
            </div>

            <div class="mt-12 p-6 bg-blue-50 rounded-lg">
                <p class="text-gray-700">
                    <strong>Note:</strong> This is a template privacy policy. Please consult with a legal professional to ensure it complies with applicable laws in your jurisdiction, including GDPR, CCPA, and other data protection regulations.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-12">
                <div>
                    <h3 class="text-xl font-bold text-white mb-6 flex items-center">
                        <i class="fas fa-rocket text-blue-400 mr-2"></i> Test Product
                    </h3>
                    <p class="text-gray-400 leading-relaxed mb-6">
                        Empowering businesses with advanced analytics and intelligent insights.
                    </p>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Product</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Pricing</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Company</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About Us</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Legal</h4>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Cookie Policy</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 pt-12">
                <p class="text-gray-400 text-sm text-center">
                    &copy; 2025 Test Product. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

3. **Update the placeholder information:**
   - Replace `privacy@example.com` with your actual email
   - Replace `Your Company Address` with your address
   - Replace `Your Phone Number` with your phone number
   - Update the company name if needed

4. **Save the file**

### Step 2: Create the Terms of Service Page

1. **Create a new file** named `terms.html` in the same folder as `index.html`

2. **Copy this template code** into `terms.html`:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta name="description" content="Terms of Service for Test Product">
    <title>Terms of Service | Test Product</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        html {
            scroll-behavior: smooth;
        }
    </style>
</head>
<body class="bg-white text-gray-900">
    <!-- Header & Navigation -->
    <header class="sticky top-0 z-50 bg-white shadow-md">
        <nav class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4 flex justify-between items-center">
            <div class="flex items-center">
                <a href="index.html" class="text-2xl font-bold text-blue-600 hover:text-blue-700 transition-colors duration-300">
                    <i class="fas fa-rocket mr-2"></i>Test Product
                </a>
            </div>
            <div class="hidden md:flex items-center space-x-8">
                <a href="index.html" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Home</a>
                <a href="index.html#features" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">Features</a>
                <a href="index.html#about" class="text-gray-700 hover:text-blue-600 font-medium transition-colors duration-300">About</a>
                <a href="https://example.com" class="bg-blue-600 text-white px-6 py-2 rounded-lg font-semibold hover:bg-blue-700 transition-colors duration-300">Get Started</a>
            </div>
        </nav>
    </header>

    <!-- Main Content -->
    <section class="py-16 md:py-24">
        <div class="max-w-3xl mx-auto px-4 sm:px-6 lg:px-8">
            <h1 class="text-4xl md:text-5xl font-bold text-gray-900 mb-8">Terms of Service</h1>
            
            <div class="prose prose-lg max-w-none text-gray-700 space-y-6">
                <p class="text-gray-600">
                    Last updated: January 2025
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">1. Agreement to Terms</h2>
                <p>
                    By accessing and using the Test Product website and services, you accept and agree to be bound by the terms and provision of this agreement. If you do not agree to abide by the above, please do not use this service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">2. Use License</h2>
                <p>
                    Permission is granted to temporarily download one copy of the materials (information or software) on Test Product's website for personal, non-commercial transitory viewing only. This is the grant of a license, not a transfer of title, and under this license you may not:
                </p>
                <ul class="list-disc list-inside space-y-2 ml-4">
                    <li>Modify or copy the materials</li>
                    <li>Use the materials for any commercial purpose or for any public display</li>
                    <li>Attempt to decompile or reverse engineer any software contained on the website</li>
                    <li>Transfer the materials to another person or "mirror" the materials on any other server</li>
                    <li>Remove any copyright or other proprietary notations from the materials</li>
                    <li>Transmit or communicate the materials to any other person or entity</li>
                </ul>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">3. Disclaimer</h2>
                <p>
                    The materials on Test Product's website are provided on an 'as is' basis. Test Product makes no warranties, expressed or implied, and hereby disclaims and negates all other warranties including, without limitation, implied warranties or conditions of merchantability, fitness for a particular purpose, or non-infringement of intellectual property or other violation of rights.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">4. Limitations</h2>
                <p>
                    In no event shall Test Product or its suppliers be liable for any damages (including, without limitation, damages for loss of data or profit, or due to business interruption) arising out of the use or inability to use the materials on Test Product's website, even if Test Product or an authorized representative has been notified orally or in writing of the possibility of such damage.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">5. Accuracy of Materials</h2>
                <p>
                    The materials appearing on Test Product's website could include technical, typographical, or photographic errors. Test Product does not warrant that any of the materials on its website are accurate, complete, or current. Test Product may make changes to the materials contained on its website at any time without notice.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">6. Links</h2>
                <p>
                    Test Product has not reviewed all of the sites linked to its website and is not responsible for the contents of any such linked site. The inclusion of any link does not imply endorsement by Test Product of the site. Use of any such linked website is at the user's own risk.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">7. Modifications</h2>
                <p>
                    Test Product may revise these terms of service for its website at any time without notice. By using this website, you are agreeing to be bound by the then current version of these terms of service.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">8. Governing Law</h2>
                <p>
                    These terms and conditions are governed by and construed in accordance with the laws of your jurisdiction, and you irrevocably submit to the exclusive jurisdiction of the courts in that location.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">9. User Accounts</h2>
                <p>
                    If you create an account on our website, you are responsible for maintaining the confidentiality of your account information and password. You agree to accept responsibility for all activities that occur under your account. You must notify us immediately of any unauthorized use of your account.
                </p>

                <h2 class="text-2xl font-bold text-gray-900 mt-8 mb-4">10. Contact Information</h2>
                <p>
                    If you have any questions about these Terms of Service, please contact us at:
                </p>
                <p>
                    <strong>Email:</strong> legal@example.com<br>
                    <strong>Address:</strong> Your Company Address<br>
                    <strong>Phone:</strong> Your Phone Number
                </p>
            </div>

            <div class="mt-12 p-6 bg-blue-50 rounded-lg">
                <p class="text-gray-700">
                    <strong>Note:</strong> This is a template terms of service. Please consult with a legal professional to ensure it complies with applicable laws in your jurisdiction and accurately reflects your business practices.
                </p>
            </div>
        </div>
    </section>

    <!-- Footer -->
    <footer class="bg-gray-900 text-gray-300 py-16 md:py-20 mt-16">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
            <div class="grid grid-cols-1 md:grid-cols-4 gap-12 mb-12">
                <div>
                    <h3 class="text-xl font-bold text-white mb-6 flex items-center">
                        <i class="fas fa-rocket text-blue-400 mr-2"></i> Test Product
                    </h3>
                    <p class="text-gray-400 leading-relaxed mb-6">
                        Empowering businesses with advanced analytics and intelligent insights.
                    </p>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Product</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#features" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Features</a></li>
                        <li><a href="index.html#benefits" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Benefits</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Pricing</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Company</h4>
                    <ul class="space-y-3">
                        <li><a href="index.html#about" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">About Us</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Blog</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Contact</a></li>
                    </ul>
                </div>
                <div>
                    <h4 class="text-lg font-bold text-white mb-6">Legal</h4>
                    <ul class="space-y-3">
                        <li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
                        <li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
                        <li><a href="https://example.com" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Cookie Policy</a></li>
                    </ul>
                </div>
            </div>
            <div class="border-t border-gray-800 pt-12">
                <p class="text-gray-400 text-sm text-center">
                    &copy; 2025 Test Product. All rights reserved.
                </p>
            </div>
        </div>
    </footer>
</body>
</html>
```

3. **Update the placeholder information:**
   - Replace `legal@example.com` with your actual email
   - Replace `Your Company Address` with your address
   - Replace `Your Phone Number` with your phone number
   - Update the company name if needed

4. **Save the file**

### Step 3: Verify Links Are Working

Your `index.html` already has links to these pages in the footer:

**Line 519:**
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Privacy Policy</a></li>
```

**Line 520:**
```html
<li><a href="terms.html" class="text-gray-400 hover:text-blue-400 transition-colors duration-300">Terms of Service</a></li>
```

**And in the footer bottom:**

**Line 545:**
```html
<a href="privacy.html" class="text-gray-400 hover:text-blue-400 text-sm transition-colors duration-300">Privacy</a>
```

**Line 546:**
```html
<a href="terms.html" class="text-gray-400 hover:text-blue-400 text-sm transition-colors duration-300">Terms</a>
```

These links will now work correctly because you've created the `privacy.html` and `terms.html` files.

### Step 4: Test the Links

1. Open `index.html` in your browser
2. Scroll to the footer
3. Click on "Privacy Policy" - should open `privacy.html`
4. Click on "Terms of Service" - should open `terms.html`
5. On the policy pages, click the logo to return to `index.html`

### Step 5: Customize the Policy Pages

Both template pages have placeholder information that you should customize:

**In privacy.html:**
- Update the "Last updated" date
- Update contact email from `privacy@example.com`
- Add your actual address and phone number
- Customize the content to match your actual practices

**In terms.html:**
- Update the "Last updated" date
- Update contact email from `legal@example.com`
- Add your actual address and phone number
- Customize the content to match your actual terms

### Creating a Blog Page (Optional)

If you want to create a blog page, follow the same pattern:

1. Create a file named `blog.html`
2. Use the same header and footer structure as `privacy.html`
3. Update the footer link in `index.html` from `https://example.com` to `blog.html`

---

## Troubleshooting Common Issues

### Issue 1: Text Changes Don't Appear

**Problem:** You edited the HTML but the changes don't show in your browser.

**Solution:**

1. Make sure you **saved the file** (Ctrl+S or Cmd+S)
2. **Refresh your browser** (F5 or Cmd+R)
3. If still not showing:
   - Clear your browser cache (Ctrl+Shift+Delete)
   - Try a different browser
   - Check that you edited the correct file

### Issue 2: Page Layout Breaks After Editing

**Problem:** After changing something, the page looks broken or misaligned.

**Solution:**

1. **Don't delete class attributes** - The `class=""` part contains all styling
   - Wrong: `<h1>Headline</h1>` (removed classes)
   - Right: `<h1 class="text-4xl font-bold">Headline</h1>` (kept classes)

2. **Don't remove HTML tags** - Tags like `<div>`, `<p>`, `<h1>` structure the page
   - Wrong: `Headline` (removed tags)
   - Right: `<h1>Headline</h1>` (kept tags)

3. **Always have matching opening and closing tags**
   - Wrong: `<div>Content</div>` (missing closing div)
   - Right: `<div>Content</div>` (proper closing tag)

### Issue 3: Links Don't Work

**Problem:** Clicking a link does nothing or goes to the wrong page.

**Solution:**

1. **Check for typos** in the URL
   - Wrong: `https://example.co` (missing 'm')
   - Right: `https://example.com`

2. **External URLs need `https://`**
   - Wrong: `<a href="example.com">`
   - Right: `<a href="https://example.com">`

3. **Email links need `mailto:`**
   - Wrong: `<a href="your-email@example.com">`
   - Right: `<a href="mailto:your-email@example.com">`

4. **Internal links need matching IDs**
   - Link: `<a href="#features">`
   - Section must have: `<section id="features">`

### Issue 4: Mobile Menu Doesn't Work

**Problem:** The hamburger menu on mobile doesn't open or close.

**Solution:**

The mobile menu should work automatically. If it doesn't:

1. Make sure JavaScript is enabled in your browser
2. Check that you haven't accidentally deleted the JavaScript code at the bottom of the file (Lines 555-587)
3. Test in a different browser

### Issue 5: Colors Look Wrong

**Problem:** Colors don't match what you expected.

**Solution:**

1. **Check the color class name** - Make sure it's spelled correctly
   - Wrong: `bg-blu-600` (typo)
   - Right: `bg-blue-600`

2. **Use correct color values**
   - Tailwind colors: `100`, `300`, `400`, `500`, `600`, `700`, `800`, `900`
   - Wrong: `bg-blue-555` (invalid value)
   - Right: `bg-blue-600`

3. **Verify the color name**
   - Valid: `blue`, `gray`, `red`, `green`, `purple`, `yellow`
   - Invalid: `bleu`, `grey` (use `gray`), `crimson`

### Issue 6: Text Size Changes Aren't Working

**Problem:** Changing `text-xl` to `text-2xl` doesn't make the text bigger.

**Solution:**

1. **Make sure you removed the old class**
   - Wrong: `class="text-xl text-2xl"` (both classes present)
   - Right: `class="text-2xl"` (only new class)

2. **Verify the class name**
   - Valid sizes: `text-sm`, `text-base`, `text-lg`, `text-xl`, `text-2xl`, `text-3xl`, `text-4xl`, `text-5xl`, `text-6xl`
   - Invalid: `text-large`, `text-huge`

3. **Check for conflicting styles** - Sometimes multiple classes can conflict
   - If you have `text-4xl md:text-5xl lg:text-6xl`, the size changes based on screen size

### Issue 7: Button Styling Changes Aren't Showing

**Problem:** Changed button colors but nothing happened.

**Solution:**

1. **Update both the normal and hover states**
   - Wrong: `<a class="bg-blue-600">` (only changed one)
   - Right: `<a class="bg-green-600 hover:bg-green-700">` (changed both)

2. **Make sure you changed the correct button**
   - There are multiple buttons on the page
   - Find the specific one you want to change

3. **Refresh your browser** to see changes

### Issue 8: Page Doesn't Look Right on Mobile

**Problem:** The page looks broken on phones or tablets.

**Solution:**

1. **Don't remove responsive classes** - These make the page work on all sizes
   - Wrong: `<h1 class="text-6xl">` (removes responsive sizes)
   - Right: `<h1 class="text-4xl md:text-5xl lg:text-6xl">` (keeps responsive sizes)

2. **Test on actual devices** - Browser mobile view isn't always accurate
   - Open your page on a real phone to test

3. **Check for hidden elements** - Some elements hide on mobile
   - `hidden md:block` = Hidden on mobile, shown on desktop
   - `block lg:hidden` = Shown on mobile, hidden on desktop

### Issue 9: Images Don't Display

**Problem:** You see a broken image icon instead of an image.

**Solution:**

1. **Check the image path** - Make sure the file exists
   - If image is in same folder: `src="image.png"`
   - If image is in subfolder: `src="images/image.png"`

2. **For background images, check the URL**
   - Wrong: `background-image: url('image.jpg')`
   - Right: `background-image: url('https://example.com/image.jpg')`

3. **Use correct file format**
   - Supported: `.jpg`, `.png`, `.gif`, `.webp`
   - Not supported: `.psd`, `.ai`

### Issue 10: Spacing Looks Wrong

**Problem:** Elements are too close together or too far apart.

**Solution:**

1. **Adjust padding** (space inside elements)
   ```html
   <div class="px-8 py-4">Content</div>
   ```
   - `px-4` to `px-12` = more horizontal space
   - `py-2` to `py-8` = more vertical space

2. **Adjust margins** (space between elements)
   ```html
   <div class="mb-8">Content</div>
   ```
   - `mb-2` to `mb-12` = more space below

3. **Adjust gap** (space between grid items)
   ```html
   <div class="grid gap-4">Items</div>
   ```
   - `gap-2` to `gap-12` = more space between items

---

## Best Practices

### 1. Always Backup Before Making Changes

**Why:** If something goes wrong, you can revert to the previous version.

**How:**
1. Before making major changes, copy your `index.html` file
2. Rename it to `index.html.backup`
3. Now you can safely edit the original

### 2. Make One Change at a Time

**Why:** If something breaks, you'll know exactly what caused it.

**Good approach:**
1. Change one text element
2. Save and test
3. Change another element
4. Save and test

**Bad approach:**
1. Change 10 things at once
2. Save
3. Something broke but you don't know what

### 3. Use Consistent Naming Conventions

**Why:** Makes it easier to find and update things later.

**Example:**
- Use the same email throughout: `your-email@yourcompany.com`
- Use the same company name: "Test Product" or "MyCompany"
- Use consistent capitalization

### 4. Keep Your File Structure Organized

**Why:** Makes maintenance easier.

**Recommended structure:**
```
your-project-folder/
├── index.html
├── privacy.html
├── terms.html
├── blog.html
└── images/
    ├── logo.png
    ├── hero.jpg
    └── feature1.jpg
```

### 5. Test on Multiple Devices

**Why:** Your page should look good everywhere.

**Test on:**
- Desktop computers
- Tablets
- Mobile phones
- Different browsers (Chrome, Firefox, Safari, Edge)

### 6. Update Links Regularly

**Why:** Broken links hurt user experience and SEO.

**Checklist:**
- [ ] All external links are correct
- [ ] All email links work
- [ ] All internal links jump to correct sections
- [ ] Privacy and Terms pages are linked

### 7. Keep Content Updated

**Why:** Outdated information looks unprofessional.

**Update regularly:**
- Customer testimonials
- Statistics (active users, ratings)
- Company information
- Contact details
- Social media links

### 8. Use Descriptive Text for Links

**Why:** Helps users and search engines understand where links go.

**Good:**
```html
<a href="https://example.com/pricing">View our pricing plans</a>
```

**Bad:**
```html
<a href="https://example.com/pricing">Click here</a>
```

### 9. Maintain Consistent Branding

**Why:** Creates a professional appearance.

**Keep consistent:**
- Colors (always use same blue, gray, etc.)
- Fonts (Tailwind uses system fonts by default)
- Logo and icon usage
- Tone of voice in copy

### 10. Document Your Changes

**Why:** Helps you remember what you changed and why.

**Example:**
```html
<!-- Updated: Jan 15, 2025 - Changed CTA button to "Sign Up Now" -->
<a href="https://example.com">Sign Up Now</a>
```

### 11. Validate Your HTML

**Why:** Ensures your code is correct and will work in all browsers.

**How:**
1. Visit [HTML Validator](https://validator.w3.org/)
2. Upload your `index.html` file
3. Fix any errors reported

### 12. Test Accessibility

**Why:** Ensures your page works for everyone, including people with disabilities.

**Quick checks:**
- [ ] Can you navigate with keyboard only (Tab key)?
- [ ] Do all images have alt text?
- [ ] Is text readable on all color backgrounds?
- [ ] Do buttons have clear hover states?

---

## Quick Reference

### File Locations of Key Elements

| Element | Location (Line #) |
|---------|------------------|
| Logo/Brand Name | 28-31 |
| Navigation Links | 35-42 |
| Get Started Button (Header) | 43 |
| Hero Headline | 65-68 |
| Hero Subheadline | 70-73 |
| Hero Description | 75-78 |
| Primary CTA Button | 80-85 |
| Secondary CTA Button | 87-90 |
| Statistics | 92-102 |
| Features Section Title | 114-120 |
| Feature 1 Title | 132 |
| Feature 2 Title | 152 |
| Feature 3 Title | 172 |
| Benefits Section Title | 192-198 |
| Benefit 1 Title | 208 |
| Benefit 2 Title | 225 |
| Benefit 3 Title | 241 |
| Benefit 4 Title | 258 |
| CTA Section Headline | 274-277 |
| CTA Section Description | 278-280 |
| Testimonials Section Title | 302-308 |
| Testimonial 1 Quote | 320 |
| Testimonial 1 Author | 330 |
| About Us Section Title | 412-418 |
| Our Story Title | 427 |
| Our Mission Title | 440 |
| Footer Company Name | 463 |
| Footer Copyright | 540-549 |
| Social Media Links | 474-483 |

### Common Tailwind Color Combinations

**Blue Theme (Current):**
- Primary: `bg-blue-600`
- Hover: `hover:bg-blue-700`
- Text: `text-blue-600`
- Light Background: `bg-blue-50` or `bg-blue-100`

**Green Theme:**
- Primary: `bg-green-600`
- Hover: `hover:bg-green-700`
- Text: `text-green-600`
- Light Background: `bg-green-50`

**Purple Theme:**
- Primary: `bg-purple-600`
- Hover: `hover:bg-purple-700`
- Text: `text-purple-600`
- Light Background: `bg-purple-50`

**Red Theme:**
- Primary: `bg-red-600`
- Hover: `hover:bg-red-700`
- Text: `text-red-600`
- Light Background: `bg-red-50`

### Common Font Size Conversions

| Tailwind Class | Pixel Size | Usage |
|---|---|---|
| `text-sm` | 14px | Small text, captions |
| `text-base` | 16px | Body text |
| `text-lg` | 18px | Larger body text |
| `text-xl` | 20px | Section descriptions |
| `text-2xl` | 24px | Subheadings |
| `text-3xl` | 30px | Small headings |
| `text-4xl` | 36px | Medium headings |
| `text-5xl` | 48px | Large headings |
| `text-6xl` | 60px | Extra large headings |

---

## Resources

### Learning Resources

- **Tailwind CSS Documentation:** https://tailwindcss.com/docs
- **HTML Basics:** https://developer.mozilla.org/en-US/docs/Web/HTML
- **Font Awesome Icons:** https://fontawesome.com/icons
- **CSS Tricks:** https://css-tricks.com/

### Tools

- **HTML Validator:** https://validator.w3.org/
- **CSS Validator:** https://jigsaw.w3.org/css-validator/
- **Color Picker:** https://htmlcolorcodes.com/
- **Responsive Design Tester:** https://responsively.app/

### Getting Help

- **Stack Overflow:** https://stackoverflow.com/ (for coding questions)
- **Tailwind Community:** https://tailwindcss.com/community
- **MDN Web Docs:** https://developer.mozilla.org/
- **Web.dev:** https://web.dev/ (best practices)

---

## Final Checklist

Before launching your landing page, verify:

- [ ] All text has been updated to your content
- [ ] All links are correct and working
- [ ] All external URLs are updated (signup, pricing, etc.)
- [ ] All email addresses are updated
- [ ] Company name is consistent throughout
- [ ] Logo/icon is appropriate for your brand
- [ ] Colors match your brand guidelines
- [ ] Privacy Policy page is created and linked
- [ ] Terms of Service page is created and linked
- [ ] Page looks good on mobile devices
- [ ] Page looks good on desktop
- [ ] All buttons work and link to correct places
- [ ] Contact information is accurate
- [ ] Social media links are correct
- [ ] No broken images
- [ ] No typos or grammatical errors
- [ ] Testimonials are accurate or replaced with real ones
- [ ] Statistics are accurate or updated
- [ ] Navigation menu is complete
- [ ] Footer links are all working
- [ ] Page loads quickly

---

## Support & Questions

If you encounter issues not covered in this guide:

1. **Check the troubleshooting section** - Most common issues are covered
2. **Validate your HTML** - Use the HTML validator to find errors
3. **Check browser console** - Open Developer Tools (F12) to see error messages
4. **Search online** - Search for your specific error message
5. **Ask for help** - Share your code on Stack Overflow or relevant forums

---

**Happy customizing! Your landing page is now ready to be personalized to your needs.**