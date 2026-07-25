
#  Global Health Data Analysis

### Where the world is healing — and where it isn't.

---

## What is this project about?

This project looks at health data from countries all over the world.

Simple question it answers:
**"Which countries are doing well in health, and which ones are struggling — and why?"**

4 health indicators studied:

- **Life Expectancy** — how long people are expected to live
- **Maternal Mortality** — mothers dying due to pregnancy issues
- **HIV** — how common HIV infections are
- **TB (Tuberculosis)** — how common TB infections are

Goal: clean messy real-world data → find patterns → turn numbers into charts anyone can understand.

---

##  Why does this matter?

Global averages hide a lot.

A country can "look fine" on paper. The real story is in the *differences* between nations.

This project shows where the world is improving in health — and where it's falling behind.

---

## Step 1: Cleaning the Data (Before Telling the Story)

Real-world data is messy. Had to clean it before analyzing it.

- **Fixed column names** — no extra spaces, all lowercase, underscores instead of spaces
  (e.g. `Life Expectancy ` → `life_expectancy`)
- **Removed duplicate rows** — same data wasn't counted twice
- **Filled missing values** — many countries don't report every year, so gaps were filled smartly:
  - Next available value for that country (forward fill)
  - If not available, previous value (backward fill)
  - If neither works, median value (fallback)
- **Removed outliers** — extreme, unusual values removed using **IQR (Interquartile Range)**
  Think: removing the "weird one-off" numbers that don't fit the real trend
- **Sorted data properly** — by country + year, so filling made logical sense
  (2010 data shouldn't be filled using 2020 numbers)

---

##Step 2: Visualizing the Data (Turning Numbers into Charts)

Once the data was clean, I created **8+ charts** to visually explore the story hidden in the numbers:

1. **Life expectancy trend over the years** (global average) — is the world living longer overall?<img width="630" height="349" alt="Screenshot 2026-07-25 at 7 10 05 PM" src="https://github.com/user-attachments/assets/f3e6c967-3712-4b19-849b-2d6ec1571f30" />


2. **Maternal mortality decline curve** — is maternal death decreasing over time?<img width="629" height="357" alt="Screenshot 2026-07-25 at 7 10 12 PM" src="https://github.com/user-attachments/assets/b12b6152-86ff-4e73-8e5d-9b5fa4d5c294" />


3. **HIV & TB distribution charts** — how spread out or concentrated are these diseases?<img width="1116" height="443" alt="Screenshot 2026-07-25 at 7 10 20 PM" src="https://github.com/user-attachments/assets/038314eb-8291-4257-8c26-13e9b8235b6f" />

4. **Top 5 countries by life expectancy** — who's leading, and by how much?<img width="953" height="469" alt="Screenshot 2026-07-25 at 7 04 19 PM" src="https://github.com/user-attachments/assets/f4177da2-e432-438c-a540-7f34038e667a" />


5. **Top 10 countries by TB cases** — which nations are hit hardest by TB?<img width="677" height="598" alt="Screenshot 2026-07-25 at 7 04 33 PM" src="https://github.com/user-attachments/assets/8258d727-883e-426b-8932-67def9d2d60c" />


and many more like :

7. **Maternal mortality vs. life expectancy** — do they move together?
8. **Correlation chart** — which health factors are most strongly linked to life expectancy?

---

##Key Insight 

> Countries with the **highest life expectancy** also have the **lowest maternal mortality** and **well-controlled TB**.




##  Tools Used

| Tool | What it was used for |
|------|----------------------|
| **Python** | The programming language used for everything |
| **Pandas** | Cleaning and organizing the data |
| **NumPy** | Handling numbers and calculations |
| **Matplotlib** | Creating charts and graphs |
| **Seaborn** | Making charts look better and more insightful |

---

### Full Notebook

You can view the complete analysis, code, and charts here:

 [Open Google Colab Notebook](https://colab.research.google.com/drive/1np79jAvOaiTBFFahSwwbfbLff3L2b022?usp=sharing)

---

##  In One Line

**This project cleans messy global health data and uses visual storytelling to show that strong maternal healthcare and TB control go hand-in-hand with people living longer, healthier lives.**
