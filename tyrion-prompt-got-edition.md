# Claude Code Prompt: Tyrion Training Website

## Project Overview

Build a single-page interactive training website that teaches a global team at MFG (Google's media agency) how to adopt a new media intelligence process called **Tyrion**. The experience should feel like playing a 16-bit Game of Thrones–themed RPG — medieval fantasy aesthetic, polished pixel art, and deeply fun. Lean into the GoT connection (the process is literally called "Tyrion"). The entire learning journey should take ~10 minutes.

**CRITICAL PRIORITY: This is a training tool first, a game second.** Every design choice must serve comprehension and ease of use. The GoT theme exists to make learning sticky and enjoyable — it should never confuse, slow down, or get in the way of someone understanding what Tyrion is and what they need to do. If there's ever a tension between "cool game moment" and "clear training moment," clarity wins every time.

## Design & Art Direction

- **Visual style**: 16-bit Game of Thrones RPG. Think SNES-era Final Fantasy or Fire Emblem, but set in Westeros. Stone castle UI frames, parchment-textured content panels, pixel art torches that flicker with CSS animation, iron throne motifs, medieval banner/flag decorations, and a world map aesthetic for navigation. Dialogue should appear in RPG-style text boxes (bordered, with a character name label above). Use pixel art icons: swords, shields, ravens, scrolls, goblets, dragon eggs, castle towers.
- **Thematic framing**: Tyrion Lannister is the implicit spirit guide — clever, strategic, sees what others miss. The whole metaphor: Tyrion (the process) brings intelligence and visibility to the realm (Google's PAs), just like Tyrion Lannister navigates the overlapping ambitions of rival houses. Each PA is like a Great House with its own domain/territory. Overlaps = border disputes. Tyrion = the Hand of the King bringing order through information, not force.
- **Color palette**: Deep medieval tones — dark charcoal/black backgrounds, aged gold/amber for headings and accents, deep crimson (Lannister red) for highlights and CTAs, stone grey for UI frames, forest green gradients for the investment scale (ties into "darker green = heavier investment" — style this like a kingdom's resource/treasury meter). Occasional ice blue for contrast (The Wall / winter motifs).
- **Typography**: Use "MedievalSharp" or "UnifrakturMaguntia" from Google Fonts for major titles and level headers (gothic/medieval feel). Use "Press Start 2P" for pixel UI elements like progress bars and button labels. Use a clean sans-serif (Inter or system) for body text to maintain readability.
- **Layout**: Click-through progression styled like chapters of a quest. Each "level" is a distinct screen the user advances through. Include a persistent progress bar styled as a castle wall being built — each level adds a tower/section. Or use a Westeros-style map at the top where regions light up as you progress.
- **Interactions**: Level transitions should have brief medieval-themed animations — parchment unfurling, a raven flying across the screen, torch-lighting effects, or a castle gate opening. Include an opening "title scroll" screen and a "Training Complete" victory screen styled as a royal decree/proclamation with pixel fireworks.
- **Pixel art elements to create via CSS/SVG**: A small pixel Tyrion character (golden hair, goblet in hand) that appears as a guide/narrator. Pixel castle towers, banners, shields for each region (NA, EMEA, APAC). A pixel Iron Throne. A pixel raven for "messages/updates." A pixel scroll for documents. Keep these simple but recognizable — 32x32 or 64x64 style.
- **Responsive**: Must work on desktop and mobile.

## UX & Training Principles

These rules govern the entire build. When in doubt, refer back here.

1. **One idea per screen.** Each chapter/level should teach ONE concept. Don't cram multiple ideas into a single view. The user should be able to glance at any screen and immediately know: "This is about ___."

2. **Plain language always visible.** The GoT flavor text (e.g., "The Great Houses overlap...") is fun framing, but every screen MUST also include a clear, plain-English summary of the actual point. Use a visible callout box, tooltip, or sidebar labeled something like "Translation" or "In plain terms" that restates the point without any theme language. Example: the GoT framing says "Tend to your kingdom's borders on the map" — the plain callout says "Update your region's slides in the Tyrion deck at least once a month."

3. **No dead ends or confusion.** Every screen must have an obvious, large "Next" / "Continue" button. The user should never wonder "what do I click?" or "am I done?" Progress should feel automatic and guided — like a theme park ride, not a maze.

4. **Progressive disclosure.** Don't dump all information at once. Reveal content in digestible chunks — a few sentences at a time, advanced by clicking "Next" within a chapter if needed. Think RPG dialogue boxes: 2-3 sentences per box, click to advance.

5. **Skippable animations.** All transitions and animations (raven flights, parchment unfurls, etc.) must be skippable by clicking/tapping anywhere. Nobody should wait for an animation to finish before they can read. On repeat visits, animations should feel snappy, not tedious.

6. **Always know where you are.** The progress indicator (castle wall, map, or bar) must be visible at all times. Label each chapter clearly: "Chapter 1 of 3" or equivalent. Include a chapter-select/table-of-contents accessible from any screen so users can jump to what they need.

7. **Key actions are unmissable.** The two things people actually need to DO (update the deck + include Tyrion in meetings) should be the most visually prominent elements in the entire site — bigger, bolder, more highlighted than anything else. These are not buried in body text. They get their own dedicated visual treatment with clear CTAs.

8. **Quiz confirms, doesn't block.** The mini-quiz at the end of Chapter 1 is a comprehension check, not a gate. If someone gets it wrong, show the right answer with a brief explanation and let them proceed. Don't force retries or make people feel bad — this is a training for busy professionals, not a test.

9. **Accessible to non-GoT fans.** Not everyone on a global team has watched Game of Thrones. The metaphors (houses = PAs, domains = territories, etc.) should be intuitive even without GoT knowledge. Include a brief "legend" or glossary mapping theme terms to real terms at the start, and always pair fantasy language with plain language.

10. **Mobile-first content sizing.** Body text must be minimum 16px. Buttons must be large touch targets (min 44x44px). No tiny pixel text for critical information. The pixel font (Press Start 2P) is for decorative UI labels only — never for paragraphs of content people need to read.

## Content Structure (4 Levels + FAQ)

### START SCREEN
- Title: "TYRION" in large medieval/gothic font with a pixel Iron Throne behind or below it
- Subtitle: "A Game of Domains // ~10 min to complete"
- Tagline: "In the game of media, you win or you overlap."
- A "BEGIN YOUR QUEST" button styled as a medieval stone button or wax-sealed scroll
- Brief flavor text in an RPG dialogue box: "Welcome, brave MFGer. The realm of Google's Product Areas grows more tangled by the day. Houses overlap. Territories blur. But one process can bring order to the chaos. Your quest: learn the ways of Tyrion."
- A small pixel Tyrion character (with goblet) stands beside the dialogue box as narrator
- **Quick legend (visible on start screen or as a dismissible tooltip):** A small key mapping GoT terms to real terms so non-fans aren't lost:
  - Great Houses = Google's Product Areas (Search, YouTube, Pixel, etc.)
  - Domains/Territories = The audiences, partnerships, and messaging spaces each PA operates in
  - The Realm = The full Google media landscape across all markets
  - The Hand = Global coordinator (Ed)
  - Wardens = Regional accountable leads
  - The Map = The Tyrion deck (shared slides)

### LEVEL 1: "What is Tyrion & Why?"
**Title card**: "CHAPTER I — RAVENS FROM THE CAPITAL" with a parchment/scroll unfurling animation. A pixel raven flies across the screen.

**Content to present (delivered via RPG-style dialogue boxes with pixel Tyrion as narrator):**

- **Context**: Michael Bailey is here and implementing changes to how Media Lab (and therefore MFG) approaches media. Regional ML leads (Carrie, Emily, Sylvie) have been communicating these shifts. *(Frame as: "A new Hand has arrived at court...")*
- **The Problem**: Google's Product Areas (PAs) today overlap in audiences, partnerships, and messaging. Sometimes good, sometimes bad — almost always unintentional. The integration of Gemini across PAs is compounding these overlaps and may create problems or suppress efficiencies. *(Frame as: "The Great Houses of Google — each with their own territory — have begun encroaching on each other's domains...")*
- **What Tyrion Does**: A new process that starts with PA Overlap. It brings visibility to overlaps by creating "domains" for each PA in each market. *(Frame as: "Tyrion is the realm's intelligence network — mapping every house's territory so all can see where borders cross.")*
- **The Concept**: Tyrion = MFG creating visibility of multiple Google Product Area's Domains.
- **Success Definition**: Any MFGer, anywhere in the world, can see what any other PA domain is doing. *(Frame as: "When the map is complete, any knight in any kingdom can see the full realm.")*

**Design notes for this level:**
- Present the "problem" like a fantasy war map — overlapping territories (PAs) shown as colored regions on a Westeros-style map, with borders blurring and clashing
- Use a "fog of war" visual: before Tyrion, the map is obscured/dark. After Tyrion, territories are clearly labeled and visible — like lifting fog from a strategy game map
- Include a mini-quiz styled as a "trial" or "riddle from the Maester": e.g., "What is Tyrion's purpose? [A] To police the Great Houses [B] To bring visibility to domain overlaps [C] To merge all houses into one" — correct answer is B, with a "Correct! You may proceed" animation. If wrong, show the right answer and let them continue — don't block progress.

**Plain-language summary box for this level (always visible on screen):**
> **In plain terms:** Tyrion is a new process that maps where Google's Product Areas overlap. The goal: anyone at MFG can see what every PA is doing in every market. That's it.

### LEVEL 2: "Your Mission"
**Title card**: "CHAPTER II — YOUR SWORN DUTIES" with a quest-log/royal decree visual. A wax seal stamps onto the screen.

**Content — two Royal Decrees (quests):**

**Decree 1: Guard the Realm's Map (Update the Tyrion Deck)**
- Update your slides in the shared deck whenever decisions are made (minimum once a month)
- Find your region and markets — keep info current. Leave a comment on your slide whenever you update. *(Frame as: "Tend to your kingdom's borders on the map.")*
- Information should reflect MFG's recommendations. When ML/PMM agrees, mark it with an **asterisk** as locked/real (example: *"Emily has decided that Search in UK is World Cup"*) *(Frame as: "When the Crown approves, mark it with the Royal Seal ✱")*
- **Key visual mechanic**: The darker the green on a slide, the heavier the investment. This allows two PAs to be in the same domain but prioritizes how much they spend to show up there. *(Style this as a "Treasury Meter" — a medieval resource bar going from pale green (light investment) to deep forest green (heavy investment), decorated with gold coins or pixel treasure chests.)*
- **Link placeholder**: [INSERT LINK TO TYRION DECK] — style this as a glowing enchanted scroll button or a golden chest that opens on hover

**Decree 2: Bring Tyrion to the Council (Include in PA Meetings & Decks)**
- Check Tyrion while developing strategy and media plans — look for problems or opportunities created by PA overlap *(Frame as: "Consult the map before marching to war.")*
- In client meetings, Tyrion doesn't need to be topic #1 (can be appendix). Just make clients aware it's available. *(Frame as: "It need not be the first item on the King's agenda — but it must be in the scrolls.")*
- Include Tyrion as a chapter in all big PA decks.

**Critical callout (styled as a quote on parchment, attributed to pixel Tyrion with goblet):**
> 🍷 "The goal of Tyrion is VISIBILITY. NOT policing Google. They're going to do what they're going to do." — Styled like a famous GoT quote card, with ornate borders and a pixel Tyrion portrait beside it.

**Design notes:**
- Present the two decrees as a "Royal Quest Log" on aged parchment with wax seals, checkboxes styled as shield/sword icons
- The green gradient investment scale ("Treasury Meter") should be a prominent, well-designed visual — medieval resource bar with pixel gold accents

**Plain-language summary box for this level (always visible on screen):**
> **In plain terms:** You have two jobs: (1) Update your slides in the Tyrion deck at least once a month. (2) Include Tyrion as a topic in your PA meetings and decks. That's it. The goal is visibility, not policing.

### LEVEL 3: "How It Works"
**Title card**: "CHAPTER III — THE SMALL COUNCIL" with a round-table/war-room visual. Torches light up on either side.

**Content — The Small Council (Accountability structure):**

- **Ed** = The Hand of the King (global coordinator/stalker). Present as a pixel character seated at the head of a medieval council table, or standing at a war map with pins. Dialogue: "I'll be watching. Everywhere."
- **Regional Houses (present as a "Great Houses" roster — each region is a house with a sigil/banner):**
  - **House NA** 🏰: Erica/Mindy (Wardens — Accountable) → Bannermen (Informed): Kimberly, Sarah, Theresa, Rachel
  - **House EMEA** 🏰: Jo P/Rosanna (Wardens — Accountable) → Bannermen (Informed): Grant, Regional Investment Lead
  - **House APAC** 🏰: Kenward/Jamarr (Wardens — Accountable) → Bannermen (Informed): Karl, Regional Investment Lead

**Operational rules (styled as "Laws of the Realm" on a stone tablet or royal decree):**
1. The Hand will establish a raven network (group chat) with the lead strategist, planner, and CS in every region.
2. Each house is responsible for keeping the realm's map (Tyrion) updated — at least once per moon (month).
3. The Hand will convene ONE gathering of all Wardens (kick-off meeting).
4. For follow-up councils: send the MINIMUM number of delegates to represent your house. Do not send envoys from every market and every PA. *(Frame as: "Send your wisest counselor, not your entire army.")*

**Design notes:**
- The accountability structure should look like a **"Great Houses" selection screen** — three house banners/shields (NA, EMEA, APAC) each with a distinct color/sigil. Click or hover to reveal the roster.
- Each house has a pixel banner flag and a list showing "Wardens" (larger, highlighted, with a small crown or sword icon) and "Bannermen" (smaller, indented)
- Ed's "Hand of the King" role should have a special visual treatment — a pixel Hand pin icon or a unique character sprite

**Plain-language summary box for this level (always visible on screen):**
> **In plain terms:** Ed coordinates globally. Each region has accountable leads (NA: Erica/Mindy, EMEA: Jo P/Rosanna, APAC: Kenward/Jamarr). Update monthly. Send minimal delegates to follow-up meetings.

### LEVEL 4 / BONUS LEVEL: "Extra Credit"
**Title card**: "CHAPTER IV — THE FORBIDDEN LIBRARY" with a Citadel/Maester's library visual. Candles flicker, old books line pixel shelves.

**Reference documents (styled as ancient tomes or enchanted scrolls):**
1. **"The Original Petition to the Crown"** — The deck presented to Michael and Carrie to propose creating domains. [INSERT LINK] *(Style as a glowing ancient tome with a Lannister-gold binding)*
2. **"The Japan Scrolls"** — Japan Annual Planning, where they sort out domains. [INSERT LINK] *(Style as a rolled parchment sealed with wax)*

**Design notes:**
- Style these as items in a medieval library or treasure vault — the user has "unlocked" access by completing training
- Each item glows or pulses subtly, with a hover state that reveals a 1-sentence description before clicking through to the link
- The room should feel like you've earned entry — "You have proven worthy. The Maester grants you access to the archives."

### FAQ SECTION
**Title**: "THE MAESTER'S COUNSEL — FAQ"

**Generate a smart FAQ based on the content above. Include at minimum:**
- "What exactly is a 'domain' in Tyrion?"
- "How often do I need to update the deck?"
- "What does the green shading mean?"
- "Do I need to bring up Tyrion in every client meeting?"
- "Who do I contact if I have questions?"
- "Is Tyrion meant to restrict what PAs can do?"
- "What if two PAs are in the same domain?"
- "How does Gemini factor into this?"
- "What does 'locked/real' mean with the asterisk?"
- "I'm not sure what my region's domains look like — where do I start?"

**Design notes:**
- Style as an accordion on aged parchment — each question is a sealed scroll that unfurls when clicked
- Use a pixel Maester character or a wise old advisor icon next to each answer
- Keep the GoT voice light here — answers should be clear and practical, with only subtle thematic flavor (e.g., "Send a raven to Ed" instead of "Contact Ed")

### UNGAME VERSION
**Title**: "THE RAVEN'S SCROLL — Plain Text Version"
**Access**: A persistent button/tab next to the FAQ link, available from any screen. Styled as a simple parchment icon or a "📜 Just the facts" toggle. Should be easily visible but not competing with the main game flow.

**Purpose**: A no-frills, straight-text version of all training content for people who want to skim, reference later, or simply prefer reading over playing. Think of it as the "screenplay" version of the movie — same content, no production.

**Design notes:**
- Opens as a full-screen overlay or a separate scrollable page, styled as clean parchment with minimal decoration (light medieval border at most, no animations, no pixel art, no dialogue boxes)
- Use clear section headers, short paragraphs, and simple formatting
- Should be printable / copy-pasteable
- Include a "Return to Game" button at the top and bottom

**Content to include (reorganized for easy scanning):**

**WHAT IS TYRION?**
Tyrion is a new media intelligence process for MFG. Its purpose is to create visibility into how Google's Product Areas (PAs) overlap in audiences, partnerships, and messaging across markets. Michael Bailey is implementing changes to how Media Lab approaches media, and regional ML leads (Carrie, Emily, Sylvie) are communicating these shifts. The integration of Gemini across PAs is compounding overlaps and may create problems or suppress efficiencies. Tyrion addresses this by creating "domains" for each PA in each market, so any MFGer anywhere in the world can see what any other PA domain is doing.

Key concept: Tyrion = MFG creating visibility of multiple Google Product Area's Domains.

**WHAT YOU NEED TO DO**

Task 1 — Keep the Tyrion Deck Updated:
- Update your slides in the shared deck whenever decisions are made (minimum once a month). [INSERT LINK TO TYRION DECK]
- Find your region and markets. Keep information current. Comment on your slide whenever you make an update.
- Slides should reflect MFG's recommendations. When ML/PMM agrees, mark with an asterisk as locked/real (e.g., *Emily has decided that Search in UK is World Cup*).
- The darker the green, the heavier the investment. Two PAs can share a domain — the shading shows who's spending more to show up there.

Task 2 — Include Tyrion in PA Meetings & Decks:
- Check Tyrion while developing strategy and media plans. Look for problems or opportunities created by PA overlap.
- In client meetings, Tyrion doesn't need to be topic #1 — it can be in the appendix. Just make clients aware it's available.
- Include Tyrion as a chapter in all big PA decks.

Remember: The goal is VISIBILITY. Not policing Google. They're going to do what they're going to do.

**WHO IS RESPONSIBLE**

Global Coordinator: Ed (will act as global stalker for now)

Regional Accountability:
- NA: Erica/Mindy (Accountable) · Informed: Kimberly, Sarah, Theresa, Rachel
- EMEA: Jo P/Rosanna (Accountable) · Informed: Grant, Regional Investment Lead
- APAC: Kenward/Jamarr (Accountable) · Informed: Karl, Regional Investment Lead

How it runs:
- Ed will set up a group chat with the lead strategist, planner, and CS in every region.
- Each region keeps Tyrion updated at least once a month.
- Ed will set up one kick-off meeting with all accountables.
- For follow-up meetings, send the minimum number of delegates to represent your region. Don't send people from every market and every PA.

**REFERENCE DOCUMENTS**
1. The deck presented to Michael and Carrie proposing the creation of domains. [INSERT LINK]
2. Japan Annual Planning — an example of how domains are sorted out. [INSERT LINK]

### COMPLETION SCREEN
- "THE REALM IS MAPPED" or "YOU HAVE SERVED THE REALM" in large medieval font with pixel fireworks, dragon silhouettes flying overhead, and banners unfurling
- Show a "Knighted" badge or "Seal of the Hand" achievement graphic — pixel wax seal or coat of arms
- A pixel Tyrion raises his goblet: "That wasn't so bad, was it? Now go forth and bring visibility to the realm."
- Recap the 3 key takeaways on a royal proclamation/scroll:
  1. Tyrion = visibility into PA domain overlaps (the realm's map)
  2. Update the deck monthly + include Tyrion in PA meetings (guard the borders, attend the council)
  3. Know your regional accountability chain (know your house, know your wardens)
- Optional: "Share your completion" or "Return to the Throne Room" button

## Technical Requirements

- **Stack**: Single HTML file with embedded CSS and JS (or a simple React app if complexity demands it). Prioritize a single self-contained file for easy sharing.
- **No backend needed** — this is a static informational site.
- **Animations**: Use CSS animations and transitions. Keep it lightweight — no heavy libraries. GSAP is acceptable if needed for complex sequences. Key animations: flickering torches (CSS), parchment unfurling (CSS transform), raven flight (CSS keyframes), fog-of-war reveal (opacity/clip-path), banner waving (CSS), text appearing letter-by-letter in dialogue boxes (JS).
- **Pixel Art**: Create all pixel art elements using CSS/SVG — no external image dependencies. Key sprites needed: Tyrion character (small, with goblet), castle towers, house banners (3 regions), scroll/parchment, raven, sword/shield icons, treasure chest, wax seal, torch (animated flame). Keep sprites simple (32x32 or 64x64 pixel grid style) but recognizable.
- **Fonts**: Load "MedievalSharp" from Google Fonts for chapter titles and major headings. Load "Press Start 2P" for pixel UI elements (progress bar labels, button text, quiz options). Use Inter or system sans-serif for body text readability.
- **Sound**: Optional. If included, make it toggleable and OFF by default. Medieval ambient (lute, tavern) or simple UI click sounds only.
- **Links**: Wherever the content references a shared deck or document, create prominent, styled placeholder buttons with text like "[INSERT DECK LINK]" that can be easily find-and-replaced with real URLs. Style these as glowing enchanted items (scrolls, tomes, chests).
- **Progress**: Implement a visible progress bar styled as either: (a) a castle wall being built stone by stone, or (b) a Westeros-style map where regions illuminate as you advance, or (c) a simple medieval banner/shield bar that fills with gold.
- **Navigation**: Users should be able to go back to previous chapters and skip ahead if revisiting. Include a chapter-select styled as a realm map or tome's table of contents.
- **Mobile-friendly**: Responsive design, touch-friendly buttons, readable text sizes. Pixel art should scale cleanly.

## File Output

Save the final website to `/mnt/user-data/outputs/tyrion-training/index.html` (and any supporting assets in the same folder). If it's a single HTML file, that's ideal.

## Quality Bar

This will be shared with a global team at a major agency working on Google. It needs to look polished and professional while being genuinely fun. Think: "a senior creative director who loves GoT built this as a passion project" — not "someone slapped a medieval font on a PowerPoint." The Game of Thrones RPG aesthetic should feel intentional, crafted, and delightful — the kind of thing people Slack to each other saying "you HAVE to see how they rolled out this new process." The GoT theming should enhance comprehension (houses = PAs, domains = territories, visibility = mapping the realm) not distract from it.
