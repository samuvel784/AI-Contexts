# Memories That Stay Forever

## Website Overview

**Live URL:** https://class-memory.vercel.app

**Tagline:** "From strangers to unforgettable stories"

A premium digital yearbook built for the 2023–2026 Computer Applications batch. This website preserves the memories, friendships, photos, videos, and personal stories of 38 students in an interactive, visually rich format.

---

## About This Website

This website serves two purposes:

**1. A digital yearbook** — Preserving the memories of the 2023–2026 Computer Applications batch for students, families, and friends to enjoy.

**2. A demo / portfolio showcase** — This website demonstrates Samuvel's ability to build premium digital yearbook websites. It is a working sample that shows what you can request for your own batch — whether 10th standard, 12th standard, or college. If you're interested in getting a similar website, scroll to the footer and click "Contact" under the About section.

---

## Purpose

This website exists to preserve the precious moments of a college batch's journey together — the friendships, laughter, and lessons that shaped them. It serves as a digital time capsule where batchmates and their families can look back and remember their shared experience.

---

## Who Is This For?

- **Students and alumni** of the 2023–2026 Computer Applications batch
- **Friends and family** of batch members who want to see profiles and memories
- **Potential customers** looking for a custom digital yearbook website for their own batch
- **Anyone looking for inspiration** to create a similar digital yearbook for their own batch
- **General visitors** who appreciate nostalgic, memory-focused websites

---

## Get Your Own Digital Yearbook

Samuvel builds custom digital yearbook websites for any batch. This website serves as a live demo — what you see here is what you can get for your own class or group.

### Pricing

| Option | Price |
|--------|-------|
| Same template (customize with your batch data) | **₹1000** |
| With modifications (colours, layout, extra features) | **₹1200 – ₹2000** |
| Per student (for larger batches) | **₹30 per student** |

Available for 10th standard, 12th standard, and college batches (UG and PG).

### What You Get

- A fully custom digital yearbook website hosted and ready to share
- Individual profiles for every student with photos, quotes, and messages
- Image gallery and video gallery
- Premium animated design with 3D effects
- Mobile-friendly responsive layout
- One-time payment — no monthly fees or subscriptions

### How to Order

1. Scroll to the footer of any page on this website
2. Click "Contact" under the About section
3. You'll be taken to Samuvel's portfolio where you can reach out

---

## Main Features

| Feature | Description |
|---------|-------------|
| **Animated Hero Section** | 3D bird animation with star field, floating orbs, and scroll-triggered effects |
| **Friendship Quotes Section** | Four heartwarming quotes about the batch experience |
| **Student Carousel** | Horizontally scrollable cards for all 38 students, with auto-scroll and drag support |
| **Student Profiles** | Individual pages for each student with personal bio, quote, best moment, message to class, avatar, and media |
| **Image Gallery** | Masonry-style photo gallery with hover zoom and lazy loading |
| **Video Gallery** | Column-based video gallery with hover-to-play, click-to-toggle playback |
| **Combined Media Gallery** | Images and videos shown together on each student profile page |
| **Scroll Progress Bar** | A thin glowing progress bar at the top of the page showing how far you've scrolled |
| **Ambience Toggle** | A footer button to toggle a nostalgic visual effect |
| **Mobile Responsive Design** | Fully functional on phones, tablets, and desktops |
| **404 Page** | A themed error page when a page is not found |

---

## Website Structure

### Homepage (`/`)

The landing page contains:
- **Hero Section** — VANTA.BIRDS 3D animation with flying birds, twinkling stars, glowing orbs, and the site title "Memories That Stay Forever"
- **Batch Stats** — Shows 38 Dreamers, 3 Years, ∞ Memories
- **Navigation Buttons** — "Browse Memories" (scrolls to student section) and "Our Story" (scrolls to friendship section)
- **Class Stats** — Department badge (Computer Applications), year range (2023–2026)
- **Friendship Section** — Four quote cards about friendship and batch life
- **Batch Timeline** — Year-by-year journey from 2023 to 2026
- **Student Carousel** — Scrollable row of all 38 student cards (drag with mouse or finger, or use arrow buttons)
- **Media Navigation** — Two large buttons linking to the Images and Videos pages
- **Closing Quote** — "Every face here is a chapter. Every name, a memory." signed by Class of 2023–2026

### Images Page (`/images`)

Displays a masonry (Pinterest-style) gallery of batch photos. Images load lazily and have hover zoom effects. If an image fails to load, a "Failed to load" message with a Retry button appears.

### Videos Page (`/videos`)

Displays a column-based gallery of batch videos. Each video plays inline when you hover over it or click on it. Click again to pause.

### Student Profile Page (`/student/:id`)

Individual page for each student (IDs 1 through 38). Contains:
- **Back Button** — Return to previous page
- **Profile Header** — Avatar with rotating gradient ring, student name, tagline, department badge, year badge
- **Personal Memory** — The student's own reflection on their three years
- **Favourite Quote** — A meaningful quote from the student
- **Best Moment** — Their favourite memory from batch life
- **Message to Class** — A farewell or thank-you message directed at classmates
- **Media Gallery** — Combined batch images and videos
- **Previous/Next Navigation** — Buttons to move between adjacent student profiles

### 404 Page (any unrecognized route)

Shows "This memory doesn't exist yet" with a "Return to Memories" button linking back to the homepage.

---

## Navigation

### Top Navigation Bar

The navbar is fixed at the top of every page and contains:
- **Memories logo** (left) — Click to return to the homepage
- **Images link** — Navigate to the Images gallery
- **Videos link** — Navigate to the Videos gallery

On mobile, the navbar links collapse into a hamburger menu button.

### Footer Links (on every page)

The footer contains:
- **Brand section** — "Memories" logo with a description of the yearbook
- **Batch Info** — Year (2023–2026), number of students (38), department (Computer Applications)
- **Navigate section** — Links to Home, Images, Videos, All Students (scrolls to carousel), Our Story (scrolls to friendship section)
- **Ambience** — Toggle button for a nostalgic visual effect
- **About** — "What We Collect" modal and "Contact" link to Samuvel's portfolio

### Section Anchors on Homepage

- `#students` — Scrolls to the student carousel
- `#friendship` — Scrolls to the friendship quotes section
- `#hero` — Scrolls to the top hero section

---

## Student Directory

All 38 students with their ID numbers, names, and roll numbers. Use the ID to navigate directly to a student's profile at `/student/[ID]` (e.g., `/student/5`).

| ID | Name | Roll Number |
|----|------|-------------|
| 1 | Aarav Krishnamurthy | CS23001 |
| 2 | Priya Sundaram | CS23002 |
| 3 | Karthik Rajan | CS23003 |
| 4 | Ananya Iyer | CS23004 |
| 5 | Rahul Murugan | CS23005 |
| 6 | Deepika Sundararajan | CS23006 |
| 7 | Arjun Venkatesh | CS23007 |
| 8 | Sneha Pillai | CS23008 |
| 9 | Vikram Patel | CS23009 |
| 10 | Meera Natarajan | CS23010 |
| 11 | Rohan Menon | CS23011 |
| 12 | Kavya Subramanian | CS23012 |
| 13 | Aditya Reddy | CS23013 |
| 14 | Lakshmi Balaji | CS23014 |
| 15 | Siddharth Kumar | CS23015 |
| 16 | Divya Chandran | CS23016 |
| 17 | Nikhil Sharma | CS23017 |
| 18 | Pooja Raghunathan | CS23018 |
| 19 | Akash Krishnan | CS23019 |
| 20 | Revathi Mohan | CS23020 |
| 21 | Pranav Suresh | CS23021 |
| 22 | Nithya Venkatesan | CS23022 |
| 23 | Harish Babu | CS23023 |
| 24 | Swetha Anand | CS23024 |
| 25 | Vineeth Raj | CS23025 |
| 26 | Gayathri Mani | CS23026 |
| 27 | Suresh Pandian | CS23027 |
| 28 | Anjali Nair | CS23028 |
| 29 | Manoj Selvam | CS23029 |
| 30 | Dharani Kumari | CS23030 |
| 31 | Ravi Chandrasekaran | CS23031 |
| 32 | Vaishnavi Prakash | CS23032 |
| 33 | Dinesh Moorthy | CS23033 |
| 34 | Keerthana Srinivasan | CS23034 |
| 35 | Naveen Kumar | CS23035 |
| 36 | Preethi Rajendran | CS23036 |
| 37 | Ashwin Gopal | CS23037 |
| 38 | Ramya Lakshmi | CS23038 |

**How to find a student by name:**
- Open the homepage and scroll to the student carousel
- Drag or use the arrow buttons to scroll through the cards until you find the name
- Click the card to open their profile
- Or navigate directly using the student's ID: `https://class-memory.vercel.app/student/[ID]`

**Note:** There is no search bar on the website. Use the table above or browse the carousel to find a specific student.

---

## Complete User Journeys

### Journey 1 — Landing on the Website

**Step 1 — Arrive at the Homepage**

**What the user sees:** A dark cosmic background with glowing gold and rose-coloured birds flying across the screen. Stars twinkle. The title "Memories That Stay Forever" appears with a subtitle: "From strangers to unforgettable stories."

**What the user does:** Nothing — the animation plays automatically. Scroll down to explore.

**What happens:** As the user scrolls, the hero section fades out smoothly and new content appears.

---

**Step 2 — See Batch Stats**

**What the user sees:** Numbers appear: 38 Dreamers, 3 Years, ∞ Memories.

**What the user does:** Continue scrolling.

**What happens:** The friendship section comes into view.

---

**Step 3 — Read Friendship Quotes**

**What the user sees:** Four beautifully designed quote cards with animated entry effects. Each quote reflects on the batch's journey.

**What the user does:** Read the quotes as they animate in. Continue scrolling.

**What happens:** A timeline section appears showing the batch's journey year by year (2023 → 2024 → 2025 → 2026).

---

### Journey 2 — Browsing Students

**Step 1 — Reach the Student Carousel**

**What the user sees:** A section titled "The Unforgettable 38" with a horizontal row of student cards. Cards show each student's avatar, name, and tagline. The carousel auto-scrolls slowly.

**What the user does:** Use any of these methods to browse:
- Drag left/right with your mouse or finger
- Click the left/arrow buttons next to the "Drag to explore" text
- Wait for auto-scroll

**What happens:** Cards move smoothly. Each card has a coloured gradient ring around the avatar.

---

**Step 2 — Explore a Student**

**What the user sees:** Student cards with avatar, name, and tagline.

**What the user does:** Click or tap any student card.

**What happens:** The browser navigates to that student's profile page (e.g., `/student/1`).

---

### Journey 3 — Viewing a Student Profile

**Step 1 — Arrive at Profile Page**

**What the user sees:** A detailed profile page with a back button, the student's avatar (with a rotating gradient ring), name, tagline, department badge, and year badge.

**What the user does:** Scroll down to see more.

**What happens:** Info cards animate into view one by one.

---

**Step 2 — Read Personal Details**

**What the user sees:** Four information cards:
- **Personal Memory** — The student's reflection
- **Favourite Quote** — A meaningful quote
- **Best Moment** — Their top memory
- **Message to Class** — A farewell message

**What the user does:** Read each card.

**What happens:** Cards fade in with a slight delay between each.

---

**Step 3 — View Media Gallery**

**What the user sees:** A "Memories" section with batch photos and videos displayed in a grid.

**What the user does:** Click a video to play it (click again to pause). Hover over images to see a zoom effect.

**What happens:** Videos play inline. Only one video plays at a time.

---

**Step 4 — Navigate to Another Student**

**What the user sees:** "Previous" and "Next" buttons at the bottom of the profile.

**What the user does:** Click "Next" to go to the next student (e.g., from `/student/1` to `/student/2`), or "Previous" to go back.

**What happens:** The next student's profile loads. At student 1, only "Next" appears. At student 38, only "Previous" appears.

---

**Step 5 — Return to Main Page**

**What the user sees:** An "All" or "Back" button in the profile header.

**What the user does:** Click "← All" or the browser's back button, or use the navbar "Memories" logo.

**What happens:** You return to the homepage (or your previous page).

---

### Journey 4 — Browsing Images

**Step 1 — Navigate to Images**

**What the user does:** Click the "Images" link in the navbar, the "Images" button on the homepage, or the "Images" link in the footer.

**What happens:** The page navigates to `/images`.

---

**Step 2 — View the Gallery**

**What the user sees:** A masonry (Pinterest-style) grid of photos with a "Back" button at the top and "Images" as the page title.

**What the user does:** Scroll down to see all photos. Hover over any photo to see a zoom effect.

**What happens:** Images load lazily as you scroll (they appear as you get near them).

---

**Step 3 — Handle Loading Failures (if any)**

**What the user sees:** If an image fails to load, a placeholder appears with "Failed to load" message and a "Retry" button.

**What the user does:** Click "Retry" to attempt loading the image again.

**What happens:** The image tries to load again.

---

**Step 4 — Return**

**What the user does:** Click the "Back" button at the top of the page.

**What happens:** You return to the homepage.

---

### Journey 5 — Watching Videos

**Step 1 — Navigate to Videos**

**What the user does:** Click the "Videos" link in the navbar, the "Videos" button on the homepage, or the "Videos" link in the footer.

**What happens:** The page navigates to `/videos`.

---

**Step 2 — View the Video Gallery**

**What the user sees:** A column-based grid of videos with a "Back" button at the top and "Videos" as the page title.

**What the user does:** Hover over any video to start playing it. Click a video to toggle play/pause.

**What happens:** Videos play inline with sound. Hover away or click again to pause.

---

**Step 3 — Handle Loading Failures (if any)**

**What the user sees:** If a video fails to load, a placeholder appears with "Failed to load video" and a "Retry" button.

**What the user does:** Click "Retry."

**What happens:** The video tries to load again.

---

**Step 4 — Return**

**What the user does:** Click the "Back" button at the top of the page.

**What happens:** You return to the homepage.

---

### Journey 6 — Navigating Between Students

**Step 1 — On a Student Profile**

**What the user sees:** Previous and Next buttons at the bottom of the profile page.

**What the user does:** Click "Next" or "Previous."

**What happens:** The page navigates to the adjacent student's profile. The transition is animated.

---

### Journey 7 — Contacting Samuvel

**Step 1 — Open the Footer**

**What the user does:** Scroll to the bottom of any page.

**What happens:** The footer is visible with various links.

---

**Step 2 — Click Contact**

**What the user does:** Click the "Contact" link in the "About" section of the footer.

**What happens:** A new browser tab opens with Samuvel's portfolio website.

---

### Journey 8 — Handling Missing Pages

**Step 1 — Visit an Invalid URL**

**What the user does:** Navigate to a page that doesn't exist (e.g., `/random-page`).

**What happens:** The 404 page displays with the message "This memory doesn't exist yet" and a subtitle "The page you're looking for has faded like an old photograph."

---

**Step 2 — Return to Safety**

**What the user sees:** A "Return to Memories" button.

**What the user does:** Click the "Return to Memories" button.

**What happens:** The browser navigates back to the homepage.

---

## Feature Documentation

### Animated Hero Background

**What It Does:** Creates a visually stunning introduction to the website with 3D birds flying across a starry cosmic background.

**How To Access It:** It appears automatically on the homepage when you first visit the site.

**How To Use It:** Simply watch — the animation runs on its own. You can also move your mouse to interact with the birds (they respond to cursor movement).

**Tips:** The birds, stars, and glowing orbs are designed to create a nostalgic, emotional mood. Spend a moment enjoying the animation before scrolling.

---

### Friendship Section

**What It Does:** Displays four emotionally resonant quotes about the batch's journey, followed by a year-by-year timeline.

**How To Access It:** Scroll down past the hero section on the homepage. Alternatively, click "Our Story" in the footer.

**How To Use It:** Read the quotes as they fade in. Continue scrolling to see the 2023–2026 timeline.

**Tips:** Each quote has a different accent colour (gold, rose, sky, lavender). The timeline on the right side shows the progression of the batch's journey.

---

### Student Carousel

**What It Does:** Shows all 38 students in a horizontally scrollable row of cards, each displaying an avatar, name, and tagline.

**How To Access It:** Scroll down past the friendship section on the homepage, or click "All Students" in the footer.

**How To Use It:**
- **Desktop:** Drag left or right with your mouse, or use the ◀ / ▶ arrow buttons
- **Mobile:** Swipe left or right with your finger
- The carousel auto-scrolls slowly but pauses when you interact with it

**Tips:** Auto-scroll resumes about 1.5–2 seconds after you stop interacting. Click any student card to open their full profile.

---

### Student Profiles

**What It Does:** Shows detailed information about each of the 38 batch members, including their personal memory, favourite quote, best moment, and message to the class.

**How To Access It:** Click any student card on the homepage carousel, or navigate directly to `/student/1` through `/student/38`.

**How To Use It:**
1. Click a student card to open their profile
2. Scroll down to read their personal memory, quote, best moment, and message
3. Browse the media gallery section to see batch photos and videos
4. Use the "Previous" and "Next" buttons at the bottom to move between students

**Tips:** Each profile has a unique colour scheme based on the student's ID. The avatar has a rotating gradient ring around it. Videos in the gallery play when clicked.

---

### Image Gallery

**What It Does:** Provides a masonry (Pinterest-style) gallery for viewing batch photos.

**How To Access It:** Click "Images" in the navbar, or the "Images" button on the homepage, or "Images" in the footer.

**How To Use It:**
1. Navigate to the Images page
2. Scroll down to browse all photos
3. Hover over any photo to see a slight zoom effect
4. If a photo fails to load, click "Retry"

**Tips:** The masonry layout adjusts automatically for different screen sizes: 3 columns on desktop, 2 on tablet, 1 on mobile. Images load lazily, so they'll appear as you scroll.

---

### Video Gallery

**What It Does:** Provides a column-based gallery for watching batch videos inline.

**How To Access It:** Click "Videos" in the navbar, or the "Videos" button on the homepage, or "Videos" in the footer.

**How To Use It:**
1. Navigate to the Videos page
2. Hover over any video to start playing
3. Click a video to toggle play/pause
4. Click "Retry" if a video fails to load

**Tips:** Videos play with sound. The gallery layout adjusts for different screen sizes.

---

### Scroll Progress Bar

**What It Does:** Shows a thin glowing bar at the very top of the page that fills up as you scroll down.

**How To Access It:** It appears automatically on the homepage once you start scrolling.

**How To Use It:** No action needed — it's a visual indicator of your scroll position.

**Tips:** The bar uses a gold-to-rose gradient and has a subtle glow effect.

---

### Ambience Mode

**What It Does:** A nostalgic visual effect that can be toggled on or off.

**How To Access It:** Scroll to the footer and find the "Ambience" section.

**How To Use It:** Click the "Toggle Ambience" button. When active, it shows "Nostalgia Mode On."

**Tips:** A gentle reminder appears below the button: "Some memories are best felt in silence."

---

### Mobile Navigation

**What It Does:** On smaller screens, the top navigation bar collapses into a hamburger menu.

**How To Access It:** On any mobile device (screen width less than 768px), the navbar links (Home, Images, Videos) become hidden behind a three-line hamburger icon.

**How To Use It:** Tap the hamburger icon to open the menu. Tap any link to navigate. The menu closes automatically after tapping a link.

---

### 404 Error Page

**What It Does:** Shows a themed error page when someone visits a URL that doesn't exist.

**How To Access It:** Navigate to any unrecognized route (e.g., `/xyz`).

**How To Use It:** Click "Return to Memories" to go back to the homepage.

**Tips:** The page has a spring-animated "404" heading and the message: "This memory doesn't exist yet."

---

## Visual Design Guide

### Theme & Colour Palette

The website uses a "Midnight Yearbook" theme with a deep cosmos background and warm accents:

- **Background (#070714)** — Deep navy-black representing the night sky and timelessness
- **Gold (#d4a853)** — Primary accent, represents nostalgia and cherished memories
- **Rose (#e88fa0)** — Secondary accent, represents friendship and warmth
- **Sky (#7eb3e8)** — Tertiary accent, represents dreams and the future
- **Lavender (#b09fe8)** — Used for variety in quotes and highlights
- **Text (#f0ece4)** — Warm off-white, easy on the eyes against the dark background

### Typography

- **Cormorant Garamond** — Used for headings and display text (elegant serif font)
- **DM Sans** — Used for body text and buttons (clean modern sans-serif)
- **Playfair Display** — Used for quotes and accent text (classic italic style)

### Glass-morphism Effect

Cards, buttons, and panels use a glass effect with semi-transparent backgrounds, subtle borders, and backdrop blur — creating a layered premium look.

### Student Avatar System

Each student has an avatar image chosen in this order:
1. **Custom SVG avatars** — Pre-made illustrations stored on the server (38 unique designs, each with a unique colour gradient)
2. **Auto-generated fallback** — If the custom avatar fails to load, the site generates an avatar showing the student's initials on a coloured gradient background based on their ID number

Each avatar is surrounded by a rotating gradient ring with two colours assigned uniquely per student.

### Animations

- **3D Birds (VANTA.BIRDS)** — Five birds fly across the hero section, responding to mouse movement
- **Star Field** — 80 twinkling stars in the hero section with varying sizes and pulse speeds
- **Floating Orbs** — Four large glowing orbs that pulse slowly behind the hero content
- **Scroll-triggered entries** — Content fades and slides up as you scroll down
- **Page transitions** — Pages animate in when navigating between routes
- **Hover effects** — Cards lift, images zoom, buttons glow on hover

---

## Browser & Device Compatibility

### Supported Browsers

- Google Chrome (version 90+ recommended)
- Mozilla Firefox (version 90+ recommended)
- Apple Safari (version 14+ recommended)
- Microsoft Edge (version 90+ recommended)

### Not Supported

- Internet Explorer (any version)
- Very old versions of Chrome, Firefox, Safari, or Edge

### Requirements

- **JavaScript must be enabled** — The site will not load without it
- **Internet connection required** — No offline mode available
- **WebGL support recommended** — Needed for the 3D bird animation (most modern devices support this)

### Mobile Devices

- Works on iOS (Safari, Chrome) and Android (Chrome, Firefox, Samsung Internet)
- Video autoplay on mobile is limited by browser policies — tap or click videos to play them
- The hamburger menu appears on screens narrower than 768px
- Touch/swipe gestures work for the student carousel

### Known Limitations

- The 3D bird animation may not render on very low-end devices
- Some ad blockers may prevent the bird animation from loading
- Videos stream over the internet and may use mobile data — use Wi-Fi if concerned about data usage

---

## Troubleshooting Guide

### Problem: Images won't load

**Possible Causes:**
- Slow internet connection
- Image file was moved or deleted
- Browser caching issue

**Solution:**
1. Wait a few seconds — images load lazily and may appear with a delay
2. Click the "Retry" button if it appears on a failed image
3. Refresh the page and try again
4. Check your internet connection
5. Try a different browser

### Problem: Videos won't play

**Possible Causes:**
- Slow internet connection
- Video file format not supported by your browser
- Video file missing

**Solution:**
1. Hover over the video (on the Videos page) — it should start playing
2. Click the video to toggle play/pause
3. Click "Retry" if a failure message appears
4. Refresh the page and try again
5. Videos play with sound — check your device volume

### Problem: Page shows "This memory doesn't exist yet"

**Possible Causes:**
- You entered an incorrect URL
- You clicked a broken link

**Solution:**
1. Click "Return to Memories" to go to the homepage
2. Use the navbar to navigate to Images or Videos
3. Ensure you're using one of these valid URLs:
   - `https://class-memory.vercel.app/` (Homepage)
   - `https://class-memory.vercel.app/images` (Image Gallery)
   - `https://class-memory.vercel.app/videos` (Video Gallery)
   - `https://class-memory.vercel.app/student/1` through `/student/38` (Student Profiles)

### Problem: Website is not loading

**Possible Causes:**
- The website host (Vercel) may be experiencing downtime
- Your internet connection may be down
- DNS issues

**Solution:**
1. Check your internet connection
2. Try accessing the site in a different browser
3. Try clearing your browser cache
4. Wait a few minutes and try again — Vercel hosting is generally very reliable
5. Check if other websites load correctly

### Problem: Slow performance

**Possible Causes:**
- The 3D bird animation requires graphics processing
- Your device may be low on memory
- Large media files loading

**Solution:**
1. The site is designed to work on most modern devices
2. Close other heavy applications or browser tabs
3. Try on a different device if available
4. The site uses lazy loading for images, which helps performance

### Problem: Mobile experience is different

**Possible Causes:**
- The site is designed to be responsive but has some differences on mobile

**Solution:**
1. On mobile, the navbar collapses to a hamburger menu (three lines icon)
2. The image gallery shows 1 column on small phones
3. The student carousel works with touch/swipe
4. All features are available on mobile, just presented differently

### Problem: 3D bird animation not showing

**Possible Causes:**
- An ad blocker or script blocker is preventing VANTA.js from loading
- Your browser does not support WebGL
- JavaScript is disabled in your browser
- Slow internet causing scripts to time out

**Solution:**
1. Disable ad blockers or script blockers for this website
2. Ensure JavaScript is enabled in your browser settings
3. Try a modern browser like Chrome or Firefox
4. Wait for the page to fully load — scripts may take a moment

### Problem: Page appears blank or white

**Possible Causes:**
- JavaScript is disabled in your browser
- A browser extension is blocking the page
- Browser is too old to support the React framework

**Solution:**
1. Enable JavaScript in your browser settings
2. Temporarily disable browser extensions and refresh
3. Try a different browser
4. Clear your browser cache and try again

### Problem: Fonts look different or missing

**Possible Causes:**
- Google Fonts are blocked by a firewall, network, or extension
- Slow or intermittent internet connection
- Network restrictions (corporate, school, or public Wi-Fi)

**Solution:**
1. The site will fall back to system fonts — content is still readable
2. Try disabling extensions that block external resources
3. Try a different network connection

### Problem: Videos won't play on iPhone or iPad

**Possible Causes:**
- iOS Safari restricts autoplay for videos with sound
- Low Power Mode may limit video playback
- Slow internet connection

**Solution:**
1. Tap the video directly to start playback
2. Disable Low Power Mode in your device's Settings
3. Check your internet connection
4. Try a different browser app (Chrome for iOS)

### Problem: Student carousel is not responding

**Possible Causes:**
- Auto-scroll was paused by a recent interaction
- Temporary JavaScript glitch

**Solution:**
1. Wait 2–3 seconds — auto-scroll resumes after inactivity
2. Use the arrow (◀ ▶) buttons instead of dragging
3. Refresh the page
4. Try scrolling with your keyboard arrow keys when the carousel is in view

### Problem: Broken link or missing content

**Possible Causes:**
- Content may have been moved or removed during updates

**Solution:**
1. Use the main navigation (navbar or footer) to find what you need
2. If you found a specific issue, contact the website creator through the Contact link in the footer

---

## Questions and Answers

### General Questions

**Q: What is this website?**
A: It is a digital yearbook for the 2023–2026 Computer Applications batch. It preserves memories, photos, videos, and personal messages from 38 students.

**Q: What is it used for?**
A: It is used to remember and celebrate the journey of a college batch — their friendships, experiences, and memories from three years together.

**Q: Who is this website for?**
A: It is for batch members, their friends and family, and anyone who wants to explore or reminisce about the 2023–2026 batch.

**Q: Is this website free?**
A: Yes, it is completely free to browse. No payment or registration is required.

**Q: Why should I use this website?**
A: To revisit memories, read classmates' messages, view batch photos and videos, and stay connected with the spirit of your batch.

**Q: Does this website have a mobile app?**
A: No, but the website works well on mobile browsers.

**Q: Can I search for a student by name?**
A: There is no search bar on the website. To find a specific student, scroll through the carousel on the homepage and look at the name on each card, or navigate directly using the student's ID number (e.g., `/student/5`). See the Student Directory section in this guide for a complete name-to-ID mapping.

**Q: Is this website just for this batch, or can I get one for my batch?**
A: Both. This website serves as the yearbook for the 2023–2026 Computer Applications batch, and it also serves as a live demo of what Samuvel can build for other batches. If you want a similar website for your class, use the Contact link in the footer.

**Q: How much does a custom yearbook website cost?**
A: Pricing starts at ₹1000 for the same template customized with your batch data. With modifications (colours, layout, extra features), it ranges from ₹1200–₹2000. Per-student pricing is ₹30 each. Contact Samuvel for details.

**Q: What batches or school levels is this available for?**
A: It's available for 10th standard, 12th standard, and college batches (UG and PG courses).

**Q: Is this a subscription? Do I have to pay monthly?**
A: No. This is a one-time payment with no monthly fees or subscriptions. Once built, the website is yours.

**Q: Can I see what the website looks like before ordering?**
A: Yes — this very website is a live demo. Browse around and see exactly what you'd get for your batch.

**Q: What if my batch has more than 38 students?**
A: The template handles any number of students. Per-student pricing is ₹30 for each additional student beyond the base template.

**Q: Can I change the colours and design of my yearbook?**
A: Yes. The base template uses a dark cosmic theme with gold accents, but modifications can include custom colours, layouts, and additional features at ₹1200–₹2000.

### Navigation Questions

**Q: How do I return to the homepage?**
A: Click the "Memories" logo in the top-left corner of the navbar, or click "Home" in the footer.

**Q: Where can I find the Images page?**
A: Click "Images" in the top navbar, or the "Images" button on the homepage, or "Images" in the footer.

**Q: Where can I find the Videos page?**
A: Click "Videos" in the top navbar, or the "Videos" button on the homepage, or "Videos" in the footer.

**Q: How do I see all students?**
A: Scroll to the student carousel on the homepage, or click "All Students" in the footer.

**Q: Where is the contact information?**
A: Scroll to the footer and click "Contact" under the About section.

**Q: How do I get back to the student carousel after scrolling?**
A: Click "All Students" in the footer, or scroll up to the top and then down to the carousel section.

### Feature Questions

**Q: How do I view a student's profile?**
A: Click any student card in the carousel on the homepage.

**Q: How do I go to the next student?**
A: On any student profile page, click the "Next" button at the bottom.

**Q: How do I go to the previous student?**
A: On any student profile page, click the "Previous" button at the bottom.

**Q: How do I view images?**
A: Navigate to the Images page from the navbar or homepage buttons.

**Q: How do I watch videos?**
A: Navigate to the Videos page. Hover over a video to play it, or click to toggle play/pause.

**Q: How do I scroll through the student carousel?**
A: Drag left or right with your mouse or finger, or use the arrow buttons.

**Q: How do I read friendship quotes?**
A: Scroll down on the homepage past the hero section — the friendship quotes appear automatically.

**Q: How do I use the Ambience toggle?**
A: Scroll to the footer and click "Toggle Ambience" or "Nostalgia Mode On."

**Q: Can I download photos from the gallery?**
A: The website does not have a dedicated download button. On desktop, right-click any image and select "Save image as..." to save it to your device. On mobile, long-press the image and select "Save Image."

**Q: Can I download videos?**
A: The website does not have a download button. On desktop, you may be able to right-click a video and select "Save video as..." to save it. On mobile, this option depends on your browser.

**Q: How do I view a photo in full screen?**
A: The website does not have a dedicated full-screen photo viewer (lightbox). On desktop, right-click an image and select "Open image in new tab" to view it larger. On mobile, tap and hold to open options.

**Q: Can I watch videos in full screen?**
A: Yes. On desktop, right-click the video and select "Enter fullscreen" or use the fullscreen icon in your browser's video controls. On mobile, tap the video and look for the fullscreen icon.

**Q: How do I share a student's profile on social media?**
A: Copy the student's URL from your browser's address bar (e.g., `https://class-memory.vercel.app/student/5`) and paste it into any social media platform, message, or email. When shared, most platforms show a preview with the site title and description.

**Q: How do I share the website with someone?**
A: Copy the main URL (`https://class-memory.vercel.app`) and share it however you like. The link will show a preview titled "Memories That Stay Forever · Class of 2026" when shared on most platforms.

**Q: Can I leave a comment or message on the website?**
A: No. The website is a read-only digital yearbook. There is no comment section, chat feature, or way to submit messages. If you need to reach the creator, use the Contact link in the footer.

**Q: Can I see all 38 students at the same time?**
A: No, the student carousel shows one row at a time. You can scroll through them by dragging or using the arrow buttons. Each card represents one student.

**Q: Who is student number 1?**
A: Student ID 1 is Aarav Krishnamurthy (Roll Number: CS23001). Each student has a unique ID from 1 to 38. See the Student Directory section for the complete list.

**Q: Does the website work without internet?**
A: No. The website requires an active internet connection to load. It does not have an offline mode.

**Q: Does this website use cookies?**
A: No. The website does not set any cookies, track user activity, or collect personal information from visitors. It is a fully static site with no backend.

**Q: What should I do if a student's information is incorrect?**
A: Contact Samuvel through the Contact link in the footer to request updates or corrections to any student's profile information.

**Q: How were the student avatars created?**
A: Most students have custom SVG avatar illustrations with unique colour gradient combinations. If an avatar image fails to load, the website automatically generates a fallback avatar showing the student's initials on a coloured background.

**Q: Why is the website theme dark?**
A: The dark cosmic theme (deep navy-black background with gold and rose accents) was designed to create a nostalgic, emotional, and premium feel — like looking at memories against a night sky. It is intentional and not changeable by visitors.

**Q: How do I request a similar website for my batch?**
A: Scroll to the footer of any page, click "Contact" under the About section, and reach out through Samuvel's portfolio. Pricing starts at ₹1000 for the same template.

**Q: Can I navigate using my keyboard?**
A: Basic keyboard navigation works. Use the Tab key to move between links and buttons, and press Enter to activate them. The carousel can be scrolled with arrow keys when in view. Videos can be controlled with the spacebar (play/pause) when focused.

### Mobile Questions

**Q: Does this website work on mobile?**
A: Yes, the website is fully responsive and works on phones and tablets.

**Q: How do I open the menu on mobile?**
A: Tap the hamburger icon (three horizontal lines) in the top-right corner of the navbar.

**Q: How do I scroll through the student carousel on mobile?**
A: Swipe left or right with your finger on the carousel.

**Q: Can I use this on a tablet?**
A: Yes, the website is designed to work on tablets as well.

### Troubleshooting Questions

**Q: Why can't I see images?**
A: Images load lazily — scroll down and wait for them to appear. If an image fails, click "Retry." Check your internet connection.

**Q: Why won't videos play?**
A: Hover over a video to play it (on the Videos page) or click to toggle. Check your device volume and internet connection.

**Q: Why am I seeing "This memory doesn't exist yet"?**
A: You've reached a page that doesn't exist. Click "Return to Memories" to go back to the homepage.

**Q: Why is the website slow?**
A: The 3D bird animation can be demanding on some devices. Try closing other applications or tabs.

**Q: Why isn't the carousel moving?**
A: The auto-scroll pauses when you interact with it. It should resume after a couple of seconds of inactivity.

**Q: Why can't I find a specific student?**
A: There are 38 students with IDs 1 through 38. Navigate to `/student/1` through `/student/38` to browse them all. Use the Student Directory section in this guide for a complete name-to-ID mapping.

**Q: Why is the 3D bird animation not showing?**
A: The bird animation may be blocked by an ad blocker, your browser may not support WebGL, or JavaScript may be disabled. Try disabling ad blockers for this site, ensuring JavaScript is enabled, or switching to a modern browser.

**Q: Why is the page blank or white?**
A: This website requires JavaScript to display content. Enable JavaScript in your browser settings, disable script-blocking extensions, or try a different browser.

**Q: Why don't videos play on my iPhone or iPad?**
A: iOS restricts video autoplay for videos with sound. Tap the video directly to start playback. If still not working, check that Low Power Mode is off and try a different browser.

**Q: Why does the website look different on my phone?**
A: The website is responsive — it adapts to smaller screens. On mobile, the navbar collapses to a hamburger menu, the image gallery switches to fewer columns, and the carousel supports swipe gestures. All content is still accessible.

**Q: Why is the carousel not scrolling automatically?**
A: Auto-scroll pauses when you interact with the carousel (dragging, hovering, clicking). It should resume after 1.5–2 seconds of inactivity. You can also use the arrow buttons to scroll manually.

**Q: Why do fonts look different or wrong?**
A: Custom fonts (Cormorant Garamond, DM Sans, Playfair Display) load from Google Fonts. If they don't load due to network or firewall restrictions, the site falls back to standard system fonts. Content remains readable.

**Q: Will this website work with JavaScript turned off?**
A: No. This website is built with React and requires JavaScript to render any content. Without JavaScript, you will see a blank page.

### Contact Questions

**Q: How do I contact the website creator?**
A: Scroll to the footer of any page and click "Contact" under the About section. This opens Samuvel's portfolio website.

**Q: How do I report a problem?**
A: Use the Contact link in the footer to reach Samuvel through his portfolio website.

**Q: Can I request changes to the website?**
A: Use the Contact link in the footer. The "What We Collect" modal (click in the footer) mentions that similar websites can be created for other batches.

**Q: Who made this website?**
A: The website was created by Samuvel, as indicated by the Contact link in the footer pointing to his portfolio.

---

## Quick Answers

**Q: What is this website?**
A: A digital yearbook for the 2023–2026 Computer Applications batch, preserving memories, photos, videos, and messages.

**Q: Is it free?**
A: Yes, completely free to browse — no registration or payment needed.

**Q: How do I view students?**
A: Scroll down on the homepage and click any student card in the carousel.

**Q: How do I view images?**
A: Click "Images" in the navbar or on the homepage.

**Q: How do I watch videos?**
A: Click "Videos" in the navbar or on the homepage. Hover to play, click to toggle.

**Q: How do I return to the homepage?**
A: Click the "Memories" logo in the top-left corner.

**Q: Where are my settings?**
A: This website does not have user accounts or settings — it is a read-only yearbook.

**Q: How do I create an account?**
A: This website does not have user accounts or registration. It is a static digital yearbook — anyone can browse freely.

**Q: How do I log in?**
A: This website does not have a login system. No account is needed to browse.

**Q: How do I reset my password?**
A: This website does not have passwords or user accounts.

**Q: How do I upload a photo?**
A: This website does not support user uploads. Media is pre-loaded by the website creator.

**Q: How do I edit my profile?**
A: This website does not have editable profiles. Student information is pre-loaded.

**Q: How do I share a student's profile?**
A: Copy the URL from your browser's address bar. Each student has a unique URL: `/student/1`, `/student/2`, etc.

**Q: How do I share an image?**
A: Navigate to the Images page and copy the URL from your browser's address bar.

**Q: How do I share a video?**
A: Navigate to the Videos page and copy the URL from your browser's address bar.

**Q: How do I contact support?**
A: Scroll to the footer and click "Contact" under the About section.

**Q: How many students are in this batch?**
A: 38 students.

**Q: What years does this cover?**
A: 2023 to 2026.

**Q: What department?**
A: Computer Applications.

**Q: Does this work on mobile?**
A: Yes, the website is fully responsive and works on phones and tablets.

**Q: Can I get a yearbook like this for my batch?**
A: Yes — contact Samuvel through the footer. Pricing starts at ₹1000.

**Q: How do I find a student by name?**
A: Use the Student Directory table in this guide, or browse the carousel on the homepage.

**Q: Can I download images or videos?**
A: Right-click (desktop) or long-press (mobile) and select "Save" options from your browser.

**Q: Why is the 3D animation missing?**
A: Disable ad blockers for this site, enable JavaScript, or switch to Chrome/Firefox.

**Q: Does this site use cookies?**
A: No cookies, no tracking, no data collection.

**Q: Is there a search bar?**
A: No. Browse the student carousel or use direct URLs (`/student/1` through `/student/38`).

**Q: Can I comment or leave a message?**
A: No. The site is read-only. Contact the creator via the footer for any requests.

**Q: What browsers are supported?**
A: Chrome, Firefox, Safari, and Edge (modern versions). Internet Explorer is not supported.

---

## Contact Information

The website was created by **Samuvel** as both a digital yearbook for the 2023–2026 batch and a live portfolio showcase.

**How to reach out:**
- Scroll to the footer of any page
- Click "Contact" under the About section
- This opens Samuvel's portfolio website where you can get in touch

**How to request your own digital yearbook:**
1. Visit this website and scroll to the footer
2. Click "Contact" under the About section
3. Reach out through Samuvel's portfolio with your batch details

**Pricing summary for custom yearbooks:**
| Option | Price |
|--------|-------|
| Same template (customized with your data) | **₹1000** |
| With modifications (custom colours, layout) | **₹1200 – ₹2000** |
| Per student pricing | **₹30 per student** |
| Available batches | 10th, 12th, and college (UG/PG) |

This is a one-time payment — no monthly fees or subscriptions. Contact Samuvel for a quote tailored to your batch size and requirements.

---

## Data & Privacy

### What Information Is Displayed

**From Students:**
- Profile photos (avatar images)
- Names and student IDs
- Personal memories, quotes, and messages written by each student
- Best moments and taglines

**What Is Not Collected:**
- No email addresses
- No phone numbers
- No physical addresses
- No payment information
- No browsing data is tracked
- No cookies are used for tracking

### How Information Is Managed

All data is pre-loaded into the website by the creator. There is no user registration, no login system, and no way for visitors to submit or modify data through the website. The website is a static showcase — no data is collected from visitors.

### Content Updates

If a student wishes to update or remove their information, they should contact Samuvel through the Contact link in the footer.

---

## Website Summary

### One Sentence Description

A digital yearbook for the 2023–2026 Computer Applications batch that preserves student profiles, photos, videos, and memories in an interactive, visually rich format.

### Short Summary

Memories That Stay Forever is a premium digital yearbook built for the 2023–2026 Computer Applications batch. It features 38 student profiles with personal memories, quotes, and messages, along with an image gallery, video gallery, and an emotionally themed design. The website uses 3D bird animations, a star field, and a dark cosmic theme to create a nostalgic atmosphere. It is fully responsive and works on all devices. No registration, login, or backend is required — it's a static website anyone can browse freely.

### Detailed Summary

Memories That Stay Forever is a digital yearbook designed to preserve the memories of the 2023–2026 Computer Applications batch. The website welcomes visitors with a stunning animated hero section featuring 3D birds that fly across a starry cosmic background, setting a nostalgic and emotional tone.

Below the hero section, visitors find a friendship quotes area with four hand-crafted reflections on the batch's journey, followed by a year-by-year timeline from 2023 to 2026. The student carousel displays all 38 batch members in horizontally scrollable cards, each showing an avatar (with a coloured gradient ring), the student's name, and a personal tagline. Clicking any card opens a detailed profile page.

Each student profile includes a personal memory, a favourite quote, their best moment from the three years, and a message addressed to the class. Profiles also show a media gallery combining batch photos and videos. Navigation between students is easy with Previous/Next buttons at the bottom of each profile.

The Images page presents batch photos in a masonry (Pinterest-style) layout with hover zoom effects and lazy loading. The Videos page shows batch videos in a column-based layout where videos play on hover and can be toggled with a click.

The website includes a scroll progress bar, mobile-responsive navigation with a hamburger menu, and a themed 404 error page. The footer provides access to all pages, a "What We Collect" information modal, a Contact link to the creator Samuvel, and an Ambience toggle for a nostalgic visual effect.

The website is built purely on the frontend with no backend, no authentication, and no user accounts. All data is pre-loaded, making it a fast, secure, and private experience for everyone who visits.

### Key Features List

- 3D bird animated hero background
- 38 student profiles with personal memories
- Horizontally scrollable student carousel
- Masonry image gallery with lazy loading
- Inline video gallery with hover-to-play
- Combined media gallery on profiles
- Emotional friendship quotes section
- Year-by-year batch timeline (2023–2026)
- Scroll progress indicator
- Mobile-responsive design
- Ambience toggle
- Themed 404 error page
- Glass-morphism UI design
- Dark cosmic theme with gold accents

### Target Audience Summary

This website is primarily for the 38 students of the 2023–2026 Computer Applications batch and their families and friends. It is also useful for anyone looking to create a similar digital yearbook for their own batch (the creator offers this as a service). General visitors who appreciate creatively designed memory websites are also welcome.

---

*This knowledge base was generated for SCOUT AI to assist users of the Memories That Stay Forever website. Last updated: May 2026.*
