# USER_GUIDE.md — How to Use ProfessorGPT

## Getting Started

Once the app is running (see SETUP.md), you'll see the ProfessorGPT interface with six tabs across the top.

---

## Step-by-Step Workflow

### 1. Upload Tab — Start Here

This is always your first step.

**Option A — Paste a Transcript**
1. Copy your lecture transcript from any source (Canvas, Zoom auto-captions, class notes, PDF)
2. Paste it into the text area
3. Click **✨ Process Lecture**

**Option B — Upload a Text File**
1. Switch to "Upload file"
2. Click the upload button and select a `.txt` file
3. Click **✨ Process Lecture**

**Option C — Try a Demo**
- Click **🧠 ML Fundamentals** or **📈 Finance Basics** to load a sample lecture
- Great for testing the app before using your own material

**What happens next:** The app calls Claude AI 4 times in parallel to generate all your study materials. This takes about 20–30 seconds. A progress bar shows status.

---

### 2. Notes Tab

View your AI-generated structured notes:

- Notes are organized with **headers** for major topics and **bullet points** for details
- Click **↻ Regenerate** to get a fresh version with different phrasing
- Click **⬇ Download** to save the notes as a `.md` (Markdown) file, which opens in any text editor or Notion

**Pro tip:** The notes summarize key ideas — use them alongside your original transcript, not as a replacement.

---

### 3. Flashcards Tab

10 key terms from your lecture, displayed as interactive cards:

- Click any card to **reveal the definition**
- Click again to flip back
- Cards are arranged in a 2-column grid
- Use **↻ Regenerate** to get different terms

**Study tip:** Go through all cards once, then focus on the ones you hesitate on.

---

### 4. Q&A Tab

8 practice questions with hidden answers:

- Click on any question to **expand the full answer**
- Questions range from definition-level to application-level
- Use **↻ Regenerate** for a new set of questions

**Study tip:** Cover the answer and try to answer each question out loud first — active recall is more effective than passive reading.

---

### 5. Ask AI Tab — RAG-Powered Chat

An AI tutor that knows your lecture:

- Type any question in the chat box and press **Enter** or click **Send**
- The AI answers using **only your lecture content** (RAG grounding)
- If a question isn't covered in the lecture, the AI will say so honestly
- Your conversation history is preserved — you can ask follow-up questions
- Click **🗑 Clear Chat** to start a fresh conversation

**Example questions to try:**
- "Can you explain [concept] in simpler terms?"
- "What's the difference between [A] and [B]?"
- "Give me an example of [topic] from the lecture"
- "What are the most important things to remember?"

---

### 6. Exam Prep Tab

A 6-question multiple choice practice exam:

1. Read each question carefully
2. Select your answer using the radio buttons
3. After answering all questions, click **📊 Grade My Exam**
4. See your score and a question-by-question review with explanations
5. Click **↻ New Exam** to generate a completely different exam

**Grading:** 80%+ = Great job · 60–79% = Review missed questions · Below 60% = Revisit notes and flashcards

---

## Tips for Best Results

- **Longer transcripts = better outputs.** Aim for at least 500 words.
- **Clean transcripts work best.** Remove auto-caption errors before pasting if possible.
- **Regenerate freely.** Each regeneration gives a slightly different perspective on the material.
- **Use all 5 tools together** — notes for reference, flashcards for memorization, Q&A for comprehension, chat for clarification, exam for testing.

---

## Frequently Asked Questions

**How long can my transcript be?**  
Up to ~4,000 words is processed optimally. Longer transcripts are automatically trimmed to the first 4,000 words for generation — the RAG chat will still search across the full transcript.

**Is my transcript stored?**  
No. Your transcript is held in your browser session only and deleted when you close the tab.

**Can I use this for any subject?**  
Yes! ProfessorGPT works for any lecture-style content — STEM, business, law, medicine, humanities.

**The AI gave a wrong answer in chat. What should I do?**  
Always cross-reference with your original lecture notes. Click **↻ Regenerate** on the relevant tool, or ask the chat to clarify.
