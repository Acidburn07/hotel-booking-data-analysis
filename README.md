# Hotel Booking Data Analysis

Group final project for **Data Processing with Python** (HAMK, CA25 Customer Projects).

We analyse 1,000 hotel bookings from a City Hotel (Lisbon) and a Resort Hotel (Algarve), with arrival dates from July 2015 to August 2017. We look at booking patterns, cancellations, guest characteristics, prices and the differences between the two hotels.

**Deadline:** Wednesday 21 October 2026, 23:59. One member submits this repository's link on Moodle.

## Group members

| Member | Role | GitHub |
|---|---|---|
| Sandesh Bishokarma | TODO: role (A / B / C / D) | @Acid-Burn-del |
| TODO: full name | TODO | TODO |
| TODO: full name | TODO | TODO |
| TODO: full name | TODO | TODO |

Roles are described in [docs/WORKFLOW.md](docs/WORKFLOW.md). Tasks are tracked in [Issues](../../issues), grouped by [milestone](../../milestones).

## Research questions

1. TODO: categorical comparison, e.g. *Do cancellation rates differ between the City Hotel and the Resort Hotel?*
2. TODO: numerical variable, e.g. *Is lead time associated with cancellation?*
3. TODO: time pattern or relationship, e.g. *How do booking volume and average daily rate vary by arrival month for each hotel?*

## Repository contents

| Path | Contents |
|---|---|
| `data/hotel_bookings_final_project.csv` | Instructor-supplied source data. **Never edit or overwrite it.** It's included only so the notebook runs; it isn't one of our outputs. |
| `notebooks/Hotel_Booking_Final_Project.ipynb` | **Master notebook**, the version we submit. Only the integrator merges finished sections into it. |
| `notebooks/work/` | Each member's personal working notebook |
| `outputs/hotel_bookings_cleaned.csv` | Cleaned dataset (exported by the master notebook) |
| `outputs/hotel_booking_summary.csv` | Summary table (exported by the master notebook) |
| `report/` | Project report (.pdf or .docx) |
| `video/` | Link to the recorded group video |
| `docs/WORKFLOW.md` | How we work: roles, branches, merging, checklist |

## How to run

```bash
pip install -r requirements.txt
jupyter notebook notebooks/Hotel_Booking_Final_Project.ipynb
```

You can also open the notebook in VS Code and choose **Run All**. Before submitting, run **Restart → Run All** and check that it finishes with no errors and writes both CSV files to `outputs/`.

## Data source

António, N., de Almeida, A., & Nunes, L. (2019). Hotel booking demand datasets. *Data in Brief*, 22, 41–49. https://doi.org/10.1016/j.dib.2018.11.126. The course dataset is a 1,000-record sample of it with 20 selected variables.
