# 👋 Hi, I'm Tatiana — Data & AI Integration Specialist

I work with data quality, AI data operations, Python automation, and API integrations.  
My background combines AI annotation, data validation, workflow automation, and system logic.  
This portfolio includes my practical projects in Python, automation, and AI data workflows.

---

## 🚀 Featured Projects

### 1️⃣ Data Quality Dashboard for Customer Claims
**Tools:** Excel, CRM, internal reporting systems  
Analyzed customer claims, categorized defect types, tracked resolution times, and created a dashboard to identify recurring issues and improve processes.

➡️ *LinkedIn project section*

---

### 2️⃣ Workflow Automation using n8n
**Tools:** n8n, webhooks, email integration  
Built an automated workflow to collect, validate, and store structured data. Added notifications for inconsistent entries and documented the workflow logic.

➡️ *LinkedIn project section*

---

### 3️⃣ Search Relevance Evaluation Framework
**Tools:** internal annotation tools  
Created structured guidelines for evaluating search relevance, defined criteria for quality levels, and improved annotation consistency for AI search models.

➡️ *LinkedIn project section*

---

### 4️⃣ Python Script for Data Cleaning & Validation
**Tools:** Python, Pandas  
A script that checks CSV files for missing values, duplicates, incorrect formats, and inconsistent entries, then generates a cleaned dataset.

```python
import pandas as pd

df = pd.read_csv("data.csv")

missing = df.isnull().sum()
duplicates = df.duplicated().sum()

numeric_like_strings = (
    df.select_dtypes(include="object")
      .apply(lambda x: x.str.match(r"^\d+(\.\d+)?$").sum())
)

print("=== Data Quality Report ===")
print("Missing values:\n", missing)
print("\nDuplicate rows:", duplicates)
print("\nNumeric-like strings in object columns:\n", numeric_like_strings)

df_cleaned = df.drop_duplicates()
df_cleaned = df_cleaned.fillna("N/A")

df_cleaned.to_csv("cleaned_data.csv", index=False)
print("\nCleaned file saved as cleaned_data.csv")
