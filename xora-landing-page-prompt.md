Role: Act as a World-Class Senior Creative Technologist and Lead Frontend Engineer.

Objective: Architect a high-fidelity, cinematic "1:1 Pixel Perfect" multilingual landing page for XORA, a software engineering company headquartered in Malaysia.

Aesthetic Identity: "High-End Cryptographic Tech" / "Engineering Atelier." The site should feel like a bridge between a cryptography lab and an avant-garde luxury architecture journal.

## 1. COMPANY PROFILE (FACTUAL SOURCE OF TRUTH)

- Name: XORA.
- Headquarters: Malaysia (UTC+8, time zone Asia/Kuala_Lumpur).
- Definition: XORA is a software engineering company headquartered in Malaysia that delivers integrated, end-to-end technology solutions. It brings together distributed teams of distinguished programmers and developers from more than 17 countries and takes products from first architecture to secure, intelligent systems running in production.
- Disciplines: Computer Science (algorithms, performance, and research-grade problem solving). Software Engineering (custom software, platforms, and scalable system architecture). Data Analytics (data pipelines, analytics, and decision intelligence). Cybersecurity (security audits, penetration testing, and secure-by-design engineering). AI Development (building, training, and integrating AI models into real products).
- Operating Model: One integrated partner across software, data, security, and AI instead of separate vendors. Distributed squads across time zones deliver around the clock, coordinated from the Malaysia headquarters.
- Name Meaning: XORA comes from XOR, the logic operator that outputs true only when its inputs differ. Core idea: different minds, one precise output. Difference is the signal.
- Positioning: Talent is selected for excellence, not cost.
- Audience: Companies of every size, from startups building their first product to enterprises modernizing critical systems.
- Truthfulness: Do not invent facts. No client names or logos, testimonials, awards, certifications, founding year, street address, team size, or statistics beyond this profile. Readouts inside the animated micro-UIs are illustrative telemetry, not claims.

## 2. CORE DESIGN SYSTEM (STRICT)

- Palette: Cipher (Primary): #1E1B4B, Signal (Accent): #C8F54A, Quartz (Background): #EEF0F3, Void (Text/Dark sections): #0A0A12.
- Signal Rule: Signal is a light-emitting color. Use it freely on Cipher and Void surfaces (glows, cursors, live dots, buttons). On light surfaces use it only as a filled shape (pill, dot, block, button) carrying Void text, never as thin text or hairlines.
- Typography: Headings: "Plus Jakarta Sans" & "Outfit" (Tracking tight). Drama/Emphasis: "Cormorant Garamond" (Must use Italic for the human side of engineering: talent, craft, intelligence, difference). Data: "JetBrains Mono" for code telemetry and engineering readouts.
- Visual Texture: Implement a global CSS Noise overlay (SVG turbulence at 0.05 opacity) to eliminate flat digital gradients. Use a rounded-[2rem] to rounded-[3rem] radius system for all containers.
- Brand Mark: An inline SVG XOR mark (two overlapping circles where only the non-overlapping parts are filled, the XOR symmetric difference) beside a "XORA" wordmark.

## 3. CONTACT SYSTEM (STRICT)

- Only two public channels exist: the Malaysian contact number and GitHub. No email, no street address, no contact form, no other social links.
- Contact Number: +60XXXXXXXXX (replace with the real number). Define it once as const CONTACT_NUMBER at the top of the script and never print it in the markup or the initial DOM. It stays hidden behind a "Contact Number" button: clicking reveals it with a short decode animation (digits scrambling into place), rendered inside <bdi dir="ltr"> so it never flips in Arabic, alongside two actions: Call (tel: link) and WhatsApp (https://wa.me/ followed by the digits only).
- CTAs: "Start a Project" and every engagement button open WhatsApp with a prefilled message in the visitor's current language (e.g., "Hi XORA, I'd like to start a project." / "Hi XORA, I'm interested in the Dedicated Squad engagement.").
- GitHub: https://github.com/Bbobkr (inline SVG GitHub icon; opens in a new tab with rel="noopener noreferrer").

## 4. MULTILINGUAL SYSTEM (STRICT)

- Languages (15): English (en, default), العربية (ar, RTL), 中文 (zh, Simplified), Bahasa Melayu (ms), Español (es), Français (fr), Deutsch (de), Português (pt), Русский (ru), 日本語 (ja), 한국어 (ko), हिन्दी (hi), Türkçe (tr), Italiano (it), Bahasa Indonesia (id).
- Dictionary: One I18N object with identical keys for every language and a t(key) helper that falls back to English. Every visible string comes from the dictionary; zero hard-coded copy in JSX. The English copy in this prompt is the source of truth: translate it with native, marketing-grade fluency (complete, no placeholders, no English leftovers), but keep code tokens, endpoints, version numbers, UTC offsets, the contact number, and the engagement tier names (Blueprint, Dedicated Squad, Global Lab) untranslated.
- Locked Translations (use exactly):
  - Hero: ar "الاختلاف هو" + "الإشارة." / zh "差异，即是" + "信号。"
  - Manifesto: ar "شركات التعهيد تسأل: أين المواهب الأرخص؟" vs. "نحن نسأل: أين المواهب الاستثنائية؟" (drama word: الاستثنائية) / zh "外包在问：哪里的人才最便宜？" vs. "我们在问：哪里的人才最卓越？" (drama word: 卓越)
- Language Switcher: A globe icon plus the current language code inside the navbar pill, opening a glassmorphic popover grid of native language names. Selecting a language updates <html lang> and dir, document.title and the meta description, persists to localStorage (wrapped in try/catch), and syncs a ?lang=xx URL parameter. First visit auto-detects from navigator.language and falls back to English.
- RTL: Arabic switches to dir="rtl". Build every layout with logical Tailwind utilities (ms-/me-, ps-/pe-, start-/end-, text-start) so the entire page mirrors cleanly, and mirror any horizontal GSAP offset with a direction multiplier.
- Script-Aware Fonts: Swap font stacks through CSS variables keyed on :lang(). Arabic: "IBM Plex Sans Arabic" + "Amiri" (drama). Chinese: "Noto Sans SC" + "Noto Serif SC". Japanese: "Noto Sans JP" + "Noto Serif JP". Korean: "Noto Sans KR" + "Noto Serif KR". Hindi: "Noto Sans Devanagari" + "Noto Serif Devanagari". Russian: "Manrope" + "Cormorant Garamond". Lazy-load each script's Google Fonts stylesheet the first time its language is needed.
- Script Safety: Never synthesize italics, never apply letter-spacing (tight or wide), and never force uppercase on Arabic, CJK, or Devanagari; in those scripts, drama words use the serif face upright. Give Arabic and Devanagari headlines a taller line-height so marks never clip.
- Text Engineering: Split text for GSAP reveals by word with Intl.Segmenter (fallback: split on spaces), never by character, which breaks Arabic letter joining; CJK needs the segmenter because it has no spaces. The typewriter must advance by grapheme (Intl.Segmenter with granularity "grapheme") so Hindi and Arabic never flash broken glyphs. Generate weekday initials with Intl.DateTimeFormat(lang, { weekday: "narrow" }).
- Layout Resilience: Design for the longest language (German, Russian): clamp() type scales and no fixed-width text containers.
- Switch Behavior: On language change, cross-fade the content without replaying the intro, then call ScrollTrigger.refresh() after document.fonts.ready so pinned and sticky sections recalculate for the new text lengths.

## 5. COMPONENT ARCHITECTURE & BEHAVIOR

A. NAVBAR (The Floating Island)
A fixed, pill-shaped container holding the XOR mark and wordmark, links (Capabilities, Philosophy, Protocol, Engagement), the language switcher, and a Signal "Start a Project" button (opens WhatsApp, see Contact System). On mobile, the links collapse into a menu while the language switcher stays visible. Morphing Logic: Transparent with white text at the hero top. Transitions into a white/60 glassmorphic blur with Cipher text and a subtle border upon scrolling.

B. HERO SECTION (Difference is the Signal)
- Visuals: 100dvh height. Background image of Earth at night seen from orbit (https://images.unsplash.com/photo-1451187580459-43490279c0fa?auto=format&fit=crop&w=2400&q=80) with a heavy Cipher-to-Void gradient overlay.
- Layout: Content pushed to the bottom-start third (bottom-left in LTR, bottom-right in RTL). In the opposite bottom corner, a small mono coordinate tag: "HQ / MALAYSIA / UTC+8 / 17+ COUNTRIES".
- Typography: Large scale contrast. "Difference is the" (Bold Sans) vs. "Signal." (Massive Serif Italic), with the final period rendered as a glowing Signal dot. Above it, a mono eyebrow: "// XOR: output is true only when inputs differ." Below it: "Headquartered in Malaysia, XORA compiles elite engineers, data scientists, security specialists, and AI builders from 17+ countries into one precise engineering force." CTAs: "Start a Project" (Signal) and "Explore Capabilities" (ghost).
- Animation: GSAP staggered fade-up for all text parts.

C. FEATURES (The Precision Micro-UI Dashboard)
Replace standard cards with Interactive Functional Artifacts.
- Card 1 (Engineering Audit, "Continuous diagnostics across code, security, and data."): Implement a "Diagnostic Shuffler." 3 overlapping white cards that cycle vertically using unshift(pop()) logic. Every 3 seconds, they rotate with a spring-bounce transition (cubic-bezier(0.34, 1.56, 0.64, 1)). Labels: "Code Health Index", "Threat Surface Score", "Data Integrity Rate", each with a mono readout ("96 / 100", "LOW · 3 vectors", "99.98%").
- Card 2 (Follow-the-Sun Stream, "17+ countries in rotation. Your product never sleeps."): Implement a "Telemetry Typewriter." A live text feed, rendered in a dark Void terminal well inside the card, cycling through messages like "Sprint 24 handoff: UTC+8 → UTC+2 → UTC-3... complete", "Penetration test on /api/v2/auth... 0 critical", "Retraining forecast model... accuracy +4.2%", "Encrypting data at rest... AES-256 verified", "Deploying build 3.8.1 to 12 edge regions..." with a blinking Signal cursor. Include a small "Live Feed" pulsing dot.
- Card 3 (Release Orchestration, "Predictable release windows, engineered and shipped on schedule."): A "Mock Cursor Release Scheduler." A weekly grid (S M T W T F S, localized) where an automated SVG cursor enters, moves to a day, clicks (visual scale-down), activates the day as a Cipher release window, then moves to a "Deploy" button before fading out. Compute every cursor target from element refs (getBoundingClientRect), never hard-coded coordinates, so the sequence works in RTL and in every language.

D. PHILOSOPHY (The Manifesto)
A high-contrast Void section with a parallaxing texture: a circuit-board macro (https://images.unsplash.com/photo-1518770660439-4636190af475?auto=format&fit=crop&w=2400&q=80) rendered grayscale at low opacity and tinted with Cipher. Text Layout: Huge typography comparison. "Outsourcing asks: Where is talent cheapest?" vs. "We ask: Where is it exceptional?" using split-text GSAP reveals, with "exceptional" in Massive Serif Italic.

E. PROTOCOL (Sticky Stacking Archive)
Vertical stack of 3 full-screen cards using sticky top-0. Stacking Interaction: Using GSAP ScrollTrigger, as a new card scrolls into view, the card underneath must scale down to 0.9, increase its blur filter to 4px, and fade its opacity to 0.5.
- 01 Decode: "We map your architecture, data, and threat surface before a single line is written." Artifact: A counter-rotating cipher rotor: two concentric rings of binary glyphs spinning in opposite directions around a pulsing ⊕ (XOR) core.
- 02 Engineer: "Distributed squads build in parallel against one uncompromising standard: every commit reviewed, scanned, and hardened." Artifact: A scanning laser line sweeping across a grid of bit cells, flipping each cell 0 ↔ 1 as it passes with a brief Signal glow.
- 03 Evolve: "AI-driven monitoring and continuous delivery keep your system learning, secure, and online around the clock." Artifact: A live waveform whose path morphs from analog noise into a clean digital square wave, with a pulse of light traveling along it.

F. ENGAGEMENT & FOOTER
- Three-tier engagement grid (no public prices; the price slot shows the engagement model). Each button opens WhatsApp with a prefilled message naming its tier:
  - "Blueprint" (Fixed Scope): architecture, code, and security audit in 2 to 4 weeks. Button: "Request an Audit".
  - "Dedicated Squad" (Monthly): a cross-functional team of engineers, data, security, and AI specialists embedded in your roadmap. Button: "Build My Squad".
  - "Global Lab" (Enterprise): multi-squad, multi-region, follow-the-sun delivery with a 24/7 SLA. Button: "Talk to Us".
- The middle card ("Dedicated Squad") should "pop" with a Cipher background and a Signal button.
- Footer: Deep Void, rounded-t-[4rem].
  - Brand column: the XOR mark, a two-sentence company definition drawn from the Company Profile, and "Headquartered in Malaysia".
  - High-end utility links as in-page anchors (Capabilities: Software Engineering, Data Analytics, Cybersecurity, AI Development. Company: Philosophy, Protocol, Engagement. Legal: Privacy, Terms).
  - Contact column with exactly two items: the "Contact Number" reveal button and the GitHub link.
  - Bottom bar: a "System Operational" status indicator with a pulsing Signal dot, a live HQ clock ("Malaysia HQ" plus the current time via Intl.DateTimeFormat with timeZone "Asia/Kuala_Lumpur"), and a mono line "17+ countries · 24/7 coverage".

## 6. TECHNICAL REQUIREMENTS (STRICT SINGLE-FILE SETUP)

- Tech Stack: React 18/19, Tailwind CSS, GSAP 3 (with ScrollTrigger).
- NO EXTERNAL ICON CDNS: External libraries like lucide-react cause fatal reference errors in browser-based Babel setups. You MUST write 5-6 inline functional React SVG components for ANY icons you need (GlobeIcon, PhoneIcon, WhatsAppIcon, GitHubIcon, ArrowIcon, MenuIcon; e.g., const GlobeIcon = () => <svg>...</svg>;). Do not use <script src="...lucide..."></script>.
- GSAP REGISTRATION: You MUST explicitly call gsap.registerPlugin(ScrollTrigger); immediately after the React imports.
- TRUE CUSTOM ARTIFACTS: Do not be lazy. For the Protocol cards, do NOT just place a static faded icon in the background. You must code actual custom, animated SVG components (a real counter-rotating cipher rotor, a real laser scan flipping bit cells, a real morphing waveform, using CSS/GSAP).
- POLISHED SPACING: Use generous paddings (p-12 to p-24) and ensure viewport heights (min-h-screen or h-[100vh]) are correctly calculated so sticky elements stack cleanly without overlapping text, in every language.
- CLEAN CODE: NEVER output non-breaking spaces (NBSPs / \xA0). Use standard space characters for all indentation to prevent Babel syntax errors.

Execution Directive: "Do not build a website; build a digital instrument. Every scroll should feel intentional, every animation should feel weighted and professional. Eradicate all generic AI patterns, deliver exactly one working HTML file."
