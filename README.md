# Data Spaces as Enablers of AI

## Project Overview

This project demonstrates how data spaces can enable Artificial Intelligence by turning separate organizational datasets into governed, combined, and AI-ready data.

The notebook uses energy data as a practical example. Electricity consumption, wind generation, and solar generation data are treated as if they are owned by different organizations. A simplified data space connector is then used to control access, apply usage policies, harmonize the data, and combine it for analysis.

The goal is not to build a full machine learning model, but to show how data spaces prepare separate datasets for AI analytics and forecasting.

## Dataset

The dataset used is the German daily energy time series dataset from Open Power System Data (OPSD). It contains daily records of:

- Electricity consumption
- Wind power generation
- Solar power generation

The data covers Germany’s electricity system from 2006 to 2017.

Dataset source:

```text
https://raw.githubusercontent.com/jenfly/opsd/master/opsd_germany_daily.csv
```

Original reference:

```text
https://open-power-system-data.org/
```

## Project Objectives

The objectives of this project are to:

1. Demonstrate how data may exist in separate organizational silos.
2. Simulate a simple data space connector.
3. Apply access control and usage policies.
4. Harmonize data from different providers.
5. Combine the datasets into one data-space view.
6. Visualize how combined data becomes more useful for AI analytics.
7. Show how data spaces support AI readiness.

## Simulated Data Providers

The notebook splits the dataset into three simulated providers:

| Provider | Data Held |
|---|---|
| GridOperatorDE | Electricity consumption |
| WindEnergyCo | Wind generation |
| SolarEnergyCo | Solar generation |

This represents a real-world situation where different organizations each hold part of the data needed for AI analysis.

## Installation Requirements

To run this project locally, Python 3.8 or later is recommended.

Install the required Python libraries:

```bash
pip install -r requirements.txt
```

If you are using Google Colab, most of these libraries are already installed.

## How to Run the Project

### Option 1: Run with Jupyter Notebook

1. Download or clone the project folder.
2. Open a terminal or command prompt in the project folder.
3. Install the requirements:

```bash
pip install -r requirements.txt
```

4. Start Jupyter Notebook:

```bash
jupyter notebook
```

5. Open the notebook file:

```text
Data_Spaces_as_Enablers_of_AI.ipynb
```

6. Run the cells from top to bottom.

### Option 2: Run with VS Code

1. Open the project folder in VS Code.
2. Install the Python and Jupyter extensions if needed.
3. Open:

```text
Data_Spaces_as_Enablers_of_AI.ipynb
```

4. Select a Python kernel.
5. Run all cells from top to bottom.

### Option 3: Run with Google Colab

1. Open Google Colab.
2. Upload the notebook file.
3. Upload the CSV file if the notebook is set to use the local CSV.
4. Run the cells from top to bottom.

## Project Structure

Recommended project structure:

```text
data-spaces-ai-project/
│
├── README.md
├── requirements.txt
├── Data_Spaces_as_Enablers_of_AI.ipynb
│
├── data/
│   └── opsd_germany_daily.csv
```


## File Descriptions

| File/Folder | Description |
|---|---|
| `README.md` | Explains the project, setup instructions, and how to run the notebook |
| `requirements.txt` | Lists the Python packages required to run the project |
| `Data_Spaces_as_Enablers_of_AI.ipynb` | Main notebook containing the code, explanation, and visualizations |
| `data/opsd_germany_daily.csv` | Local copy of the German energy dataset used in the notebook |


## Main Steps in the Notebook

The notebook performs the following steps:

1. Loads the energy dataset.
2. Splits the dataset into three simulated provider datasets.
3. Creates a simplified data space connector.
4. Registers data assets and usage policies.
5. Tests approved and denied access requests.
6. Harmonizes the datasets.
7. Combines the datasets into one data-space view.
8. Creates derived features such as renewable energy share.
9. Generates visualizations for analysis.

## Visualizations Generated

The notebook produces visualizations such as:

1. **Siloed provider view**  
   <img width="1090" height="790" alt="image" src="https://github.com/user-attachments/assets/25231f22-0c85-49a3-a46f-e5d14739d94d" />
   Shows that each provider only sees its own data before sharing.


2. **Combined data-space view**  
   <img width="1189" height="489" alt="image" src="https://github.com/user-attachments/assets/f454babe-cd8e-4763-94c4-e1c5c393d742" />
   Shows electricity consumption compared with wind and solar generation after data sharing.


3. **Monthly renewable share**
   <img width="1189" height="390" alt="image" src="https://github.com/user-attachments/assets/a8586626-fcdc-4348-8af1-488531d51c7b" />
   Shows the share of electricity consumption covered by renewable generation.

4. **Correlation matrix**
   <img width="598" height="479" alt="image" src="https://github.com/user-attachments/assets/ed1d353e-70b1-4685-bd2b-1eda9da771e6" />
   
   Shows relationships between consumption, wind generation, solar generation, renewable generation, and renewable share.

## Key Insight

The project shows that data spaces help turn separate datasets into useful AI-ready data. Without the data space, each provider only has a limited view. With the data space, access can be governed, data can be harmonized, and the combined dataset can support analytics, forecasting, and decision-making.

## Conclusion

This project demonstrates how data spaces can support AI by enabling trusted, governed, and controlled data sharing. The energy example shows how separate datasets from different providers can be combined into a richer dataset for renewable energy analytics and AI readiness.
