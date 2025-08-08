# NLP Analysis of Clinical Notes on SDOH and Chronic Diseases

This project uses Natural Language Processing (NLP) techniques to analyze unstructured clinical discharge notes in order to identify patterns related to Social Determinants of Health (SDOH) and chronic diseases. For additional information on chronic diseases, visit CDC website, https://www.cdc.gov/chronicdisease/about/index.htm.

In terms of data source for this project, the MIMIC-III (Medical Information Mart for Intensive Care III) modified table, NOTEEVENTS, will be used. For purposes of this project, table name, NOTEVENTS, has been changed to ClinicalNotes.

## 📘 Project Description

The notebook processes the `ClinicalNotes.csv` dataset, which includes discharge summaries containing variables:
- `SUBJECT_ID`: Unique patient identifier
- `HADM_ID`: Hospital admission ID
- `TEXT`: Unstructured clinical notes

Using Python NLP libraries, we clean and vectorize the notes and use a custom tool — `countingappliance` — to extract and count occurrences of key terms linked to SDOH and chronic health conditions.

> ⚠️ The dataset is not included due to licensing restrictions. Please refer to [MIMIC-III Access Instructions](https://mimic.mit.edu/docs/gettingstarted/) to obtain the dataset.


## 🚀 Technologies Used

- Python
- Pandas
- NLTK / spaCy
- scikit-learn
- Google Colab

## 📈 Potential Extensions

- Train ML models for prediction tasks
- Use embeddings for semantic analysis
- Analyze other free-text datasets

---

## 📄 License

This project is licensed under the MIT License.
