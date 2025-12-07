# Mental Health in Tech
### Group D9. Hendrik Jaks, Robin Juul, Karel Allik
<br>

## Motivation
Since tech industries continue to shape the future of work and society, it is important to take note of the mental health of the people working in the industry.  It is widely known that working in tech often involves long hours, high cognitive loads, and remote work. Thus, it is critical to understand the well-being of the workforce. These factors can contribute to burnout, anxiety, and the development of mental health disorders. By analyzing this data and expanding it, we can provide insight into mental health trends and additionally identify the factors that strongly correlate with mental health disorders. 

## Business Goals
- Raise awareness of mental health in the tech industry.
- Help identify risk factors and reduce stigma surrounding mental health.
- Track long-term trends in mental health in the tech industry.

## Data Mining Goals  
 1. Expand the Kaggle dataset (Mental Health in the Tech Workplace in 2014, 2016 - 2019 [1]) with additional data from the years 2020-2023 [2]
 2. Predict whether a respondent has a mental health disorder (Random Forest / Gradient Boosting / Kernel SVM / Deep Learning with Sentence-BERT)
 3. Build a classifier that detects stigmatizing vs supportive language in text answers (RoBERTa) and analyse the result on a yearly basis.
<br>

## Repository Structure
The main components are:  
- `data/`
   - `raw/`
     Contains original unprocessed files:
     - the Kaggle SQLite database (2016–2019),
     - individual csv files for 2020-2023,
     - and more
  - `intermediate/`
    Contains intermediate files that are used to save intermediate results  
  - `processed/`
    Contains the cleaned and combined dataset used for analysis and stigmatizing or supportive language predictions.
- `notebooks/`
    Includes Jupyter notebooks for:
    - loading Kaggle data from SQLite,
    - Goal 1 (cleaning and combining datasets),
    - Goal 2 (mental health disorder prediction),
    - Goal 3 (language classification: stigmatizing vs supportive).
- `figures/`
   Includes pdf-files containing graphs.
- `models/`
   Contains our pretrained model for stigmatizing or supportive language predictions.

<br>
<br>

## To replicate our analysis:

**1. Clone the repository.**  
`git clone https://github.com/karelallik/Mental-Health-in-Tech.git`

**2. Load Kaggle data from SQLite**  
Open the notebook `load_kaggle_data.ipynb` and run all cells.  
This will convert the Kaggle SQLite data (2016–2019) into a raw CSV file.

**3. Clean and combine the datasets**  
Open the notebook `data_cleaning.ipynb` and run all cells.  
This notebook cleans the datasets and merges the 2016–2019 data with the 2020–2023 data.

**4. Run Goal 2: Mental health disorder prediction**  
Open the notebook `goal2_predict_mental_health_disorder.ipynb`.   
Install the following packages in the first cell. Then run the rest of the cells to reproduce the prediction results. 

**5. Run Goal 3: Language classification (stigmatizing vs supportive)**  
Open the notebook `goal3....ipynb`.  
Install the following packages in the first cell.  
Run all cells to train the RoBERTa classifier and reproduce the yearly analysis.
NB! If You want to use the Gemini-labeling, your own API key must be used (paste in place of `YOUR_API_KEY`).



### Links:
[1] https://www.kaggle.com/datasets/anth7310/mental-health-in-the-tech-industry/data <br>
[2] https://osmhhelp.org/research.html<br>
