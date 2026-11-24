# NLP Analysis of Clinical Notes on SDOH and Chronic Diseases

**[📊 View the interactive dashboard](https://mufidaha.github.io/Natural-Language-Processing-of-Clinical-Notes-on-SDOH-and-Chronic-Diseases/)**

## The question
How often do hospital discharge notes document social determinants of health (SDOH) alongside chronic diseases?

## Key findings
- **86% of notes** mention at least one leading chronic disease term (pulmonary 57%, pneumonia 37%, coronary 36%, cancer 35%).
- Clear social-need terms are rare: **housing in 4 notes, transportation in 1, violence in 2** out of 327.
- **Data quality catch:** "physical" appears in 94% of notes, most likely from the "Physical Exam" section header, so raw keyword counts overstate SDOH documentation. Section detection and negation handling are the next step.

## Data
327 discharge summaries from a MIMIC-III NOTEEVENTS subset (course dataset). MIMIC requires credentialed access through [PhysioNet](https://mimic.mit.edu/docs/gettingstarted/), so the data is **not** included here; the dashboard shows only aggregate counts.

## Method
1. Load notes with pandas
2. Clean: remove punctuation, lowercase, replace line breaks
3. Tokenize (NLTK), remove stopwords and numbers → 13,887 unique words
4. Word frequencies (pandas `value_counts`, word cloud)
5. Document-term matrix with scikit-learn `CountVectorizer` (327 × 13,869)
6. A "counting appliance" that pulls SDOH and chronic-disease terms per note

## Files
- `MA_Natural_Language_Processing_of_Clinical_Notes_on_SDOH_and_Chronic_Diseases.ipynb` — notebook (Google Colab)
- `index.html` — dashboard (served by GitHub Pages)

## Tools
Python · pandas · NLTK · scikit-learn · WordCloud · Google Colab

## License
MIT
