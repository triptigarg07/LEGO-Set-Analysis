## Overview 🏗️

This project aims to analyze LEGO sets using Power BI, providing insights into pricing, piece count, and various themes. The dataset consists of 4,385 LEGO sets, categorized based on themes, age ranges, and other parameters. This case study presents the methodology, key findings, and insights derived from the analysis using Exploratory Data Analysis (EDA) and DAX (Data Analysis Expressions) for advanced calculations.

 ![Dashboard](/legoset_analysis_page-0001.jpg)

## Objectives 🎯

The primary goals of this analysis include:
- Conducting Exploratory Data Analysis (EDA) to identify patterns and trends.
- Understanding price variations among LEGO sets.
- Analyzing the relationship between piece count and price.
- Exploring the distribution of LEGO sets across different themes.
- Identifying trends based on licensed vs. non-licensed sets.
- Creating an interactive report with images, tooltips, and advanced DAX measures to enhance user experience.

## Tools & Technologies Used 🛠️

- 📊 Power BI for data visualization and analysis.
- ⚡ DAX (Data Analysis Expressions) for calculated measures.
- 📈 EDA techniques for data exploration.
- 🛠 Excel/CSV files for data storage and processing.

## Dataset Details 📂

- Total Sets Analyzed: 4,385
- Average Price: $44.7
- Average Pieces per Set: 411
- Categories: Normal: 4,289 Extended: 80 Collection: 10 Book: 5 Licensed: 1,283 Modern Day: 725 Action/Adventure: 551 Miscellaneous: 443

## Methodology 🛠️

### 1. Loading and Preparing the Data

- Data Cleaning and EDA 🔍:
        - Connected to the lego_sets.csv file.
        - Removed minifigs, bricksetURL, and thumbnailURL fields.
        - Reviewed data types and filtered out records missing price, age, pieces, or image URL values.
        - Conducted Exploratory Data Analysis (EDA) 📊 to summarize key trends and outliers.

- Feature Engineering & DAX Measures 📌:
        - Created conditional columns for:
            - Age Range: Over 18, 10 to 17, 5 to 9, 1 to 4.
            - Price Range: $ (<$25), $$ (>$25), $$$ (>$50), $$$$ (>$100), $$$$$ (>$500).
  
- Added calculated DAX measures:
        - Total Sets (DISTINCTCOUNT(set_id)).
        - Total Groups (DISTINCTCOUNT(theme_group)).
        - Avg. Age, Avg. Price, Avg. Pieces (AVERAGE(price), AVERAGE(pieces)).
        - Price-to-Piece Ratio (DIVIDE(price, pieces)).
  
### 2. Designing the Report Layout & Visuals 

- Sketching and Layout Planning 📝: Designed a structured dashboard layout to optimize user experience.

- Report Components 📊: 
        - Card visuals for Total Sets, Avg. Pieces, Avg. Price, and Price-to-Piece Ratio.
        - Slicers for filtering by Theme Group, Theme, Age Range, and Price Range.
        - Table visual displaying Name, Set ID, Theme, Age Range, Avg. Pieces, Avg. Price, Price Range.
        - Detailed report section for a selected LEGO set:
             - Name, Image, Price, Year, Pieces, Age.
             - Placeholder values shown when multiple sets are selected.

  ![Filters](/filters_applied.jpg)

- Data Visualization Enhancements 📈
        - Used decomposition trees to analyze trends over time.
        - Applied conditional formatting to highlight high-value sets.

  ![Dashboard](/legoset_analysis_page-0002.jpg)

- Interaction Customization ⚙️:
        - Prevented table selections from filtering top-level cards.
        - Used cross-filtering and drill-through pages for an in-depth analysis of themes and price segments.

   ![Selected Legoset](/selected_legoset.jpg)

### 3. Adding Interactive Components 🖱️

- Parameters & Filters:
        - Created a numeric range parameter (Max Price) from 0-850, incrementing by 5.
        - Added a slicer and a measure to filter the table based on the max price selected.

- Tooltips & Image Hover Effects 🖼️:
        - Enabled tooltips to display LEGO set images when hovering over a table row.
        - Ensured that when scrolling, the image of the LEGO set remains visible along with its key details.

  ![tooltip](/tootlip_legoset.jpg)

- Bookmarks & Page Navigation 🔄:
        - Implemented a reset button to clear all filters.
        - Used bookmarks for "on hover" and "on press" effects.

  ![Reset Button](/reset_button.jpg)
  
        - Created a decomposition tree visual on a separate report page analyzing Total Sets by Category, Theme Group, Theme, and Name.

  ![Tree Visual](/exploring_categories.jpg)
        
## Key Findings 🔍

### 1. Price Trends
- The average price of a LEGO set is $44.7.
- Sets with higher piece counts generally have a higher price, but some themes like Star Wars and Marvel Super Heroes command a premium.
- The highest-priced sets belong to large-scale models such as Imperial Star Destroyer and Millennium Falcon.

### 2. Piece Count Distribution
- The average LEGO set has 411 pieces.
- Rocket Assembly & Transport (1,055 pieces, $150) is among the largest sets analyzed.
- Smaller seasonal sets, such as Christmas Snow Hut Ornament (45 pieces, $8), have significantly lower piece counts.

### 3. Popular Themes
- Licensed themes (e.g., Star Wars, Marvel Super Heroes, Disney) account for 1,283 sets, indicating their strong market presence.
- Star Wars is one of the most dominant themes, with 388 sets available.
- Ninjago and Friends also feature prominently in the dataset.

### Conclusion 🎯

This Power BI project demonstrated my ability to analyze large datasets, create dynamic dashboards, and extract actionable insights from LEGO set data. It highlights my skills in:
      ✅ Data Visualization – Designed engaging, interactive dashboards using Power BI to communicate insights effectively.
      ✅ Exploratory Data Analysis (EDA) – Identified pricing trends, piece distribution, and popular themes within LEGO sets.
      ✅ DAX & Data Transformation – Utilized advanced DAX functions to compute key metrics like Total Sets, Avg. Price, and rice-to-Piece Ratio.
      ✅ Business Intelligence & Reporting – Implemented slicers, tooltips, and decomposition trees to enhance user interactivity.
      ✅ Data-Driven Insights – Found that licensed LEGO themes (e.g., Star Wars, Marvel) are priced higher due to collectibility and branding.
