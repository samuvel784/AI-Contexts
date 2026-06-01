# Special Wishes

## Website Overview

**Website:** [special-wishes-kohl.vercel.app](https://special-wishes-kohl.vercel.app)
**Tagline:** Express emotions through music, animation & storytelling
**Developer:** Samuvel (solo developer)

Special Wishes is a digital greeting card platform that lets users create interactive, animated greeting pages for birthdays, anniversaries, Valentine's Day, and many other occasions. Each greeting is a complete multimedia experience with 3D envelope animations, image slideshows, background music, animated letter cards, and sharing features.

---

## Purpose

The platform solves the problem of generic, impersonal digital greetings. Instead of sending a plain text message or a static e-card, users can create a full interactive experience for their loved ones — complete with animations, music, photos, and heartfelt messages — all delivered through a shareable link.

---

## Who Is This For?

- Anyone who wants to send a personalized, memorable greeting
- People celebrating birthdays, anniversaries, holidays, and special occasions
- Users who want to add music, images, and animations to their messages
- Those looking for a creative way to express feelings to loved ones

---

## Main Features

| Feature | Purpose | User Benefit | Location |
|---------|---------|--------------|----------|
| **Greeting Creation Wizard** | Multi-step form to create animated greeting cards | Easy, guided process with all customization options | Homepage → Select occasion |
| **24 Occasion Types** | Pre-designed themes for different celebrations | Always find the right theme for any event | Homepage & /more page |
| **3D Envelope Animation** | Interactive envelope with wax seal and particle effects | Stunning visual reveal experience | Greeting view (/g/:code) |
| **Image Slideshow** | Ken Burns effect slideshow with swipe navigation | Display multiple photos beautifully | Greeting view |
| **Background Music** | Upload or select music that plays during greeting | Adds emotional depth to the experience | Greeting creation & view |
| **Animated Letter Cards** | Up to 5 message boxes with slide animations | Multiple heartfelt messages displayed elegantly | Greeting view |
| **Final Message Card** | 3D rotating card with word-by-word reveal | Special final message on card back | Greeting view |
| **Password Protection** | Optional password to view greeting | Privacy control for sensitive messages | Greeting creation |
| **Expiry Date** | Date when greeting is permanently deleted | Automatic deletion for privacy — greeting and all files gone forever with no recovery | Greeting creation |
| **Auto-Save Drafts** | Saves progress every 3 seconds to localStorage | Never lose your work (24-hour restore window) | Greeting creation |
| **Token System** | Purchase tokens to create/edit greetings | Pay-as-you-go model, tokens never expire | Premium page |
| **Dashboard** | View, search, filter, edit, delete all greetings | Full management of your creations | /dashboard |
| **QR Code Sharing** | Generate downloadable QR code for any greeting | Easy physical or digital sharing | Share modal |
| **Swipe-to-Copy Link** | Interactive slider to copy greeting link | Quick link sharing | Share modal |
| **Social Sharing** | Share via WhatsApp, Facebook, Twitter, Telegram, Email | Multiple sharing options | Share modal & success screen |
| **HeartStorm Game** | Interactive heart-fill physics game | Fun interactive element before thank you page | /heartstorm (from FinalMessageCard) |
| **Countdown Animation** | Cinematic 3-2-1 countdown before reveal | Builds anticipation | Greeting view |
| **Celebration Effects** | Confetti, emoji particles, and 3D celebration card | Festive ending to the greeting experience | Greeting view |
| **Music Player** | Play/pause/mute controls for background music | User control over audio | Greeting view |
| **Multi-Language Support** | English, Hindi, Tamil | Accessible to more users | Site-wide |
| **View Tracking** | Each greeting tracks number of views | Know when your greeting has been seen | Dashboard |
| **Sound Effects** | Synthesized audio via Web Audio API (envelope crack, celebration chord) | Immersive audio feedback without external files | Greeting view |
| **Pre-Made Music Tracks** | 5 Pixabay-licensed tracks ready to use | No need to upload music — pick a track | Greeting creation |
| **Animated Backgrounds** | 5 types (nebula, party, moon, nature, snow) plus starfield and cinematic | Immersive visual atmosphere for every occasion | Site-wide |
| **Error Boundary** | Catches and displays React errors with "Try Again" button | Prevents blank pages on unexpected errors | Site-wide |
| **Heart Loader** | Full-screen heart-themed loading overlay with floating hearts | Pleasant loading experience during data fetches | Site-wide |

---

## Complete Occasion Reference

| Occasion | Icon | Description |
|----------|------|-------------|
| Birthday | 🎂 | Celebrate their day |
| Valentine's Day | 💝 | Express your love |
| Anniversary | 💍 | Celebrate togetherness |
| New Year | 🎆 | Celebrate new beginnings |
| Christmas | 🎄 | Celebrate the festive season |
| Diwali | 🪔 | Festival of lights |
| Mother's Day | 🌸 | Honor your mother |
| Father's Day | 👔 | Appreciate your father |
| Wedding | 💒 | Congratulations to the couple |
| Friendship Day | 🤝 | Celebrate friendship |
| Graduation Day | 🎓 | Celebrate achievement |
| Teacher's Day | 📚 | Thank your teachers |
| Thanksgiving | 🦃 | Give thanks |
| Baby Shower | 🍼 | Celebrate upcoming arrival |
| Retirement | 🏖️ | New chapter begins |
| Easter | 🥚 | Spring celebration |
| Halloween | 🎃 | Spooky celebrations |
| Pregnancy | 👶 | Welcome new life |
| Brother's Day | 👦 | Celebrate brotherhood |
| Sister's Day | 👧 | Cherish sisterhood |
| Good Luck | 🍀 | Best wishes for success |
| Welcome Baby | 🐣 | Welcome new bundle of joy |
| Get Well Soon | 💊 | Wishing you recovery |
| General Wishes | ✨ | Any special occasion |

---

## Website Structure

### Public Pages (No Login Required)

| Page | Route | Description |
|------|-------|-------------|
| **Homepage** | `/` | Hero section, occasion grid (15 main occasions), features section, footer |
| **All Occasions** | `/more` | Full list of all 24 occasions |
| **About** | `/about` | Developer info, platform vision, technology approach, future plans |
| **Contact** | `/contact` | Support info, what to contact about, portfolio link |
| **Terms & Conditions** | `/terms` | Terms of service (14 sections) |
| **Privacy Policy** | `/privacy` | Privacy policy (14 sections) |
| **Information** | `/information` | Platform info, Google sign-in info, refund policy, cookie policy, DMCA |
| **Sign Up / Login** | `/google-auth` | Google OAuth sign-in with terms agreement |
| **View Greeting** | `/g/:shortCode` | Interactive greeting viewing experience (7 stages) |
| **View Greeting (Legacy)** | `/view/:id` | Older greeting viewer (reads from localStorage) |
| **Thank You Page** | `/thankyou/:shortCode` | Thank you screen after HeartStorm game |
| **404 Not Found** | `*` | Catch-all for unknown routes |

### Authenticated Pages (Login Required)

| Page | Route | Description |
|------|-------|-------------|
| **Dashboard** | `/dashboard` | Greeting management, stats, search, filter, sort, bulk delete |
| **Edit Greeting** | `/dashboard/edit/:id` | Edit an existing greeting (costs 100 tokens) |
| **Premium / Buy Tokens** | `/premium` | Token purchase plans (4 tiers) |
| **Premium Success** | `/premium-success` | Payment verification result |
| **Profile** | `/profile` | User profile, token balance, logout |
| **HeartStorm Game** | `/heartstorm` | Interactive heart-fill physics game (reached from FinalMessageCard) |

---

## Complete User Journeys

### Journey 1 — First Visit / Landing

**Step 1 — Arrive at Homepage**

**What the user sees:** A gradient background with floating decorative emojis (💌, ✨, 💖, 🎁), a glass-morphism navbar with the heart logo and "Special Wishes" brand, a hero section with an envelope icon, animated title ("Special Wishes"), subtitle about music/animation/storytelling, and a grid of occasion cards.

**What the user does:** Scrolls down to browse the occasion cards.

**What happens:** Each card shows an icon, occasion name, and short description. Hovering shows a shine effect (scale 1.05, icon rotates 12deg). A "More" button shows "+9 occasions" for additional options.

**Scrolling further:** Below the occasion grid, a "Create Magical Moments" features section shows 4 cards:
- **3D Envelope** — "Interactive envelope with stunning open animation"
- **Background Music** — "Auto-plays with smooth fade effects"
- **Ken Burns Slideshow** — "Cinematic photo transitions with zoom"
- **Animated Letters** — "Messages that slide and glow beautifully"

**If not logged in and clicking an occasion:** An auth popup appears: "Sign Up Required" with "Please sign up to create greetings." and buttons "Sign Up with Google" / "Cancel".

**If logged in and clicking an occasion:** The CreateGreetingForm opens with the selected occasion pre-filled.

**URL Parameter:** Visiting `/?occasion=<occasionId>` (e.g., `/?occasion=birthday`) auto-selects that occasion and clears the URL parameter via replace navigation. Invalid occasion IDs are silently ignored.

---

### Journey 2 — Sign Up / Login

**Step 1 — Click Sign Up**

**What the user sees:** The "Sign Up" button in the navbar (gradient pink/red button).

**What the user does:** Clicks the Sign Up button.

**What happens:** Navigates to `/google-auth`.

**Step 2 — Google Authentication Page**

**What the user sees:** A starry animated background, a glass card with the heart logo, title "Join Special Wishes", description about creating meaningful greetings, a "Continue with Google" button (disabled initially), and a checkbox to agree to Terms & Conditions and Privacy Policy.

**What the user does:** 
1. Checks the "I agree" checkbox
2. Clicks "Continue with Google"

**What happens:** Redirected to Google's OAuth consent screen.

**Step 3 — Google Consent (or Already Authenticated)**

**What the user does:** Selects a Google account and clicks "Continue" to grant basic profile access (name, email, profile picture). If already authenticated, the user is auto-redirected to `/` without showing the consent screen.

**What happens:** Redirected back to the homepage, now logged in. The navbar shows the user's token balance, profile avatar, and a dropdown menu with Dashboard, Buy Tokens, and Logout options.

---

### Journey 3 — Create a Greeting

**Step 1 — Select Occasion**

**What the user sees:** The occasion grid on the homepage showing 15 cards.

**What the user does:** Clicks on an occasion card (e.g., "Birthday Wishes").

**What happens:** The CreateGreetingForm opens with the selected occasion's icon and name in the header.

**Step 2 — Fill in Details**

**What the user sees:** A multi-section form with glass-morphism cards containing:
- Greeting Title (pre-filled with "Happy [Occasion]!")
- Your Name (required) and Recipient Name (required)
- Messages section with one textarea (max 5 messages, 500 chars each)
- Image upload section (max 5 images, 3MB each)
- Music upload section (1 file, max 10MB, MP3/WAV/OGG)
- Expiry Date picker (required, can't be in the past). Warning: On this date the greeting and all its content are automatically and permanently deleted from the system.
- Password Protection (optional)

**What the user does:** 
1. Edits the title if desired
2. Enters sender and recipient names
3. Writes messages (can add more with "Add" button, up to 5)
4. Uploads images (click "Add Photo", select from computer)
5. Optionally uploads a music file
6. Selects an expiry date from the calendar popup
7. Optionally sets a password

**What happens:** Form auto-saves draft to localStorage every 3 seconds.

**Step 3 — Submit / Create**

**What the user sees:** A large gradient "Generate Shareable Link" button at the bottom.

**What the user does:** Clicks "Generate Shareable Link".

**What happens (token check):** The system checks if the user has at least 100 tokens. If not, a token warning modal appears with an "Upgrade to Premium" button.

**What happens (success):** If tokens are sufficient, 100 tokens are deducted, images and music are uploaded to cloud storage, a unique 6-character short code is generated (with up to 10 retry attempts if collisions occur), and the greeting is saved to the database.

**Step 4 — Share the Link**

**What the user sees:** A success screen with a green checkmark, title "Your Greeting is Ready!", the shareable link displayed in a read-only input, a "Copy Link" button, social share buttons (native share, Email, WhatsApp, Telegram), a "Create Another" button, a "Preview" button, and a warning: "This link cannot be recovered if lost".

**What the user does:** Clicks "Copy Link" or one of the social share buttons.

**What happens:** The link is copied to clipboard, or the share dialog opens. The user can now send the link to their recipient.

---

### Journey 4 — View a Greeting (7-Stage Experience)

**Stage 1 — 3D Envelope (6-Phase Animation)**

**What the user sees:** A dark background with twinkling stars (via StarryBackground), a premium 3D deep crimson velvet envelope with gold wax seal, decorative gold trim, and a "👆 Tap to open" prompt below with bobbing animation. Three expanding ring borders pulse around the envelope. The wax seal glows with periodic gold pulsing.

**What the user does:** Clicks or taps on the envelope.

**What happens — 6-phase animation sequence (total ~3.4s):**
1. **Idle/Hover** — Envelope floats gently. On mouse hover, it scales up slightly (1.03-1.04) with sparkle dots on the seal and text "✦ Click to reveal ✦". (No duration limit — waits for user click.)
2. **Seal Click (350ms)** — Wax seal cracks with SVG stroke animation (3 crack paths drawn), sound effect plays (sawtooth sweep 150→50Hz + sine pop 800→200Hz). Text: "...Breaking the seal..."
3. **Shake (800ms)** — Envelope shakes vigorously in multiple directions with rotations. 40 particles burst out (hearts, stars, dots, rings in 12 jewel colors) with physics (gravity 0.22, drag 0.98). Text: "✨ Opening your surprise..."
4. **Flap Open (1.2s)** — Top flap rotates open in 3D (rotateX 0→-190deg), 16 light rays burst radially from center, shimmer sweep across the body. Text: "Revealing your message..."
5. **Letter Rise (2s)** — The letter card rises from inside with spring-like cubic bezier animation as the envelope sinks and scales down (0.95). Text: "💌 Your special message awaits..."
6. **Transition** — After letter fully rises, transitions to the next stage.

**Particle System:** Each burst creates 40 particles with types (heart, star, dot, ring), 12 jewel colors, random velocities, gravity, and drag. Rendered via requestAnimationFrame with proper RAF cancellation on unmount.

**Stage 2 — Password Gate (if password was set)**

**What the user sees:** A dark starry background with a lock icon, title "Protected Message", a password input field, a "Unlock Message" button, and a hint section.

**What the user does:** Enters the password and clicks "Unlock Message".

**What happens:** If correct, proceeds to Music Gate. If wrong, shows "Incorrect password" error and tracks attempts. An attempt counter appears after the first failure. The input shakes on error and clears on retry. An eye toggle shows/hides the password. A hint section reads: "The password was shared with you when this greeting was created."

**Stage 3 — Music Gate**

**What the user sees:** Starry background, 20 animated waveform bars dancing with staggered delays (0.08s each), title "A Special Message for [Recipient Name]" with sender name below, a "Play with Music" button and a "Skip Music" button.

**What the user does:** Clicks "Play with Music" or "Skip Music".

**What happens:** If "Play with Music" is clicked, music starts with a fade-in effect (shows "Starting Music..." loading text). After 900ms, proceeds to Countdown with 0.8s entrance fade-up animation. If "Skip Music" is clicked (or if no music URL was provided, a single "View Greeting" button appears instead of two), proceeds after 700ms with 700ms fade-out exit.

**Stage 4 — Countdown**

**What the user sees:** A cinematic background with a large glowing number (3, 2, 1) that starts at scale-0 rotate-180 and animates to scale-100 rotate-0. An outer ping ring animates around each number. Text below: "Get ready..."

**What happens:** Numbers count down from 3 to 1 (1 second each). Each number shows for 1s then exits with scale-up + fade-out (400ms). At zero, a glowing ring pulses for 800ms, text changes to "Here we go!", then after 600ms exits. Total duration: ~3.8 seconds. After countdown, transitions to Slideshow (if images exist) or directly to Letters.

**Stage 5 — Image Slideshow (if images uploaded)**

**What the user sees:** Full-screen images displayed one at a time with Ken Burns zoom/pan effect, navigation arrows, progress dots with aria-labels, image counter badge "{n} / {total}", and progress bar. Each image shows a "Loading image..." placeholder until loaded; failed images show an error placeholder.

**What the user does:** Can click arrows, press Left/Right arrow keys, or swipe (30px threshold) to navigate between images. Each image auto-advances after 6000ms.

**What happens:** Adjacent images are preloaded for smoother transitions. Aspect ratio detection: portrait images get narrower containers, landscape/square get wide. After the last image, transitions to the Letter stage.

**Stage 6 — Romantic Letter Cards**

**What the user sees:** A vintage paper-styled letter with gold SVG ornament corners (4 positions), top/bottom flourishes with diamonds, and animated message text appearing at 20 chars/second with a blinking cursor. A "✨ Tap to see full message ✨" prompt appears during animation. Title is shown only on first card. Card counter "Message {n} of {total}" at the top. Each message appears one at a time with slide-up animation. Navigation arrows at the bottom to move between messages. The signature "Forever by your side, {senderName}" appears on the last card.

**What the user does:** Clicks right arrow to advance to the next message.

**What happens:** After all messages are viewed, a "Continue" or "Reveal" button appears. Clicking it transitions to the Final Card.

**Stage 7 — Final Message Card**

**What the user sees:** A 3D rotating card (Celebration3D) with gold accents, floating occasion-specific emojis orbiting the card, and 20 floating background particles. The front face shows the greeting title, "With love from {senderName}", "To: {recipientName} 💖", and the occasion icon. The card auto-rotates slowly (0.3deg per 50ms) with drag sensitivity 0.5, X clamped to ±30deg. CelebrationEffect overlays with 30-40 occasion-specific emoji particles dropping from the top (new particle every 300ms, max 40 kept) with 4 corner gradient glows. Default message if none provided: "In all the world there no heart for me like yours..."

**Background types (randomly selected from 5):** Nebula (deep space), Party (disco lights), Moon (night sky), Nature (sun/hills), Snow (winter)

**3D Floating Elements (6 emojis per occasion):**
- Birthday: 🎂 🎈 🎁 🎉 🎊 ✨
- Anniversary: 💍 💖 🌹 💕 💑 ✨
- Valentine: 💘 💝 💖 🌹 💕 ❤️
- Wedding: 💒 👰 🤵 💍 🌸 💖
- Graduation: 🎓 📚 🏆 ⭐ 🎊 ✨
- Baby: 👶 🍼 🧸 💕 🌟 ✨
- Mother's Day: 💐 🌷 💖 👩‍👧 🌸 💕
- Father's Day: 👔 🏆 💙 👨‍👧 ⭐ 💖
- Plus default: 💖 ✨ 🌟 💫 🎉 🌸

**What the user does:**
- Drag the card to rotate it in 3D space (0.5 sensitivity, X clamped to ±30deg)
- Auto-rotation pauses while dragging and resumes when released
- Card flips to show back face when rotated past 90-270deg Y rotation
- The back face reveals a word-by-word message (5 words per second, 200ms interval, color transition to purple)
- After all words are revealed, a "Next ✨" button appears with pulsing golden glow animation

**What the user can do next:**
- **Click "Replay"** — Restarts the entire greeting experience from the Envelope stage (calls onReplay, restarts from envelope)
- **Click "Next ✨"** — Navigates to the HeartStorm game page (`/heartstorm?code=xxx`) for an interactive celebration

---

### Journey 5 — Dashboard Management

**Step 1 — Access Dashboard**

**What the user does:** Clicks their profile avatar in the navbar and selects "Dashboard" from the dropdown menu.

**What happens:** Navigates to `/dashboard`.

**Step 2 — View Dashboard**

**What the user sees:** A sidebar with "Special Wishes" brand, "My Wishes" and "Buy Tokens" navigation. The main content area shows: 4 stats cards (Total Wishes, Active, Expired, Total Views), a search bar, filter buttons (All/Active/Expired), a sort dropdown (Newest/Oldest), a "Select" button for bulk mode, and a list of greeting cards showing occasion icon, title, recipient name, creation date, expiry status, view count, and action buttons.

**Step 3 — Manage Greetings**

**What the user does:** Can perform any of these actions on each greeting:
- Click the share icon to open the QR Code share modal
- Click the copy icon to copy the link
- Click the preview icon to open the greeting in a new tab
- Click the edit icon (only for active greetings) to edit (costs 100 tokens)
- Click the more menu (⋮) for Edit (100 tokens) and Delete options

**Step 4 — Edit a Greeting**

**What the user does:** Clicks the edit icon or "Edit (100 tokens)" from the menu.

**What happens:** A confirmation dialog shows the current token balance, the 100-token cost, and the balance after editing. If the user has enough tokens and confirms, tokens are deducted and the user is redirected to the edit form.

**Step 5 — Delete a Greeting**

**What the user does:** Clicks "Delete" from the menu or selects multiple greetings in bulk mode and clicks the floating "Delete" button.

**What happens:** A confirmation dialog asks "Are you sure?" with the greeting title. Confirming permanently deletes the greeting.

---

### Journey 6 — Purchase Tokens

**Step 1 — Go to Premium Page**

**What the user does:** Clicks "Buy Tokens" from the profile dropdown, "Buy Tokens" in the dashboard sidebar, or "Premium Plan" in the footer.

**What happens:** Navigates to `/premium`.

**Step 2 — Choose a Plan**

**What the user sees:** A dark theme page with starfield background (90 twinkling stars, DM Serif Display font for headings), 4 plan cards in a grid with individual accent colors (red, purple, gold, sky blue):
- **Starter Plan** — ₹5 / 100 tokens (1 greeting)
- **Pro Plan** — ₹20 / 420 tokens (4 greetings) — marked "MOST POPULAR" with a bounce-in animation badge
- **Premium Plan** — ₹100 / 2200 tokens (22 greetings)
- **Elite Plan** — ₹200 / 4500 tokens (45 greetings)

Each card shows: "TOKEN-BASED SYSTEM" corner badge, plan name with gradient title, price, token count pill, 7 feature checklist items, "Buy Now" button, and a footer reading "Secure payment via Cashfree".

**What the user does:** Clicks "Buy Now" on a plan.

**Step 3 — Complete Payment**

**What happens:** The Cashfree payment system loads. A secure payment popup appears where the user can complete the payment using their preferred method (UPI, card, net banking, etc.).

**Step 4 — Verify Payment**

**What happens:** After payment, the user is redirected to `/premium-success`. The page shows a verifying state, then either a success message ("Payment Successful! Your tokens have been added.") with auto-redirect to homepage after 3 seconds, or an error message.

---

### Journey 7 — Share a Greeting from Dashboard

**Step 1 — Open Share Modal**

**What the user sees:** A dialog/modal with:
- A QR code (with heart logo in center, responsive size: min(180px, max(120px, windowWidth-160)))
- "Download QR Code" button (saves as `special-wish-{title}.png`)
- A "Swipe right to copy link" interactive slider
- Social share buttons: Native Share, WhatsApp, Facebook, Twitter, Telegram

**What the user does:** Can perform any action:
- Swipe the slider to copy the link
- Click "Download QR Code" to save a PNG image
- Click WhatsApp/Facebook/Twitter to share on social media
- Click the native Share button for device sharing options

---

### Journey 8 — Logout

**Step 1 — Open Profile Menu**

**What the user does:** Clicks their profile avatar in the navbar.

**What happens:** A dropdown menu appears with the user's name, email, and options: Dashboard, Buy Tokens, and Logout.

**Step 2 — Click Logout**

**What the user does:** Clicks "Logout" (🚪 icon).

**What happens:** The user is signed out and returned to the homepage. The navbar now shows the "Sign Up" button.

---

## Feature Documentation

### Greeting Creation Form

**What It Does:** A multi-step guided form for creating interactive greeting cards with images, music, messages, and privacy settings.

**How To Access It:** Click any occasion card on the homepage, or use URL `/?occasion=<occasionId>`.

**Fields:**
- **Greeting Title** — Auto-generated based on occasion ("Happy [Occasion]!"), editable
- **Your Name** (required) — Sender's name displayed in the greeting
- **Recipient Name** (required) — Recipient's name displayed in the greeting
- **Messages** (required, max 5) — Each message up to 500 characters, numbered, with character counter (turns amber at 450 chars, red at 500). Add button (+) available until 5 messages. Delete button on each message when >1
- **Images** (required, max 5) — JPG/PNG/etc, max 3MB each. Upload via "Add Photo" button (clicking resets the file input). Preview thumbnails with hover-to-remove (X button on desktop, tap on mobile). Shown in Ken Burns slideshow during viewing
- **Background Music** (optional, 1 file) — MP3/WAV/OGG, max 10MB. Shows file name and size after selection with remove option. Auto-plays with fade-in during viewing
- **Expiry Date** (required) — Calendar popover (react-day-picker), past dates disabled, cannot be selected. WARNING: On this date the greeting is permanently deleted — all images, music, and messages are erased. No recovery is possible. This is enforced for privacy.
- **Password Protection** (optional) — Password input field, limits access to those who know the password

**Cost:** 100 tokens per greeting creation. 100 tokens per edit.

**Form Animations:** Each section fades up with staggered 100-400ms delays. Image upload area has hover border highlight. Submit button has shadow-xl glow.

**Form Layout:** The submit button and token info are within a `<footer>` element inside the form, visually separated by a top border.

**Submit Process:**
1. Click "Generate Shareable Link" button (shows "Creating Magic..." with spinner while submitting)
2. System checks for 100 tokens — if insufficient, a token warning modal appears with "Unlock Premium Features" heading, "🎁 Get 100 tokens to create your first greeting!" message, and "Upgrade to Premium" / "Maybe Later" buttons
3. If sufficient, 100 tokens are deducted, images/music uploaded to Supabase storage, a unique 6-character short code generated (with up to 10 attempts), and greeting saved to DB

**Success Screen:**
- Green checkmark, "Your Greeting is Ready! 🎉"
- Read-only link input with "Copy Link" button (shows "Copied!" briefly)
- Social share buttons: Native Share, Email, WhatsApp, Telegram
- "Create Another" button and "Preview" button
- Expiry info: "Expires on: {formatted date}"
- Warning: "NOTE: This link cannot be recovered if it is lost, so please save it somewhere safe or share it quickly."

**Auto-Save:** Progress saves to localStorage every 3 seconds (debounced). If you close the browser and return within 24 hours, you'll see a "Draft restored" toast notification. Only works for create mode (not edit mode) and when logged in.

**States:**
- **Normal:** All form fields editable
- **Loading (edit mode):** Spinner with "Loading greeting..."
- **Submitting:** Button disabled, spinner + "Creating Magic..." text
- **Success:** Share link screen shown
- **Token Warning Modal:** Insufficient tokens overlay
- **Edit Mode:** Pre-populated form from existing greeting data

**Common Use Cases:**
- Birthday greeting with photos from a party
- Anniversary greeting with couple photos and romantic music
- Valentine's Day greeting with love messages

**Important:** The generated link cannot be recovered if lost. Save or share it immediately.

---

### Greeting Viewing Experience

**What It Does:** A 7-stage interactive experience that guides the recipient through the greeting.

**How To Access It:** Open a greeting link (`/g/abcdef`).

**Stages:**
1. **Envelope** — Interactive 3D envelope. Tap to open. The envelope has a red velvet texture, gold wax seal, and particle burst on opening.
2. **Password** — If the creator set a password, this screen appears. Enter the password to continue.
3. **Music** — Choose to play background music or skip it. Music fades in gradually.
4. **Countdown** — 3-2-1 countdown with cinematic effects.
5. **Slideshow** — Images displayed with Ken Burns zoom/pan effect. Navigate with arrows or swipe.
6. **Letters** — Messages displayed one by one on elegant paper-style cards with gold ornaments. Click arrows to advance.
7. **Final Card** — A 3D rotating card with the final message. Word-by-word reveal animation. Includes a "Replay" button.

**Tips:**
- If you missed something, click "Replay" on the final card to restart
- Music plays in the background throughout the experience
- The greeting can be viewed multiple times until its expiry date, when it is permanently deleted

---

### Dashboard

**What It Does:** Central hub for managing all your created greetings.

**How To Access It:** Click your profile avatar → "Dashboard" or navigate to `/dashboard`.

**Dashboard Layout:**
- **Sidebar:** "Special Wishes" brand, "My Wishes" navigation (active), "Buy Tokens" link, user section (avatar, name, email), buttons for "My Profile" (`/profile`), "Home" (`/`), and Logout icon
- **Header:** "Back to Home" link, title "My Wishes" with subtitle "Manage and track your special wishes", "New Wish" button (`/`)

**Stats Cards (4):**
1. **Total Wishes** — Gifts icon, count of all greetings created
2. **Active** — Check mark (green), count of non-expired greetings
3. **Expired** — X mark (red), count of expired greetings
4. **Total Views** — Trending up (amber), sum of all views across all greetings

**Search/Filter/Sort:**
- **Search:** Text input with placeholder "Search wishes...", searches by title and recipient name
- **Filter:** Three buttons — All / Active / Expired
- **Sort:** Dropdown — Newest First / Oldest First

**Bulk Mode:**
- Toggle with "Select" / "Done" buttons
- When active: each greeting shows a checkbox, info bar says "Select wishes to delete", buttons for "Select All" / "Deselect All"
- Floating bottom action bar shows "{n} selected" with "Delete" and "Cancel" buttons

**Pagination:**
- 10 greetings per page
- Shows "Showing {start} to {end} of {total}"
- Page number buttons (max 5 visible), Previous/Next chevron buttons
- Hidden when total count ≤ 10

**Wish Card (per greeting):**
- Occasion emoji, greeting title, "To: {recipient_name}"
- Creation date (formatted: "MMM d, yyyy")
- Expiry info: "Expires: MMM d, yyyy" (green) or "Expired: MMM d, yyyy" (red)
- View count: "{n} views"
- Status badge: "Active" (green) or "Expired" (red)
- Action buttons row: Share (QR icon), Copy Link (copy icon), Preview (external link icon), Edit (pencil icon — only for active), More menu (⋮ — contains Edit - 100 tokens and Delete)

**Per-Greeting Actions:**
- **Share** — Opens ShareModal with QR code, swipe-to-copy, social buttons
- **Copy Link** — Copies greeting URL to clipboard, shows brief checkmark animation (2s)
- **Preview** — Opens greeting in new tab
- **Edit** — Shows confirmation dialog with current balance, -100 token cost, post-edit balance. If insufficient tokens, shows "You don't have enough tokens" warning with disabled button. Costs 100 tokens, only available for active greetings
- **Delete** — Confirmation dialog: "Are you sure you want to delete '{title}'? This action cannot be undone." With Cancel/Delete buttons

**Edit Confirmation Dialog Details:**
- Title: "Edit Greeting" with pencil icon
- Shows greeting title, current token balance, "-100 tokens" (red), and balance after editing
- Button: "Edit - 100 tokens" (disabled when insufficient tokens, when editing is in progress, or when token balance is loading)
- Warning text when insufficient: "You don't have enough tokens. Please purchase more to edit greetings."
- Loading spinner while deducting tokens

**States:**
- **Loading:** Spinner animation while greeting list fetches
- **Empty (no greetings):** Gift icon, "No wishes yet" heading, "Create your first special wish!" subtext, "Create Wish" button navigating to `/`
- **Search/filter with no results:** Shows empty state card
- **Error:** Toast notification "Failed to load greetings"

**Common Use Cases:**
- Check how many views your greetings received
- Find a specific greeting by searching
- Remove expired greetings in bulk
- Edit a greeting to fix a typo

---

### Premium / Token System

**What It Does:** Token-based economy for creating and editing greetings.

**How To Access It:** Navbar token badge → "Buy Tokens", navigate to `/premium`, or click "Buy Tokens" in the Dashboard sidebar.

**Token Plans:**

| Plan | Price | Tokens | Greetings | Badge |
|------|-------|--------|-----------|-------|
| Starter | ₹5 | 100 | ~1 | 1 Greeting |
| Pro (Popular) | ₹20 | 420 | ~4 | 4 Greetings |
| Premium | ₹100 | 2200 | ~22 | 20+2 Greetings |
| Elite | ₹200 | 4500 | ~45 | 40+5 Greetings |

**Features Included in Every Plan:**
1. Create N Cinematic Greetings (varies by plan)
2. Priority Processing
3. 2D Envelope Animations
4. Background Music & Slideshow
5. Mobile & Desktop Optimized
6. Secure Cloud Storage
7. Shareable Link

**Premium Page Details:**
- Dark theme page with starfield background (90 twinkling stars)
- 4 plan cards with individual accent colors (red, purple, gold, sky blue)
- Each card shows: plan name, description, price, token count pill, feature checklist, and "Buy Now" button
- Pro plan is marked with a "MOST POPULAR" badge and bounce-in animation
- Footer note: "Tokens never expire · Use anytime · Any occasion / We add more plans in future..."

**Premium Success Page:**
- URL: `/premium-success?order_id=<orderId>`
- Three states:
  - **Verifying** — Title "Verifying Payment", message "Your premium activation is being processed...", spinner, order ID displayed
  - **Success** — Title "Success!", message "Payment Successful! Your tokens have been added.", auto-redirects to homepage after 3 seconds, 20 floating hearts with rise animation
  - **Error** — Title "Payment Failed", error-specific message, buttons to "Go back to Premium Page" or "Retry Verification", footer with "If payment was deducted, contact support with order ID"

**Payment Flow:**
1. User clicks "Buy Now" on a plan
2. Frontend creates a payment order via backend API (`POST /api/payment/create-order`)
3. Cashfree SDK loads dynamically from CDN
4. Cashfree checkout popup opens (mode: production, redirect: _self)
5. After payment, user is redirected to `/premium-success?order_id=<orderId>`
6. Success page verifies payment with backend and credits tokens

**How Tokens Work:**
- Creating a greeting costs 100 tokens
- Editing a greeting costs 100 tokens
- Tokens never expire
- Your balance updates in real-time via Supabase realtime subscription
- Payment is processed securely via Cashfree (no card data stored on site)
- If you don't have enough tokens during creation, a warning modal appears with "Upgrade to Premium" and "Maybe Later" buttons

**Refund Policy:** Payments are generally non-refundable as digital services are delivered immediately. Contact support if you experience technical payment issues.

---

### Sharing

**What It Does:** Multiple ways to share your greeting link with recipients.

**How To Access It:** From the success screen after creating a greeting, or from the Dashboard via the share icon.

**Sharing Methods:**
- **Copy Link** — Copies the URL to clipboard
- **QR Code** — Displays a scannable QR code (downloadable as PNG)
- **Swipe-to-Copy** — Interactive slider to copy the link
- **Native Share** — Uses your device's share dialog
- **WhatsApp** — Opens WhatsApp with pre-written message
- **Facebook** — Opens Facebook share dialog
- **Twitter** — Opens Twitter with tweet text
- **Telegram** — Opens Telegram share dialog
- **Email** — Opens email client with subject and body

**Tips:**
- Save the link immediately after creation — it cannot be recovered if lost
- Download the QR code to print on physical cards or gifts
- The link format is: `https://special-wishes-kohl.vercel.app/g/abcdef`

---

### HeartStorm Game

**What It Does:** An interactive physics-based heart-filling game. Touch and hold to spawn hearts, fill the screen to 100 hearts, then release for an explosive physics animation before the Thank You page.

**How To Access It:** Click the "Next ✨" button on the Final Message Card at the end of the greeting experience, which navigates to `/heartstorm?code=yourCode`.

**How To Play:**
1. **Touch and Hold** — Hearts spawn continuously at random positions on screen (every 20ms)
2. **Fill the Screen** — Keep holding until hearts reach 100 hearts maximum
3. **Release** — When full, release triggers explosion: all hearts fly outward with physics (gravity 0.5, wind 0.3, rotation, random velocity 12-20)
4. **Wait** — Hearts fade out over 6 seconds with physics simulation via requestAnimationFrame
5. **Thank You** — After 6 seconds, auto-navigates to Thank You page

**Heart Colors:** 21 colors across 5 palettes — classic reds/pinks (#ff4d6d, #ff99ac, #dc143c, etc.), luxury tones (burgundy #800020, wine red #a4133c), soft dreamy tones (#ff85a2, #ffb3c6), vibrant neon (#ff0080, #ff1493), and white glow (#ffffff).

**Heart Sizes:** 20-28px each, random rotation, spawning animation (pulse scale 0→1.3→1 over 300ms).

**Tips:**
- Works on both desktop (mouse down/up) and mobile (touch start/end)
- If you release before reaching 100 hearts, hearts stop spawning without explosion
- The phrase "TOUCH AND HOLD" appears initially, then "RELEASE..." when full
- After explosion, auto-navigates to Thank You page after 6 seconds

---

### Thank You Page

**What It Does:** A romantic final page displayed after the HeartStorm game, thanking the user and providing a reply link back to the platform.

**How To Access It:** After completing the HeartStorm game (hearts explode → 6s delay → auto-navigate to `/thankyou/:shortCode`).

**What the user sees:**
- Pink background (#f153a2)
- Animated pop-up white card (scale 0.7→1 entry animation)
- Title: "𝓓𝓮𝓪𝓻❤️" (stylized Unicode)
- Subtitle: "In every universe, I have never failed to love you.💕"
- 40 floating hearts with `floatUp` animation (bottom→top, infinite loop, random positions via `Math.random()`)
- "Reply 💗❤️" gradient-styled link button (bottom-right, hover scale effect)

**What the user can do:**
- Click "Reply 💗❤️" — Navigates to the homepage (`/`) to start creating their own greeting
- The floating hearts continue animating indefinitely

---

### Pre-Made Music Tracks

**What It Does:** In addition to uploading your own music, you can choose from 5 pre-made background music tracks sourced from Pixabay.

**Available Tracks:**

| Track | Artist | Mood |
|-------|--------|------|
| Peaceful Morning | Ambient | Calm, relaxing |
| Happy Vibes | Upbeat | Energetic, cheerful |
| Love Story | Romantic | Romantic, heartfelt |
| Celebration | Festive | Joyful, triumphant |
| Gentle Piano | Piano | Soft, gentle |

**How To Access It:** During greeting creation, select a music track from the available options or upload your own MP3/WAV/OGG file.

**Tips:**
- Tracks are hosted on Pixabay's CDN and stream during the greeting
- Music starts when the recipient clicks "Play with Music" at the Music Gate
- Music fades in gradually over 900ms for a smooth start
- The recipient can always skip or mute the music

---

### Sound Effects

**What It Does:** The greeting experience includes synthesized sound effects using the Web Audio API (no external audio files needed).

**Available Sounds:**
- **Envelope Crack** — A sawtooth oscillator sweep from 150Hz to 50Hz with a sine "pop" (800Hz→200Hz), simulating the wax seal breaking when the envelope is opened
- **Celebration Chord** — A C-E-G-C arpeggiated chord with shimmering triangle wave overlay, played when the final card is reached
- **Tick** — (Planned, not yet implemented)

**How To Access It:** Sounds play automatically at key moments during the greeting viewing experience. No configuration needed.

**Technical Note:** If the AudioContext is suspended (due to browser autoplay policy), it is resumed when the user first interacts with the page.

---

### Greeting Customization Options

The platform supports several customization options for the greeting appearance. These are defined in the app's type system and available for use:

**Greeting Themes (10):**
Hearts, Stars, Particles, Confetti, Flowers, Snow, Butterflies, Rain, Fireworks, Default

**Font Styles (6):**
Default, Dancing Script, Pacifico, Great Vibes, Satisfy, Caveat

**Animation Speeds (3):**
- Slow — 2000ms per animation
- Normal — 1000ms per animation (default)
- Fast — 500ms per animation

**Letter Styles (4):**
Classic, Modern, Polaroid, Folded

---

### Visual Backgrounds

**What It Does:** Different pages and views use animated backgrounds to create the right atmosphere. There are multiple background systems:

**StarryBackground** — Used on login, premium, and greeting view pages:
- 100 twinkling stars with random positions, sizes (1-3.5px), and animation delays
- 5 shooting star streaks moving diagonally
- Up to 3 colored glow blobs (pink, purple, rose-gold) with slow morphing animation
- Subtle noise/grain texture overlay at 3.5% opacity
- Configurable star count, blob visibility, background color, and fixed/absolute positioning

**CinematicBackground** — Used on romantic greeting pages:
- 6 animated color schemes cycling every 8 seconds
- 40 twinkling stars, 15 falling stars with diagonal trails
- 12 floating hearts in various colors
- 20 floating particles in white/gold/pink/blue
- 8 cross-shaped sparkle bursts at random positions
- 2 ambient glow clouds
- Supports `prefers-reduced-motion` for accessibility

**AnimatedBackground (5 types):**
- **Nebula** — Deep space gradient with 3 nebula clouds, 80 stars
- **Party** — Dark purple with 20 colored light bars, disco ball effect
- **Moon** — Night sky with glowing moon, SVG clouds, 40 stars
- **Nature** — Sky gradient with sun cycle, green hills, grass texture
- **Snow** — Winter sky with 50 falling snowflakes, snow ground, snowman

---

### Multi-Language Support

**What It Does:** The interface is available in multiple languages.

**Supported Languages (3 active):**
- English (default) — en
- Hindi — hi (हिन्दी)
- Tamil — ta (தமிழ்)

**Additional Language Files (bundled but not yet activated):**
- Spanish (es) — file exists but not imported
- French (fr) — file exists but not imported

**Translation Coverage (3 namespaces):**
- `common` — 16 UI keys (home, create, dashboard, login, logout, save, cancel, delete, edit, share, download, copy, search, loading, error, success)
- `greeting` — 12 greeting-related keys (title, subtitle, recipientName, senderName, message, selectOccasion, addImages, addMusic, setPassword, createGreeting, preview, shareLink)
- `dashboard` — 9 dashboard keys (myWishes, totalWishes, active, expired, totalViews, searchWishes, noWishes, createFirst)
- `occasions` — 5 occasion names (birthday, valentinesDay, anniversary, christmas, newYear)

**Language Persistence:** The selected language is saved to localStorage under the key `'language'` and restored on next visit.

**How To Switch:** Use the language selector in the interface (location varies by page).

---

## Troubleshooting Guide

### Login Issues

**Problem: Google sign-in popup doesn't open**
- **Cause:** Popup blocker in your browser
- **Solution:** Allow popups for the site, or try again after disabling the popup blocker

**Problem: Already logged in but seeing "Sign Up" button**
- **Solution:** Clear your browser cache and cookies, then refresh the page

**Problem: "Redirecting to Google" but nothing happens**
- **Solution:** Check your internet connection. Try using a different browser.

### Creation Issues

**Problem: "Please upload at least one image" error**
- **Solution:** Images are required. Upload at least 1 image (max 5, 3MB each, JPG/PNG format).

**Problem: "Please select an expiry date" error**
- **Solution:** An expiry date is required. Select a future date from the calendar.

**Problem: "Insufficient tokens" message**
- **Solution:** You need at least 100 tokens to create a greeting. Purchase tokens from the Premium page.

**Problem: Image upload fails**
- **Possible causes:** File exceeds 3MB limit, file is not a supported image format
- **Solution:** Resize the image to under 3MB, use JPG or PNG format

**Problem: Music upload fails**
- **Possible causes:** File exceeds 10MB, file is not a supported audio format
- **Solution:** Use a smaller audio file (max 10MB) in MP3, WAV, or OGG format

**Problem: My draft wasn't restored**
- **Possible cause:** More than 24 hours have passed since you started
- **Solution:** Drafts are only preserved for 24 hours. Start a new greeting.

### Viewing Issues

**Problem: "Greeting Expired" message**
- **Cause:** The expiry date set by the creator has passed. The greeting has been permanently deleted from the system for privacy. No recovery is possible.
- **Solution:** Contact the person who sent you the greeting to request a new one

**Problem: "Greeting Not Found" message**
- **Cause:** The link is incorrect, the greeting was deleted, or the short code is invalid
- **Solution:** Verify the link with the sender

**Problem: Images aren't loading**
- **Possible cause:** Slow internet connection
- **Solution:** Wait for images to load. The page preloads images for smoother viewing.

**Problem: Music isn't playing**
- **Possible cause:** Browser autoplay policy blocked audio
- **Solution:** Click anywhere on the page first to enable audio, then try "Play with Music" again. Or use "Skip Music" to continue without audio.

**Problem: Can't enter the correct password**
- **Solution:** Contact the person who created the greeting. The password is shared separately by the creator.

### Payment Issues

**Problem: Cashfree payment popup doesn't open**
- **Solution:** Disable popup blocker. Try a different browser. Ensure stable internet connection.

**Problem: Payment was deducted but tokens not added**
- **Solution:** This is handled automatically. Visit the Premium Success page. If tokens still don't show, contact support with your transaction details.

**Problem: "Failed to start payment" error**
- **Solution:** Check your internet connection. Try again. If the problem persists, try a different plan or contact support.

### Dashboard Issues

**Problem: My greetings aren't showing**
- **Solution:** Make sure you're logged in with the correct Google account. Check your filter setting (try "All" instead of "Active" or "Expired").

**Problem: Can't find a greeting in the list**
- **Solution:** Use the search bar to search by title or recipient name. Check if the greeting has expired or been deleted.

**Problem: Edit button is disabled**
- **Solution:** Only active (non-expired) greetings can be edited. If the greeting has expired, you'll need to create a new one.

### Technical Issues

**Problem: The page isn't loading properly**
- **Solution:** Refresh the page. Clear your browser cache. Try a different browser (Chrome, Firefox, Safari, Edge all supported).

**Problem: Can I use this on my phone/tablet?**
- **Solution:** Yes! The site is fully responsive and works on mobile and tablet devices. The HeartStorm game supports touch input.

**Problem: Can I use this offline?**
- **Solution:** No, an internet connection is required to create and view greetings.

**Problem: My session expired**
- **Solution:** Log out and log back in with Google. Your data (greetings, tokens) is preserved.

---

## Questions and Answers

### General Questions

**Q: What is Special Wishes?**
A: A digital greeting card platform where you can create interactive, animated greeting pages with images, music, and messages for any occasion.

**Q: Is Special Wishes free?**
A: Creating and editing greetings costs tokens (100 tokens each). You do not receive free tokens on sign-up. Tokens can be purchased starting at ₹5 for 100 tokens.

**Q: Who created Special Wishes?**
A: Special Wishes was created by Samuvel, a solo developer and student passionate about building meaningful digital products.

**Q: What occasions are available?**
A: There are 24 occasions including Birthday, Valentine's Day, Anniversary, New Year, Christmas, Diwali, Mother's Day, Father's Day, Wedding, Friendship Day, Graduation, Teacher's Day, Thanksgiving, Baby Shower, Retirement, Easter, Halloween, Pregnancy, Brother's Day, Sister's Day, Good Luck, Welcome Baby, Get Well Soon, and General Wishes.

**Q: Can I request a new occasion?**
A: Contact the developer through the portfolio link on the Contact page with your suggestion.

**Q: Is my data safe?**
A: Yes. Authentication is handled securely via Google OAuth. Data is stored in Supabase with encrypted connections. Payment details go through Cashfree directly — the site never stores your card information.

**Q: Can I recover a greeting after it expires?**
A: No. Expired greetings are permanently deleted — all images, music, and messages are erased. This is done automatically for privacy. No recovery is possible.

**Q: Why are greetings deleted instead of just hidden?**
A: The expiry system is designed as a privacy protocol. Once a greeting's intended lifetime is over, all associated data is permanently removed from the system so it cannot persist indefinitely.

### Account Questions

**Q: How do I create an account?**
A: Click "Sign Up" in the top-right corner, agree to the Terms & Conditions and Privacy Policy, then click "Continue with Google" and select your Google account.

**Q: Why do I need to sign in with Google?**
A: Google authentication provides secure, password-free login. Your Google password is never shared with the site.

**Q: What if I don't have a Google account?**
A: Currently, only Google sign-in is supported. You'll need a Google account to use Special Wishes.

**Q: Can I use email and password instead of Google?**
A: No, only Google authentication is available.

**Q: How do I log out?**
A: Click your profile avatar in the top-right corner, then click "Logout" (🚪 icon) from the dropdown menu.

**Q: How do I delete my account?**
A: Email samuvel072@gmail.com with your account deletion request.

**Q: I forgot which Google account I used.**
A: Try signing in with each of your Google accounts. The correct one will show your greetings on the Dashboard.

**Q: Can I be signed in on multiple devices?**
A: Yes, your account can be used on multiple devices simultaneously.

### Creating Greetings

**Q: How do I create a greeting?**
A: Click an occasion card on the homepage, fill in the form with a title, your name, recipient name, messages, images, expiry date, and optionally music and password, then click "Generate Shareable Link".

**Q: How many images can I upload?**
A: Up to 5 images, each up to 3MB in size.

**Q: What formats can images be?**
A: JPG, PNG, and other standard image formats supported by your browser. Maximum 5 images, 3MB each.

**Q: How many messages can I write?**
A: Up to 5 messages, each up to 500 characters.

**Q: What music formats are supported?**
A: MP3, WAV, and OGG formats. Maximum file size is 10MB.

**Q: Can I skip adding music?**
A: Yes, music is optional. The recipient will see a "View Greeting" button instead of music controls.

**Q: What happens if I don't set a password?**
A: Anyone with the link can view the greeting without needing a password.

**Q: What is an expiry date?**
A: The date on which the greeting is permanently deleted from the system. Before deletion, viewers see "Greeting Expired". After deletion, the greeting and all its content (images, music, messages) are gone forever. No recovery. This automatic deletion is enforced for privacy.

**Q: Can I create a greeting without an expiry date?**
A: No, an expiry date is required. Choose a future date.

**Q: How much does it cost to create a greeting?**
A: 100 tokens per greeting. Tokens are purchased through the Premium page.

**Q: How do I save my progress while creating?**
A: The form auto-saves to your browser every 3 seconds. If you close and return within 24 hours, your draft will be restored.

**Q: Can I create a greeting from a URL directly?**
A: Yes, visiting `/?occasion=birthday` (replace 'birthday' with any occasion ID) auto-selects that occasion and opens the creation form.

**Q: What happens if the short code generation fails?**
A: The system retries up to 10 times to generate a unique 6-character code. If all attempts fail, the greeting creation fails with an error.

**Q: Can I edit a greeting after creating it?**
A: Yes, from the Dashboard. Click the edit icon on an active greeting. Editing costs 100 tokens.

**Q: Is there an edit history or versioning?**
A: No. Each edit overwrites the previous content. There is no version history or undo for edits.

**Q: Can I delete a greeting?**
A: Yes, from the Dashboard. Click the delete option in the menu, or use bulk select to delete multiple greetings at once.

### Viewing Greetings

**Q: How do I view a greeting?**
A: Open the link shared with you (format: `/g/abcdef`). The experience plays automatically.

**Q: How do I enter the password?**
A: If the greeting is password-protected, a password screen will appear. Enter the password provided by the sender.

**Q: Can I skip the music?**
A: Yes, click "Skip Music" when the music gate screen appears.

**Q: Can I replay the greeting?**
A: Yes, click "Replay" on the final card to experience the greeting from the beginning.

**Q: How long does a greeting stay viewable?**
A: From the moment you create it until the expiry date you select at creation. After that date, it is permanently deleted.

**Q: What does "Greeting Expired" mean?**
A: The expiry date set by the creator has passed. The greeting is no longer accessible.

**Q: What does "Greeting Not Found" mean?**
A: The link is invalid, the greeting was deleted, or the short code doesn't exist.

**Q: Can I view a greeting multiple times?**
A: Yes, as long as it hasn't expired and hasn't been deleted.

**Q: Why can't I see images in the greeting?**
A: Check your internet connection. Images may take a moment to load.

### Tokens & Payments

**Q: What are tokens?**
A: Tokens are the currency used on Special Wishes. Creating or editing a greeting costs 100 tokens.

**Q: How do I get tokens?**
A: Purchase tokens from the Premium page (`/premium`). Plans start at ₹5 for 100 tokens.

**Q: What payment methods are accepted?**
A: Payments are processed through Cashfree, which accepts UPI, credit/debit cards, net banking, and other popular Indian payment methods.

**Q: Do tokens expire?**
A: No, purchased tokens never expire and can be used anytime.

**Q: Can I get a refund for purchased tokens?**
A: Payments for digital services are generally non-refundable. Contact support if you experienced a technical issue.

**Q: What if my payment fails but money was deducted?**
A: Contact the developer through the portfolio link with your transaction details for assistance.

**Q: Can I transfer tokens to another user?**
A: No, tokens are tied to your account and cannot be transferred.

**Q: How do I check my token balance?**
A: Your token balance is displayed next to the coin icon in the navbar, and on your Profile page (`/profile`).

**Q: What happens if I run out of tokens while creating?**
A: You'll see a warning screen with an option to purchase more tokens or cancel.

**Q: What does the token warning modal say exactly?**
A: The modal shows an "Unlock Premium Features" heading, body text "Creating beautiful greetings is our passion...", a "🎁 Get 100 tokens to create your first greeting!" callout, and buttons for "Upgrade to Premium" and "Maybe Later".

**Q: Is my card information stored on the site?**
A: No. Payments are processed entirely through Cashfree's secure platform. The site never sees or stores your card details.

### Sharing

**Q: How do I share my greeting?**
A: After creating, you'll see a success screen with sharing options. You can also share from the Dashboard by clicking the share icon on any greeting.

**Q: Can I share via WhatsApp?**
A: Yes, click the WhatsApp button in the share modal or on the success screen.

**Q: Can I generate a QR code?**
A: Yes, the share modal displays a QR code that you can download as a PNG image.

**Q: How do I copy the link?**
A: Click "Copy Link" on the success screen, or swipe the slider in the share modal.

**Q: I lost the link — can I recover it?**
A: No. The link cannot be recovered. Always save or share it immediately after creating. You can find your greeting's link in the Dashboard. Also, if the greeting has already expired, it has been permanently deleted and cannot be recovered.

**Q: Can I share on social media?**
A: Yes, share directly to WhatsApp, Facebook, Twitter, Telegram, or Email from the share modal.

### Dashboard

**Q: How do I access my Dashboard?**
A: Click your profile avatar → "Dashboard", or navigate to `/dashboard`.

**Q: How do I search for a specific greeting?**
A: Use the search bar on the Dashboard. It searches by greeting title and recipient name.

**Q: What do the stats cards mean?**
A: **Total Wishes** = all greetings you've created. **Active** = greetings that haven't expired. **Expired** = greetings past their expiry date. **Total Views** = sum of all views across all your greetings.

**Q: Can I delete multiple greetings at once?**
A: Yes, click "Select" to enter bulk mode, check the greetings you want to delete, and click the floating "Delete" button.

**Q: How do I edit a greeting from the dashboard?**
A: Click the edit icon (pencil) on an active greeting. A confirmation dialog will show the 100-token cost. Confirm to proceed.

**Q: Why does editing cost tokens?**
A: Editing regenerates and re-uploads content, which uses system resources.

**Q: Why is the edit button not showing?**
A: Only active (non-expired) greetings can be edited.

**Q: Can I preview my greeting before sharing?**
A: Yes, click the preview icon (external link) on any greeting card in the Dashboard.

### Contact & Support

**Q: How do I contact support?**
A: Visit the Contact page and use the "Contact via Portfolio" link to reach the developer.

**Q: How do I contact Samuvel?**
A: Through the portfolio website linked on the Contact page.

**Q: Where can I report a bug?**
A: Report bugs through the Contact page or the portfolio link.

**Q: How long does it take to get a response?**
A: The platform is managed by a solo developer. Please allow reasonable time for a response.

### Technical

**Q: Does Special Wishes work on mobile?**
A: Yes, the site is fully responsive and works on mobile phones and tablets.

**Q: What browsers are supported?**
A: Chrome 90+, Firefox 88+, Safari 14+, Edge 90+, and mobile browsers.

**Q: Why is the page not loading?**
A: Check your internet connection. Try refreshing or clearing your browser cache.

**Q: My upload is stuck — what should I do?**
A: File uploads depend on your internet speed. Large files (close to 3MB for images, 10MB for music) may take time. If stuck, check if the file exceeds the size limit.

**Q: Is there a mobile app?**
A: Not yet. A mobile app is planned for future development.

**Q: The greeting link doesn't work on mobile**
A: Ensure you're using a supported browser. The link works on all devices.

### Customization

**Q: Can I customize the greeting appearance?**
A: The platform supports 10 themes (hearts, stars, confetti, etc.), 6 font styles (Dancing Script, Pacifico, etc.), 3 animation speeds, and 4 letter styles. These customization options are defined in the app's type system.

**Q: What pre-made music tracks are available?**
A: 5 tracks from Pixabay: Peaceful Morning (calm), Happy Vibes (upbeat), Love Story (romantic), Celebration (festive), and Gentle Piano (soft). You can also upload your own music.

**Q: Can I use my own music instead of pre-made tracks?**
A: Yes, you can upload your own MP3, WAV, or OGG file (max 10MB) during greeting creation.

**Q: What sound effects does the greeting have?**
A: The greeting uses Web Audio API synthesized sounds: an envelope crack effect (seal breaking) when opening the 3D envelope, and a celebration chord (C-E-G-C arpeggio) when reaching the final card. No external audio files are needed.

**Q: Can I turn off the sound effects?**
A: The Music Player provides mute controls. Click the mute button in the floating player during the greeting experience.

### Greetings & Viewing

**Q: Why are only 15 occasions shown on the homepage?**
A: The homepage shows 15 main occasions. Click "More" (+9 occasions) to see all 24 occasions on the `/more` page.

**Q: What's the difference between `/g/code` and `/view/:id`?**
A: `/g/:shortCode` is the current greeting viewer that fetches from the database. `/view/:id` is a legacy route that reads greeting data from localStorage and may not work for new greetings.

**Q: Can I use keyboard to navigate the slideshow?**
A: Yes, press the Left Arrow (←) and Right Arrow (→) keys to navigate between images in the slideshow.

**Q: What happens when I click "Next" on the final card?**
A: The "Next ✨" button appears after all words on the final card are revealed. Clicking it navigates to the HeartStorm game page (`/heartstorm?code=xxx`) for an interactive celebration experience.

**Q: What does the HeartStorm game involve?**
A: Touch and hold to spawn hearts (up to 100). When full, release to trigger an explosion with physics simulation (gravity, wind, rotation). After 6 seconds, auto-navigates to a romantic Thank You page.

**Q: How does the draft auto-save work?**
A: The form saves to your browser's localStorage every 3 seconds while you fill it out. If you close the browser and return within 24 hours, your draft is automatically restored with a "Draft restored" toast notification.

### Tokens & Payments

**Q: Are there any free tokens available?**
A: Currently, no free tokens are given on sign-up. All tokens must be purchased from the Premium page. Plans start at ₹5 for 100 tokens.

**Q: What happens to my uploaded files after the greeting expires?**
A: When a greeting passes its expiry date, a backend cleanup script (cron job) deletes the greeting record and its associated images and music files from cloud storage.

**Q: How does auto-expire work?**
A: A backend cron service periodically checks for greetings where `expires_at` has passed. It deletes the greeting record and associated files (images from `greeting-images` bucket, music from `greeting-music` bucket).

### Profile & Account

**Q: Can I change my name or email on Special Wishes?**
A: Your name and email come from your Google account. To change them, update your Google account settings. The changes will reflect on Special Wishes.

**Q: How do I check my token balance?**
A: Your token balance is shown in the navbar (coin icon + number), on the Profile page (`/profile`), and in the Dashboard sidebar. The balance updates in real-time.

**Q: What happens if I delete my Google account?**
A: Your Special Wishes account will still exist but you won't be able to log in. Contact samuvel072@gmail.com to request account deletion.

### Technical

**Q: What languages are supported?**
A: Three languages are active: English (default), Hindi (हिन्दी), and Tamil (தமிழ்). Spanish and French translation files exist but are not yet activated in the app.

**Q: How much translation coverage is there?**
A: The app has 4 translation namespaces: common UI (16 keys like home, login, save), greeting creation (12 keys), dashboard (9 keys), and occasion names (5 keys).

**Q: Can I use the site as a PWA?**
A: The site has a manifest.json with standalone display mode and heart icons at multiple sizes. However, full PWA functionality (service worker, offline support) is not yet implemented.

**Q: Does Special Wishes have dark mode?**
A: The site uses a dark theme by default. There is no light mode toggle currently.

**Q: Where are my uploaded files stored?**
A: Images and music are stored in Supabase Storage (`greeting-images` and `greeting-music` buckets) with encrypted connections.

**Q: What robots.txt rules are configured?**
A: The site allows crawling by Googlebot, Bingbot, Twitterbot, facebookexternalhit, and all other user agents on all paths.

---

## Quick Answers

**Q: How do I create an account?**
A: Click "Sign Up" in the navbar, agree to terms, and sign in with Google.

**Q: How do I log in?**
A: Click "Sign Up" and sign in with your Google account.

**Q: How do I log out?**
A: Click your profile avatar → "Logout".

**Q: How do I create a greeting?**
A: Click an occasion card on the homepage, fill in the form, and click "Generate Shareable Link" (costs 100 tokens).

**Q: How do I edit a greeting?**
A: Go to Dashboard, click the edit icon on an active greeting (costs 100 tokens).

**Q: How do I delete a greeting?**
A: Go to Dashboard, click the menu on a greeting card → "Delete".

**Q: How do I share a greeting?**
A: Use the share options on the success screen after creation, or click the share icon on the Dashboard.

**Q: How do I get tokens?**
A: Visit the Premium page (`/premium`) and purchase a token plan.

**Q: How much does a greeting cost?**
A: 100 tokens per creation or edit.

**Q: Do tokens expire?**
A: No, tokens never expire.

**Q: How many images can I upload?**
A: Up to 5 images, each max 3MB.

**Q: How many messages can I write?**
A: Up to 5 messages, each max 500 characters.

**Q: What if I forget my password?**
A: There's no password — you sign in with Google. Use your Google account to log in.

**Q: How do I change my profile picture?**
A: Your profile picture comes from your Google account. Change it in your Google account settings.

**Q: How do I delete my account?**
A: Email samuvel072@gmail.com with your request.

**Q: How do I contact support?**
A: Visit the Contact page and click "Contact via Portfolio".

**Q: Why can't I view a greeting?**
A: It may be expired, deleted, or the link may be incorrect.

**Q: Where can I find my greetings?**
A: On the Dashboard (`/dashboard`).

**Q: Can I use this on mobile?**
A: Yes, it works on all devices.

**Q: Can I recover an expired greeting?**
A: No. Expired greetings are permanently deleted for privacy. No recovery.

**Q: How do I select an occasion from a URL?**
A: Visit `/?occasion=occasionId` (e.g., `/?occasion=birthday`).

---

## Contact Information

- **Website:** [special-wishes-kohl.vercel.app](https://special-wishes-kohl.vercel.app)
- **Developer Portfolio:** [portfolio-beta-sam.vercel.app](https://portfolio-beta-sam.vercel.app)
- **Account Deletion Requests:** samuvel072@gmail.com
- **Support:** Visit the Contact page → "Contact via Portfolio" link
- **Crawling:** robots.txt allows Googlebot, Bingbot, Twitterbot, facebookexternalhit, and all other bots
- **PWA:** manifest.json with standalone display, heart icons (16x16 to 512x512), theme color #e879f9

All genuine messages received through the portfolio are reviewed. Please allow reasonable time for a response as this is a solo-developed project.

---

## Data & Privacy

### What Information Is Collected

**Account Information:**
- Full name (from Google account)
- Email address (from Google account)
- Google profile image
- Google account ID

**Greeting Content (you provide):**
- Recipient name, sender name, messages
- Uploaded images and music
- Expiry date and password (if set)

**Technical Information:**
- IP address, browser type, device type
- Usage logs and access timestamps
- User agent string (logged when a greeting is viewed, stored in `greeting_views` table)

### What Information Is NOT Collected
- Google password (never shared with the site)
- Credit/debit card numbers (handled by Cashfree)
- Gmail, Google Drive, or other Google service data
- Contacts, files, or personal documents

### Third-Party Services
- **Supabase** — Database, authentication, and file storage (images in `greeting-images` bucket, music in `greeting-music` bucket)
- **Google** — Authentication (OAuth 2.0), only basic profile info (name, email, avatar)
- **Cashfree** — Payment processing (card details handled entirely on Cashfree's secure platform)
- **Pixabay** — Background music tracks (5 pre-licensed tracks streamed from Pixabay CDN)
- **Vite/React** — Frontend framework and build tool

### Data Retention
- Data is retained while your account is active
- Expired greetings are permanently deleted on their expiry date by an automated backend process. This includes the greeting record, all uploaded images, music files, and view history. NO RECOVERY IS POSSIBLE. This deletion is enforced for user privacy — content does not persist beyond its intended lifetime.
- Deleted greetings are removed from the system
- Account deletion can be requested via email
- Draft data stored in your browser's localStorage has a 24-hour retention window

### Your Rights
- You can request account deletion at any time
- You own the content you upload
- Your data is never sold to third parties

---

## Website Summary

**One Sentence:** Special Wishes is a digital greeting card platform that lets you create interactive, animated greeting pages with images, music, and heartfelt messages for any occasion.

**Short Summary (50-100 words):**
Special Wishes allows users to create personalized digital greeting cards for 24 different occasions. Each greeting features a 3D envelope animation, image slideshow with Ken Burns effect, background music, animated letter cards, and a 3D rotating final card. Greetings can be password-protected and set to expire on a chosen date, after which they are permanently deleted for privacy. The platform uses a token system (purchased via Cashfree) where creating or editing a greeting costs 100 tokens. Users can manage all their greetings from a Dashboard, share via QR code or social media, and track view counts.

**Detailed Summary (300-500 words):**
Special Wishes is a full-featured digital greeting platform developed by Samuvel, designed to make sending personalized greetings a rich, multimedia experience. Unlike traditional e-cards, Special Wishes delivers a complete interactive journey for the recipient.

The platform supports 24 occasion types including birthdays, anniversaries, Valentine's Day, festivals (Christmas, Diwali), family days (Mother's Day, Father's Day), and more. Each greeting creation goes through a guided form where users add a title, their name, the recipient's name, up to 5 heartfelt messages (500 characters each), up to 5 images (3MB each), optional background music (10MB), an expiry date, and optional password protection. The form auto-saves drafts every 3 seconds with 24-hour restoration.

When a recipient opens a greeting link, they experience a 7-stage journey: an interactive 3D crimson envelope with a wax seal that cracks open with particle effects, an optional password gate, a music selection screen, a 3-2-1 cinematic countdown, a Ken Burns-effect image slideshow, animated letter cards with gold ornaments, and a final 3D rotating card with a word-by-word message reveal.

The platform uses a token economy where creating or editing a greeting costs 100 tokens. Tokens are purchased through four plans via Cashfree (starting at ₹5 for 100 tokens, up to ₹200 for 4500 tokens) and never expire. The Dashboard provides full CRUD management with search, filter, sort, pagination, bulk delete, and view tracking.

Sharing options include QR code generation (downloadable PNG), swipe-to-copy link, and direct sharing to WhatsApp, Facebook, Twitter, Telegram, and Email. The interface supports English, Hindi, and Tamil (with Spanish and French files bundled but not yet activated).

Each greeting has an expiry date — on that date it is permanently deleted from the system for privacy. No recovery is possible. This automatic deletion is a core privacy protocol: once a greeting's intended lifetime is over, all data is permanently removed.

Beyond the core experience, the platform includes a HeartStorm physics game (touch/hold to fill the screen with hearts, release for explosion), a romantic Thank You page with floating hearts, synthesized sound effects via Web Audio API, 5 pre-made Pixabay music tracks in addition to custom uploads, 10 greeting themes, 6 font styles, and customizable animation speeds. Expired greetings are automatically cleaned up by a backend cron job.

Special Wishes is built with React, TypeScript, Vite, and Tailwind CSS, hosted on Vercel. User authentication is handled via Google OAuth, data is stored in Supabase with encrypted connections, and payments are processed entirely through Cashfree — the site never stores payment information. The platform is fully responsive and works on desktop, tablet, and mobile devices.
