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

### 5️⃣ API Integration: Fetching and Validating Public Data
**Tools:** Python, Requests, Pandas  
A script that retrieves JSON from a public REST API, validates required fields and types, and saves clean data into a CSV file.

```python
import requests
import pandas as pd

url = "https://jsonplaceholder.typicode.com/posts"

response = requests.get(url)
response.raise_for_status()

data = response.json()

required_fields = ["userId", "id", "title", "body"]
validated_data = []

for item in data:
    if all(field in item for field in required_fields):
        if (
            isinstance(item["userId"], int)
            and isinstance(item["id"], int)
            and isinstance(item["title"], str)
            and isinstance(item["body"], str)
        ):
            validated_data.append(item)

df = pd.DataFrame(validated_data)
df.to_csv("api_posts_cleaned.csv", index=False)

print(f"Saved {len(df)} valid records to api_posts_cleaned.csv")
```

---

## 🧰 Skills

- Data Annotation & Data Quality  
- Python (Pandas, Requests)  
- API Integration  
- Automation (n8n)  
- Data Validation  
- Process Optimization  
- Computer Vision & Speech Data  
- CRM / ERP / POS systems  

---

## 🌍 Languages
- Russian — Native  
- English — Professional  
- Spanish — Professional  

---

## 📫 Contact
- LinkedIn: [*your link here*  ](https://www.linkedin.com/feed)
- Email: chumatv@gmail.com

---

Thanks for visiting my portfolio!
```
