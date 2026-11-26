# Which Place Has the Most Homelessness?

Math with real local data: students check every number against its source, then compare six places by raw count and by rate per 10,000 people.

**Live site:** <https://jontaylormed.github.io/counts-vs-rates/>

**Source:** <https://github.com/jontaylormed/counts-vs-rates>

**Site created by Claude and Jon Taylor.**

[![License: CC BY-NC-SA 4.0](https://img.shields.io/badge/License-CC%20BY--NC--SA%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc-sa/4.0/)

---

## What it does

One 45-minute lesson in five steps. Students compare King County, WA with five other places, using the January 2024 Point-in-Time counts.

| Step | What the student does |
|---|---|
| 1. Meet the data | Sees the six raw counts, picks which place has "the most," and says why |
| 2. Verify | Opens each place's HUD report and finds the total there, with a "show me where" guide and a fallback for blocked sites |
| 3. Organize | Builds two bar charts by choosing the axis scale and setting each bar. Calculates each rate per 10,000 people with a built-in calculator |
| 4. Analyze | Compares the two rankings and writes what the data can and cannot say |
| 5. Reflect | Answers optional reflection prompts, then saves the work as a PDF to hand in |

The repository also holds:
- `slides.html`, slides to launch and close the class (press N for speaker notes);
- `lesson-plan.md`, the teacher guide with timing, answer key and discussion notes;
- `sources.md`, every figure with its source, link, date checked and a search phrase a student can type to find it.

## Who it's for

High school, grades 9–12.

Common Core State Standards for Mathematics:

| Standard | What it asks |
|---|---|
| HSN.Q.A.1 | Use units to understand problems, and choose and interpret the scale and origin in graphs |
| HSN.Q.A.2 | Define appropriate quantities for descriptive modeling |
| HSN.Q.A.3 | Choose a level of accuracy that fits the limits of the measurement |
| MP3 | Construct viable arguments and critique the reasoning of others |
| MP4 | Model with mathematics |

Reviewed along the way: 6.RP.A.1 (ratio language), 6.RP.A.2 (unit rate), 6.RP.A.3 (ratio and rate reasoning) and 7.RP.A.3 (multistep ratio problems).

## How it teaches

- **Check every claim.** Students find each count in the original government report before they use it. The lesson names the exact row and column, and it tells students when they've found a nearby number instead, such as the shelter-only column.
- **Structure before numbers.** Students commit to an answer from the raw counts first. Then they build the rate themselves and see whether the ranking changes.
- **Students build it, and students conclude.** No finished chart is handed out: students choose each chart's scale and set each bar. The lesson presents data and questions, not opinions, and shows how the count was made and who it may miss.
- **Care for students.** The lesson uses person-first language. It never asks students about their own circumstances, and sharing a reflection is always optional.

## How the math was checked

- **Checks page:** [`checks.html`](https://jontaylormed.github.io/counts-vs-rates/checks.html) runs 120 checks in the browser. All 120 pass. It compares:
  - every count, population, date and report link in the lesson with `sources.md` (Data set 4, table 4a);
  - each answer-key rate and both rankings in `lesson-plan.md` with those numbers;
  - the lesson's rate checker, which must accept the right rate and name common slips, such as forgetting × 10,000 or dividing upside down;
  - the page itself, for outside requests and stored data.
- **Sources:** every figure in `sources.md` was read from the original source (HUD, the U.S. Census Bureau, KCRHA) and recorded with its link and the date it was checked, November 16, 2026.
- **Hand check:** each rate was recalculated by hand, from 20.3 per 10,000 (Maricopa County) to 101.4 (San Francisco). The U.S. rate of 22.7 rounds to HUD's published "about 23 of every 10,000."
- **Known limits:**
  - A Point-in-Time count is one night in January and is an undercount.
  - Counting methods differ from place to place.
  - Matching each HUD area to a county is a reading of the names, not a HUD statement.
  - The U.S. count includes territories, but the U.S. population used covers only the 50 states and DC.
  - The lesson teaches all of these limits, and `sources.md` lists them in full.

## Accessibility

- **Keyboard:** every step works with the keyboard. Chart bars are sliders: the arrow keys move them, and each bar also has a box for typing its value. Dialogs close with Escape, and focus outlines are visible.
- **Screen readers:** feedback is announced through a live region. Each chart bar reads out its value.
- **Contrast:** text colors are 5.4:1 or higher against their backgrounds, and form borders are about 3:1.
- **Motion:** the only motion is a short progress-bar slide.
- **Language and text size:** the lesson uses plain language. There is no separate text-size setting; the page follows browser zoom.
- **Devices:** it is built to run on a school laptop or Chromebook.

## Privacy

- No login, no tracking and no cookies.
- Nothing a student types is sent anywhere.
- Work is kept only in that browser tab and is erased when the tab closes. It is never kept on the device after that, so a shared laptop holds nothing for the next student.
- A student's name goes only onto their PDF and is never saved.
- The page loads nothing from other sites. Links to government reports open only when a student clicks them.

## Running it

Open `index.html` in any modern browser.

`checks.html` reads the other files, so open it from the live site or any local web server, not as a file.

To use it with a learning platform, link to the live site and have it open in a new tab. Don't paste the code into a course page: many platforms strip the code the lesson needs.

**Publishing:** GitHub Pages, deployed from the `main` branch at the repository root. There is no build step.

## License

[CC BY-NC-SA 4.0](LICENSE). Free to share and adapt for non-commercial use, with credit, under the same license. The data comes from U.S. government and King County public sources, cited in `sources.md`.
