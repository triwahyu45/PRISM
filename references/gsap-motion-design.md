---
name: gsap-motion-design
description: >-
  Advanced animation design and implementation with GSAP 3, ScrollTrigger, and @gsap/react.
  Use when building high-performance web animations, micro-interactions, scroll-driven reveals,
  and smooth transitions without layout shift.
---

# GSAP Motion Design & Implementation Skill

Keahlian integrasi animasi GreenSock (GSAP 3) untuk antarmuka web modern kelas dunia (Awwwards / Dribbble).

## 1. Instalasi & Setup Next.js App Router
```bash
npm install gsap @gsap/react
```

## 2. Inisialisasi Aman (SSR & Hydration Safe)
Selalu gunakan hook `useGSAP` dari `@gsap/react` atau `useEffect` dengan registrasi plugin:
```tsx
'use client';

import React, { useRef } from 'react';
import gsap from 'gsap';
import { ScrollTrigger } from 'gsap/ScrollTrigger';
import { useGSAP } from '@gsap/react';

if (typeof window !== 'undefined') {
  gsap.registerPlugin(ScrollTrigger, useGSAP);
}
```

## 3. Aturan Animasi Anti-AI Look
1. **Subtle & Restrained**: Jarak perpindahan Y-axis kecil (8–16px), jangan membuat elemen meluncur jauh dari luar layar.
2. **Natural Easing**: Gunakan `power1.out`, `expo.out`, atau `back.out(1.4)`.
3. **Stagger Delays**: Jeda stagger antar item kecil (0.03s–0.06s).
4. **Prefers-Reduced-Motion**: Wajib hormati pengguna yang menonaktifkan animasi:
   ```ts
   gsap.matchMedia().add('(prefers-reduced-motion: reduce)', () => {
     // Render final state immediately without animation
   });
   ```
