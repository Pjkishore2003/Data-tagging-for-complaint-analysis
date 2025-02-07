# Data Tagging for Complaint Classification

## Project Overview
This project involves tagging free-text complaint data by aligning it with predefined taxonomy categories. The dataset consists of three main fields:
- **Complaint**
- **Cause**
- **Correction**

The tagging process assigns appropriate labels to each entry based on:
- **Root Cause**
- **Symptom_Condition**
- **Symptom_Component**
- **Fix_Condition**
- **Fix_Component**

## Dataset
- **Task Dataset:** Contains free-text complaints that require tagging.
- **Taxonomy Sheet:** Provides predefined categories for classification.
- **Tagged Dataset:** The final output with applied tags.

## Approach
1. **Understanding the Data**
   - Reviewed the provided complaint dataset and taxonomy sheet.
   - Analyzed sample tagged examples for reference.

2. **Tagging Methodology**
   - Applied TF-IDF vectorization and fuzzy matching for text classification.
   - Used a function to clean and preprocess text before matching.
   - Implemented a similarity-based approach to assign categories from the taxonomy.
   - Handled ambiguous cases through a combination of cosine similarity and fuzzy matching.

3. **Validation and Accuracy Calculation**
   - Compared tagged data with the original dataset.
   - Measured tagging accuracy across multiple fields.
   - Documented observations and improvements.

## Insights & Observations
- Identified common patterns in complaints and fixes.
- Recognized frequent root causes that could help improve product/service quality.
- Potential use case for automation via NLP-based classification models.
- TF-IDF and fuzzy matching improve tagging accuracy but may require additional training data.

## Files in This Repository
- `datatagged_Dataset.xlsx`: The final tagged dataset.
- `DA - Task 1.xlsx`: Contains the original dataset, taxonomy reference, and the summary report.
- `README.md`: This documentation file.
- `tagging_script.py`: The Python script used for data tagging.

## How to Use
1. Ensure you have installed dependencies:
   ```sh
   pip install fuzzywuzzy python-Levenshtein pandas numpy scikit-learn openpyxl
   ```
2. Run the script to generate a tagged dataset:
   ```sh
   python tagging_script.py
   ```
3. Open the output file `datatagged_Dataset.xlsx` to explore the assigned categories.

## Future Enhancements
- Improve accuracy with fine-tuned NLP models.
- Implement a graphical interface for manual review and adjustments.
- Extend the taxonomy for better classification coverage.

## Contributing
Feel free to submit issues or pull requests to enhance the dataset and tagging methodology.


