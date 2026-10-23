# Australia’s Tyre Trade Analysis

A beginner Python project exploring Australia’s trade in rubber tyres, treads and tubes with 22 trading partners from 2006 to 2025.

## Research Question

With which trading partners does Australia have a tyre-trade deficit, surplus or balance, and how have these balances changed over time?

## Data

The project uses DFAT trade data for SITC 625: rubber tyres, treads and tubes.

- Period: 2006–2025
- Values: Australian dollars in thousands
- Trade balance: Australian exports minus Australian imports

Partners with any missing year were excluded from each complete-data table. Their records were saved separately. Missing values were not treated as zero trade.

| Stage | Exports | Imports |
|---|---:|---:|
| Partners assessed | 167 | 134 |
| Partners with complete data | 38 | 41 |
| Partners excluded for missing data | 129 | 93 |

An inner merge retained 22 partners with complete import and export data across all 20 years.

## Analysis

The notebook covers:

- Cleaning the raw export and import files.
- Examining missing data and retaining excluded records separately.
- Matching partners and calculating annual trade balances.
- Classifying 2025 balances as surplus, deficit or balanced.
- Counting surplus, deficit and balanced years for each partner.
- Visualising trends with interactive charts and a country selector.
- Comparing trade balances between 2006 and 2025.

## Key Findings

- Australia recorded deficits with 20 of the 22 matched partners in 2025. Only New Zealand and the United Arab Emirates recorded surpluses.
- Australia recorded deficits with 16 partners in every year examined.
- New Zealand had the most surplus years: 19 out of 20.
- No partner recorded an exactly balanced trade position in any year.
- China had the largest deficit in 2025, at approximately AUD 1.187 billion, and the largest widening of its deficit since 2006.
- Between 2006 and 2025, balances became more negative for 14 partners and more positive for eight.

All balances are reported from Australia’s perspective.

## Tools

- Python
- pandas
- Plotly
- ipywidgets
- Jupyter Notebook / VS Code

## Running the Project

1. Download or clone this repository.
2. Install the Python packages imported by the notebook.
3. Place `tyre_export.csv` and `tyre_import.csv` in the notebook’s working directory.
4. Open the notebook in Jupyter or VS Code with notebook support.
5. Run the cells from top to bottom.

For the interactive country selector, enter country names separated by commas and click Plot. Names must match the dataset’s spelling and capitalisation.

The selector requires a running Python kernel; it will not work in GitHub’s static notebook preview. The selector code currently uses Plotly’s `vscode` renderer, which may need changing for another environment.

## Limitations

The 22 matched partners form a selected subset with complete data. Findings do not represent all Australian tyre trade.

Trade values are not adjusted for inflation. The analysis describes patterns and associations over time but does not establish their causes. Comparing 2006 with 2025 also does not capture fluctuations between those endpoints.

## Learning and AI Assistance

This is a self-directed learning project developed to practise pandas, data analysis and interactive visualisation.

I directed the research questions and project scope. I used ChatGPT/Claude extensively to explain unfamiliar Python and pandas syntax, generate portions of the implementation, troubleshoot errors and draft documentation. Some analytical approaches were also developed through these discussions.

I worked through the suggested code, questioned unexpected results and checked the main findings against the tables. The project reflects work completed with AI assistance while I continue developing the ability to implement these techniques independently.
