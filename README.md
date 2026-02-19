# Modern CSS Marquee (Running Text) Component

A lightweight, modern running text (marquee) component built with pure HTML and CSS.

Designed for landing pages, directories, marketplaces, and service websites that require a high-visibility call-to-action section without relying on JavaScript libraries.

This component prioritizes performance, visual clarity, and conversion optimization.

---

## Preview

<img width="1191" height="91" alt="running text html css js" src="https://github.com/user-attachments/assets/fd4109e4-9720-4382-881d-a056230cd8f3" />

---

## Overview

This implementation uses:

- CSS `transform` animation for smooth scrolling
- Infinite loop technique (duplicated content structure)
- Gradient background styling
- Edge fade effects using pseudo-elements
- Animated CTA highlight (glow/blink effect)
- Fully clickable container (ideal for WhatsApp or lead links)

The animation is hardware-accelerated and optimized using:

`css
will-change: transform;`

Key Features

1. Smooth Infinite Scrolling

The animation transitions from translateX(0) to translateX(-50%), ensuring seamless looping without visible jumps.

`@keyframes marquee-scroll {
  from { transform: translateX(0); }
  to { transform: translateX(-50%); }
}`

The -50% shift works because the content block is duplicated.
When the animation resets, the second block aligns perfectly with the first.

2. Edge Fade Masking

Left and right gradient overlays are created using ::before and ::after pseudo-elements.

This provides:

Improved visual polish

Reduced harsh text clipping

Better readability on continuous scroll

3. High-Visibility CTA

The glow/blink animation increases attention density around the call-to-action trigger.

Example animation:

`@keyframes glowBlink {
  0%, 100% {
    color: #ffd700;
    text-shadow: 0 0 5px #ffd700, 0 0 10px goldenrod;
  }
  50% {
    color: #fff;
    text-shadow: none;
  }
}`

4. Lightweight Architecture

No JavaScript dependency

No external libraries

Fully responsive

Minimal layout complexity

Hardware-accelerated animation
