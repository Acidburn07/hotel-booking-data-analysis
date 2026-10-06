# How we work

## Roles

| Role | Owner | Notebook sections | Research question & charts | Report / video part |
|---|---|---|---|---|
| **A – Data lead** | Tanka Raj Aryal | 1 Context, 3 Load & inspect, 4 Cleaning log & cleaned copy | Supplies the clean data | Intro, dataset, cleaning decisions |
| **B – Profiling** | Sushant Koirala | 5 Derived variables, 6 Single-variable analysis (2 categorical + 2 numerical) | Numerical distribution chart | What the variables look like |
| **C – Relationships** | Sandesh Bishokarma | 7 Crosstab (hotel × cancellation) + groupby (lead time by cancellation) | RQ1 + RQ2, categorical and grouped charts | Findings for RQ1 and RQ2 |
| **D – Integrator** | Anup Kandel | 7 Time analysis, 9 Exports & verification, merging the master notebook | RQ3, time-based chart | Findings for RQ3, conclusion, recommendation |

Roles are split by complexity: High → Anup, Moderate → Sandesh, Easy → Sushant, remaining role → Tanka.

**Shared issues have a lead:** kickoff (#1) and conclusions (#13): Sandesh · final 4 charts (#11): Anup · report (#14): Tanka · video (#15): Sushant · setup (#2): everyone.

Each member also writes the *What can we observe?* text under their own charts. All four review the conclusions together.

## Day-to-day workflow in VS Code

Notebooks (`.ipynb`) are JSON files and are hard to merge in git. To avoid conflicts, **nobody edits the master notebook except the integrator.**

1. **First time:** in VS Code, open the Command Palette, run **Git: Clone**, and paste
   `https://github.com/Acidburn07/hotel-booking-data-analysis.git`.
2. Copy `notebooks/Hotel_Booking_Final_Project.ipynb` to `notebooks/work/<your-first-name>.ipynb`. Work only in your copy.
3. **Before you start each day:** pull (Source Control → `…` → Pull).
4. **When a section is done:** commit with a clear message, e.g. `Cleaning log: duplicates and zero-night decisions (#3)`. Then push.
   Writing `#3` links the commit to issue 3. Writing `Closes #3` closes that issue when it reaches `main`.
5. Comment on your issue to tell the integrator the section is ready. The integrator copies your finished cells into the master notebook.

Everyone can push straight to `main`, as long as you only touch your own file in `notebooks/work/`. If you prefer pull requests, make a branch named `<name>/<topic>` and open a PR.

## Notebook rules

- Keep the original DataFrame as `raw`, and do all cleaning on `clean = raw.copy()`.
- Read data from `../data/hotel_bookings_final_project.csv` and write exports to `../outputs/`.
- Every chart needs a title, axis labels, a legend if needed, the sample size (n), and a **What can we observe?** paragraph with no causal claims.
- Keep the printed output short. Show `head()` or a sample, not whole tables.
- Delete every `TODO` before submission.

## Before submitting (integrator)

- [ ] All 4 full names are in the README, the notebook and the report
- [ ] The master notebook passes **Restart → Run All** with no errors, and its outputs are saved in the file
- [ ] `outputs/` contains both CSVs, read back and verified in the notebook
- [ ] The report is in `report/`
- [ ] The video link is in `video/README.md` and is viewable by anyone with the link
- [ ] The repository is public. Test the link in a private browser window, then submit it on Moodle
