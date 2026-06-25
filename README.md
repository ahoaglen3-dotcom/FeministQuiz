# Feminism Is for Everybody — Reading Quiz

A self-contained, web-based reading-comprehension quiz for students, based on
bell hooks' *Feminism Is for Everybody: Passionate Politics* (South End Press, 2000).
The original book is included in this repo as `bell_hooks-feminism_is_for_everybody.pdf`.

## How to use it

Just open **`index.html`** in any web browser — no server, build step, or
internet connection required. It's a single HTML file with all styles and
logic embedded, so you can also email it to students or drop it on any
file share / learning-management system.

### For the classroom
- Share the file (or host it — see below) and have students take the quiz.
- Each attempt draws **10 questions at random from a 20-question bank**:
  **5 true/false** and **5 multiple-choice**, mixed together. Different
  students (and re-takes) generally see a different set.
- Students answer all 10 questions, then press **Submit answers**.
- They immediately get a score plus an explanation for every question, each
  grounded in a specific argument from the book.
- **Retake quiz** draws a fresh set of 10 questions for another attempt.

> Note: this is a self-check study tool. Scoring happens in the browser, so it
> is meant for learning and review rather than for secure/proctored grading.

## What it covers

The 20-question bank (10 true/false + 10 multiple-choice) spans the book's main arguments, including:
- hooks' definition of feminism ("a movement to end sexism, sexist exploitation, and oppression")
- Why feminism is not "anti-male," and how everyone is socialized into sexism
- Patriarchy and "white supremacist capitalist patriarchy"
- Reformist vs. revolutionary feminism, and "lifestyle feminism"
- Mass media's portrayal of feminism
- Class, race, and the limits of "sisterhood"
- Reproductive rights, beauty, work, violence, masculinity, spirituality, and visionary feminism

## Hosting it online (optional)

Any static host works. For example, with GitHub Pages: enable Pages for this
repo and point it at the branch root; `index.html` will be served as the site
home page.

## Editing the questions

All questions live in the `QUESTIONS` array inside the `<script>` block of
`index.html`. Each entry has a `type` (`"mc"` or `"tf"`), a `q` (question),
`options` (array of choices — true/false items use `["True","False"]`),
`answer` (0-based index of the correct option), and `explain` (feedback text).
Add, remove, or reword entries there and reload the page.

The number drawn from each group per attempt is controlled by the
`TF_PER_QUIZ` and `MC_PER_QUIZ` constants near the top of the app logic
(both default to `5`). Just make sure the bank still has at least that many
questions of each type.
