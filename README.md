# Data Science Projects

A portfolio of data science work by **Trevor Kauyu**: Data Quality & AI Assurance Engineer.

Machine learning, NLP, computer vision and business-intelligence dashboards, mostly on Zimbabwean data. Each project is documented the same way: the problem, the method, the **real results**, and an honest list of limitations, because a model you can't evaluate is a model you can't trust.

## Projects

| # | Project | What it does | Stack |
|---|---|---|---|
| 01 | [Loan Approval Prediction](projects/01-loan-approval-prediction/) | Predicts loan approval for a commercial bank and compares four classifiers. Includes an assurance review showing the best model only matches the always-approve baseline | Python · pandas · scikit-learn · XGBoost |
| 02 | [Mobile Money Sentiment & Market Share](projects/02-mobile-money-sentiment-analysis/) | MSc dissertation: 409k tweets cleaned to 28k customer complaints about EcoCash, scored with VADER, compared with regulator subscriber data, and an LSTM-CNN subscriber forecast | Python · NLTK (VADER) · TensorFlow/Keras · pandas |
| 03 | [COVID-19 Chest X-Ray Classification](projects/03-covid-19-chest-xray-classification/) | Transfer learning with VGG16 to classify chest X-rays as COVID-19, pneumonia or normal | Python · TensorFlow/Keras · OpenCV |
| 04 | [San Francisco Food Inspection Risk](projects/04-sf-food-inspection-risk/) | IBM Data Science capstone: explores 6,499 restaurant inspections, maps them, and tries KNN and logistic regression to predict the risk category | Python · pandas · scikit-learn · Folium · Foursquare API |
| 05 | [ZimParks Biodiversity Dashboard](projects/05-zimparks-biodiversity-dashboard/) | R Shiny dashboard mapping Zimbabwe's national parks with species tables, trees and charts (demo species data) | R · Shiny · Leaflet · tidyverse |
| 06 | [Zimbabwe Health Facility Locator](projects/06-zim-health-facility-locator/) | Live R Shiny app that helps people find clinics, pharmacies and hospitals in Zimbabwe | R · Shiny · Leaflet |
| 07 | [Zimbabwe Mental Health Dashboard](projects/07-zim-mental-health-dashboard/) | Power BI survey dashboard: stress triggers, diagnosis, help barriers by age, gender and occupation | Power BI · DAX · Power Query |
| 08 | [Tour de France Dashboard](projects/08-tour-de-france-dashboard/) | Maven Analytics challenge: 109 Tours of winners, stages, speeds and finishers | Power BI · DAX · Power Query |

## Principles behind every project

1. **Honest results.** Only numbers the notebook actually produced, compared with a simple baseline, with the limitations stated next to them.
2. **Data quality first.** Cleaning, de-duplication and filtering decisions are documented, because they shape every result.
3. **Privacy by default.** No personal data, account numbers or credentials in the repository. Notebook outputs are scrubbed before publishing (see [docs/CONVENTIONS.md](docs/CONVENTIONS.md)).
4. **Credit where due.** Datasets, courses and code adapted from others are named with links.
5. **Reproducible where possible.** Each README lists the environment and where the data comes from; where data can't be published, it says so.

## Repository layout

```
data-science-projects/
├── projects/
│   └── NN-project-name/        # one self-contained folder per project
│       ├── README.md           # problem, method, results, limitations
│       ├── notebooks/          # Jupyter notebooks (outputs scrubbed of personal data)
│       ├── app/                # Shiny apps
│       ├── dashboard/          # Power BI exports
│       ├── data/               # small, publishable data only
│       ├── report/             # reports and slides
│       └── assets/             # charts and screenshots used in the README
├── templates/
│   └── PROJECT_README.md       # starting point for new projects
└── docs/
    └── CONVENTIONS.md          # naming, privacy and documentation rules
```

## Adding a new project

1. Copy `templates/PROJECT_README.md` into `projects/NN-short-name/README.md`.
2. Add notebooks, apps or exports, and run the privacy checklist in [docs/CONVENTIONS.md](docs/CONVENTIONS.md) on the outputs.
3. Put the charts the README uses in `assets/`.
4. Add a row to the **Projects** table above.

## More work

- [AI Workflow Automation](https://github.com/Travoltah/ai-workflow-automation): n8n + Claude workflows with evaluation suites
- [QA Test Automation](https://github.com/Travoltah/qa-test-automation): Selenium, Postman and test planning

## Contact

- Portfolio: [trevor-kauyu.vercel.app](https://trevor-kauyu.vercel.app)
- LinkedIn: [linkedin.com/in/trevor-kauyu](https://www.linkedin.com/in/trevor-kauyu/)

## License

Code and documentation: [MIT](LICENSE). Datasets, papers and images from third parties keep their own licences; each project README names the source.
