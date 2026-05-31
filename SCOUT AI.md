# SCOUT AI

## Website Overview

SCOUT AI is a personal AI assistant built by Sam (Samuvel). It acts as a conversational guide that helps people understand Sam's projects — what they do, how they work, and how to use them. You talk to it through a chat interface, and it answers based on knowledge documents that Sam has written about each project.

SCOUT stands for **Sam's Conversational Oracle for Understanding Tech**.

---

## Purpose

SCOUT AI exists to answer questions about Sam's creative and technical work. Instead of reading through documentation or exploring projects on your own, you can simply ask SCOUT and get a clear, human-like answer.

It also serves as a showcase of modern web development — built with React, TypeScript, and powered by Google's Gemini AI.

---

## Who Is This For?

- **Visitors and recruiters** who want to learn about Sam's projects
- **Users of Sam's apps** who need help or have questions
- **Developers and designers** curious about Sam's technical work
- **Anyone** who wants to know what Sam has built and how it works

---

## Main Features

| Feature | Purpose | Benefit | Where to Find It |
|---------|---------|---------|------------------|
| **Chat Interface** | Ask questions and get answers | Natural conversation, no searching needed | Main screen after clicking "Start a Conversation" |
| **Knowledge Base** | Project info fetched from GitHub documents | Always up-to-date, covers multiple projects | Loaded automatically when you chat |
| **Quick Reply Buttons** | Suggested topics to ask about | One-click questions, no typing needed | Below each SCOUT response |
| **Copy Message** | Copy any response to clipboard | Save info or share it elsewhere | Hover over a message → Copy icon |
| **Export Chat** | Download entire conversation as a file | Keep a record of your session | Header toolbar → Download icon |
| **Clear Chat** | Delete all messages and start fresh | Privacy, clean slate | Header toolbar → Trash icon |
| **Retry on Error** | Re-send your last question if something went wrong | Recover from failures easily | Hover over the error message → Retry icon |
| **Delete Message** | Remove a single message from chat | Correct mistakes, remove sensitive info | Hover over any message → Delete icon |
| **Dark / Light Mode** | Toggle between themes | Comfortable viewing in any lighting | Header toolbar → Sun/Moon icon |
| **Rate Limit Cooldown** | Shows countdown when you need to wait | Knows exactly when you can try again | Appears automatically in the input bar |
| **Code Highlighting** | Displays code in color-coded blocks | Easy to read and copy code snippets | Automatically when SCOUT responds with code |
| **Knowledge File Indicator** | Shows how many knowledge files are loaded | Transparency about what info SCOUT has | Header toolbar |
| **Refresh Knowledge** | Reload latest documents from GitHub | Get updated info without waiting for cache | Header toolbar → Refresh icon |
| **Clear Knowledge** | Remove all loaded knowledge | Force SCOUT to fetch fresh on next question | Header toolbar → X icon |

---

## Website Structure

SCOUT AI is a single-page application — everything happens on one page without navigating to different URLs.

### Layout

The page is split into three areas:

**Header** (top bar):
- SCOUT AI logo and "Personal Assistant" label
- Green pulsing dot indicating the AI is ready
- Knowledge file count (shows how many files are loaded)
- Action buttons: Refresh Knowledge, Clear Knowledge, Export Chat, Clear Chat, Dark Mode Toggle

**Main Content** (center):
- **Landing screen** (when no chat has started): SCOUT AI logo animated, "Start a Conversation" button, three feature badges (Instant Response, Privacy First, Made with Care), and "Powered by Google's Gemini AI" footer
- **Chat view** (after starting): Messages displayed in a scrollable list. Your messages appear on the right, SCOUT AI's messages on the left. Below the last message, quick reply buttons appear.

**Input Bar** (bottom):
- A text area where you type your question
- A Send button (or Stop button when SCOUT is responding)
- A character counter showing how many characters you've typed

### No Logins or Accounts

There are no sign-in, sign-up, or profile pages. Anyone can use SCOUT AI immediately by visiting the website.

---

## Complete User Journeys

### Landing Journey — First Visit

#### Step 1 — Arrive at the Site

**What the user sees**

A dark (or light) screen with a large animated SCOUT AI logo in the center. Below it, "SCOUT AI" in bold text with "AI" faded. The subtitle reads: "Sam's Conversational Oracle for Understanding Tech. Ask me anything about Samuvel's projects, skills, or creative journey."

Three badges are shown at the bottom: "Instant Response", "Privacy First", and "Made with Care". At the very bottom: "Powered by Google's Gemini AI".

The top bar shows "SCOUT AI — Personal Assistant" with a green pulsing dot.

**What the user does**

Reads the description.

**What happens**

The page is ready for interaction. The user can scroll or interact with the "Start a Conversation" button.

---

#### Step 2 — Start a Conversation

**What the user sees**

A large card with a sparkle icon and "Start a Conversation" heading. Below it: "I'd love to share Samuvel's creative work and professional journey with you." A "Get Started" button with an animated arrow.

**What the user does**

Clicks the "Start a Conversation" card or button.

**What happens**

A welcome message from SCOUT AI appears: "Hey! I'm SCOUT — Sam's Conversational Oracle for Understanding Tech. Ask me anything about his projects..." The chat view is now active.

---

### Sending a Message Journey

#### Step 1 — Type Your Question

**What the user sees**

A text input at the bottom of the screen with the placeholder: "Feel free to ask me anything about Samuvel's work..."

**What the user does**

Types a question (e.g. "What projects has Sam built?") into the text area. The Send button changes from gray (disabled) to active (dark/colored).

**What happens**

A character counter appears showing the count as you type. The text area expands automatically if you type more than one line.

---

#### Step 2 — Send the Message

**What the user does**

Presses Enter on the keyboard (without holding Shift), or clicks the Send button.

**What happens**

Your message appears as a bubble on the right side. A typing indicator shows: "SCOUT AI... typing" with three bouncing dots. When the response arrives, it appears as a bubble on the left side with the SCOUT AI label and icon. Quick reply buttons appear below the response.

---

#### Step 3 — Interact with the Response

**What the user sees**

The response may contain formatted text, links (in blue), code blocks (with syntax highlighting), and bullet points.

**What the user does**

- **Copy**: Hover over the message → click the Copy icon
- **Ask a follow-up**: Click a quick reply button or type a new question
- **Retry**: If the message shows an error, hover and click the Retry icon

**What happens**

The selected action is performed immediately.

---

### Handling Rate Limits Journey

#### Step 1 — Get Rate Limited

**What the user sees**

An error toast appears at the bottom: "AI is temporarily rate limited. Try again in X seconds." The text input is disabled and shows "Quota cooldown — Xs" with a countdown number.

**What the user does**

Waits for the countdown to reach zero.

**What happens**

The countdown decreases by 1 every second. When it reaches 0, the input becomes active again and the placeholder returns to normal.

---

#### Step 2 — Retry After Cooldown

**What the user sees**

The input is active again. The error message has disappeared (it auto-dismisses after 5 seconds).

**What the user does**

Types their question again and sends it.

**What happens**

The message is sent and a new response is generated.

---

### Exporting Chat Journey

**What the user sees**

In the header toolbar, a Download icon button.

**What the user does**

Clicks the Download icon. A file downloads automatically.

**What happens**

The entire conversation is saved as a Markdown (.md) file named `scout-chat-YYYY-MM-DD.md`. Each message shows who said it, the timestamp, and the content.

---

### Clearing Chat Journey

**What the user sees**

In the header toolbar, a Trash icon button.

**What the user does**

Clicks the Trash icon.

**What happens**

All messages are deleted. The screen returns to the landing page with the "Start a Conversation" button. The chat history is permanently removed.

---

### Dark Mode Toggle Journey

**What the user sees**

In the header toolbar, a Sun icon (if currently in dark mode) or a Moon icon (if currently in light mode).

**What the user does**

Clicks the Sun/Moon icon.

**What happens**

The entire page transitions to the opposite theme over 0.5 seconds. All backgrounds, text colors, and element styles change. The choice is remembered even if you close and reopen the page.

---

### Using Quick Replies Journey

**What the user sees**

Below the latest SCOUT response, small pill-shaped buttons appear with suggested topics: "Tell me more", "Show all projects", "What can you help with?", "Visit Portfolio".

**What the user does**

Clicks any of the pill buttons.

**What happens**

The button text is sent as a new message, and SCOUT responds appropriately.

---

## Feature Documentation

### Chat Interface

**What It Does**

The main feature — you type a question and SCOUT AI responds with an answer based on Sam's project knowledge.

**How To Access It**

Click "Start a Conversation" on the landing page, or if you've already chatted, just use the text input at the bottom.

**How To Use It**

1. Type your question in the text area at the bottom
2. Press Enter (or click the Send button)
3. Wait for the response
4. Read, copy, or follow up

**Common Use Cases**

- "What projects has Sam built?"
- "Tell me about [project name]"
- "How do I use [project feature]?"
- "What tech stack does [project] use?"

**Tips**

- You can use Shift+Enter to add a new line without sending
- The input accepts up to 4,000 characters
- Responses include clickable links and highlighted code blocks

**Common Problems**

- **No response**: The AI might be rate limited. Wait for the cooldown or try again later.
- **Slow response**: Large responses with code or links may take a few seconds.

**Solutions**

- Check the error toast message at the bottom of the screen
- If you see a cooldown timer, wait for it to finish
- Try rephrasing your question

---

### Knowledge Base

**What It Does**

SCOUT AI reads markdown files from a public GitHub repository to learn about Sam's projects. Each file covers one project with details about its features, usage, and purpose.

**How To Access It**

It loads automatically — you don't need to do anything. The header shows how many files are currently loaded (e.g. "2 files").

**How To Use It**

Just ask questions naturally. If the knowledge covers your question, SCOUT will answer with specific details. If not, SCOUT will say it doesn't have that information.

**Tips**

- You can click the Refresh icon in the header to reload the latest files
- You can click the X icon to clear loaded knowledge (forces SCOUT to fetch fresh files on the next question)

**Common Problems**

- **SCOUT says "I don't have that detail"**: The question isn't covered in the loaded documents
- **Zero files showing**: Knowledge hasn't loaded yet — try refreshing

**Solutions**

- Knowledge files are managed by Sam — new information is added by creating markdown files in the GitHub repository
- If you need info about a project not covered, reach out to Sam directly

---

### Export Chat

**What It Does**

Downloads your entire conversation as a Markdown file to your computer.

**How To Access It**

Click the Download icon in the header toolbar.

**How To Use It**

1. Have at least one message in the chat
2. Click the Download icon
3. Open the downloaded `.md` file in any text editor

**Tips**

- The file is timestamped so you can track when the conversation happened
- Messages include timestamps and sender labels

---

### Clear Chat

**What It Does**

Removes all messages from the current session and returns to the landing screen.

**How To Access It**

Click the Trash icon in the header toolbar.

**How To Use It**

1. Click the Trash icon
2. All messages are removed immediately (no confirmation dialog)
3. The page returns to the start screen

**Tips**

- Export your chat before clearing if you want to keep the conversation
- There is no undo — once cleared, messages are gone

---

### Dark Mode

**What It Does**

Switches the entire interface between light and dark color schemes.

**How To Access It**

Click the Sun (dark mode) or Moon (light mode) icon in the header toolbar.

**How To Use It**

Click the icon — it toggles between themes instantly.

**Tips**

- Your preference is saved automatically and persists across visits
- The transition is smooth and animated (500ms)

---

### Code Highlighting

**What It Does**

When SCOUT responds with code, it's displayed in a formatted block with a colored background, line numbers, and a language label.

**How To Access It**

Automatically appears whenever SCOUT includes code in a response.

**How To Use It**

- Click the Copy button in the top-right of any code block to copy the code
- Use the scrollbar to view longer code blocks

**Tips**

- Supported languages include JavaScript, TypeScript, Python, HTML, CSS, JSON, and more
- Line numbers help you reference specific lines

---

## Troubleshooting Guide

### Unable to Send a Message

**Possible Causes**

- A rate limit cooldown is active
- The input is empty
- You've exceeded the 4,000 character limit
- A response is currently being generated

**Solution**

- Wait for any cooldown timer to reach zero
- Type something in the input
- Reduce your message length
- Wait for the current response to finish

---

### Response Shows an Error

**Possible Causes**

- The AI service is temporarily unavailable
- Daily AI quota has been exceeded
- Network connectivity issues
- The request timed out

**Solution**

- Hover over the error message and click the Retry icon
- Wait a few seconds and try again
- Check your internet connection
- If the problem persists, try again later

---

### Rate Limited

**Possible Causes**

- Too many requests sent in a short time
- Daily AI usage quota has been reached

**Solution**

- Wait for the countdown timer shown in the input bar
- The timer counts down automatically — no need to refresh
- Once the timer reaches 0, you can send messages again
- If you see "Daily quota exhausted", wait until the next day or ask Sam to switch API keys

---

### Response is Empty

**Possible Causes**

- The AI generated an empty response
- The request was interrupted

**Solution**

- Click the Retry icon on the last response to re-send your question
- Try rephrasing your question

---

### Knowledge is Missing

**Possible Causes**

- Knowledge files haven't loaded yet
- The question isn't covered by any loaded file
- Knowledge was cleared

**Solution**

- Check the header to see if files are loaded (e.g. "2 files")
- Click the Refresh icon to reload
- If files show 0 after refresh, the GitHub repository may be empty or unreachable

---

## Questions and Answers

### General Questions

**Q: What is SCOUT AI?**

A: SCOUT AI stands for Sam's Conversational Oracle for Understanding Tech. It's a personal AI assistant built by Sam (Samuvel) that answers questions about his projects. You can ask it anything about what Sam has built, how his apps work, and how to use them.

---

**Q: Who built SCOUT AI?**

A: SCOUT AI was built by Sam (Samuvel), a creative developer and digital builder. It's one of his projects that showcases modern AI-powered web applications.

---

**Q: Is SCOUT AI free to use?**

A: Yes, SCOUT AI is completely free to use. There are no paywalls, subscriptions, or sign-up fees.

---

**Q: What technology powers SCOUT AI?**

A: SCOUT AI is powered by Google's Gemini AI model (Gemini 2.5 Flash). The frontend is built with React, TypeScript, Tailwind CSS, and Framer Motion. It runs as a serverless application on Vercel.

---

**Q: Why would I use SCOUT AI?**

A: If you want to learn about Sam's projects, understand how they work, or get help using them, SCOUT AI provides quick, conversational answers without needing to search through documentation.

---

**Q: How does SCOUT AI get its knowledge?**

A: SCOUT AI reads markdown files from a public GitHub repository owned by Sam. Each file contains information about a specific project. When you ask a question, SCOUT searches through the loaded knowledge and generates an answer.

---

### Using the Chat

**Q: How do I start a conversation?**

A: Click the "Start a Conversation" button on the landing page. A welcome message from SCOUT will appear, and you can begin typing your questions.

---

**Q: How do I send a message?**

A: Type your question in the text area at the bottom of the screen and press Enter, or click the Send button (the arrow icon).

---

**Q: How do I add a new line without sending?**

A: Press Shift+Enter to insert a new line in your message without sending it.

---

**Q: How do I copy a response?**

A: Hover over any message and click the Copy icon (two overlapping squares). The icon will briefly turn into a green checkmark to confirm.

---

**Q: How do I delete a message?**

A: Hover over the message you want to delete and click the Trash icon. The message is removed immediately.

---

**Q: How do I retry a failed response?**

A: If a response shows an error, hover over it and click the Retry icon (circular arrows). Your last question will be re-sent.

---

**Q: How do I clear the entire chat?**

A: Click the Trash icon in the header toolbar. All messages will be deleted and the page returns to the start screen.

---

**Q: How do I export my conversation?**

A: Click the Download icon in the header toolbar. A Markdown file containing the full conversation will be downloaded to your computer.

---

### Knowledge and Content

**Q: How do I add new knowledge?**

A: Knowledge is managed by Sam. He creates markdown files in the public GitHub repository. You cannot add knowledge yourself, but you can ask Sam to include new information.

---

**Q: How do I refresh the knowledge?**

A: Click the Refresh icon in the header toolbar near the file count. This reloads the latest files from the GitHub repository.

---

**Q: Why does SCOUT say "I don't have that detail"?**

A: The information you're asking about isn't covered in the loaded knowledge files. SCOUT can only answer based on what Sam has written in the documents.

---

**Q: What projects does SCOUT know about?**

A: This depends on what files are currently loaded. Check the header — it shows the number of files loaded. The specific files include projects like Universal Chat Area and Special Wishes, and can be expanded by Sam at any time.

---

### Theme and Display

**Q: How do I switch to dark mode?**

A: Click the Sun icon (when in dark mode) or Moon icon (when in light mode) in the header toolbar. The theme switches immediately and your preference is remembered.

---

**Q: Does SCOUT AI work on mobile?**

A: Yes, the interface is responsive and works on phones and tablets. The text area and buttons are sized for touch interaction.

---

**Q: Can I see code examples from SCOUT?**

A: Yes. When SCOUT responds with code, it's displayed in a formatted block with syntax highlighting, line numbers, and a copy button.

---

### Errors and Troubleshooting

**Q: Why can't I send a message?**

A: There are a few possible reasons: a rate limit cooldown is active (wait for the timer), you haven't typed anything, your message exceeds 4,000 characters, or SCOUT is currently generating a response.

---

**Q: Why do I see "AI is temporarily rate limited"?**

A: This means too many requests were sent in a short time. A countdown will show how long you need to wait. The input will become active again automatically once the cooldown ends.

---

**Q: Why is SCOUT not responding?**

A: Check the error message at the bottom. It could be a rate limit, a network issue, or a temporary service disruption. Try waiting a moment and sending your question again.

---

**Q: The page shows "Something went wrong" — what do I do?**

A: This is the error boundary. Click the "Reload Application" button to refresh the page. If it happens repeatedly, clear your browser cache and try again.

---

**Q: Does SCOUT AI need an account or login?**

A: No. SCOUT AI is open to everyone without any sign-in, registration, or authentication.

---

## Quick Answers

**Q: What is SCOUT AI?**
A: An AI assistant built by Sam that answers questions about his projects.

**Q: Who built it?**
A: Sam (Samuvel), a creative developer and digital builder.

**Q: Is it free?**
A: Yes, completely free. No sign-up required.

**Q: How do I start?**
A: Click "Start a Conversation" on the landing page.

**Q: How do I send a message?**
A: Type in the text area and press Enter.

**Q: How do I copy a response?**
A: Hover over the message and click the Copy icon.

**Q: How do I export my chat?**
A: Click the Download icon in the toolbar.

**Q: How do I clear the chat?**
A: Click the Trash icon in the toolbar.

**Q: How do I switch themes?**
A: Click the Sun/Moon icon in the toolbar.

**Q: What if I get rate limited?**
A: Wait for the countdown timer — it shows exactly when you can try again.

**Q: What if SCOUT gives an error?**
A: Hover over the error and click the Retry icon.

**Q: How does SCOUT know about projects?**
A: It reads markdown files from Sam's public GitHub repository.

**Q: Can I add knowledge?**
A: Only Sam can add knowledge by creating files in the GitHub repository.

**Q: Do I need an account?**
A: No, no login or sign-up needed.

**Q: How do I contact Sam?**
A: Visit his portfolio website or reach out through his GitHub profile.

---

## Contact Information

SCOUT AI is a project by Samuvel (Sam).

- **Portfolio**: [https://samuvel.vercel.app](https://samuvel.vercel.app) (shown in quick replies as "Visit Portfolio")
- **GitHub**: [https://github.com/samuvel784](https://github.com/samuvel784)
- **SCOUT AI app**: Hosted on Vercel

---

## Data & Privacy

- **No accounts required**: You can use SCOUT AI without signing in or providing any personal information
- **No tracking or analytics**: The app does not use analytics scripts, tracking pixels, or cookies for advertising
- **Messages stay in your browser**: Chat history is saved locally using localStorage — it doesn't leave your device
- **No data selling**: Your conversations are never sold or shared with third parties
- **Knowledge source is public**: SCOUT reads from a public GitHub repository — the same files are visible to everyone
- **AI service**: Google's Gemini API processes your questions to generate responses. This is the only external service involved
- **Export control**: You can export your data anytime (Download icon) or clear it entirely (Trash icon)
- **Open source**: The codebase is public on GitHub for transparency

---

## Website Summary

### One Sentence Description

SCOUT AI is a personal AI assistant that answers questions about Samuvel's projects using conversational chat powered by Google's Gemini AI.

### Short Summary

SCOUT AI (Sam's Conversational Oracle for Understanding Tech) is a free, no-login AI assistant built by Samuvel. It helps people learn about his projects by answering questions in a natural chat interface. Knowledge is loaded from markdown files in a public GitHub repository, and the app is built with React, TypeScript, and Tailwind CSS. Features include dark mode, chat export, message copying, code highlighting, and automatic retry on errors. No accounts, no tracking, and no data collection.

### Detailed Summary

SCOUT AI is a conversational AI assistant created by Sam (Samuvel) to help people understand his creative and technical projects. It uses a chat-based interface where users can ask questions naturally and receive detailed, accurate answers based on knowledge documents that Sam maintains.

The frontend is a single-page React application styled with Tailwind CSS and animated with Framer Motion. It runs as a serverless application and uses Google's Gemini AI model to generate responses. Knowledge is loaded on demand from a public GitHub repository containing markdown files that describe each project in detail.

Key features include a full chat interface with message history, copy and delete controls, export to Markdown, dark/light mode toggle, and automatic rate limit handling with a visible countdown timer. Code responses are displayed with syntax highlighting and line numbers.

SCOUT AI is designed with privacy in mind — there are no user accounts, no sign-up forms, no tracking scripts, and no data collection. Chat history is stored locally in the browser and can be exported or cleared at any time. The application is open source.

### Key Features List

- Chat-based AI assistant powered by Google Gemini
- Knowledge loaded from GitHub repository (always up-to-date)
- Dark and light mode themes
- Export conversations to Markdown files
- Copy individual responses to clipboard
- Delete individual messages
- Retry failed responses
- Clear entire chat history
- Quick reply buttons for one-click questions
- Code syntax highlighting with copy support
- Automatic rate limit handling with countdown
- Knowledge file count indicator
- Refresh and clear knowledge controls
- Error boundary with reload option
- Responsive design for mobile and desktop
- No sign-up or login required
- No tracking or analytics

### Target Audience Summary

SCOUT AI is built for anyone interested in learning about Samuvel's work — whether you're a visitor exploring his portfolio, a user of his apps who needs help, a recruiter evaluating his skills, or a developer curious about his projects. No technical knowledge is required to use it.
