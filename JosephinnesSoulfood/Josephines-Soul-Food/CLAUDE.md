# Josephine's Soul Food - Project Guide

## Project Overview
A modern, luxurious website for Josephine's Soul Food, a Black-owned soul food restaurant in Toledo, Ohio. Built with Next.js 14, React, TypeScript, and Tailwind CSS.

## Tech Stack
- **Framework**: Next.js 14 (App Router)
- **Language**: TypeScript
- **Styling**: Tailwind CSS with CSS Variables
- **State Management**: Zustand (for cart)
- **UI Components**: Custom components + shadcn/ui

## File Structure

```
josephines-soul-food/
├── public/
│   ├── images/
│   │   ├── branding/          # Logo, portraits, brand assets
│   │   ├── menu/              # Food photos, restaurant images
│   │   └── locations/         # Delivery zone images
│   └── videos/                # Hero and news feature videos
│
├── src/
│   ├── app/                   # Next.js App Router pages
│   │   ├── page.tsx           # Homepage
│   │   ├── layout.tsx         # Root layout (Header + Footer)
│   │   ├── globals.css        # Global styles & CSS variables
│   │   ├── about/             # About page
│   │   ├── menu/              # Menu page
│   │   ├── catering/          # Catering page
│   │   ├── order/             # Order flow
│   │   │   ├── page.tsx       # Order type selection
│   │   │   └── checkout/      # Checkout page
│   │   └── shop/              # Store/merchandise page
│   │
│   ├── components/
│   │   ├── home/              # Homepage-specific components
│   │   │   ├── VideoHero.tsx         # Hero section with background image
│   │   │   ├── MarqueeBanner.tsx     # Scrolling announcements
│   │   │   ├── FeaturedMenu.tsx      # Featured dishes grid
│   │   │   ├── DeliveryZones.tsx     # Delivery area cards
│   │   │   ├── FoodGallerySlider.tsx # Image carousel
│   │   │   ├── StoryPreview.tsx      # Family story section
│   │   │   ├── NewsFeature.tsx       # News video section
│   │   │   ├── TestimonialCarousel.tsx # Reviews carousel
│   │   │   └── FloatingPhone.tsx     # Click-to-call button
│   │   │
│   │   ├── layout/            # Layout components
│   │   │   ├── Header.tsx     # Navigation header
│   │   │   └── Footer.tsx     # Site footer
│   │   │
│   │   └── ui/                # Reusable UI components
│   │       ├── Button.tsx     # Custom button component
│   │       ├── Container.tsx  # Layout container
│   │       └── [shadcn]       # shadcn/ui components
│   │
│   ├── data/
│   │   └── menuData.ts        # Menu items data
│   │
│   ├── lib/
│   │   ├── store.ts           # Zustand cart store
│   │   └── utils.ts           # Utility functions (cn helper)
│   │
│   └── types/
│       └── index.ts           # TypeScript type definitions
│
├── package.json
├── tailwind.config.ts
├── tsconfig.json
└── CLAUDE.md                  # This file
```

## Design System

### Colors (CSS Variables in globals.css)
- `--color-primary`: #816B3B (warm brown/gold - main brand color)
- `--color-primary-dark`: #6B5830
- `--color-primary-light`: #9C8350
- `--color-gold`: #B89D6B

### Typography
- **Display/Headings**: Playfair Display (serif)
- **Body**: Inter (sans-serif)

### Section Padding Convention
- Standard sections: `py-16 lg:py-20`
- Hero/special sections: Custom sizing

### Component Patterns
- All client components use `'use client'` directive
- Sections follow consistent header pattern:
  ```tsx
  <div className="flex flex-col items-center text-center mb-16">
    <span className="badge...">Badge Text</span>
    <h2 className="font-display text-4xl sm:text-5xl lg:text-6xl...">Title</h2>
    <p className="text-xl text-gray-600...">Description</p>
  </div>
  ```

## Key Pages

### Homepage (`/`)
Sections in order:
1. FloatingPhone (fixed position)
2. VideoHero
3. MarqueeBanner
4. FeaturedMenu
5. DeliveryZones
6. FoodGallerySlider
7. StoryPreview
8. NewsFeature
9. TestimonialCarousel

### Menu (`/menu`)
Full categorized menu with ordering capability

### About (`/about`)
Family story and restaurant history

### Order (`/order`)
Multi-step ordering flow with checkout

## Unused Components (Can Be Removed)
These components exist but are not currently used:
- `src/components/home/AnimatedStats.tsx`
- `src/components/home/OrderCTA.tsx`
- `src/components/home/StickyOrderButton.tsx`
- `src/components/home/StorySection.tsx`
- `src/components/home/Testimonials.tsx`

## Running the Project

```bash
# Install dependencies
npm install

# Run development server
npm run dev

# Build for production
npm run build

# Start production server
npm start
```

## Important Notes

1. **Images**: All food photos are in `/public/images/menu/`
2. **Videos**: News feature video is in `/public/videos/media-news.mp4`
3. **Contact Info**:
   - Phone: (419) 242-6666
   - Address: 902 Lagrange St, Toledo, OH 43604
4. **Hours**: Mon-Thu 11am-8pm, Fri-Sat 11am-9pm, Sun 12pm-7pm

## Git Repository
https://github.com/docrolds/Josephines-Soul-Food
