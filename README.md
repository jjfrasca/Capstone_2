Predicting US Vacancy Rates by Zip Code
==============================

Springboard Capstone 2

**the problem**
*What is the current vacancy rate in a certain zip code?*

Lack of specific current vacancy rate data hampers real estate investors ability to definitively know a key factor in their decision for where to invest. Currently many investors rely on local knowledge of an area - ie. local real estate agents, property managers etc. for this knowledge - so the info is hard to get and hard to tell if accurate.  There is vacancy rate data for the US as a country in up to the current year on the Federal Reserve of Economic Development website (FRED). There is also vacancy rate data by zip code available up to 2018 through the American Housing Community, but currently there does not seem to be vacancy rate data by zipcode for the current year.

**the approach**
The goal was to predict current vacancy rate by zip code using housing market indicators and other econometrics.

**the findings** 
- I found vacancy rates had different trends/correlations between variables depending on the different time periods. This was interesting to see that during different economic periods in US history the variables had very different relationships.
- The best performing model was the Random Forest, with R2 on the test set of  .92. However Adjusted R2 on test data showed a score of .78 which seems to suggest some of performance is skewed by the large number of variables. Not only did this model have the highest performance, it also took shorter to run compared to the models where hyperparameters were optimized
- From the Lasso Regression model it seems that the top 10 features in predicting vacancy rate comprise:  zip code, rent price, year, size rank, home price, State(s).
- When examining projected 2020 vacancy rate data, results seem to suggest tourist areas near beaches have the highest vacancy rates while wealthier, faster growing suburbs outside major cities have the least vacancy. This seems to make sense generally and also with trends witnessed during the COVID-19 Pandemic.
- When examining vacancy adjusted rent/price ratios, a metric used for rental real estate investment, results seem to show that places that may be good to invest are in cities with low home prices, relatively higher vacancy rates. More suburban areas with higher home prices (especially in CA), may be less desireable potential areas to invest in real estate. But real estate investors should also be sure to consider other variables when choosing an area to invest (ie. crime rate, unemployment, population and job growth etc.)


Project Organization
------------

    ├── LICENSE
    ├── Makefile           <- Makefile with commands like `make data` or `make train`
    ├── README.md          <- The top-level README for developers using this project.
    ├── data
    │   ├── external       <- Data from third party sources.
    │   ├── interim        <- Intermediate data that has been transformed.
    │   ├── processed      <- The final, canonical data sets for modeling.
    │   └── raw            <- The original, immutable data dump.
    │
    ├── docs               <- A default Sphinx project; see sphinx-doc.org for details
    │
    ├── models             <- Trained and serialized models, model predictions, or model summaries
    │
    ├── notebooks          <- Jupyter notebooks. Naming convention is a number (for ordering),
    │                         the creator's initials, and a short `-` delimited description, e.g.
    │                         `1.0-jqp-initial-data-exploration`.
    │
    ├── references         <- Data dictionaries, manuals, and all other explanatory materials.
    │
    ├── reports            <- Generated analysis as HTML, PDF, LaTeX, etc.
    │   └── figures        <- Generated graphics and figures to be used in reporting
    │
    ├── requirements.txt   <- The requirements file for reproducing the analysis environment, e.g.
    │                         generated with `pip freeze > requirements.txt`
    │
    ├── setup.py           <- makes project pip installable (pip install -e .) so src can be imported
    ├── src                <- Source code for use in this project.
    │   ├── __init__.py    <- Makes src a Python module
    │   │
    │   ├── data           <- Scripts to download or generate data
    │   │   └── make_dataset.py
    │   │
    │   ├── features       <- Scripts to turn raw data into features for modeling
    │   │   └── build_features.py
    │   │
    │   ├── models         <- Scripts to train models and then use trained models to make
    │   │   │                 predictions
    │   │   ├── predict_model.py
    │   │   └── train_model.py
    │   │
    │   └── visualization  <- Scripts to create exploratory and results oriented visualizations
    │       └── visualize.py
    │
    └── tox.ini            <- tox file with settings for running tox; see tox.readthedocs.io


--------

<p><small>Project based on the <a target="_blank" href="https://drivendata.github.io/cookiecutter-data-science/">cookiecutter data science project template</a>. #cookiecutterdatascience</small></p>
