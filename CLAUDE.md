# Micro-Meditation Course - Claude Code Instructions

## Project Type
Next.js 14+ website with Tailwind CSS, deployed to Cloudflare Pages as static export.

## Tech Stack
- **Framework:** Next.js 14+ with App Router
- **Styling:** Tailwind CSS
- **Images:** next/image component
- **Fonts:** next/font/google
- **Export:** Static (output: 'export' in next.config.js)

## Design System

### Typography (use next/font)
```typescript
// app/layout.tsx
import { Poppins, Source_Sans_Pro } from 'next/font/google'

const displayFont = Poppins({
  subsets: ['latin'],
  weight: ['400', '700', '900'],
  variable: '--font-display'
})

const bodyFont = Source_Sans_Pro({
  subsets: ['latin'],
  weight: ['400', '500', '600'],
  variable: '--font-body'
})
```

### Colors (in globals.css)
```css
:root {
  --color-primary: #00A693;
  --color-accent: #FF6B35;
  --color-surface: #FAFBFC;
  --color-text: #1A202C;
  --color-text-muted: #718096;
}
```

### Effects to Include
- subtle gradients
- micro-animations
- geometric shapes
- offset elements

## Available Images
**CRITICAL: Use these images from assets/images/ - do NOT use placeholder images!**

- 633c957c47580_MMmethod.svg
- 63560d4aaefaa_AntarMounaMeditation.webp
- 6356108dd13e6_FullYogicBreathPranayama.webp
- 635610eb27251_UjjayiBreathPranayama.webp
- 635610fa4ffd0_MantraJappaMeditation.webp
- 63561114b380a_NaturalBreathAwareness.webp
- 6356112bce2db_KakiPranayama.webp
- 6356113f9f94f_NadiShodhanaPranayama.webp
- 63561173a2413_KayaSthariyiumMeditation.webp
- 635616027611b_HowdoesMicro-MeditationWork.webp
- 6356193d44068_Whattoexpect.webp
- 6356194ff0fea_YourMeditationTeacher.webp
- 635641b743b22_MicroMeditationTestimonials.webp
- 635b13a6c3e4b_mandala1.png
- 63813483141fb_tik-tok.png
- 638134939ecae_youtube.png
- 638134a84b9a8_facebook.png
- 638134ba9c0fd_instagram.png
- 63ce0fd62a787_FemaleSquareFormat.jpeg
- 63cf1c1f14c2b_pexels-liza-summer-6382714.jpeg
- 64ab8284799f8_Breathwork.webp
- 64ab82975c241_focused-attention.webp
- 64ab82a493801_Relaxation.webp
- 64ab82b20c0eb_Mindfulness.webp
- 64ab82c6b2f1c_EmotionalRegulation.webp
- 64ab82d881680_Energyexpansion.webp
- 64ac84c68bc6f_startmeditation.webp
- 64ac84da5ce12_thekey.webp
- 64ac84ec3539f_freegift.webp

### How to use images:
```tsx
import Image from 'next/image'

// For images in public/assets/images/
<Image
  src="/assets/images/filename.jpg"
  alt="Description"
  width={800}
  height={600}
/>
```

## Required Pages (App Router)
1. `app/page.tsx` - Homepage
2. `app/services/page.tsx` - Services
3. `app/about/page.tsx` - About
4. `app/contact/page.tsx` - Contact

## Next.js Config for Static Export
```javascript
// next.config.js
/** @type {import('next').NextConfig} */
const nextConfig = {
  output: 'export',
  images: {
    unoptimized: true, // Required for static export
  },
}
module.exports = nextConfig
```

## Quality Checklist
- [ ] All images from assets/images/ used (NO placeholders)
- [ ] Lighthouse Performance > 90
- [ ] Mobile responsive (375px)
- [ ] LocalBusiness schema
- [ ] Distinctive design (NOT generic)
- [ ] Animations and hover states

## DO NOT
- Use Inter, Roboto, or Arial fonts
- Use placeholder images (unsplash, placeholder.com, etc.)
- Create cookie-cutter layouts
- Skip the design direction
- Use placeholder text (use scraped content)

## Workflow
1. Read prd.json for stories
2. Copy assets/images/ to public/assets/images/
3. Complete stories in order using the downloaded images
4. Mark "passes": true when done
5. Deploy when all stories pass
