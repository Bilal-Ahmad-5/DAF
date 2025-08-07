📊 ## E-Commerce Data Analysis Project

## Project Overview
This comprehensive project analyzes a large-scale e-commerce dataset containing over 541,000 transactions and fine-tunes the LLaMA-2 7B language model to generate meaningful insights from transaction data. The workflow demonstrates a complete data science pipeline from raw data processing to AI model deployment, featuring:

- Comprehensive data cleaning and preprocessing
- Exploratory data analysis with visualizations
- Advanced AI model fine-tuning using QLoRA
- Text generation capabilities for transaction insights

## Dataset Description
The dataset contains 541,909 transaction records with 8 features describing customer purchases across 38 countries. Key features include:
- **InvoiceNo**: Unique transaction identifier
- **StockCode**: Product identifier
- **Description**: Product description
- **Quantity**: Number of items purchased
- **InvoiceDate**: Timestamp of transaction
- **UnitPrice**: Price per item
- **CustomerID**: Unique customer identifier
- **Country**: Purchase location

After rigorous cleaning, the final dataset contains 460,251 high-quality records.

## Data Cleaning Process
The data underwent extensive preprocessing to ensure quality:
1. Removed 1,454 records with missing product descriptions
2. Filled 135,080 missing CustomerIDs using mean imputation
3. Eliminated 5,268 duplicate records
4. Removed 24,132 invalid records (cancellations, negative quantities/prices)
5. Applied IQR method to remove 65,174 statistical outliers
6. Final dataset reduction: 15% (460,251 records)

## Key Insights from Analysis
Exploratory analysis revealed significant patterns:
- Transaction quantities typically range from 1-10 items (mean: 9.55)
- Most products priced between $1-4 (mean: $4.61)
- United Kingdom dominates transaction volume
- 4,372 unique customers identified (mean ID: 15,287)
- Visualizations show distributions, geographical patterns, and purchase trends

## AI Model Fine-Tuning
We customized LLaMA-2 7B using cutting-edge techniques:
- **QLoRA Method**: 4-bit quantization for efficient fine-tuning
- **Parameters**: LoRA dimension 64, alpha 16, learning rate 2e-4
- **Training**: 1 epoch, batch size 4, 921 steps (48 minutes)
- **Result**: Final loss 0.7929 - model understands transaction patterns
- **Output**: Saved production-ready model "Beepseek-R1" for deployment

## Sample Application
The fine-tuned model generates contextual insights from transaction data:

**Input**: "InvoiceNo 536365 StockCode 85123A Description WHITE HANGING HEART T-LIGHT HOLDER Quantity 6"

**Output**: 
"Sure, here is the invoice: 2023-03-14 14:40 123456789 United Kingdom  
WHITE HANGING HEART T-LIGHT HOLDER  
Quantity: 6, Unit Price: $4.25, Total: $25.50  
This decorative candle holder features an elegant heart design with metal hanger."

## Usage Instructions
1. Install dependencies: pandas, numpy, matplotlib, seaborn, transformers, trl, peft, bitsandbytes
2. Process data: Load CSV, clean missing values, remove duplicates and invalid records, eliminate outliers
3. Run analysis: Explore distributions, country patterns, and customer behaviors
4. Model inference: Load fine-tuned model, generate insights from transaction prompts
5. Deploy: Integrate model into applications for automated report generation

## Dependencies
Python packages: pandas, numpy, tensorflow, scikit-learn, matplotlib, seaborn, transformers, trl, peft, accelerate, bitsandbytes, tf-keras

## License
MIT License - open for collaboration and commercial use
