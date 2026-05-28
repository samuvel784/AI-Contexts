# Universal Chat Area — Complete Frontend UX/UI Documentation

> A privacy-focused realtime community chat platform built with React 19 + TypeScript + Tailwind CSS v4 + framer-motion + Three.js.

---

## Overview

| Detail | Info |
|--------|------|
| **Live Site** | [https://universal-chat-area.vercel.app](https://universal-chat-area.vercel.app) |
| **GitHub Repository** | [https://github.com/samuvel784/Universal-Chat](https://github.com/samuvel784/Universal-Chat) |
| **Tech Stack** | React 19, TypeScript 6, Vite 8, Tailwind CSS v4, framer-motion, Three.js, Supabase, IndexedDB (Dexie.js) |
| **Framework** | React + TypeScript SPA (Single Page Application) |
| **Styling** | Tailwind CSS v4 with `@tailwindcss/typography` plugin, dark mode via `.dark` class variant |
| **Animation** | framer-motion (page transitions, modal animations, micro-interactions), CSS `@keyframes`, Three.js (3D hero scene) |
| **State Management** | Zustand (`useChatStore`) + React Context (`AuthContext`) |
| **Routing** | React Router v6 with `BrowserRouter`, lazy-loaded routes via `React.lazy()` |
| **Authentication** | Google Sign-In (GSI — Google Identity Services) |
| **Realtime** | Supabase Realtime (WebSocket) for presence, broadcast, and database changes |
| **Offline** | Service Worker (cache-first + network-first), IndexedDB local cache |
| **PWA** | Installable Progressive Web App with manifest.json |
| **Build Tool** | Vite 8 |

---

## About the Site

### Why Universal Chat Area?

Universal Chat Area was built to provide a **modern, privacy-conscious, realtime chat experience** without the bloat, tracking, and data harvesting common in mainstream messaging platforms. It combines the immediacy of apps like Discord/Slack with a strong privacy stance: **no email verification required, no phone number, no tracking cookies, no analytics scripts**.

The site demonstrates how modern web technologies (React 19, Supabase Realtime, IndexedDB, Service Workers, Three.js) can come together to create a desktop-quality chat application that runs entirely in the browser — with full offline support and realtime synchronization.

### What Are the Uses of This Site?

1. **Community Chat** — Join the #general channel to talk with other users in real time. Share messages, react with emojis, and engage in threaded conversations.
2. **Friend System** — Search for other users by name or unique ID, send friend requests, accept/reject incoming requests, and build a friends list.
3. **Direct Messaging** — DM with friends privately in realtime.
4. **Profile Customization** — Set a display name, bio, custom status, and avatar color. Identifiable by a unique `#000000` ID.
5. **Privacy-First Communication** — All messages are end-to-end managed through your browser. No data sold, no tracking, no ads.
6. **Offline Resilience** — Service worker caches assets; IndexedDB stores recent messages locally for offline access.
7. **Cross-Device** — Sign in with Google on any device; your profile, friends, and messages sync automatically.
8. **Learning & Demonstration** — Serves as a showcase of modern React + Supabase + realtime architecture patterns.

### Is It a Privacy App?

**Yes.** The application is designed with privacy as a core principle:

- **No email verification required** — Sign in with Google, that's it. No password storage, no email lists.
- **No phone number required** — Unlike many chat apps, Universal Chat never asks for a phone number.
- **No tracking or analytics** — No Google Analytics, no tracking pixels, no cookies for advertising. The app uses no third-party analytics scripts.
- **No data selling** — User data (messages, profiles, friend lists) is never sold or shared with third parties.
- **Local-first caching** — Messages are cached locally in IndexedDB. You can view previously loaded messages even when offline.
- **Minimal data collection** — Only the data needed to operate the chat (Google ID, display name, email, messages, friend relationships). Full data portability via the database schema.
- **Open source** — The entire codebase is public on GitHub for transparency and auditability.
- **PostgreSQL with Row-Level Security** — Database queries are scoped to authenticated users.
- **No ads** — The platform is ad-free and has no monetization through user data.

---

## 1. Entry & Loading

When a user first visits `https://universal-chat-area.vercel.app`, the browser loads a single-page application via Vite. The page background is near-white `#fafafa` in light mode or deep near-black `#050816` in dark mode. While the app bootstraps, the user sees a **loading fallback**: three small indigo-500 dots centered on screen, each bouncing at staggered intervals (0ms, 150ms, 300ms).

The app uses **React Router v6** with lazy-loaded routes wrapped in `<Suspense>`, so each page loads on demand. Page transitions use framer-motion's `AnimatePresence` with `popLayout` mode: outgoing page fades and slides upward while the incoming page fades and slides upward from below — all in 0.35s with `easeOut` easing.

**Font**: Inter (Google Fonts) with system fallbacks, loaded globally. The entire UI uses this single typeface varying only in weight (400/600/700/800) and size.

### Loading Fallback Component

- Full viewport centered (`flex items-center justify-center h-screen`).
- Three dots: `w-2 h-2` rounded-full indigo-500.
- Staggered `animate-bounce` with `animationDelay` at 0ms, 150ms, 300ms.
- Background: `bg-[#fafafa]` light / `bg-[#050816]` dark.
- Smooth dark mode transition on `html` element (500ms).

### Global Styles (`index.css`)

- **Body background**: `#fafafa` light, `#050816` dark.
- **Text colors**: `text-gray-900` light / `text-gray-100` dark.
- **bg-dot-grid**: A radial gradient dot pattern overlay (subtle 1px dots every 24px).
- **Focus-visible**: 2px offset indigo-500 outline on all interactive elements.
- **Custom scrollbar** (`.custom-scrollbar`): thin (4px), thumb `rgba(255,255,255,0.15)` with 0.2s transition, hover `rgba(255,255,255,0.3)`, track transparent.
- **Selection**: `bg-indigo-500/30 text-white`.
- **`animate-fade-in`** keyframe: opacity 0→1, translateY 8px→0 over 0.2s.
- **`scroll-behavior: smooth`** on html.
- **`@view-transition`** for smooth navigation.
- **`prefers-reduced-motion`**: Disables all animations and transitions.

---

## 2. Global Background Layer

Beneath every page, two persistent background layers run at `z-index: -10`:

### 2.1 ParticleField

A full-screen HTML5 `<canvas>` element, `fixed inset-0 pointer-events-none -z-10`. Renders **80 glowing dots** (30 on mobile) floating upward with sinusoidal drift. Nearby particles (within 120px) are connected by thin semi-transparent indigo lines (`rgba(129,140,248,alpha)`). Particles gently **repel from the user's cursor** within a 200px radius. Colors adapt: vibrant neon in dark mode, pastel in light mode. Animation pauses when `document.hidden`. Follows `prefers-reduced-motion`.

### 2.2 BackgroundOrbs

Fixed fullscreen overlay, `pointer-events-none -z-10`. 8 large animated gradient orbs (200px to 800px) with `blur-3xl`. Colors: indigo/purple/cyan/violet/fuchsia/blue/sky gradients. Each orb has `x` and `y` animation paths with different durations (12s–32s). Dark mode: more saturated colors with higher opacity (15% vs 8%). Includes `bg-dot-grid` pattern overlay. Respects `prefers-reduced-motion`.

---

## 3. Header & Navigation (SiteLayout)

Every page except `/chat`, `/auth`, and profile pages uses **SiteLayout** — a persistent shell with header and footer.

### 3.1 Desktop Header

Sticky at the top (`z-40`) with `backdrop-blur-xl`. Frosted glass: `bg-white/70` light, `bg-gray-900/70` dark. Subtle bottom border: `border-gray-200/50` light, `border-gray-800/50` dark. Content capped at `max-w-6xl` with responsive padding.

**Left — Logo**: Gradient icon (indigo-to-purple `MessageSquare`) + text **"Universal Chat"**. Group hover scale effect on icon. Links to `/`.

**Center — Desktop Navigation** (`hidden md:flex`): Six links — Home, Chat, About, FAQ, Guidelines, Blog. Each has `rounded-xl` with `transition-all`. Active page: indigo text + light indigo bg (`bg-indigo-50 dark:bg-indigo-900/30`). Inactive: `text-gray-600` dark `text-gray-400`, hover becomes `text-gray-900 dark:hover:text-white` + `bg-gray-100 dark:hover:bg-gray-800`.

**Right — Controls**:

1. **Dark Mode Toggle**: Rounded button cycling Sun/Moon icons. 500ms color transition on entire app.
2. **Profile / Sign In**:
   - If authenticated: user avatar (or initial) + display name in `bg-indigo-100 dark:bg-indigo-900/40` pill, linking to `/profile`.
   - If not: "Sign In" button with `LogIn` icon, gradient purple-to-indigo bg, `shadow-lg`.
3. **Join Chat**: Outline button linking to `/chat`, `hidden sm:inline-flex`.

### 3.2 Mobile Navigation

Below `md` breakpoint, center nav collapses into a **hamburger menu** button. Tapping opens a **slide-in overlay** from the right (framer-motion spring, damping:25, stiffness:200):

- **Backdrop**: `fixed inset-0 z-50`, `bg-black/50 backdrop-blur-sm`.
- **Side Panel**: `fixed top-0 right-0 bottom-0 w-72 max-w-[80vw]`, frosted glass (`bg-white/90 dark:bg-gray-900/90 backdrop-blur-xl`), border-left. Spring animation: x: 320 → 0.
- **Header**: "Menu" title + X close button.
- **Nav Links**: Same six links, stacked vertically.
- **Bottom Section**: "Sign In with Google" gradient button + "Join Chat" outline button.

Tapping a link or backdrop closes the panel via `AnimatePresence` exit animation.

### 3.3 Footer

Frosted glass (`bg-white/50 dark:bg-gray-900/50 backdrop-blur-md`) with top border (`border-gray-200/50 dark:border-gray-800/50`). 3-column grid on `md`:

1. **Brand Column**: Logo + name + "A modern realtime community chat platform. Sign in with Google and start connecting instantly." description.
2. **Links Column**: Heading "LINKS" (uppercase, tracking-wider). 5 links: Privacy Policy, Terms of Service, Contact, FAQ, Community Guidelines. Hover turns indigo (`hover:text-indigo-600`).
3. **Platform Column**: Heading "PLATFORM". Tech info: "Built with React + Supabase", "Powered by Vercel + Supabase", "Google sign-in required".

**Bottom Bar**: Copyright line — `© 2026 Universal Chat Area. All rights reserved.`

---

## 4. Homepage (LandingPage) — Route: `/`

Single-scroll page, `overflow-hidden`.

### 4.1 Hero Section (`min-h-[90vh]`)

- **Background**: `<ThreeHeroScene />` — Three.js scene with alpha channel. 5 floating bubbles (SphereGeometry, MeshPhysicalMaterial, opacity 0.25, roughness 0.3, metalness 0.1) in colors: `#818cf8`, `#a78bfa`, `#67e8f9`, `#f472b6`, `#c084fc`. 80 point particles (PointsMaterial) floating in a sphere. Bubbles bob with sinusoidal motion, particles rotate slowly. Responsive: resizes with window.

- **Animated Content** (fade-up 0.8s):
  - **Badge pill**: `inline-flex` with `Zap` icon + "Sign in with Google" (or "Community" if authenticated).
  - **Heading**: "**Universal Chat Area**" — "Chat Area" in gradient text (`from-indigo-500 to-purple-600 bg-clip-text text-transparent`), extra-bold `font-extrabold`.
  - **Subtitle**: "A privacy-focused realtime community chat platform. Connect instantly with friends — no email verification, no phone number, no tracking."
  - **CTA Buttons** (gap-4, flex-wrap):
    - **Primary**: "Sign In with Google" / "Build Your Friends" — gradient indigo-to-purple (`from-indigo-600 to-purple-600`), `shadow-2xl`, shadow intensifies on hover (`hover:shadow-indigo-500/25 active:scale-95`).
    - **Secondary**: "Learn More" — outline, `ring-1 ring-gray-300 dark:ring-white/20`, border turns indigo on hover (`hover:ring-indigo-600`).

- **Parallax effect**: `heroOpacity` and `heroScale` driven by framer-motion `useScroll` + `useTransform`.

### 4.2 Animated Stats Section

Glassmorphism container (`bg-white/30 dark:bg-gray-900/30 backdrop-blur-xl rounded-3xl border`). 4-column grid (`md:grid-cols-4`):

| Stat | Value | Icon |
|------|-------|------|
| Messages Sent | 50,000+ | MessageSquare |
| Active Users | 1,200+ | Users |
| Uptime | 99.9%+ | Zap |
| Countries | 150+ | Globe |

Each stat: gradient icon, animated count via `requestAnimationFrame` with quartic easing over 8 seconds, label text.

### 4.3 Chat Preview Section

Mock terminal window: traffic-light dots (red/yellow/green) + URL "universal-chat.app". 4 animated mock messages with staggered delays:

1. Tamil (purple avatar): "Hey everyone! Love how instant this is 👋"
2. You (indigo): "This is amazing! Just signed in with Google?"
3. Vel (pink): "Totally! Sign in with Google and you're in..."
4. Tamil: "Messages persist in the cloud..."

### 4.4 Tech Stack Section

"Built with modern technologies" label. 5 chip badges in a row: **React 19** (React icon), **TypeScript** (TypeScript icon), **Supabase** (Supabase icon), **Vercel** (Vercel icon), **IndexedDB** (Database icon) — each with icon + name.

### 4.5 Core Features Section

Badge pill "**CORE FEATURES**" with Zap icon. 6 stat row: Sub-100ms latency, 100% client-side encryption, Zero server storage, Instant reload, Offline history, Free.

Below: 5 feature cards in `md:grid-cols-3` layout, each in a **TiltCard** (3D tilt on mouse move via custom `useTilt` hook, `transformStyle: preserve-3d`, framer-motion scroll-into-view animation):

1. **Realtime Messaging** (Zap icon) — "Messages appear instantly as you type. No page refreshes needed."
2. **Privacy First** (Shield icon) — "No email verification, no phone number, no tracking cookies. Your data stays yours."
3. **Emoji & Reactions** (Smile icon) — "Express yourself with emoji reactions on any message."
4. **Offline-First** (Wifi icon) — "Messages are cached locally. Browse your conversation history even offline."
5. **Safe Community** (MessageSquare icon) — "Report inappropriate content. Friend system keeps your circle private."

Cards: glassmorphism (`bg-white/30 dark:bg-gray-900/30 backdrop-blur-xl`), border `border-gray-200/50 dark:border-white/10`, hover border turns indigo, icon scales on hover.

### 4.6 Testimonials Section

Badge "**Community**" with pulsing dot. 3 testimonial cards: Avatar (gradient circle), name, role ("React Developer", "UI Designer", "Community Member"), 4/5 star rating (SVG stars), italic quote.

### 4.7 FAQ Section (Accordion)

5 expandable items: glass card, clickable header with rotating ChevronDown icon (`transform transition-transform duration-300`), animated content with framer-motion height/opacity transition.

Questions: "How do I create an account?", "Where are my messages stored?", "Is my data safe?", "How does moderation work?", "What happens if I close my browser?"

---

## 5. Auth Page (AuthPage) — Route: `/auth`

### 5.1 Layout

`min-h-screen bg-[#050816]` (always dark) + decorative blur circles.

**Two columns side-by-side** (`lg:flex-row`, stacked on mobile):

**Left Column** (content, flex-1):
- Gradient `MessageSquare` icon (28px).
- Heading: "Sign in to **Universal Chat**" — "Universal Chat" in gradient text.
- Description: "Connect instantly with your Google account."
- 4 benefit items with staggered fade-in animation (framer-motion `staggerChildren: 0.1`):
  1. Send messages & share media (MessageSquare icon)
  2. Persistent profile across devices (Shield icon)
  3. Friend notifications & mentions (Zap icon)
  4. Synced conversations anywhere (Wifi icon)
- Footer: Green checkmark + "Free • No spam • One-click sign-in"

**Right Column** (auth card):
- Glassmorphism card: `bg-white/5 backdrop-blur-xl border border-white/10 rounded-3xl p-8`.
- Logo + "Welcome Back" heading + "Sign in with your Google account" text.

### 5.2 Auth States

| State | UI Behavior |
|-------|-------------|
| **Loading** (checking auth / loading client ID) | Three bouncing dots centered. |
| **Default** | Google Sign-In button rendered via GSI (Google Identity Services). Configured as `"standard" "pill" "outline" "large" "signin_with"`. Below: "By signing in, you agree to our Terms of Service and Privacy Policy" links. |
| **Signing in** | Bouncing dots + "Signing in..." replacing the button. |
| **Error** | Red toast notification: `bg-red-500/10 rounded-xl px-4 py-2` with error message text. |

### 5.3 Post-Auth: SpinModal

After successful first-time sign-in, a **SpinModal** appears:

1. **Phase "idle"**: "Get Your ID" gradient button with Sparkle icon.
2. **Phase "spinning"**: 6 digit boxes (`separate motion.div` per digit) cycle random numbers via setInterval, each stopping sequentially left-to-right with framer-motion settle animation.
3. **Phase "done"**: Full `#000000` ID revealed with copy button (Check icon confirmation for 2s). "Share this with friends!" text. "Start Chatting" dismiss button (navigates to `/chat`).

Modal: Dark themed (`bg-[#0a0a1a]`, `border-white/10`), decorative blurred circles (indigo + purple). `max-w-sm`.

---

## 6. Chat Interface (ChatPage) — Route: `/chat`

Requires authentication. Unauthenticated users are redirected to `/auth`.

### 6.1 Auth Loading State

Full-screen centered: gradient icon + SVG chat bubble path animation (`Path` with `strokeDasharray`/`strokeDashoffset` animation) + pulsing aura (`animate-pulse` on blur circle) + 3 bouncing dots + "Loading..." text.

### 6.2 Join Screen

Before joining: gradient icon, "#general" title, "Join the conversation" description, **"Join #general"** button (gradient `from-indigo-600 to-purple-600`, spring animation on click). After clicking, full chat interface renders.

### 6.3 AppLayout (Main Chat Shell)

`flex h-screen overflow-hidden dark:bg-[#050816]`:

**Desktop Sidebar** (`w-80 max-w-[85vw]`, `hidden md:flex`): Frosted glass (`bg-white/70 dark:bg-gray-900/70 backdrop-blur-xl`), `border-r border-gray-200/50 dark:border-gray-800/50`, `shadow-2xl`, `z-20`, `overflow-y-auto`.

**Sidebar sections**:

1. **Header** (p-6, border-b): Gradient icon (`bg-gradient-to-br from-indigo-500 to-purple-600`) with `whileHover={{ scale: 1.05, rotate: -5 }}`, title "Universal". Close button (X) only visible on mobile.

2. **Channels** (mb-4): "CHANNELS" label (uppercase, `tracking-[0.2em]`, text-xs, font-bold, text-gray-500). "# General" button with `#` in indigo circle. Active: `bg-indigo-100 dark:bg-indigo-900/30`. Hover: `hover:bg-gray-100 dark:hover:bg-gray-800`.

3. **Friends** (mb-6):
   - "FRIENDS" label (same style) + Users icon.
   - **Find People** button: UserPlus icon, opens FriendSearchModal.
   - **Friend Requests** button: Bell icon, optional red badge count (`.bg-red-500 text-white text-xs min-w-[18px]`), opens FriendRequestList.
   - Friend list rows: avatar circle (first letter, `bg-indigo-500`), display name, status text ("Online" or "X unread"), unread badge (red pill, "9+" overflow for >9).
   - Each row: `motion.button` with `whileHover={{ x: 2 }}`, `initial={{ opacity: 0, x: -10 }}`, staggered `transition={{ delay: index * 0.05 }}`.
   - Friend status dot: green (online) with breathing pulse animation, red (unread > 0).
   - Empty state: "No friends yet. Use \"Find People\" to search and add friends."

4. **Online Users** (mb-6):
   - "ONLINE" label + animated count badge (indigo pill, scales on update via framer-motion spring).
   - Online user rows: avatar circle, name, green dot with pulsing animation (`motion.span animate={{ scale: [1, 1.2, 1] }}`).
   - Empty state: "No users online yet."

5. **Quick Links** (border-t, pt-4):
   - "QUICK LINKS" label.
   - Profile (User icon, Link to `/profile`).
   - Home (Home icon, Link to `/`).
   - Community Guidelines (BookOpen icon, Link to `/guidelines`).
   - Each: `text-gray-600 dark:text-gray-400`, hover icon turns indigo.

6. **Bottom Profile Area** (p-4, border-t): User avatar (bg shows identity's avatarColor), display name, custom status (if any). Unique ID display: `#000000` format with copy button (shows Check icon for 2s, then reverts to Copy icon).

**Mobile Sidebar Overlay**: Same backdrop + spring pattern (slide from left, -320→0). Contains same SidebarContent with `onClose` prop.

**Mobile Header** (`md:hidden`): Frosted glass (`bg-white/80 dark:bg-gray-900/80 backdrop-blur-md`). Left: Menu button + gradient icon + title "#general". Right: Exit button (if joined, `hover:bg-red-500/10 text-red-500`), Users icon with online count badge.

**Desktop Room Header** (`hidden md:flex`): Frosted glass (`bg-white/60 dark:bg-gray-900/60 backdrop-blur-xl`). Left: Indigo dot + title "#general" + green dot + "X online" count + connection status badge. Right: Exit button + Dark mode toggle + Search button + Settings button.

**Connection Status Badge**:
- `connected`: `text-emerald-500`, "Connected".
- `reconnecting`: `text-amber-500 animate-pulse`, "Reconnecting...".
- `offline`: `text-red-500`, "Offline".

### 6.4 MessageList

Uses `@tanstack/react-virtual` for efficient rendering of large lists.

**MessageBubble** (individual message):

- `motion.div` with `initial={{ opacity: 0, y: 8 }}` fade-in.
- Max width: `max-w-[75%]`.
- **My messages**: Right-aligned (`flex-row-reverse`), gradient bg `from-indigo-600 to-indigo-700`, white text, `rounded-2xl rounded-tr-none`.
- **Others' messages**: Left-aligned, frosted glass `bg-white/80 dark:bg-gray-800/80 backdrop-blur-sm`, border, `rounded-2xl rounded-tl-none`.

**Hover Actions Toolbar** (appears on mouse hover or 500ms long-press on touch):

- `motion.div` with fade-up animation, `bg-white/80 dark:bg-gray-800/80 backdrop-blur-md`, `rounded-xl`, `shadow-lg`.
- **My messages**: Reply, Copy, Edit (Pencil), Delete (Trash2, `hover:text-red-500`).
- **Others' messages**: Reply, Copy, Report (Flag, `hover:text-amber-500`), Mute (VolumeX, `hover:text-red-500`).
- Divider lines between buttons.

**Sender Header**: Shown for first message in a group or after 5-minute gap. For others: Avatar (clickable → UserProfilePopover) + sender name in their avatarColor + "(edited)" badge. For own messages: no avatar, just "(edited)" badge.

**Reply Preview**: In bubble, `pl-3 border-l-2 border-indigo-500/50` showing replied-to sender name + truncated text. "Reply to {name}" label.

**Editing State**:
- Textarea replaces message text.
- Cancel + Save buttons below.
- Enter saves, Escape cancels.
- Max 500 characters.

**Message Status Indicators** (own messages):
- `sending`: Clock icon with `animate-pulse`.
- `sent`: Single checkmark.
- `delivered`: Double checkmark.
- `read`: Double checkmark in `text-blue-300`.

**ReactionBar**:
- Existing reactions shown as pill buttons (emoji + count).
- User's own reactions highlighted (`bg-indigo-100 dark:bg-indigo-900/40`).
- "+" button to add reaction — opens picker with 6 emojis: 👍 ❤️ 😂 😮 😢 🙏.
- Reactions appear on bubble hover.

**Thread Replies**: If message has replies, shows "X replies" button with MessageCircle icon.

**Date Separators**: Gradient line (`h-px bg-gradient-to-r from-transparent via-gray-300 dark:via-gray-600 to-transparent`) with date label pill ("Today" / "Yesterday" / full date format).

**System Messages**: Centered, italic, `text-xs text-gray-500`, pill-shaped badge.

**Scroll-to-Bottom Button**:
- Appears when scrolled up >200px.
- Shows "X new" count if messages arrived while scrolled up.
- `rounded-full`, `shadow-xl`, indigo hover, `bg-indigo-600 text-white`.
- Framer-motion scale bounce on appear.

**Typing Indicator**: Three bouncing dots + "{name} is typing..." text in indigo, italic.

**Skeleton Loading**: 6 placeholder message bubbles with `animate-pulse`.

**Empty State**: Animated MessageSquare icon (pulse scale via framer-motion), "No messages yet", "Start the conversation by sending a message below."

**Seen State**: IntersectionObserver marks messages as "delivered" when scrolled into view.

### 6.5 MessageInput

Frosted glass container: `bg-white/80 dark:bg-gray-900/80 backdrop-blur-xl p-2 rounded-2xl ring-1 ring-gray-200/50 dark:ring-white/10`. Focus state: `focus-within:ring-2 focus-within:ring-indigo-500/40`. Max width: `max-w-4xl mx-auto`.

**Elements in order**:

1. **Emoji Button**: Smile icon (`Smile` from lucide-react), toggles emoji picker. `hover:bg-gray-100 dark:hover:bg-gray-800 rounded-lg p-2`.
2. **Textarea**: `flex-1`, transparent bg, border-none, `resize-none`, placeholder "Type something amazing...", max 500 chars, auto-resizes up to 160px (`max-h-40`), `focus:outline-none`.
3. **Char Counter**: Visible after 200 chars, turns `text-red-500` at 450+.
4. **Send Button**: Indigo gradient when active (`from-indigo-600 to-purple-600`), disabled gray when empty/sending. Active: `hover:scale-105 active:scale-95`, `shadow-lg hover:shadow-indigo-500/25`. Send icon (`Send` from lucide-react).

**Emoji Picker**:
- `grid grid-cols-5 gap-1`, 20 emojis.
- `bg-white dark:bg-gray-800 border border-gray-200 dark:border-gray-700 rounded-2xl shadow-2xl`, `p-3`.
- Animated: `initial={{ opacity: 0, y: 10, scale: 0.95 }}` → `animate={{ opacity: 1, y: 0, scale: 1 }}`.
- Closes on outside click.

**Rate Limiting**: 1-second cooldown between sends (`COOLDOWN_MS = 1000`).

**Typing Broadcast**: Sends `typing_start`/`typing_stop` events via Supabase Realtime with 2s cooldown.

### 6.6 Reply Bar

When replying to a message, a bar appears above the input: "Replying to: {name} \"{text}\"" with Cancel button. `bg-white/50 dark:bg-gray-800/50 backdrop-blur-sm`, `rounded-t-2xl`, `px-4 py-2`.

### 6.7 DM Header Bar

When viewing a DM conversation: Back button (ArrowLeft `hover:bg-gray-100 dark:hover:bg-gray-800 rounded-lg p-2`), peer avatar+name+"DM" label. `bg-white/30 dark:bg-gray-800/30 backdrop-blur-sm`, border-b.

### 6.8 Realtime Features

- Supabase Realtime channel `'chat-room'`.
- Presence tracking (join/leave).
- Broadcast events: `new_message`, `reaction`, `message_edit`, `typing_start`, `typing_stop`, `message_seen`, `user_status`.
- Postgres changes fallback for reliability.
- DM conversations use polling (2s interval).
- General chat has 30s sanity re-fetch.
- Tab title updates with unread count.
- Browser Notification API request + display.

---

## 7. Modals & Overlays

All modals use `AnimatePresence` + `motion.div` with backdrop blur overlay. Standard pattern: `fixed inset-0 z-50 flex items-center justify-center`, backdrop `bg-black/50 backdrop-blur-sm`, content `bg-white dark:bg-gray-900 rounded-2xl shadow-2xl`.

### 7.1 SettingsModal

**Trigger**: Settings button in chat header (gear icon).
**Size**: `max-w-md`.

**Contents**:
1. "Enter to send" toggle: `checkbox` switch (`w-10 h-6 rounded-full`, indigo when active).
2. "Font size" selector: 3 segmented buttons (Small/Medium/Large). Active: `bg-indigo-600 text-white`. Inactive: `bg-gray-100 dark:bg-gray-800`.
3. "Message density" selector: 2 buttons (Compact/Comfortable). Same styling.

Settings persist to `localStorage` under `chat_settings`. Footer: "Done" gradient button. Close via X, backdrop click, Escape, or Done.

### 7.2 SearchOverlay

**Trigger**: `Ctrl+K`/`Cmd+K` or search button in chat header.
**Size**: `max-w-lg`.

**UI**:
- Search input with `Search` icon, placeholder "Search messages...".
- Keyboard hint: `esc` in `<kbd>` element.
- Results: scrollable list (`max-h-[50vh]`), each result shows avatar, sender name, timestamp, channel indicator (`#`), message text with `<mark>` highlighted match terms (via `dangerouslySetInnerHTML`).
- Keyboard navigation: ArrowUp/Down to select, Enter to open, Escape to close.
- **Empty states**: "No messages found" (with query) / "No messages in this room" (empty).
- Bottom bar: "↑↓ Navigate ↵ Select ⎋ Close" instructions.

### 7.3 FriendSearchModal

**Trigger**: "Find People" button in sidebar Friends section.
**Size**: `max-w-md`.

**UI**:
- Search input with `Search` icon, placeholder "Search by name or #ID...", 300ms debounce.
- **Loading**: Centered `Loader2` spinner (animate-spin).
- **Empty states**:
  - No query: "Type a name or #ID to search" with UserPlus icon.
  - No results: "No users found" with Search icon.
- User result rows: Avatar (gradient circle), display name, bio/ID# (clickable link), action button:
  - **Add** (UserPlus, indigo-600 bg) → sends friend request.
  - **Sent** (UserCheck, disabled, gray bg) — after request sent.
  - **Loading** — spinner while request in flight.
- Close via X, backdrop click, Escape.

### 7.4 FriendRequestList

**Trigger**: Bell icon in sidebar Friends section.
**Size**: `max-w-md`.

**UI**:
- **Loading**: Centered `Loader2` spinner.
- **Empty**: "No friend requests" with UserPlus icon.
- **Incoming section**: Each request: avatar, display name, "Wants to be friends" text, Accept (green `bg-emerald-600`) and Reject (red `bg-red-600`) buttons with loading spinner states.
- **Outgoing section**: Each request: avatar, display name, "Pending" status with Clock icon.

### 7.5 UserProfilePopover

**Trigger**: Click on any other user's avatar in message list.
**Position**: `absolute top-full left-0 mt-2`, `w-56`.

**UI**:
- User avatar (large, `w-14 h-14 rounded-full`), display name.
- Action button based on friend status:
  - `none`: "Add Friend" (indigo-600 bg)
  - `pending_sent`: "Pending" (amber bg)
  - `pending_received`: "Accept" (indigo bg)
  - `friends`: "Remove Friend" (red text, `hover:bg-red-500/10`)
  - `loading`: "..." with spinner
- Closes on outside click or scroll.

### 7.6 Modal Close Behaviors Summary

| Modal | Close Methods |
|-------|---------------|
| SettingsModal | X button, backdrop click, Escape, Done button |
| SearchOverlay | X button, backdrop click, Escape, Enter on result |
| FriendSearchModal | X button, backdrop click, Escape |
| FriendRequestList | X button, backdrop click, Escape |
| UserProfilePopover | Outside click, scroll |
| SpinModal | "Start Chatting" button only |

---

## 8. PageTransition Component

Wraps children in `motion.div`. Variants: `initial: { opacity: 0, y: 12 }`, `animate: { opacity: 1, y: 0 }`, `exit: { opacity: 0, y: -12 }`. Duration: 0.35s, easeOut. `will-change: transform, opacity`. Applied to every page via `AnimatedRoutes`.

---

## 9. ErrorBoundary

Full-screen centered error state:
- `bg-[#050816]` dark background.
- Gradient icon container (MessageSquare, 40px).
- "Something went wrong" heading.
- "An unexpected error occurred. Please try reloading the page." description.
- "Reload" button with `RotateCcw` icon, gradient bg, shadow, `active:scale-95` effect.

---

## 10. Profile Pages

### 10.1 My Profile (`/profile`)

Protected route (redirects to `/auth` if not authenticated).

**Layout**: `min-h-screen bg-[#050816]`, `max-w-lg mx-auto`, `px-4 py-8`.

**Back button**: "Back to Home" with ArrowLeft icon, `hover:bg-white/5 rounded-lg p-2 transition-colors`.

**Profile card**: Glassmorphism (`bg-white/5 backdrop-blur-xl border border-white/10 rounded-3xl p-8`).

**Header**: "Profile" title + unique ID# badge (indigo pill, `bg-indigo-600/20 text-indigo-400` with copy button).

**Form fields**:

1. **Avatar section**: Current avatar (gradient bg with letter, or uploaded image on top). "Random" button (Shuffle icon, `bg-indigo-600/20`). "Remove" button (Trash2 icon, `bg-red-500/20`).
2. **Display Name**: Input, `w-full`, `bg-white/5 border border-white/10 rounded-xl px-4 py-2`, `maxLength={50}`, dark themed.
3. **Bio**: Textarea, 3 rows, same styling, `maxLength={200}`, placeholder "Tell us about yourself...".
4. **Custom Status**: Input, `maxLength={80}`, placeholder "e.g. Away, Busy, Coding...".

**Error**: `bg-red-500/10 rounded-xl px-4 py-2` container.
**Success**: `bg-emerald-500/10 rounded-xl px-4 py-2` container.

**Save button**: Gradient `from-indigo-600 to-purple-600`, disabled when saving (spinner) or on cooldown. Note: "You can edit your profile once every 3 months". Cooldown indicator: amber text + Clock icon + remaining time.

**Logout section** (mt-8, pt-8 border-t border-white/10):
- "Sign Out" button: `border border-red-500/50 text-red-500 hover:bg-red-500/10 rounded-xl`.
- "Delete Account" button: subtle red text, double-confirm dialog (first click: "Are you sure?", second click: "Click again to confirm").

### 10.2 User Profile (`/profile/:userId`)

**Loading**: Centered `Loader2` spinner (`animate-spin h-8 w-8 text-indigo-500`).

**Error / Not Found**: Back button + "User not found" card.

**Profile card** (same glassmorphism style):
- Back button (navigate -1).
- Large avatar (`w-20 h-20`, `text-3xl`).
- Display name, status.
- Bio section (if exists): italic, `bg-black/20 rounded-xl px-4 py-2`.
- "Member since" date with Clock icon.
- **Friend status area**:
  - `none`: "Add Friend" gradient button.
  - `pending_sent`: Amber "Friend Request Pending" (`bg-amber-500/20 text-amber-400`).
  - `pending_received`: Accept (green) + Reject (red) buttons.
  - `friends`: Emerald "Friends" badge (`bg-emerald-500/20 text-emerald-400`).
- Unique ID# badge with copy button.

---

## 11. Information Pages

All share: `max-w-4xl mx-auto px-4 py-20` with glass cards (`bg-white/5 dark:bg-gray-900/5 backdrop-blur-xl border border-gray-200/50 dark:border-white/10 rounded-2xl p-6`), section icons. Wrapped in SiteLayout (header + footer).

### 11.1 About Page (`/about`)

**Hero**: Heading + subtitle about the platform's purpose.

**"How It Works"** (5-step flow on md, stacked on mobile):
1. Open Browser (Monitor icon)
2. Choose Identity (Heart icon)
3. Connect via Supabase Realtime (Wifi icon)
4. Chat Realtime (Globe icon)
5. Local Storage (Lock icon)
- Animated ArrowRight icons between steps (desktop only, x-axis bounce via framer-motion `animate={{ x: [0, 5, 0] }}`).
- Each step: icon in gradient circle, title, description text.

**Architecture diagram** (glass card):
- 3 connected nodes: "Your Browser" → "Supabase" → "Other Browsers".
- Animated Wifi icons between nodes (x-axis bounce).
- Each node: gradient icon, label, sub-label.
- "Data encrypted at rest" badge.

**Mission section**: Shield icon + "Our Mission" heading + "To provide a free, open, and private communication platform..." statement.

### 11.2 FAQ Page (`/faq`)

**Search bar**: Search icon + input "Search questions...", glass styling, focus ring.

**Category badges**: All, General, Privacy, Safety, Usage, Technical — pill buttons (`rounded-full px-4 py-1.5`). Active: `bg-indigo-600 text-white shadow-md`. Inactive: `bg-white/5 border border-white/10 hover:bg-white/10`. Clicking sets filter.

**FAQ accordion**: Each item: icon + question + category badge, expandable with animated height (framer-motion `layout`). At bottom of each expanded answer:
- "Was this helpful?" section with ThumbsUp/ThumbsDown buttons (interactive, change color on click).

**11 expanded answers** covering:
1. What is Universal Chat Area? — Detailed explanation with architecture.
2. Privacy — Local-first, message flow, metadata collection.
3. Identity — UUID, name/color, Google OAuth.
4. Realtime messaging under the hood.
5. Browser closure persistence.
6. Mobile app (PWA).
7. Reporting inappropriate content.
8. Dark mode & theming.
9. Free pricing.
10. Open source.
11. Providing feedback.

### 11.3 Guidelines Page (`/guidelines`)

**Hero**: "Community Guidelines" heading + "Keep our community safe and welcoming" subtitle.

**Quick summary badges**: Row of pill buttons for each section, clicking scrolls to section (smooth scroll).

**6 accordion sections** (glass cards, clickable headers with ChevronDown rotation, animated content):
1. Allowed Behavior (ThumbsUp) — Be respectful, stay on topic, etc.
2. Prohibited Content (ThumbsDown) — No hate speech, spam, NSFW, etc.
3. Spam Policy (Ban) — No excessive self-promotion.
4. Harassment Rules (Flag) — No targeting, doxxing, etc.
5. Reporting Process (MessageCircle) — How to report violations.
6. Enforcement (Shield) — Warnings, temporary bans, permanent bans.

**Footer note**: Amber card — "Guidelines may be updated. Check back periodically."

### 11.4 Privacy Page (`/privacy`)

**Hero**: Heading + "Last updated: May 2026".

**Data Flow Visualization** (glass card):
- Animated 5-node flow: "Your Browser" → "Supabase Realtime" → "Server Persistence (Postgres)" → "Local Cache (IndexedDB)".
- Each node has gradient icon + label.
- Animated arrow icons between nodes.

**Comparison Table** (glass card, `overflow-x-auto`):
- 6 rows comparing Universal Chat vs "Other Platforms".
- Features: Authentication, Message Storage, Email Required (✗ / ✓), Phone Required (✗ / ✓), Tracking/Analytics (✗ / ✓), Data Portability.
- Universal Chat column: green checks and red X's.

**6 Policy Sections** (glass cards with icons):
1. Authentication (Shield) — Google OAuth only, no password storage.
2. Message Persistence (Database) — Messages stored in Postgres.
3. Realtime Communication (Wifi) — WebSocket connections.
4. Local Cache (Database) — IndexedDB for offline access.
5. Data Collection & Use (Eye) — Minimal data for operation.
6. Your Rights (FileText) — Access, deletion, portability.

### 11.5 Terms Page (`/terms`)

**Hero**: Heading + "Last updated: May 2026".

**5 sections** (glass cards with icons):
1. Acceptance of Terms (FileText) — Summary badge: "By using Universal Chat Area, you agree to these terms."
2. User Responsibilities (Scale) — Account security, lawful use.
3. Prohibited Uses (Ban) — Illegal activity, abuse, disruption.
4. Limitation of Liability (AlertTriangle) — Service provided "as is".
5. Intellectual Property & Content (Gavel) — User retains content ownership.

### 11.6 Contact Page (`/contact`)

**Hero**: Heading + "Have questions or feedback?" subtitle.

**3 cards** (glass, hover border turns indigo):
1. Portfolio (ExternalLink) — "Visit my portfolio" → external link.
2. Community (MessageCircle) — "Join the chat room".
3. FAQ (HelpCircle) — "Visit our FAQ page".

**CTA section**: Large gradient button "Visit Portfolio" with ExternalLink icon, `shadow-2xl hover:shadow-indigo-500/25`, `active:scale-95`.

### 11.7 Blog Page (`/blog`)

**Hero**: Heading + "Thoughts on development, privacy, and community." subtitle.

**Category filters**: Row of pill buttons: All, Architecture, Privacy, Engineering, Deployment, Community. Active: `bg-indigo-600 text-white shadow-md`. Inactive: glass style with hover effect.

**Articles grid** (`md:grid-cols-2`, gap-6):
- 7 article cards with:
  - Category badge (gradient bg).
  - Title (hover: `text-indigo-600`).
  - Excerpt.
  - Date (Calendar icon).
  - Read time (Clock icon).
- Glass card style, hover border turns indigo, `cursor-pointer`.

**Empty state**: "No articles in this category yet." — centered, with BookOpen icon.

**Footer**: "More articles coming soon." — emerald badge.

---

## 12. Color System

| Role | Light Mode | Dark Mode |
|------|-----------|-----------|
| Page background | `#fafafa` | `#050816` |
| Cards/panels | `bg-white/50-80` + `backdrop-blur` | `bg-gray-900/50-80` + `backdrop-blur` |
| Primary accent | Indigo-500/600 (`#6366F1`) | Same (different opacities) |
| Secondary accent | Purple-500/600 (`#A855F7`) | Same |
| Text primary | `text-gray-900` (`#111827`) | `text-white` / `text-gray-100` |
| Text secondary | `text-gray-600` | `text-gray-200` |
| Text muted | `text-gray-400/500` | Same |
| Borders | `border-gray-200/50` | `border-gray-800/50` or `border-white/10` |
| Success | Emerald-500/600 | Same |
| Error/Danger | Red-400/500 | Same |
| Warning | Amber-500 | Same |
| Selection | `bg-indigo-500/30 text-white` | Same |
| Scrollbar thumb | `rgba(0,0,0,0.15)` | `rgba(255,255,255,0.15)` |
| Dot-grid pattern | `rgba(0,0,0,0.05)` | `rgba(255,255,255,0.05)` |

---

## 13. Typography Scale

| Element | Weight | Size | Class |
|---------|--------|------|-------|
| Hero heading | ExtraBold (800/900) | `text-4xl` to `text-7xl` | `font-extrabold` |
| Section titles | Bold (700) | `text-2xl` to `text-3xl` | `font-bold` |
| Body text | Regular (400) | `text-sm` to `text-lg` | `font-normal` |
| Labels/headings | Bold (700) | `text-xs` uppercase | `font-bold text-xs tracking-wider` |
| Code | — | `text-xs` | `font-mono` |
| Message text | Regular | `text-sm` | `prose-sm` |
| Timestamps | SemiBold | `text-[11px]` | — |

---

## 14. Responsive Design Breakpoints

| Breakpoint | Behavior |
|-----------|----------|
| **Mobile** (<640px) | Single column layouts, slide-out nav, full-width modals, 30 particle count, stacked footer |
| **sm** (640px) | "Sign In" text visible, "Join Chat" button appears, stats 2-column |
| **md** (768px) | Desktop nav replaces hamburger, sidebar visible, 2-column grids, 3-column footer |
| **lg** (1024px) | Auth page side-by-side, feature cards 3-column |

**Mobile-specific behaviors**:
- Sidebar becomes overlay (spring animation from left).
- Shorter particle count (30 vs 80).
- All touch targets >= 44px.
- Long-press (500ms) on messages to show action toolbar.
- `visualViewport` API for keyboard handling (scroll input into view).

---

## 15. Complete Animation Inventory

| Element | Animation | Library |
|---------|-----------|---------|
| Page transitions | Opacity + y-slide (0.35s, easeOut) | framer-motion |
| Route animation | `popLayout` mode | framer-motion `AnimatePresence` |
| Mobile sidebar | Spring slide x: 320→0 (damping:25, stiffness:200) | framer-motion |
| All modals | Backdrop fade + content scale (0.95→1, spring) | framer-motion |
| FAQ accordions | Height: 0→auto + opacity | framer-motion |
| Message bubbles | Fade-up on mount (0.2s) | framer-motion |
| Hover toolbar | Fade-up (opacity + y:4) | framer-motion |
| Reactions picker | Scale (0.9→1) | framer-motion |
| Typing indicator | Three bouncing dots (staggered) | CSS `animate-bounce` |
| Stats counters | Eased count-up (quartic, 8s) | requestAnimationFrame |
| Page loading | 3 bouncing dots (staggered) | CSS `animate-bounce` |
| Avatar color change | 0.5s duration | CSS transition on parent |
| Dark mode toggle | 500ms transition | CSS `transition-colors` |
| Scroll-to-bottom | Scale bounce on appear | framer-motion |
| Message status | Pulse on `sending` | CSS `animate-pulse` |
| Online presence dot | Breathing pulse (scale 1→1.2) | framer-motion `animate` |
| Hero 3D scene | Bubble orbit + particle rotation | Three.js animation loop |
| Background orbs | Floating x/y paths (12s-32s) | framer-motion `animate` |
| Particle field | Upward drift + connection lines | Canvas requestAnimationFrame |
| Spin modal digits | Rapid cycling → settle (sequential) | setInterval + framer-motion |
| Tilt cards | 3D rotate on mouse move | Custom `useTilt` hook |
| Architecture arrows | X-axis bounce | framer-motion infinite |
| Connection status | Pulse on reconnecting | CSS `animate-pulse` |
| Friend notification badge | Scale bounce on update | framer-motion spring |
| Reduced motion | All disabled | `prefers-reduced-motion` media |

---

## 16. Keyboard Shortcuts

| Shortcut | Action |
|----------|--------|
| Enter | Send message (when "Enter to send" is enabled in settings) |
| Shift+Enter | New line in message input |
| Escape | Close modals, cancel reply, close search |
| Ctrl+K / Cmd+K | Open search overlay |
| ArrowUp/Down | Navigate search results |

---

## 17. PWA (Progressive Web App) Features

| File | Purpose |
|------|---------|
| `manifest.json` | PWA manifest — name "Universal Chat Area", `display: standalone`, theme_color `#7C3AED` (purple), SVG icons at 48/192/512px |
| `sw.js` | Service worker — cache-first for static assets, network-first for navigation + assets, offline HTML fallback page |
| `register-sw.js` | Service worker registration (loads after initial page render) |
| `robots.txt` | Allow all, sitemap link |
| `sitemap.xml` | 8 URLs with priorities (1.0 homepage → 0.5 contact) |
| `favicon.svg` | Purple lightning bolt icon |
| `icons/icon-192.svg` | 192×192 PWA icon |
| `icons/icon-512.svg` | 512×512 PWA icon |

---

## 18. Complete Error / Empty / Loading State Matrix

| Component | Loading | Empty | Error |
|-----------|---------|-------|-------|
| ChatPage auth check | Bouncing dots + "Loading..." | — | Redirect → `/auth` |
| ChatPage messages | 6 skeleton bubbles (`animate-pulse`) | Animated MessageSquare + "No messages yet" | — |
| Friend search modal | `Loader2` spinner | "No users found" / "Type a name or #ID..." | Silent catch (logged) |
| Friend request list | `Loader2` spinner | "No friend requests" | Silent catch (logged) |
| Auth page | Bouncing dots + "Signing in..." | — | Red error toast (`bg-red-500/10`) |
| Profile page | Returns null while loading | — | Red toast |
| Other user profile | `Loader2` spinner | — | "User not found" card |
| Blog articles | — | "No articles in this category yet." | — |
| FAQ search results | — | "No matching questions found." | — |
| ErrorBoundary (global) | — | — | Full-screen error + "Reload" button |
| Realtime connection | — | — | Amber pulsing "Reconnecting..." badge |
| Spin modal | Spinning digit animation | — | — |

---

## 19. Complete User Flow Walkthrough

### First-Time User

1. **Landing**: User arrives at homepage. Sees 3D bubbles floating in hero, reads "Universal Chat Area" with gradient text, subtitle about privacy-first chat. Two buttons: "Sign In with Google" (primary gradient) and "Learn More" (outline).

2. **Scroll**: User scrolls down. Stats count up (50,000+ messages, 1,200+ users, 99.9% uptime, 150+ countries). Chat preview with mock conversation. Tech stack badges. Core features in tilt cards. Testimonials. FAQ accordion.

3. **Sign In**: User clicks "Sign In with Google" → navigates to `/auth`. Sees two-column layout (benefits on left, auth card on right). Clicks Google Sign-In button → Google popup → grants permissions → first-time SpinModal triggers → digits cycle → reveals #ID → copies it → clicks "Start Chatting".

4. **Join Chat**: Navigated to `/chat`. Sees "Join #general" screen. Clicks button → full chat interface renders.

5. **First Message**: Empty state "No messages yet". Types in composer "Hello everyone!". Presses Enter. Message appears right-aligned with indigo gradient. Sending indicator → checkmark → double checkmark.

6. **Explore Sidebar**: Opens sidebar (or already visible on desktop). Sees channels, empty friends list ("No friends yet"), empty online users, quick links, own profile at bottom.

7. **Find People**: Clicks "Find People". Search modal opens. Types name. Results appear. Clicks "Add Friend". Button changes to "Sent" (disabled).

8. **Accept Request**: Other user sees bell badge → opens FriendRequestList → accepts → now mutual friends.

9. **Profile**: Clicks header profile → `/profile`. Edits display name, bio, custom status. Clicks "Random" avatar color. Saves (3-month cooldown starts).

10. **Settings**: Opens Settings modal from chat header. Toggles "Enter to send", adjusts font size to Large, density to Comfortable. Clicks Done.

11. **Search**: Presses Ctrl+K → SearchOverlay opens → types query → sees results with highlighted matches → navigates with arrows → opens message.

12. **Dark Mode**: Clicks dark mode toggle in header. Entire UI transitions to `#050816` background over 500ms.

13. **Mobile**: Resizes browser. Header shows hamburger menu. Opens → slide panel from right. Navigates to About page. Footer at bottom of page.

### Returning User

1. Arrives at landing → already authenticated → "Build Your Friends" button instead of "Sign In".
2. Goes directly to `/chat` → quick join → messages loaded from IndexedDB cache → new messages stream in via Realtime.
3. Unread count in tab title updates.
4. Scrolls up → sees previous messages with date separators.
5. Hovers message → sees action toolbar → clicks Reply → reply bar appears → types → sends.
6. Clicks emoji reaction on message → picker appears → selects 👍.

### Admin / Developer

1. Goes to `/blog` → reads articles about architecture, deployment, privacy.
2. Goes to `/about` → studies architecture diagram and data flow.
3. Goes to `/privacy` → reads data collection policies, comparison table.

---

## 20. UI Component Library Summary

| Component | Description | Used In |
|-----------|-------------|---------|
| `SiteLayout` | Header + footer shell | Landing, About, FAQ, Guidelines, Privacy, Terms, Contact, Blog |
| `AppLayout` | Sidebar + chat shell | ChatPage |
| `PageTransition` | Framer-motion page wrapper | All pages |
| `ParticleField` | Canvas particle background | All pages (via SiteLayout / inline) |
| `BackgroundOrbs` | Animated gradient orbs | All pages |
| `ThreeHeroScene` | Three.js 3D bubble scene | LandingPage hero |
| `TiltCard` | 3D tilt card wrapper | LandingPage feature cards |
| `ErrorBoundary` | Global error catch | Root App |
| `MessageList` | Virtualized message list + bubbles | ChatPage |
| `MessageInput` | Composer with emoji picker | ChatPage |
| `SearchOverlay` | Ctrl+K search modal | ChatPage |
| `SettingsModal` | Chat settings (font, density, enter-to-send) | ChatPage |
| `FriendSearchModal` | Search users by name/ID | ChatPage sidebar |
| `FriendRequestList` | Accept/reject friend requests | ChatPage sidebar |
| `UserProfilePopover` | Hover card on user avatar | MessageList |
| `SpinModal` | First-time ID reveal | AuthPage (post-auth) |
| `LoadingFallback` | 3 bouncing dots | App Suspense |
| `BackgroundOrbs` | Decorative gradient orbs | All pages |

---

*Documentation generated from source code analysis — `src/` (43 files) and `public/` (9 files).*
