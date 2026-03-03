# PetFinder Adoption Speed - EDA and Preprocessing

Exploratory data analysis and dataset preparation for predicting pet adoption speed, using the RAF PetFinder dataset. Combines tabular data, sentiment features, and image analysis.

---

## Dataset

- **Source:** RAF-PetFinder-dataset (GitHub)
- **Target variable:** AdoptionSpeed (classes 0-4, stratified split)
- **Data types:** Tabular CSV + pet images

---

## Tech Stack

- **Python 3** - core language
- **Pandas** - data loading, merging, cleaning
- **NumPy** - numerical operations
- **Matplotlib / Seaborn** - visualizations
- **Pillow (PIL)** - image loading and pixel analysis
- **scikit-learn** - stratified train/val/test split

---

## Notebook Structure

1. **Data Loading** - load train.csv and train_sentiment.csv
2. **Merge** - join sentiment features onto main dataset on PetID
3. **Feature Dropping** - remove irrelevant columns (Name, State, RescuerID, VideoAmt)
4. **Train/Val/Test Split** - 80/10/10 stratified split by AdoptionSpeed
5. **Image Loading** - load up to 3 images per pet
6. **Tabular EDA**
   - Null value analysis
   - Age distribution histogram
   - Dog vs cat counts
   - Adoption speed by age and type
   - Sterilization and vaccination vs adoption speed
   - Fee vs quantity scatter plot
   - Photo count vs adoption speed
   - Mean and variance per numeric column
7. **Image EDA**
   - Brightness distribution across 300 pet images
   - RGB channel distribution per image

---

## Split Strategy

Stratified by AdoptionSpeed to preserve class balance:

| Split | Proportion |
|-------|------------|
| Train | 80% |
| Val   | 10% |
| Test  | 10% |

---

## How to Run

```bash
pip install pandas numpy matplotlib seaborn pillow scikit-learn
jupyter notebook DubokoUcenje_PrviProjekat.ipynb
```
