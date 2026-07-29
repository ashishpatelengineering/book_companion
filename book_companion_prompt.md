# Prompt: Build a Study Companion HTML for [BOOK TITLE]

I want to learn from [BOOK TITLE] by [AUTHOR]. Please build me an interactive
HTML study companion, one chapter at a time, following all of these rules.

**I'm attaching a working HTML template (`book_companion_template.html`)**
that already has the CSS, layout, collapsible sidebar, and JavaScript
rendering logic built and tested. Use it as the starting shell, don't
rebuild the design from scratch. It contains one placeholder chapter
showing the exact data shape expected for slides and quiz questions,
replace that placeholder with real chapter content, and duplicate the
`ch1_slides` / `ch1_quiz` pattern (renamed `ch2_`, `ch3_`, etc.) for each
additional chapter, registering each one in the `chapters` array at the
bottom.

## Ground rules (non-negotiable)

**Content**:
Read the chapter, understand the ideas, then teach them. Facts, numbers, and named
examples/studies can and should be cited precisely. You don't have to copy word by word but follow the essence of the book.
But you should follow the book strictly. 

**Accuracy**: Before writing any slide content, actually read the source
chapter (I'll upload it, or you can find the real text some other way).
Every number, stat, and named example must trace back to something you
actually read, not something you're inferring or rounding from memory.
Flag clearly if you're illustrating a concept with your own example instead
of the book's.

**Pedagogy**: Think like a professor preparing a lecture after reading the
chapter, not like someone summarizing it into bullet points. Teach the
concepts in a sensible order, with clarity as the priority.

## Format rules

- One font family only. Use size and weight for hierarchy, not different
  typefaces. No em dashes anywhere in the text.
- Default to cards, short lists, and callout boxes over paragraphs. A slide
  with 2+ paragraphs and no visual structure is a fail, restructure it.
- No sentence over ~30 words. One idea per sentence.
- Every slide needs at least one concrete anchor: a real number, a named
  example, a worked mini-example, or a quote. Abstract claims with nothing
  to hook onto are the first thing people forget, don't leave any in.
- Diagrams: build small custom SVGs for the 2-4 concepts per chapter that
  are genuinely spatial/relational (a mechanism, a pipeline, a comparison).
  Don't force a diagram where a text card would teach it better. Keep
  colors and label styles consistent across every diagram in the file.
- Quiz per chapter: multiple choice and multi-select only (self-grading,
  works offline, no LLM needed to check answers). No short-answer/free-text
  questions. Include a mix of recall questions and applied "scenario"
  questions that test whether a concept can be used, not just remembered.
  Cover every slide's core idea at least once.

## Structure

- One HTML file, all chapters together, not a separate file per chapter.
- A collapsible sidebar listing all chapters (so it scales past 2-3
  chapters without eating reading width). Clicking a chapter shows that
  chapter's slide deck; a Lesson/Quiz toggle switches modes within it.
- A quiz "Retake quiz" button that resets all answers cleanly.
- Must render correctly with no internet connection, no external fonts,
  scripts, or API calls.

## Process

1. Confirm the chapter list/table of contents with me first.
2. For each chapter: read the actual source content (not just headings),
   then draft slides + quiz.
3. Before finalizing, self-check: (a) does every claim trace to the source,
   (b) does every slide have cards/lists instead of paragraph walls,
   (c) is any sentence too long, (d) does every slide have a concrete
   anchor. Fix anything that fails before showing me.
4. Validate the file (balanced code, no leftover placeholder text, working
   diagrams) before sharing it.
5. Build one chapter at a time so I can review before we continue.

Let's start by confirming the chapter list.
