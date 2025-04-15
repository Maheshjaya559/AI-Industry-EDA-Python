# AI-Industry-EDA-Python
This project performs Exploratory Data Analysis (EDA) on a global dataset related to AI adoption across industries and countries. The goal is to uncover patterns, trends, and insights regarding:  AI adoption rates  Job loss and revenue impacts  AI-generated content volumes  Public trust and regulatory environments

#🔧 Technologies Used:

*Python

*Pandas for data manipulation

*Seaborn and Matplotlib for visualizations

*Jupyter Notebook


📌 Steps Followed in the Notebook:

1. Importing Libraries
 
*The required Python libraries (pandas, matplotlib.pyplot, seaborn) were imported.


 2. Loading the Dataset

*The dataset was loaded into a pandas DataFrame using:

 data = pd.read_csv("filename.csv")  # (replace with actual name)
 

 3. Initial Data Exploration

*head() to view the first few rows

*info() and .describe() to understand data types and summary stats

*Checked for missing values


4. Data Cleaning
   
*Dropped unnecessary columns such as "Market Share of AI Companies (%)" and "Human-AI Collaboration Rate (%)"

*Ensured proper datatypes

*Renamed or formatted column headers if needed

5. Correlation Analysis

Used:

Global.select_dtypes(include='number').corr()

To analyze relationships between numerical features like:

*AI Adoption Rate

*Job Loss Due to AI

*Revenue Increase

*AI-generated Content Volume

📊 Visualization: A heatmap was used to display the correlation matrix.

6. Visualizations and Insights
📈 AI Adoption by Industry:

sns.relplot(x='Industry', y='AI Adoption Rate (%)', hue='Job Loss Due to AI (%)', data=Global)

*Showed which industries are adopting AI most aggressively and how job loss correlates.

📊 Distribution of Job Loss Due to AI:

sns.histplot(Global['Job Loss Due to AI (%)'], kde=True)

*Shows how job loss is distributed; helps spot whether the impact is skewed toward certain countries or industries.

7.AI Adoption by Country:

sns.barplot(x='Country', y='AI Adoption Rate (%)', data=Global)

*Compared how different countries are adopting AI.

🧠 Consumer Trust vs AI Impact:

Visuals compared:

*Consumer Trust in AI (%)

*Regulation status

*Revenue Increase Due to AI (%)

To help understand if countries with stricter regulation also have more or less trust in AI.

📌 Key Insights:

*Countries like the USA and France show high AI adoption and job impact.

*Legal and Media industries show unique patterns in AI-generated content volumes.

*A positive correlation is observed between AI adoption and revenue increase.

*Trust in AI seems independent of adoption rates in some regions.

📁 Folder Structure Suggestion:

📦AI_Industry_EDA_Python
 ┣ 📜EDA_using_python.ipynb
 ┣ 📜README.md
 ┣ 📂images
 ┃ ┗ 📊 (optional saved plots)
 ┗ 📜requirements.txt
 
  
