# Universal Chat Area

## Website Overview

### Purpose

Universal Chat Area is a privacy-focused realtime community chat platform. It lets users sign in with Google and instantly connect with people worldwide through instant messaging, direct messages, and community chat rooms — all without email verification, tracking, or data collection.

### Who Is This For?

- **General users** who want a private, no-signup-friction chat experience
- **Privacy-conscious individuals** who want realtime chat without tracking
- **Developers** who appreciate modern web technology
- **Digital nomads** who need persistent chat across devices
- **Community builders** looking for a free, open chat platform

### Main Value

One-click Google sign-in, instant realtime messaging, zero tracking, message history that survives refreshes, and a safe community with moderation tools — all free.

---

## Key Features

| Feature | Purpose | Where to Find It |
|---|---|---|
| **Google Sign-In** | One-click authentication, no password | Landing page "Sign In with Google" button, /auth page |
| **Realtime Chat (#general)** | Instant messaging with all online users | /chat page, "Join #general" button |
| **Direct Messages (DMs)** | Private 1-on-1 conversations with friends | Sidebar → Direct Messages list under Friends |
| **Friends System** | Add, accept, and manage friends | Sidebar → Friends section, Find People / Requests buttons |
| **Message Reactions** | React with emoji on any message | Hover a message → click reaction emoji |
| **Emoji Picker** | Insert emoji in your message | Message input bar → smiley face button |
| **Message Reply** | Reply to a specific message | Hover a message → Reply button |
| **Message Editing** | Edit your sent messages | Hover your message → Edit (pencil) button |
| **Message Deletion** | Delete your sent messages | Hover your message → Delete (trash) button |
| **Message Reporting** | Report inappropriate messages | Hover others' messages → Report (flag) button |
| **User Muting** | Hide messages from a specific user | Hover others' messages → Mute button |
| **Message Search** | Search through chat history | Chat header → Search icon, or Ctrl+K |
| **Offline Cache** | Messages persist in your browser | Automatic — no action needed |
| **Dark/Light Mode** | Toggle theme | Site header moon/sun icon, Sidebar moon/sun icon |
| **Chat Settings** | Enter-to-send toggle, font size, message density | Chat header → Settings (gear) icon |
| **Profile Editing** | Change display name, bio, status, avatar | /profile page |
| **Unique ID** | Share your personal ID so friends can find you | Shown after first sign-in, also on /profile page |
| **Community Guidelines** | Rules for respectful communication | /guidelines page |
| **FAQ** | Answers to common questions | /faq page |

---

## Website Structure

### Homepage (/)

- Animated hero section with 3D scene
- Stats counter (messages sent, active users, uptime, countries)
- Live chat preview animation
- Tech stack display
- Core features grid
- Testimonials
- FAQ accordion
- Call-to-action: "Sign In with Google" or "Build Your Friends" (when signed in)

### Auth Page (/auth)

- Google sign-in button (Google One Tap)
- Benefits list
- Unique ID Spin Modal (first-time users only — reveals your personal #ID)

### Chat Page (/chat)

- Requires sign-in
- "Join #general" prompt (first visit)
- Full chat interface: sidebar, message list, input bar
- Chat channels: #general and DMs with friends
- Online user list in sidebar
- Search overlay (Ctrl+K)
- Settings modal (gear icon)

### Profile Page (/profile)

- Requires sign-in; redirects to /auth if not signed in
- Avatar (random generator + remove)
- Display name (max 50 characters)
- Bio (max 200 characters)
- Custom status (max 80 characters)
- Unique ID display + copy button
- Save button (profile edits allowed once every 3 months)
- Sign Out button
- Delete Account button (irreversible)

### User Profile Page (/profile/:userId)

- Public view of another user's profile
- Shows their display name, bio, avatar, unique ID
- Add Friend / Friend request status

### About Page (/about)

- Information about the platform
- Mission and values

### FAQ Page (/faq)

- Comprehensive frequently asked questions

### Community Guidelines Page (/guidelines)

- Rules for respectful communication
- Moderation policies
- Naming policy

### Privacy Policy Page (/privacy)

- Data handling and privacy information

### Terms of Service Page (/terms)

- Terms and conditions

### Contact Page (/contact)

- Links to portfolio website for direct contact
- Community chat room
- FAQ page reference

### Blog Page (/blog)

- Platform updates and articles

---

## Complete User Journeys

### Landing Journey

**Step 1 — First Visit**

*What the user sees:* Animated hero with 3D scene, "Universal Chat Area" title, "Sign In with Google" CTA button.

*What the user does:* Scrolls down to explore features, stats, testimonials, and FAQ.

*What happens:* Content animates into view. Stats count up.

---

### Account Creation Journey

**Step 1 — Click Sign In**

*What the user sees:* Landing page or /auth page with Google sign-in button.

*What the user does:* Clicks "Sign In with Google".

*What happens:* Google One Tap popup appears.

**Step 2 — Select Google Account**

*What the user sees:* Google account selection dialog.

*What the user does:* Selects a Google account and clicks "Continue".

*What happens:* Page shows a loading spinner ("Signing in..."), then the Unique ID Spin Modal appears.

**Step 3 — Unique ID Spin**

*What the user sees:* A modal with 6 digit slots and a "Get Your ID" button.

*What the user does:* Clicks "Get Your ID".

*What happens:* Digits spin like a slot machine and settle on your permanent unique ID (e.g., #000042).

**Step 4 — Copy & Continue**

*What the user sees:* Your revealed #ID with a copy button and "Start Chatting" button.

*What the user does:* (Optional) Clicks the copy button to save your ID. Clicks "Start Chatting".

*What happens:* Redirects to the Home page. You are now signed in.

---

### Login Journey

**Step 1 — Navigate to /auth**

*What the user sees:* Google sign-in button.

*What the user does:* Clicks "Sign In with Google".

*What happens:* One-click sign-in (no email/password needed).

**Step 2 — Redirect**

*What the user does:* Nothing — automatic redirect.

*What happens:* Returns to Home page, signed in. Your session persists for up to 7 days.

---

### General Chat Journey

**Step 1 — Open Chat**

*What the user sees:* /chat page. If not yet joined, sees the "Join #general" prompt.

*What the user does:* Clicks "Join #general".

*What happens:* A system message "You joined the chat" appears. The full chat interface loads with recent messages.

**Step 2 — Send a Message**

*What the user sees:* Message input bar at the bottom with a text area, emoji button, and send button.

*What the user does:* Types a message, optionally clicks the smiley face to add an emoji, then presses Enter (or clicks the send arrow).

*What happens:* Message appears instantly in the chat with a "sent" status icon (checkmark). Other online users see your message in real time.

**Step 3 — Reply to a Message**

*What the user sees:* Hover over any message.

*What the user does:* Clicks the Reply button (appears on hover).

*What happens:* A "Replying to [name]" bar appears above the input. Type a reply and send.

**Step 4 — React to a Message**

*What the user sees:* The reaction bar below each message.

*What the user does:* Clicks an existing reaction emoji to toggle it, or clicks the smiley face (+) to open the emoji picker and select one.

*What happens:* The emoji appears below the message with a count. Your reaction is visible to everyone.

**Step 5 — Edit or Delete Your Message**

*What the user sees:* Hover over your own message.

*What the user does:* Clicks the Edit (pencil) icon to modify the text, or Trash icon to delete.

*What happens (Edit):* The message becomes an editable text area. Press Enter to save or Escape to cancel. An "(edited)" label appears.
*What happens (Delete):* The message is permanently removed from chat.

**Step 6 — Report or Mute**

*What the user sees:* Hover over another user's message.

*What the user does:* Click Flag to report (sent to moderators), or Volume-X to mute (hides all messages from that user).

*What happens (Report):* A report is sent to platform operators.
*What happens (Mute):* All messages from that user are hidden from your view.

---

### Direct Message Journey

**Step 1 — Find and Add a Friend**

*What the user sees:* Sidebar → Friends section → "Find People" button (user-plus icon).

*What the user does:* Clicks "Find People", then searches by name or #ID in the search modal.

*What happens:* Matching users appear. Click "+" on a user to send a friend request.

**Step 2 — Accept a Friend Request**

*What the user sees:* Sidebar → Friends section → Bell icon (shows count of pending requests).

*What the user does:* Clicks the Bell icon to open the Friend Request List, then clicks "Accept" on a request.

*What happens:* The user is added to your Direct Messages list. The sender of the request also sees you as a friend.

**Step 3 — Start a Direct Message**

*What the user sees:* Sidebar → Direct Messages list shows all friends with an online indicator (green dot).

*What the user does:* Clicks a friend's name.

*What happens:* The chat switches to a private DM conversation. A purple dot and the friend's name appear in the header. Messages sent here are only visible to you and that friend.

**Step 4 — Return to General Chat**

*What the user sees:* DM header shows a back arrow (←) button.

*What the user does:* Clicks the back arrow.

*What happens:* Returns to the #general chat channel.

---

### Profile Management Journey

**Step 1 — Open Profile**

*What the user sees:* Click your name/avatar in the site header or sidebar, or navigate to /profile.

*What happens:* Profile page loads with your current information.

**Step 2 — Edit Fields**

*What the user does:* Edit your Display Name, Bio, or Custom Status fields. Click "Random" to generate an avatar, or "Remove" to clear it.

*What happens:* Fields update locally. A "Save Profile" button becomes available.

**Step 3 — Save**

*What the user does:* Clicks "Save Profile".

*What happens:* Profile saves to server. A green success message appears. **Note:** Profile edits are limited to once every 3 months. A cooldown counter shows remaining time if you've recently edited.

---

### Logout Journey

**Step 1 — Open Profile Page**

*What the user does:* Navigate to /profile.

**Step 2 — Click Sign Out**

*What the user does:* Clicks the red "Sign Out" button.

*What happens:* Session ends. You are redirected to the Home page. Your httpOnly cookie is cleared.

---

## Feature Documentation

### Google Sign-In

**What It Does:** Authenticates you with one click using your Google account. No email verification, no password to remember.

**How To Access:** Click "Sign In with Google" on the landing page or navigate to /auth.

**How To Use:**
1. Click the Google sign-in button
2. Select your Google account
3. If first time, spin to reveal your Unique ID
4. You're now signed in

**Common Use Cases:** First-time sign up, returning login.

---

### General Chat (#general)

**What It Does:** A public realtime chat room where all signed-in users can talk.

**How To Access:** Navigate to /chat → Click "Join #general".

**How To Use:**
- Type in the input bar and press Enter to send
- Use the emoji button to add emoji to your message
- Hover messages to reply, copy, edit, delete, report, or mute

**Tips:**
- Messages are delivered via WebSocket in under 100ms
- Your recent messages are cached locally and survive page refreshes
- Use Ctrl+K (or Cmd+K) to search messages

---

### Direct Messages (DMs)

**What It Does:** Private 1-on-1 conversations with your friends.

**How To Access:** Click a friend's name in the Sidebar → Direct Messages list.

**How To Use:**
1. First add a friend using "Find People" in the sidebar
2. Accept their request or have them accept yours
3. Click their name to open the DM
4. Send messages as usual — they're private between you two

**Tips:**
- DM messages are fetched via polling (updates every 2 seconds)
- Click the back arrow (←) to return to #general

---

### Friends System

**What It Does:** Add, manage, and chat privately with friends.

**How To Access:** Sidebar → Friends section.

**How To Use:**
- **Find People:** Click the user-plus icon → search by name or #ID → click "+" to send request
- **Requests:** Click the Bell icon → Accept or Reject pending requests
- **DM:** Click any friend's name in the list to start a private conversation

**Tips:**
- Friends show an online green dot when they're active
- Friends show a red notification badge if they've sent you messages
- You can find friends by their 6-digit unique ID (e.g., #000042)

---

### Emoji Reactions

**What It Does:** React to messages with emoji.

**How To Access:** Hover over any message → click an existing reaction to toggle it, or click the smiley face (+) to add a new reaction.

**Available Emoji:** 👍, ❤️, 😂, 😮, 😢, 🙏

**How To Use:**
- Click an existing reaction to add or remove your vote
- Click the + button to open the quick picker
- The count shows how many users reacted

---

### Emoji Picker

**What It Does:** Insert emoji into your message text.

**How To Access:** Click the smiley face button in the message input bar.

**20 Emoji Available:** 😊, 😂, 😍, 😎, 🤔, 😭, 👍, 🔥, ✨, 🎉, ❤️, 🙏, 💀, 🥳, 😴, 👋, 🤝, ⭐, 🌈, 🎊

**How To Use:** Click any emoji to insert it at the cursor position in your message.

---

### Message Search

**What It Does:** Search through all visible messages in the current chat.

**How To Access:** Click the Search icon in the chat header, or press Ctrl+K (Cmd+K on Mac).

**How To Use:**
1. Type your search term
2. Results appear instantly, filtered as you type
3. Use ↑↓ to navigate, Enter to select, Escape to close

**Tips:**
- Searches all non-system messages
- Shows the most recent 50 messages when no search term is entered
- Highlighted matches appear in the result text

---

### Chat Settings

**What It Does:** Customize your chat experience.

**How To Access:** Click the Settings (gear) icon in the chat header.

**Available Options:**
- **Enter to send:** Toggle on/off (on by default)
- **Font size:** Small / Medium / Large
- **Message density:** Compact / Comfortable

**How To Use:** Adjust any setting — changes save automatically to your browser.

---

### Dark / Light Mode

**What It Does:** Toggle between light and dark themes.

**How To Access:** Click the Sun/Moon icon in the site header (info pages) or sidebar (chat page).

**How To Use:** Single click toggles. Your preference is remembered on future visits.

---

### Profile Editing

**What It Does:** Update your display name, bio, custom status, and avatar.

**How To Access:** Navigate to /profile.

**Editable Fields:**
- **Avatar:** Click "Random" to generate a random avatar, "Remove" to clear
- **Display Name:** Up to 50 characters
- **Bio:** Up to 200 characters
- **Custom Status:** Up to 80 characters (e.g., "Away", "Coding", "Busy")

**Important:** Profile edits are limited to once every 3 months. A cooldown counter shows remaining time if you've recently edited.

---

### Unique ID

**What It Does:** A permanent 6-digit identifier (#000001 style) assigned on first sign-in. Share it so friends can find you.

**How To Find:**
- Revealed during the "Spin Modal" on first sign-in
- Always visible on your /profile page
- Displayed in your sidebar user card (below your name)

**How To Share:** Click the copy icon next to your #ID to copy it to clipboard, then paste it to friends.

---

### Keyboard Shortcuts

**What They Do:** Keyboard shortcuts let you perform common actions faster without reaching for the mouse.

**Available Shortcuts:**
| Shortcut | Action | Works In |
|---|---|---|
| **Enter** | Send message (when Enter-to-send is enabled in settings) | Chat input |
| **Shift + Enter** | Insert a new line in your message | Chat input |
| **Ctrl+K** (or **Cmd+K** on Mac) | Open message search overlay | Chat page |
| **↑ / ↓** | Navigate search results | Search overlay |
| **Enter** | Select highlighted search result | Search overlay |
| **Escape** | Close search overlay, cancel edit, close modal | Anywhere |
| **Escape** (while editing) | Cancel message edit | Chat message |

**Tips:**
- Ctrl+K is the most useful shortcut — use it to quickly find past messages
- Shift+Enter is the only way to add line breaks when Enter-to-send is enabled
- Escape closes any open modal or overlay

---

### Typing Indicators

**What They Do:** Shows when another user is typing in the same chat channel.

**How It Works:**
- When you start typing in the message input, a `typing_start` signal is sent to other users in the same channel
- Other users see "[name] is typing..." below the chat header
- When you stop typing for 2 seconds or send your message, a `typing_stop` signal is sent
- The indicator disappears automatically

**Where It Works:**
- **#general:** You see typing indicators from all other users in the general chat
- **Direct Messages:** Typing indicators are **not currently supported** in DMs. This is a known limitation.

**Tips:**
- The typing indicator only shows the name, not what you're typing
- Your typing is private until you press send
- The indicator has a 2-second timeout — if you pause typing, it disappears

---

### Message Types & Status Icons

**What They Do:** Different types of messages appear in the chat, and each message has status indicators that tell you about its state.

**Message Types:**
| Type | Appearance | Description |
|---|---|---|
| **User Message** | Display name + avatar + timestamp + text | A regular message sent by a user |
| **System Message** | Centered, muted text, no avatar | Automatic messages like "You joined the chat" |
| **Edited Message** | Shows "(edited)" label next to timestamp | A message that was modified after sending |
| **Deleted Message** | "This message was deleted" placeholder | A message that was removed by the sender |

**Status Icons:**
| Icon | Meaning |
|---|---|
| ✔️ | Message sent successfully |
| **(edited)** | Message was edited after sending |
| **Purple dot** in chat header | Indicates you are in a Direct Message conversation |
| **Green dot** next to name | User is currently online |
| **Gray dot** next to name | User is offline or away |

**Tips:**
- System messages are informational and cannot be replied to or reacted to
- Edited messages keep their original timestamp — the "(edited)" label is the only indicator
- Deleted messages are replaced with a placeholder so the conversation flow is preserved

---

### Status Indicators Reference

**What They Do:** Status indicators show a user's current online presence across the platform.

**Available Statuses:**
| Indicator | Meaning | When It Appears |
|---|---|---|
| **Green dot** | User is currently online and active | User has the site open in any tab or browser |
| **Gray dot** | User is offline or idle | User closed the site, lost connection, or has been inactive |
| **No dot** | User is not a friend (online status is only shown for friends) | Only friends show presence indicators |
| **Custom status text** | User's self-set status message | Set on /profile page (e.g., "Away", "Coding", "Busy") |

**How Presence Tracking Works:**
- When you sign in and visit any page, your presence is registered via a WebSocket connection
- Your presence persists as long as you have at least one browser tab open
- When you close all tabs or navigate away, your presence drops after a short timeout (typically 10–30 seconds)
- Your online status is visible to your friends on all pages, not just the chat page
- You do not see your own green dot (you are filtered out from your own online list)

**Tips:**
- Opening the site in multiple tabs counts as a single session — closing all tabs removes you
- The green dot updates in real time — no need to refresh the page
- Custom status text is separate from online/offline status

---

### Rate Limits & Restrictions

**What They Are:** Limits in place to prevent spam, abuse, and server overload. These apply to all users equally.

**Current Limits:**
| Limit | Value | What Happens If Exceeded |
|---|---|---|
| **Message length** | 500 characters per message | The send button is disabled; shorten your message |
| **Message rate** | 60 messages per 10 seconds | Messages are rejected; wait before sending again |
| **Profile edits** | Once every 3 months | Save button is disabled; a cooldown counter shows remaining time |
| **Session expiry** | 7 days of inactivity | You are signed out and need to sign in again |
| **Friend requests** | Rate-limited to prevent spam | Requests may be temporarily blocked |

**Tips:**
- The 500-character limit is generous — most messages are well under this
- The 60-message rate limit only affects automated spam, not normal conversation
- Profile cooldown prevents abuse of the display name system
- Making any authenticated API call resets the 7-day session timer

---

### Offline & Connection Behavior

**What It Does:** Explains how the site behaves when your internet connection is lost or unstable.

**Connection States:**
| State | Indicator | What Works | What Doesn't Work |
|---|---|---|---|
| **Connected** | - (normal operation) | Everything | - |
| **Reconnecting** | "Reconnecting..." banner at top of chat | Viewing cached messages | Sending messages, reactions, edits |
| **Disconnected** | "Disconnected" banner | Viewing cached messages | All server-dependent features |

**Offline Capabilities:**
- **Cached messages:** Recent messages are stored in your browser's IndexedDB. When offline, you can scroll through previously loaded messages.
- **Theme and settings:** Dark/light mode and chat settings are saved locally and work offline.
- **Sending messages:** **Not possible offline.** Messages require a server connection.

**Reconnection Behavior:**
1. When connection drops, the site automatically attempts to reconnect every 5 seconds
2. Once reconnected, new messages since disconnection are synced from the server
3. Any messages you attempted to send while offline are **not queued** — you need to re-type them
4. Presence status updates automatically — your friends will see you as offline while disconnected

**Tips:**
- If you see "Reconnecting," wait a few seconds — reconnection is usually automatic
- If reconnection fails after 30+ seconds, try reloading the page
- The message cache persists across page refreshes, even when online

---

### Session & Multi-Tab Behavior

**What It Does:** Explains how sessions work across multiple browser tabs and devices.

**Session Basics:**
- Your session is stored in an httpOnly cookie that lasts up to 7 days
- Each browser has its own independent session cookie
- Making API calls (viewing chat, sending messages) resets the 7-day timer

**Multi-Tab Behavior:**
| Scenario | Behavior |
|---|---|
| Same browser, multiple tabs | All tabs share the same session. Opening /chat in a new tab works instantly. |
| Same browser, private/incognito | Separate session — you need to sign in again |
| Different browser on same device | Separate session — you need to sign in again |
| Different device | Separate session — you need to sign in again |
| Sign out on one tab | Only that tab is signed out. Other tabs remain signed in until refreshed. |

**Realtime & Multi-Tab:**
- Messages sent from one tab appear in real time on all other open tabs
- Typing indicators show your activity on all tabs
- Presence (online status) is shared across all tabs — closing all tabs = going offline
- Unread notification badges update in real time across tabs

**Tips:**
- Refreshing a tab never signs you out (the httpOnly cookie persists)
- If you sign out on one tab, refresh other tabs to see the sign-out take effect
- You can be signed in on desktop and mobile simultaneously

---

## Troubleshooting Guide

### Unable to Sign In

**Possible Causes:**
- Google account not selected
- Popup blocker preventing Google One Tap
- Ad blocker interfering with Google's script

**Solution:**
1. Disable ad blockers temporarily and reload
2. Allow popups from the site
3. Try a different browser
4. Check that cookies are enabled in your browser

---

### Message Not Sending

**Possible Causes:**
- Connection issue (Wi-Fi / network)
- Message exceeds 500 character limit
- Spam rate limit (max 60 messages per 10 seconds)

**Solution:**
1. Wait a few seconds and try again
2. Shorten your message
3. Check your internet connection
4. Reload the page

---

### Can't Find a Friend

**Possible Causes:**
- Wrong spelling of name or #ID
- User hasn't signed up yet

**Solution:**
1. Use their exact 6-digit unique ID (e.g., #000042) including the # symbol
2. Try searching by their display name
3. Ask them to sign in first, then search again

---

### Message Not Showing (Muted User)

**Possible Causes:** You previously muted that user.

**Solution:** There is currently no unmute option. Messages from muted users are hidden on your device only.

---

### Profile Save Cooldown

**Possible Causes:** You edited your profile within the last 3 months.

**Solution:** Wait for the cooldown period to expire. The counter shows remaining time (e.g., "2m 14d" means 2 months and 14 days).

---

### Connection Indicator Showing "Reconnecting"

**Possible Causes:** Temporary network interruption.

**Solution:** Wait a moment — the connection should restore automatically. If it persists, check your internet connection.

---

### Chat History Lost

**Possible Causes:**
- Cleared browser data / cookies
- Switched to a different device or browser

**Solution:** The local cache stores recent messages. When you sign in on a new device or after clearing data, recent messages re-sync from the server automatically. Very old messages may not be available.

---

## Questions and Answers

### General Questions

**Q: What is Universal Chat Area?**
A: A privacy-focused realtime community chat platform. Sign in with Google and start chatting instantly with people worldwide.

**Q: What is it used for?**
A: Real-time group chat (#general channel) and private 1-on-1 conversations with friends.

**Q: Who is it for?**
A: Anyone who wants a simple, private, realtime chat experience. No signup forms, no email verification, no tracking.

**Q: Is it free?**
A: Yes, completely free. No paid tiers, no ads, no subscriptions.

**Q: Why should I use it?**
A: One-click Google sign-in, instant message delivery via WebSocket, no tracking, offline message cache, emoji reactions, friend system, and a safe moderated community.

**Q: Do I need to download anything?**
A: No. It's a web app — open your browser and visit the URL. No installation required.

**Q: Does it work on mobile phones?**
A: Yes. The site is fully responsive and works on all devices including phones, tablets, and desktops.

**Q: Which browsers are supported?**
A: Modern versions of Chrome, Firefox, Safari, and Edge. Internet Explorer is not supported.

**Q: Is there an iOS or Android app?**
A: No. The site is designed as a progressive web app for browsers only. You can add it to your home screen on mobile for a near-app experience.

**Q: Can I use multiple accounts?**
A: Each Google account creates one Universal Chat account. To use multiple accounts, sign out and sign in with a different Google account.

---

### Account Questions

**Q: How do I create an account?**
A: Click "Sign In with Google" on the landing page or /auth page. Select your Google account. On first visit, a "Spin Modal" reveals your Unique ID. Click "Start Chatting" when done.

**Q: How do I log in?**
A: Same as creating an account — click "Sign In with Google" and select your account. Your session persists for up to 7 days.

**Q: How do I log out?**
A: Go to /profile and click the red "Sign Out" button.

**Q: How do I update my profile?**
A: Go to /profile, edit your display name, bio, custom status, or avatar, then click "Save Profile". Note: edits are limited to once every 3 months.

**Q: Can I delete my account?**
A: Yes. Go to /profile and click "Delete Account". A double confirmation dialog appears. This is permanent and cannot be undone.

**Q: What happens if I lose access to my Google account?**
A: Since Universal Chat uses Google OAuth for authentication, losing access to your Google account means you cannot sign in. There is no password recovery or alternative login method. Contact the admin through the portfolio form for assistance.

**Q: Can I change my email address?**
A: No. Your email is tied to your Google account and cannot be changed within Universal Chat.

**Q: Can I change my Unique ID?**
A: No. Your Unique ID (#XXXXXX) is permanently assigned on first sign-in and cannot be changed or transferred.

**Q: Can I sign in on multiple devices at the same time?**
A: Yes. Your session is independent per device. You can be signed in on multiple devices or browsers simultaneously.

**Q: Does signing out on one device sign me out everywhere?**
A: No. Each device has its own session cookie. You need to sign out on each device separately.

**Q: What happens to my data if I delete my account?**
A: All your messages, profile data, friend relationships, and reactions are permanently deleted. This cannot be undone. Your messages in other users' DMs will show as "[deleted user]".

**Q: How do I find my Unique ID?**
A: Your Unique ID (#XXXXXX) is displayed on your /profile page and in the sidebar below your name on the chat page.

---

### Feature Questions

**Q: How do I send a message?**
A: Go to /chat, click "Join #general", type in the input bar, and press Enter.

**Q: How do I reply to a message?**
A: Hover over the message and click the Reply icon. A "Replying to [name]" bar appears above the input. Type your reply and send.

**Q: How do I edit a message?**
A: Hover over your own message and click the Edit (pencil) icon. Modify the text, then press Enter to save or Escape to cancel.

**Q: How do I delete a message?**
A: Hover over your own message and click the Delete (trash) icon. The message is permanently removed.

**Q: How do I react to a message?**
A: Click an existing reaction emoji below a message, or click the + button to add a new emoji reaction.

**Q: How do I add emoji to my message?**
A: Click the smiley face button in the message input bar. Select an emoji from the picker.

**Q: How do I find and add friends?**
A: In the sidebar, click the "Find People" icon (user-plus). Search by name or #ID. Click "+" to send a friend request.

**Q: How do I accept a friend request?**
A: In the sidebar, click the Bell icon to open the Friend Request List. Click "Accept" on any pending request.

**Q: How do I reject a friend request?**
A: In the Friend Request List, click the "Reject" button next to the request. The sender will not be notified.

**Q: How do I send a direct message?**
A: Click a friend's name in the Sidebar → Direct Messages list. The chat switches to a private DM conversation.

**Q: How do I return to #general from a DM?**
A: Click the back arrow (←) in the chat header, or click "#general" in the sidebar.

**Q: Can I delete a DM conversation?**
A: No. DM conversations cannot be deleted. You can only delete individual messages you sent.

**Q: How do I search messages?**
A: Press Ctrl+K (or Cmd+K) to open the search overlay, or click the search icon in the chat header. Type your query to filter messages.

**Q: How do I report a message?**
A: Hover over another user's message and click the Flag icon. A report is sent to platform operators.

**Q: How do I mute a user?**
A: Hover over their message and click the Volume-X icon. Their messages are hidden from your view.

**Q: Can I unmute a user?**
A: There is currently no unmute option. Muting is a client-side setting stored in your browser.

**Q: How do I change to dark mode?**
A: Click the Sun/Moon icon in the site header (info pages) or sidebar (chat page).

**Q: Can I send images or files?**
A: No. Universal Chat currently supports text messages and emoji only. Images, files, and voice messages are not supported.

**Q: Can I send formatted text (bold, italic, etc.)?**
A: No. Universal Chat supports plain text only. There is no markdown or rich text formatting.

**Q: Can I share my screen or video call?**
A: No. Universal Chat is a text-based chat platform only. Screen sharing and video calls are not supported.

**Q: Can I create my own chat room?**
A: No. The platform has a single #general community channel plus private DMs. Custom rooms are not available.

**Q: Can I block a user?**
A: There is no block feature. You can mute a user to hide their messages from your view.

**Q: How do I copy a message?**
A: Hover over any message and click the Copy icon. The message text is copied to your clipboard.

**Q: Can I see when a message was edited?**
A: Edited messages show an "(edited)" label. The original timestamp is preserved.

---

### Navigation Questions

**Q: Where can I find the chat?**
A: The chat is at /chat. You can also click "Join Chat" in the site header or "Chat" in the navigation menu.

**Q: How do I return to the homepage?**
A: Click "Universal Chat" logo in the header, or use the "Home" link in the sidebar or navigation.

**Q: Where are my settings?**
A: Chat settings (enter-to-send, font size, density) are in the chat page — click the gear icon in the header. Profile settings are at /profile.

**Q: Where can I see my Unique ID?**
A: Your #ID is shown on your /profile page and in the sidebar below your name.

---

### Mobile Questions

**Q: Does this work on mobile?**
A: Yes. The site is fully responsive and works on phones and tablets.

**Q: Can I use it on tablets?**
A: Yes, the layout adapts for all screen sizes.

**Q: How do I open the sidebar on mobile?**
A: Tap the hamburger menu (three lines) icon in the mobile header.

---

### Troubleshooting Questions

**Q: Why can't I sign in?**
A: Check that popups aren't blocked, ad blockers are disabled, and cookies are enabled. Try a different browser or reload the page.

**Q: Why isn't my message showing?**
A: Your message may exceed the 500-character limit, or you may have hit the rate limit (60 messages per 10 seconds). Check your connection and try again.

**Q: Why can't I find my friend?**
A: Make sure you're searching by their exact display name or #ID. They need to have signed in at least once.

**Q: Why can't I edit my profile?**
A: Profile edits are limited to once every 3 months. Check if a cooldown counter is showing on your profile page.

**Q: Why is the connection showing as disconnected?**
A: This usually means a temporary network interruption. It should reconnect automatically within a few seconds.

---

### Contact Questions

**Q: How do I contact support?**
A: Visit the /contact page and click the portfolio link to send a message directly.

**Q: How do I contact Samuvel?**
A: Visit the /contact page and use the portfolio link. This is the primary and most reliable method to reach the admin.

**Q: Where can I report a problem?**
A: You can report problematic messages in-chat using the Flag button on any message, or visit the /contact page.

**Q: Is there live chat support?**
A: No. The community /chat is for general conversation, not official support. For direct admin contact, use the portfolio form.

**Q: How quickly will I get a response?**
A: Typically within 24–48 hours via the portfolio contact form. In-chat reports are reviewed during active moderation sessions.

**Q: What information should I include when reporting?**
A: Your Unique ID (#XXXXXX), a clear description of the issue, steps to reproduce (if a bug), and any relevant screenshots.

**Q: Can I get support by email or phone?**
A: No. All communication is through the portfolio contact form or in-chat reports. There is no email, phone, or social media support.

### Admin & Platform Questions

**Q: Who made this site?**
A: The platform is created and maintained by Samuvel, an independent developer.

**Q: Where can I learn more about the developer?**
A: Visit the portfolio at https://portfolio-beta-sam.vercel.app

**Q: Is the source code available?**
A: The source code is private and not publicly available.

**Q: How can I suggest a feature?**
A: Contact the admin through the portfolio contact form with your suggestion. Feature requests are reviewed periodically.

**Q: How do I report a bug?**
A: Contact the admin through the portfolio form with a description of the bug, steps to reproduce, and your browser/device info.

**Q: Are there plans to add new features?**
A: The platform is actively maintained. New features are considered based on user feedback and feasibility. See the Known Limitations section for what's not currently planned.

**Q: How do I become a moderator?**
A: Moderators are selected by the admin. There is no public application process.

**Q: How are moderation decisions made?**
A: Reported messages are reviewed by the admin or moderators. Actions may include warnings, message removal, or account suspension based on severity and history.

**Q: Can I appeal a moderation action?**
A: Contact the admin through the portfolio form to discuss moderation decisions.

---

## Quick Answers

**Q: How do I create an account?**
A: Click "Sign In with Google" on the landing page or /auth page. Select your Google account to sign in instantly.

**Q: How do I log in?**
A: Click the Google sign-in button and select your account. No password needed.

**Q: How do I log out?**
A: Go to /profile and click the red "Sign Out" button.

**Q: How do I send a message?**
A: Join #general on the /chat page, type in the input bar, and press Enter.

**Q: How do I reply to a message?**
A: Hover the message and click the Reply icon.

**Q: How do I edit my message?**
A: Hover your message and click the pencil icon.

**Q: How do I delete my message?**
A: Hover your message and click the trash icon.

**Q: How do I add a friend?**
A: Click the user-plus icon in the sidebar's Friends section, search by name or #ID, and click "+".

**Q: How do I start a DM?**
A: Click a friend's name in the Sidebar → Direct Messages list.

**Q: How do I search messages?**
A: Press Ctrl+K (or Cmd+K) to open the search overlay.

**Q: How do I change to dark mode?**
A: Click the Sun/Moon icon in the header or sidebar.

**Q: How do I update my profile?**
A: Go to /profile, edit your fields, and click "Save Profile".

**Q: How do I find my Unique ID?**
A: Check your /profile page or the sidebar — it's shown as #XXXXXX.

**Q: How do I contact support?**
A: Visit /contact and use the portfolio link.

**Q: Is it free?**
A: Yes, completely free with no paid tiers.

**Q: Does it work on mobile?**
A: Yes, fully responsive on phones and tablets.

**Q: How do I report a message?**
A: Hover the message and click the Flag icon.

**Q: How do I mute a user?**
A: Hover their message and click the Volume-X icon.

**Q: Why can't I edit my profile?**
A: Profile edits are allowed once every 3 months. Check the cooldown on your profile page.

**Q: Does my chat history persist?**
A: Yes, recent messages are cached in your browser and re-sync from the server when you return.

---

## Platform Information

### Technical Architecture

**Overview:** Universal Chat Area is a modern web application built with a React frontend and serverless backend, powered by Supabase for database and realtime functionality.

**Frontend Stack:**
| Technology | Purpose |
|---|---|
| **React 19** | UI framework for building the user interface |
| **TypeScript** | Type-safe JavaScript for better code quality |
| **Vite** | Build tool and development server |
| **Tailwind CSS** | Utility-first CSS framework for styling |
| **React Router** | Client-side routing between pages |
| **Supabase JS Client** | Realtime subscriptions and database queries |

**Backend Stack:**
| Technology | Purpose |
|---|---|
| **Vercel Serverless Functions** | API endpoints (/api/auth/*, /api/messages, etc.) |
| **Supabase Postgres** | Primary database storing users, messages, reactions, friends |
| **Supabase Realtime** | WebSocket-based realtime message delivery and presence |
| **Google OAuth 2.0** | Authentication via Google sign-in |

**How Data Flows:**
1. **Messages:** When you send a message, it goes to a Vercel API endpoint → Supabase database → broadcast via Realtime WebSocket to all connected clients
2. **Authentication:** Google sign-in → JWT token issued → stored in httpOnly cookie → verified on each API request
3. **Presence:** Your browser maintains a WebSocket connection to Supabase Realtime → your status is broadcast to friends
4. **DMs:** Messages are stored in the same database with a `conversation_id` → fetched via polling (every 2 seconds) since DMs use a different channel than #general

**Hosting:**
- **Frontend:** Vercel (Edge Network)
- **Database:** Supabase (Postgres)
- **Auth:** Google OAuth + custom JWT
- **Domain:** universal-chat-area.vercel.app

**Performance Notes:**
- Messages deliver in under 100ms via WebSocket in #general
- DM messages poll every 2 seconds (slightly slower than realtime)
- Message cache in IndexedDB provides instant loading on return visits
- Static pages (FAQ, About, Privacy) load instantly with no server round-trip

---

### Accessibility

**Current State:** Universal Chat Area includes basic accessibility features with room for improvement.

**Implemented:**
- **Keyboard navigation:** All interactive elements are reachable via Tab key
- **ARIA labels:** Buttons and controls have descriptive labels for screen readers
- **Focus management:** Modals, overlays, and search trap focus
- **Color contrast:** Both dark and light modes meet WCAG AA contrast ratios
- **Responsive design:** Works on all screen sizes from 320px upwards
- **Reduced motion:** The site respects `prefers-reduced-motion` OS setting — animations are disabled when the user prefers reduced motion

**Known Gaps:**
- **Screen reader optimization:** Some dynamic chat content (new messages appearing) may not be announced by screen readers
- **Skip-to-content link:** Not implemented
- **ARIA live regions:** Chat area could benefit from aria-live regions for new message announcements
- **Touch targets:** Some small icons (reactions, message actions) may be hard to tap on mobile

**Tips for Accessibility:**
- Use Tab and Shift+Tab to navigate between elements
- Use Enter to activate buttons and links
- Use Escape to close modals, overlays, and cancel edits
- Ctrl+K opens message search without using the mouse
- Dark mode may be easier on the eyes for users with light sensitivity

---

### Known Limitations

**What's Not Currently Supported:**

**Messaging & Chat:**
- No image, file, or video sharing (text + emoji only)
- No message formatting (bold, italic, code blocks, links)
- No voice messages or video calls
- No group DMs (only 1-on-1 direct messages)
- No chat rooms beyond #general and DMs
- No message pinning or starring
- No read receipts (you cannot see if someone read your message)
- DM typing indicators are not implemented
- DM messages use polling (2-second delay) instead of realtime WebSocket

**Friends & Users:**
- No block feature (only mute, which is client-side)
- No unmute option (once muted, it's permanent on your device)
- No friend removal (can't unfriend someone)
- No online status for non-friends
- Cannot change your Unique ID (#XXXXXX is permanent)

**Account & Profile:**
- No email/password login (Google only)
- No email notifications
- No password reset (uses Google OAuth)
- No profile edit history
- No export your data feature
- Profile edits limited to once every 3 months

**Platform:**
- No mobile app (browser-only progressive web app)
- No desktop app
- No API for third-party integrations
- No embeddable chat widget
- No end-to-end encryption (messages are encrypted in transit via HTTPS/TLS)
- No message history beyond what's cached locally (very old messages may not load)

**If you need any of these features,** contact the admin through the portfolio form. Feature requests are reviewed periodically, but there are no guarantees about implementation timelines.

---

## Contact Information

### General Contact

- **Contact Page:** /contact
- **Portfolio:** https://portfolio-beta-sam.vercel.app
- **Community Chat:** /chat (for community help)
- **FAQ:** /faq (for quick answers)

### Contacting the Admin (Samuvel)

The platform is developed and maintained by **Samuvel**.

**How to reach the admin:**
1. **Portfolio Contact Form:** Visit https://portfolio-beta-sam.vercel.app and use the contact form — this is the primary and most reliable method
2. **In-Chat Report:** Use the Flag button on any message to report issues directly to the admin (best for content moderation concerns)
3. **Community Help:** Ask in /chat — other users or the admin may respond

**What to include when contacting:**
- A clear description of the issue or question
- Your Unique ID (#XXXXXX) if reporting an account issue
- Steps to reproduce if reporting a bug
- Screenshots if relevant

**Response time:** Typically within 24–48 hours via the portfolio form. In-chat reports are reviewed during active moderation sessions.

**Note:** There is no phone number, live chat support, or social media support channel. All communication is through the methods listed above.

---

## Data & Privacy

- **Authentication:** Google OAuth only. No passwords stored by the platform.
- **Data Stored:** Messages (text, sender ID, timestamp), profile info (display name, bio, avatar), friend relationships.
- **Not Stored:** IP addresses, location data, device fingerprints, browsing history, tracking pixels.
- **Local Cache:** Messages are cached in your browser's IndexedDB for offline access and fast loading.
- **Cookies:** An httpOnly cookie stores your session token (expires in 7 days). No tracking cookies.
- **Account Deletion:** All your data can be permanently deleted from /profile → Delete Account.
- **Third Parties:** Supabase (database + realtime), Google (authentication only).

---

## Website Summary

### One Sentence Description

Universal Chat Area is a privacy-focused realtime community chat platform where anyone can sign in with Google and chat instantly with people worldwide — no signup forms, no tracking, and no paid tiers.

### Short Summary (50–100 words)

Universal Chat Area is a free, privacy-first realtime chat platform. Sign in with a single Google click, join the #general community chat, or DM friends privately. Messages deliver in under 100ms via WebSocket, are cached locally for offline access, and are stored securely. Features include emoji reactions, message editing/deletion, user reporting and muting, a friends system with searchable #IDs, dark mode, and customizable chat settings. Built with React, TypeScript, and Supabase, it runs on all devices with zero tracking and no data collection.

### Detailed Summary (300–500 words)

Universal Chat Area is a modern realtime communication platform designed with privacy and simplicity as its core principles. Unlike traditional chat apps that require lengthy registration forms, email verification, and phone number confirmation, Universal Chat enables instant access through Google OAuth — one click and you're in.

Upon first sign-in, each user receives a permanent, unique 6-digit identifier (e.g., #000042) that friends can use to find and connect with them. This ID is revealed through an animated "Spin Modal" slot-machine experience, making onboarding both fun and functional.

The chat experience is built on Supabase Realtime technology, delivering messages in under 100 milliseconds via persistent WebSocket connections. The #general channel serves as the main community hub where all signed-in users can converse in real time. For private conversations, the integrated friends system allows users to search for others by name or #ID, send and receive friend requests, and then open private Direct Message (DM) threads.

Every message supports rich features: emoji reactions with a quick-picker, inline replies that create threaded conversations, full editing and deletion of your own messages, and copy-to-clipboard. Users can report inappropriate messages to moderators or mute individual users client-side to hide their content.

Privacy is baked into every layer. No IP addresses, location data, or device fingerprints are collected or stored. Messages are persisted in an encrypted database for realtime delivery and moderation, and are also cached locally in IndexedDB so your chat history survives page refreshes and brief network interruptions. The session is maintained via an httpOnly cookie that automatically expires after 7 days of inactivity — no tracking cookies, no third-party analytics scripts, and no advertising.

Profile customization includes a display name, bio, custom status, and randomly generated avatar — all editable once every 3 months to prevent abuse. Dark and light themes, adjustable font sizes, and compact or comfortable message density are available in the chat settings.

Built with React 19, TypeScript, and Tailwind CSS, the platform is fully responsive and works seamlessly on desktop, tablet, and mobile browsers. The codebase runs on Vercel's edge network with a Supabase Postgres database and realtime engine powering the backend.

### Key Features List

- One-click Google sign-in — no passwords, no verification
- Realtime #general community chat with sub-100ms delivery
- Private Direct Messages with friends
- Friends system: search by name or #ID, send/accept requests
- Emoji reactions with quick-picker on every message
- Message reply, edit, delete, copy, report, and mute
- Message search via Ctrl+K overlay
- Chat settings: enter-to-send, font size, message density
- Dark and light theme toggle
- Profile editing: display name, bio, custom status, avatar
- Permanent unique #ID for friend discovery
- Offline message cache via IndexedDB
- Profanity filter and rate limiting for safe chat
- Fully responsive on desktop, tablet, and mobile
- Free — no paid tiers, no ads, no tracking

### Target Audience

- **Privacy-conscious users** who want to chat without being tracked
- **Casual chatters** who dislike lengthy signup processes
- **Community builders** looking for a simple, free realtime chat
- **Developers and tech enthusiasts** who appreciate modern web technology
- **Digital nomads** who need persistent chat across sessions and devices
- **Anyone** who wants a quick, no-friction way to connect with people online
