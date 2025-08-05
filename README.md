IP Data Analytics

A comprehensive project for collecting, processing, and analyzing over 500,000 recipe records from multiple online sources, and constructing a hierarchical tree of cuisines.

📋 Overview:

This repository contains all the code, data, and notebooks used to:

Collect recipe data (~500,000 records) from Food.com, Allrecipes, and other culinary websites.

Process & Clean raw JSON/CSV datasets by merging, normalizing fields, and handling missing values.

Explore & Visualize the data through Exploratory Data Analysis (EDA) to uncover insights about recipes, ingredients, and cuisine distributions.

Construct a hierarchical cuisine tree (Region_Tree.json) that organizes global cuisines by continent, subregion, and category.



📥 Data Sources:

Food.com

Allrecipes.com

Other public culinary websites

Each source contributed unique recipe formats, which were unified into a common schema.



🛠 Tech Stack:

Language: Python 3.x

Environment: Jupyter Notebooks (.ipynb)

Data Handling: Pandas, NumPy

Web Scraping: Requests, BeautifulSoup

Visualization: Matplotlib, Seaborn, Plotly

Tree Construction: Custom Python scripts; data stored as JSON (Region_Tree.json)



🔧 Detailed Workflow:

Scraping

Configurable source list (URLs, pagination limits).

Parallel HTTP requests with concurrent.futures to speed data fetching.

Error handling for timeouts and missing elements.

Data Processing

Field Mapping: Mapped source-specific keys to a unified schema (title, ingredients, instructions, cuisine).

Cleaning: Stripped whitespace, handled nulls, standardized units (e.g., grams, cups).

Deduplication: Used hashed signatures of recipe title + ingredient list.

EDA Modules

Distribution Analysis: Histograms of ingredient counts, prep/cook times.

Ingredient Frequency: Top 50 ingredients globally and per cuisine.

Cross-Cuisine Comparisons: Heatmaps showing shared ingredient overlap ratios.

Clustering: K-means on TF-IDF vectors of ingredient lists to identify cuisine clusters.

Cuisine Tree Generation

Parsed a reference mapping of cuisines to regions (CSV or config file).

Built a nested Python dict with continent > region > cuisine nodes.

Exported to Region_Tree.json for API or UI consumption.

📈 Key Results & Visualization Highlights

Prep Time Trends: Tropical cuisines average shorter prep times; European cuisines show higher variance.

Ingredient Specialties: Chili peppers dominate Southeast Asian cuisines, while olive oil and garlic are most frequent in Mediterranean.

Cuisine Clustering: Identified 5 major cuisine clusters based on ingredient TF-IDF similarity.





