# Day 1 — Plan of Show

Workshop runs 1:00–2:30pm (90 min). Becca arrives at the 20-minute mark
and her faculty demo serves as the hinge between the web UI section
(chat.claude.ai) and the desktop-app section (Cowork on local files).

The room enters with the desktop app installed but starts in the
browser. By the end of the session they have made a project, transcribed
a folder of images, generated an HTML page, and filled out a paper
recipe card for the homework feeding into Day 2.

---

## Pre-flight (before 1:00)

- Shared Google Drive folder staged in a known location on every demo
  machine, unzipped, in the same path.
- Designated cowork-onboarding owner identified — they do not present.
- Handouts stacked by section: Welcome & Roadmap, Three Instances /
  Interface Decision Grid, Text-File-Types Cheat Sheet, blank Recipe
  Card.
- Whiteboard or flipchart prepped for Madeleine's context-window
  drawing.

---

## 1:00 – 1:05 · Welcome and the week ahead (5 min)

- Hand out the **Welcome & Roadmap** sheet. Four-day arc: many Claudes,
  Claude Code as authoring environment, advanced tools & scaling,
  creating your own outputs.
- Show of hands — desktop app installed. Anyone stuck raises a hand and
  someone goes to them.
- Reassuring frame up front: Day 2 shows the command line, but the
  desktop app is a fully good path. About 10% of moves are easier in
  CLI; nearly everything works in either. Async handouts cover anything
  missed.
- Nothing else to install today.

## 1:05 – 1:10 · The many Claudes — triptych handout (5 min)

- Hand out the **Three Instances / Interface Decision Grid**.
- Walk the surfaces conceptually:
  - **Web (claude.ai)** — ask, get an answer.
  - **Desktop app** — chat + Cowork (local files) + a view into Claude
    Code.
  - **Claude Code in terminal + IDE** — workflows on your files at
    scale.
- All roads lead through the desktop app. Chat is cloud-based and
  mirrors the web; Cowork and Code work on this machine.

## 1:10 – 1:20 · AI in the web UI — what it does well and badly (10 min)

Everyone in claude.ai in a browser. Keep this section tight.

- **Multiplication demo (4 min).** Five-digit × five-digit. Model gets
  it wrong alone; rerun with Python; tool call produces the right
  answer. Surface what the room notices: first digits right, last
  digits right, magnitude right, middle wrong. Pattern recognition vs.
  calculation.
- **Tokens via TikTokenizer (3 min).** Paste a sentence. Show how
  *unhappily* gets split into *unha · pp · illy*. Frame: this
  intelligence is consistently inhuman. Strings in, strings out.
- **Shakespeare failure (3 min).** Ask for a close reading of
  *Coriolanus* I.ix. Model insists it does not exist; push back and it
  capitulates. Sycophancy and hallucination from missing context.
- Park the question: how do we give it the right context? Becca is
  about to show what that looks like in practice.

---

## 1:20 – 1:30 · Becca — the hinge (10 min)

Becca arrives. She is a faculty member, not staff. Two concrete
artifacts from her own teaching:

1. **Collaborative grading-rubric workflow.** Claude drafts a candidate
   rubric from her solution write-up, prior rubrics, sample student
   work, and her notes on common mistakes. She edits before grading.
   Side-by-side review of student work with the drafted rubric. The
   ingredient list — solution + prior rubrics + student samples — is
   the bridge we will use in the next section.
2. **Asynchronous online module from years of materials.** Lectures
   chunked into sub-seven-minute videos, with auto-inserted quizzes
   and an interactive Monty Hall simulation in the middle of the page.

Frame for the room: this is where the week is going. The next ten
minutes are about understanding why this works, so you can do it.

---

## 1:30 – 1:45 · The context window — memory, system prompt, drawing (15 min)

Becca has just shown the pay-off. Now name the machine underneath it.
Stay in the web UI.

- **Memory as a text file (4 min).** Settings → Capabilities. Open the
  memory file the demonstrator has accrued. This is the moment of
  vulnerability — show what the model actually remembers about you in
  plain prose. Note: Harvard instance memory is coming, not on yet.
  Mention import-from-other-providers — same thing, just paste.
- **System prompt (3 min).** Show a snippet from Anthropic's published
  system prompt for the current model. Roughly ten thousand words.
  Safety, style, tone. You do not get to edit this; it enters every
  chat before your prompt.
- **Memento metaphor (2 min).** Every new chat is a fresh day. Three
  things get injected before your first prompt: system prompt, memory,
  then you.
- **Madeleine draws the context window (4 min).** On the whiteboard.
  System prompt at the front, memory after it, your prompts and the
  model's responses appending across the window. Compaction at the end
  when the window fills.
- **Primacy, context rot, lost in the middle (2 min).** Name these.
  Point at the context-research folder in the shared drive — two
  papers there for anyone who wants to nerd out.
- Operating principle: push the ratio toward more user-vetted context,
  less freely-generated AI output, especially as the window grows.
  Becca's grading workflow is exactly this — she is filling the front
  of the window with her own materials.

## 1:45 – 1:50 · Artifacts — and the limit of staying in chat (5 min)

- Old way: ask for a population pyramid as an image. Diffusion model
  produces something pretty and nonsensical.
- New way: attach the CSV and ask for an interactive artifact comparing
  Japan and Nigeria. Claude picks a skill, runs code on the CSV,
  produces a working interactive. Code is what the model is actually
  great at.
- Set up the bridge to Cowork: artifacts live inside the chat thread.
  You made a thing, and now you cannot find it. What if you want it as
  a real file on your machine, with your other materials around it?

---

## 1:50 – 2:10 · Cowork — local files, with caveats (20 min)

Move into the desktop app.

### 1:50 – 1:55 · Open the project (5 min)
- Open the shared folder on every machine (already unzipped at
  pre-flight; if anyone is still downloading, onboarding owner handles
  them directly).
- Desktop app → Cowork → New Project → Open existing folder → select
  the unzipped folder.
- The room follows along on their own machine. Onboarding owner
  circulates; presenters do not narrate the clicks for too long.

### 1:55 – 1:58 · Security walkthrough (3 min)
- Cowork and Code can touch local files. That is the power and the
  risk. Point Cowork at a specific folder, not your home directory.
- Name the Homer-Simpson moment: you will be tempted to mash Yes on
  every permission prompt. Resist. Use the demo cards today, not
  research data.
- Harvard data tier: Level 3 OK. Anthropic does not train on this.
- Connectors (Google Drive, Calendar) are coming, in security review.

### 1:58 – 2:07 · Recipe-cards demo — rename, transcribe, publish (9 min)

Inside the shared folder there is a `recipe-photos` subfolder of
handwritten recipe-card images.

1. **Rename.** First prompt: ask Claude to give the images more
   descriptive names. Watch it look at each image and rename in place.
   Flag explicitly: if you say Yes once, Claude may take that as
   blanket permission and rename the next files without re-asking.
   That is why we are using cards today, not your dissertation.
2. **Transcribe.** Second prompt: for each card, create a text file
   with the recipe text. Sidebar fills with .txt files. Point out that
   only the files Claude touched show up in the context sidebar — not
   the whole folder.
3. **Publish.** Third prompt: give me an HTML file with all images
   embedded and the recipe text, and add historical context on each
   dish. About ten seconds of typing produces a small site. Open it.
- Address the question that always comes up: if I edit a file by hand,
  does Claude know? No. It is not watching. You have to tell it to
  re-read. Tease for Day 2: in Code you can wire this up with hooks
  and commits.

### 2:07 – 2:10 · Text-file-types cheat sheet (3 min)
- Hand out the **Text-File-Types Cheat Sheet**. Walk the ladder of
  structure:
  - Plain text: `.txt`, `.rtf`, `.md` — literary text, notes,
    transcriptions. Project Gutenberg, Shakespeare corpus in the
    shared folder.
  - Structured text: `.html`.
  - More structured: `.csv`, `.json`, code files.
- These are what go into the context window and what come out of it.
- First glance at `CLAUDE.md` and skills — they are text files too.
  We hit these on Day 2.

## 2:10 – 2:15 · The recipe metaphor (5 min)

- Callback: we just watched Claude read a stack of recipe cards. The
  context window works the same way — it is a recipe card.
  - **Ingredients** are your inputs: the files Cowork opened, the
    materials Becca handed in.
  - **Steps** are the operations and prompts.
  - **Dish** is your output: the HTML page, the rubric, the website.
- Marlon narrates what he did to make today's demo possible: photos →
  transcriptions → Claude-generated context per recipe → HTML
  template → final site. He was following his own recipe.
- Get the recipe right and the dish comes out right; leave an
  ingredient out and it will not.

## 2:15 – 2:28 · Fill out your recipe card (13 min)

- Hand out the blank **Recipe Card** worksheet. Each person fills one
  out for one real task they want to bring to tomorrow.
  - Ingredients: files, data, prompts, examples.
  - Steps: what Claude should do, in order.
  - Dish: the final output — file, website, schedule, rubric, data
    viz, whatever.
- Worked example up front: Becca's end-of-semester grading.
  Ingredients = raw grade exports from Canvas/Gradescope + Zoom
  attendance + My.Harvard upload template + interactively-built
  grading-policy doc. Steps = policy building, lateness calc,
  participation handling. Dish = ready-to-upload spreadsheets. Four
  hours → thirty minutes.
- Alt framing if it helps: you are writing a coursepack for a smart
  student who hasn't done the reading.
- Staff circulates and helps people scope down.

## 2:28 – 2:30 · Close (2 min)

- Photograph every card before people leave. These feed Madeleine,
  Marlon, and a few agents tonight as Day-2 homework input.
- People can leave whenever after the photo — the cards are the
  deliverable.

---

## What this version changes from the previous run

- Becca moves from cold open to the 20-minute hinge. The web-UI
  section now sets up *what is happening under the hood*; Becca shows
  *what that buys you*; the Cowork section then puts the same machinery
  into the room's hands.
- Context-window theory (memory, system prompt, Memento, the drawing)
  moves to **after** Becca, so it has a concrete artifact to point at
  rather than running cold.
- The population-pyramid artifact is now the explicit bridge from
  chat to Cowork — staged as a limit of staying in the browser.
- Cowork gets its full 20 minutes, split into setup, security, demo,
  and cheat sheet.
- Recipe card activity gets 13 minutes (up from 10), because Becca's
  worked example now lives inside the activity rather than as a
  separate beat.

## Open risks to watch

- **Madeleine's context-window drawing must happen live.** Last run it
  was referenced but never drawn — that lost the anchor image the
  rest of the day relies on.
- **Pre-stage the shared folder on demo machines.** Hunting for the
  download mid-session cost minutes.
- **Rename-without-confirmation incident.** Name it before the demo so
  it is a lesson, not a surprise.
- **Becca's arrival.** If she is delayed past 1:20, stretch the
  Shakespeare beat and add a second short failure example. Do not start
  the context-window section without her demo in the room — the section
  depends on it.
