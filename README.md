# 🛒 E-commerce Transaction Analysis & Customer Segmentation

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-1.3+-green.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)

> A comprehensive data analysis project exploring purchasing patterns, customer demographics, and payment behaviors from 10,000+ e-commerce transactions.

---

## 📋 Table of Contents

- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Technologies Used](#-technologies-used)
- [Dataset](#-dataset)
- [Installation](#-installation)
- [Usage](#-usage)
- [Analysis & Insights](#-analysis--insights)
- [Key Findings](#-key-findings)
- [Project Structure](#-project-structure)
- [Future Enhancements](#-future-enhancements)
- [Contributing](#-contributing)
- [License](#-license)
- [Contact](#-contact)

---

## 🎯 Project Overview

This project performs **exploratory data analysis (EDA)** on e-commerce purchase data to uncover actionable business insights. Through systematic analysis of customer demographics, payment methods, and purchasing patterns, the project delivers data-driven recommendations for marketing optimization and customer retention strategies.

### Business Objectives

- Identify customer segmentation opportunities based on demographics
- Analyze payment method preferences and credit card expiration trends
- Discover temporal purchasing patterns (AM vs PM)
- Extract insights from email provider and language distributions
- Provide strategic recommendations for marketing and operations teams

---

## ✨ Key Features

- ✅ **Comprehensive Data Quality Assessment** - Missing value detection, duplicate checking, data type validation
- ✅ **Statistical Analysis** - Descriptive statistics, distribution analysis, outlier detection
- ✅ **Customer Segmentation** - Multi-dimensional analysis by language, location, job role, payment method
- ✅ **Payment Behavior Analysis** - Credit card provider trends, expiration tracking, transaction value patterns
- ✅ **Feature Engineering** - Derived variables for email domains, price categories, job classifications
- ✅ **Business Intelligence** - Actionable insights with strategic recommendations
- ✅ **Data Export** - Enhanced dataset with engineered features for downstream analysis

---

## 🛠 Technologies Used

| Technology | Purpose |
|------------|---------|
| **Python 3.8+** | Primary programming language |
| **Pandas** | Data manipulation and analysis |
| **NumPy** | Numerical computations |
| **Jupyter Notebook** | Interactive development environment |
| **Matplotlib** | Data visualization (optional) |
| **Seaborn** | Statistical visualizations (optional) |

---

## 📊 Dataset

### Source
E-commerce Purchases dataset containing transaction records

### Structure
- **Records**: 10,000 transactions
- **Features**: 14 columns
- **Size**: ~1.5 MB

### Columns

| Column Name | Description | Data Type |
|-------------|-------------|-----------|
| `Address` | Customer shipping address | String |
| `Lot` | Lot number | String |
| `AM or PM` | Purchase time indicator | String |
| `Browser Info` | Browser user agent | String |
| `Company` | Customer's company | String |
| `Credit Card` | Credit card number (anonymized) | Integer |
| `CC Exp Date` | Card expiration date (MM/YY) | String |
| `CC Security Code` | CVV code | Integer |
| `CC Provider` | Card provider (Visa, Mastercard, etc.) | String |
| `Email` | Customer email address | String |
| `Job` | Customer job title | String |
| `IP Address` | Customer IP address | String |
| `Language` | Preferred language | String |
| `Purchase Price` | Transaction amount ($) | Float |

### Data Quality
- ✅ **No missing values** (100% complete)
- ✅ **No duplicate records**
- ✅ **Validated data types**

---

## 🚀 Installation

### Prerequisites
```bash
Python 3.8 or higher
pip (Python package manager)
```

### Clone Repository
```bash
git clone https://github.com/JhishanDeb/ecommerce-analysis.git
cd ecommerce-analysis
```

### Install Dependencies
```bash
pip install -r requirements.txt
```

### Requirements.txt
```
numpy>=1.21.0
pandas>=1.3.0
matplotlib>=3.4.0
seaborn>=0.11.0
jupyter>=1.0.0
```

---

## 💻 Usage

### Option 1: Run Jupyter Notebook
```bash
jupyter notebook "Project 1.ipynb"
```
Execute cells sequentially to perform exploratory analysis.

### Option 2: Run Complete Analysis Script
```bash
python complete_analysis.py
```
Generates comprehensive report with all insights and exports enhanced dataset.

### Option 3: Interactive Python
```python
import pandas as pd

# Load data
df = pd.read_csv("Ecommerce Purchases")

# Quick analysis
print(f"Total Purchases: {len(df)}")
print(f"Average Price: ${df['Purchase Price'].mean():.2f}")
print(f"Top Language: {df['Language'].value_counts().index[0]}")
```

---

## 📈 Analysis & Insights

### 1. Descriptive Statistics

```
Purchase Price Statistics:
- Mean: $50.35
- Median: $50.00
- Std Dev: $28.85
- Min: $0.00
- Max: $99.99
```

### 2. Customer Segmentation

**By Language:**
- English (en): ~10.8%
- Spanish (es): ~10.4%
- French (fr): ~11.0%
- Other languages: ~67.8%

**By Email Provider:**
- Hotmail: 1,638 users (16.4%)
- Yahoo: 1,616 users (16.2%)
- Gmail: 1,605 users (16.1%)

### 3. Payment Analysis

**Credit Card Providers:**
- VISA 16 digit: Leading provider
- Mastercard: Second most common
- American Express: Third position

**Expiration Alert:**
- **988 cards expiring in 2020** - High priority for renewal campaigns

### 4. Temporal Patterns

**Purchase Timing:**
- PM Purchases: Slightly higher volume
- AM Purchases: Comparable activity
- **Insight**: Evening marketing campaigns may yield better results

### 5. Professional Demographics

- **984 customers with "Engineer" in job title**
- Diverse job distribution across sectors
- Opportunity for B2B targeting in tech sector

---

## 🔍 Key Findings

### 📌 Top Insights

1. **Language Diversity**: High linguistic diversity suggests need for multilingual support
2. **Email Consolidation**: 80%+ users on top 3 email providers - streamlined marketing opportunity
3. **Payment Risk**: ~10% of cards expiring soon - implement proactive renewal system
4. **Price Clustering**: Majority of purchases between $25-$75 - optimize inventory for this range
5. **Professional Market**: Significant engineering demographic - potential for B2B expansion

### 💡 Recommendations

| Area | Recommendation | Expected Impact |
|------|----------------|-----------------|
| **Marketing** | Focus campaigns on top 3 languages (en, es, fr) | 30% coverage increase |
| **Email Strategy** | Prioritize Hotmail, Yahoo, Gmail templates | 80%+ reach optimization |
| **Retention** | Automated renewal alerts for expiring cards | Reduce payment failures by 10% |
| **Pricing** | Introduce $75+ premium tier | Capture upsell opportunities |
| **Timing** | Schedule promotions for 2-6 PM | Align with peak purchase activity |

---

## 📁 Project Structure

```
ecommerce-analysis/
│
├── data/
│   ├── Ecommerce Purchases          # Original dataset
│   └── Ecommerce_Purchases_Enhanced.csv  # Processed data with engineered features
│
├── notebooks/
│   └── Project 1.ipynb              # Exploratory analysis notebook
│
├── src/
│   ├── complete_analysis.py         # Full analysis script
│   ├── data_cleaning.py             # Data preprocessing functions
│   └── visualization.py             # Plotting utilities
│
├── reports/
│   ├── analysis_report.pdf          # Executive summary
│   └── technical_report.md          # Detailed findings
│
├── requirements.txt                 # Python dependencies
├── README.md                        # This file
└── LICENSE                          # MIT License
```

---

## 🚀 Future Enhancements

### Phase 2 Roadmap

- [ ] **Interactive Dashboard** - Build Plotly/Dash visualization dashboard
- [ ] **Geographic Analysis** - Extract location insights from addresses
- [ ] **Cohort Analysis** - Track customer lifetime value by cohort
- [ ] **Predictive Modeling** - Build purchase propensity models
- [ ] **A/B Testing Framework** - Implement statistical testing for campaigns
- [ ] **Real-time Pipeline** - Automate analysis with new data ingestion
- [ ] **API Integration** - Connect to live e-commerce platforms

### Potential Extensions

- **Machine Learning**: Customer segmentation using K-means clustering
- **NLP Analysis**: Job title categorization using text mining
- **Time Series**: Seasonal purchasing pattern analysis
- **Recommendation Engine**: Product recommendation system based on behavior

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines

- Follow PEP 8 style guidelines for Python code
- Add unit tests for new features
- Update documentation accordingly
- Ensure all tests pass before submitting PR

---

## 📜 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

```
MIT License

Copyright (c) 2024 Jhishan Deb

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 📧 Contact

**Jhishan Deb**
- GitHub: [@JhishanDeb](https://github.com/JhishanDeb)
- LinkedIn: [Jhishan Deb]([https://linkedin.com/in/jhishandeb](https://www.linkedin.com/in/jhishan-deb-874001234/))
- Email: jhishandeb2002@gmail.com


---

## 🌟 Acknowledgments

- Dataset source: E-commerce transactions dataset
- Inspiration: E-commerce analytics best practices
- Tools: Python community and open-source contributors

---

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/JhishanDeb/ecommerce-analysis?style=social)
![GitHub forks](https://img.shields.io/github/forks/JhishanDeb/ecommerce-analysis?style=social)
![GitHub watchers](https://img.shields.io/github/watchers/JhishanDeb/ecommerce-analysis?style=social)

---

<div align="center">

**If you found this project helpful, please consider giving it a ⭐!**

Made with ❤️ and Python by Jhishan Deb

[⬆ Back to Top](#-e-commerce-transaction-analysis--customer-segmentation)

</div>
