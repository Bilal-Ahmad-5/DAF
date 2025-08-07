📊 E-Commerce Data Analysis, Forecasting & AI Fine-Tuning

This project combines the power of data analytics, predictive modeling, and LLM fine-tuning to turn raw e-commerce data into actionable, AI-generated insights. From cleaning half a million+ records to fine-tuning LLaMA-2 7B using QLoRA, this pipeline delivers data-driven forecasting and intelligent transaction summaries.

🚀 Project Highlights

- 📦 Over 541,000 e-commerce transactions analyzed
- 🧹 Advanced data preprocessing and outlier removal
- 📊 In-depth exploratory analysis to identify trends
- 🔮 Forecasting transaction behavior using statistical insights
- 🤖 Fine-tuned LLaMA-2 7B with QLoRA for custom generation
- 🧠 Model can understand and explain transaction data
- 📥 Deployable AI model: Beepseek-R1

📂 Dataset Overview

A comprehensive dataset of 541,909 transactions across 38 countries, containing:

- InvoiceNo – Transaction ID
- StockCode – Product ID
- Description – Product name
- Quantity – Units purchased
- InvoiceDate – Timestamp
- UnitPrice – Price per item
- CustomerID – Unique customer
- Country – Purchase location

📉 Final cleaned dataset: 460,251 quality records after preprocessing.

🧼 Data Cleaning & Preparation
The dataset was rigorously cleaned and reduced by 15%:

- Action	Records Affected
- Removed missing descriptions	1,454
- Imputed missing CustomerIDs	135,080
- Removed duplicates	5,268
- Dropped invalid entries (cancellations, negative values)	24,132
- Removed statistical outliers via IQR	65,174

📈 Exploratory Analysis & Forecasting

Uncovered meaningful patterns:

- 🔁 Most orders have 1–10 items (avg: 9.55)
- 💰 Most products priced between $1–$4
- 🌍 UK dominates in transaction count
- 👤 4,372 unique customers identified
- 📊 Visualizations of purchase trends, product popularity, seasonal shifts

Forecasting Use Cases:

- Predicting top-selling items
- Country-level sales trends
- Customer retention and behavior modeling
- Revenue projections

🤖 Fine-Tuning LLaMA-2 7B (QLoRA)

The LLaMA-2 7B model was fine-tuned using QLoRA for transaction understanding and summarization.

Training Specs:

- QLoRA (4-bit quantized)
- LoRA dimension: 64
- Alpha: 16
- Learning rate: 2e-4
- 1 epoch, 921 steps, ~48 mins
- Final Loss: 0.7929

Model Output:

Beepseek-R1 – a compact, generative AI ready to answer and explain transactional data.

🛠 How to Use
- Install dependencies: pandas, numpy, matplotlib, seaborn, transformers, trl, peft, accelerate, bitsandbytes
- Load and preprocess transaction data
- Explore insights and trends using EDA
- Forecast using statistical models or integrate LLM
- Use Beepseek-R1 to generate intelligent invoice summaries
- Deploy in dashboards, reports, or APIs

🧰 Technologies Used
Python 3.10+

- Transformers (HuggingFace)
- QLoRA + PEFT for fine-tuning
- pandas, seaborn, matplotlib for EDA
- scikit-learn for forecasting models
- bitsandbytes, accelerate for efficiency

📜 License
Released under the MIT License – open for community use, contributions, and commercial applications.
