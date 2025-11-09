


# 🍔 McDonald's Fast Food Market Segmentation Analysis

<div align="center">

![Python](https://img.shields.io/badge/Python-3.8+-blue.svg)
![LaTeX](https://img.shields.io/badge/LaTeX-Complete-green.svg)
![Status](https://img.shields.io/badge/Status-Complete-success.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)

**Complete 10-Step Data-Driven Market Segmentation Framework**

[Overview](#overview) • [Key Results](#key-results) • [Installation](#installation) • [Documentation](#documentation) • [Usage](#usage)

</div>

---

## 📋 Table of Contents

- [Overview](#overview)
- [Key Results](#key-results)
- [Project Structure](#project-structure)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Usage](#usage)
- [Methodology](#methodology)
- [Documentation](#documentation)
- [Visualizations](#visualizations)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

---

## 🎯 Overview

This repository contains a **comprehensive market segmentation analysis** of McDonald's fast food consumers, implementing a rigorous 10-step framework using advanced clustering algorithms, statistical validation, and strategic marketing recommendations.

### Business Context

- **Industry**: Fast Food / Quick Service Restaurant (QSR)
- **Challenge**: Diverse consumer perceptions requiring targeted marketing strategies
- **Dataset**: 1,431 consumers, 11 perception variables, 4 descriptors
- **Market Coverage**: 78.3% through targeted segmentation strategy

### Project Objectives

1. **Identify** distinct consumer segments based on McDonald's brand perceptions
2. **Validate** segment stability using bootstrap resampling (ARI = 0.871)
3. **Profile** segments with perceptual and demographic characteristics
4. **Select** optimal target segments using knock-out and attractiveness criteria
5. **Design** customized marketing mix (4Ps) for each target segment
6. **Implement** continuous monitoring and evaluation framework

---

## 🏆 Key Results

### Four Distinct Segments Identified

| Segment | Name | Size | Like Rating | Visit Frequency | Strategy |
|---------|------|------|-------------|-----------------|----------|
| **1** | Price-Quality Skeptics | 16.8% | +1.03 | 1.40 | VALUE REPOSITION |
| **2** | Happy Value Hunters | **39.6%** | **+2.72** | **2.94** | **DEFEND & RETAIN** |
| **3** | Health-Concerned Pragmatists | 21.7% | +0.23 | 1.62 | LONG-TERM ONLY |
| **4** | Premium Experience Seekers | 21.9% | +2.31 | 2.86 | EXPAND & GROW |

### Strategic Recommendations

- ✅ **Primary Target**: Segment 2 (60% budget allocation)
- ✅ **Secondary Target**: Segment 4 (30% budget allocation)
- ✅ **Tertiary Target**: Segment 1 (10% budget allocation)
- 💡 **Innovation**: New "Signature Collection" premium product line
- 📈 **Expected Impact**: +8% revenue growth, +2pts market share

### Statistical Validation

- **Segment Stability**: ARI = 0.871 (Excellent)
- **Like Rating Significance**: F = 81.0, p < 0.001
- **Visit Frequency Significance**: H = 385.9, p < 0.001
- **Age Differences**: F = 28.5, p < 0.001
- **Gender Distribution**: χ² = 29.1, p < 0.001

---



---

## 💻 Technologies Used

### Programming & Data Analysis
- **Python 3.8+**: Core programming language
- **pandas**: Data manipulation and analysis
- **numpy**: Numerical computing
- **scikit-learn**: Machine learning algorithms (K-means, hierarchical clustering)
- **scipy**: Statistical analysis and testing

### Visualization
- **matplotlib**: Base plotting library
- **seaborn**: Statistical data visualization
- **plotly**: Interactive visualizations
- **tikz/pgfplots**: LaTeX diagram generation

### Documentation
- **LaTeX**: Professional documentation (article class)
- **Beamer**: Presentation slides
- **Jupyter Notebook**: Interactive analysis environment
- **Markdown**: README and documentation

### Development Tools
- **Git**: Version control
- **Anaconda**: Environment management
- **VS Code / PyCharm**: IDE
- **Overleaf**: LaTeX collaboration (optional)

---

## 🚀 Installation

### Prerequisites

- Python 3.8 or higher
- Anaconda/Miniconda (recommended)
- LaTeX distribution (TeX Live, MiKTeX, or MacTeX)
- Git

### Step 1: Clone Repository

```
git clone https://github.com/yourusername/mcdonalds-market-segmentation.git
cd mcdonalds-market-segmentation
```

### Step 2: Create Python Environment

**Option A: Using Conda (Recommended)**

```
conda env create -f environment.yml
conda activate mcd-segmentation
```

**Option B: Using pip**

```
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt
```

### Step 3: Verify Installation

```
python -c "import pandas, sklearn, seaborn; print('All packages imported successfully!')"
```

### Step 4: Compile LaTeX Documents (Optional)

```
cd docs/latex/
pdflatex step_01_decide_to_segment.tex
# Repeat for all steps or use provided PDFs in docs/pdfs/
```

---

## 📊 Usage

### Quick Start: Run Complete Analysis

```
# Navigate to notebooks directory
cd notebooks/

# Launch Jupyter
jupyter notebook

# Open and run notebooks in sequence:
# 01_data_exploration.ipynb
# 02_segmentation_analysis.ipynb
# 03_profiling_description.ipynb
# 04_monitoring_system.ipynb
```

### Example: Segment Extraction

```
import pandas as pd
from src.clustering import perform_kmeans_segmentation
from src.validation import calculate_stability

# Load data
data = pd.read_csv('data/mcdonalds_data.csv')

# Extract segments
segments, model = perform_kmeans_segmentation(data, n_clusters=4, random_state=42)

# Validate stability
stability_score = calculate_stability(data, n_clusters=4, n_iterations=50)
print(f"Segment Stability (ARI): {stability_score:.3f}")
```

### Example: Generate Segment Profile

```
from src.profiling import create_segment_profile
import matplotlib.pyplot as plt

# Create profile visualization
fig, ax = create_segment_profile(data, segments)
plt.savefig('outputs/figures/segment_profile.png', dpi=300, bbox_inches='tight')
plt.show()
```

### Example: Export Evaluation Matrix

```
from src.profiling import generate_evaluation_matrix

# Generate targeting recommendations
evaluation_df = generate_evaluation_matrix(data, segments)
evaluation_df.to_csv('outputs/reports/segment_evaluation.csv', index=False)
print(evaluation_df)
```

---

## 🔬 Methodology

### 10-Step Segmentation Framework

1. **Step 1: Decided to Segment**
   - Business case justification
   - Competitive analysis
   - Resource assessment

2. **Step 2: Specified Ideal Target**
   - Knock-out criteria (6 requirements)
   - Attractiveness criteria (brand affinity, visit frequency)

3. **Step 3: Collected Data**
   - n = 1,431 consumers
   - 11 perception variables (binary)
   - 4 descriptor variables

4. **Step 4: Explored Data**
   - Univariate analysis
   - Correlation analysis
   - Principal Component Analysis

5. **Step 5: Extracted Segments**
   - Hierarchical clustering (Ward's linkage)
   - K-means clustering (25 random starts)
   - Optimal k = 4 determination

6. **Step 6: Profiled Segments**
   - Perception patterns
   - Marker variable identification
   - Segment naming

7. **Step 7: Described Segments**
   - Demographic analysis (age, gender)
   - Behavioral analysis (visit frequency, like rating)
   - Statistical significance testing

8. **Step 8: Selected Targets**
   - Knock-out criteria evaluation
   - Attractiveness scoring
   - Three-tier targeting strategy

9. **Step 9: Customized Marketing Mix**
   - Product strategy (value vs. premium)
   - Pricing strategy (3-tier architecture)
   - Distribution strategy (omnichannel)
   - Promotion strategy (segment-specific campaigns)

10. **Step 10: Evaluation & Monitoring**
    - KPI framework (3-level hierarchy)
    - Real-time dashboard
    - Alert system (Green/Yellow/Red)
    - Quarterly reviews

### Statistical Methods

- **Clustering**: K-means (Euclidean distance), Hierarchical (Ward's method)
- **Validation**: Bootstrap resampling (50 iterations), Adjusted Rand Index (ARI)
- **Hypothesis Testing**: ANOVA, Chi-square, Kruskal-Wallis
- **Effect Size**: Cohen's d, Cramér's V

---

## 📖 Documentation

### Individual Step Documents (LaTeX PDFs)

All 10 steps are available as standalone professional LaTeX documents:

- 📄 [Step 1: Deciding to Segment](docs/pdfs/Step_1_Decide_to_Segment.pdf)
- 📄 [Step 2: Specifying Ideal Target](docs/pdfs/Step_2_Specify_Target.pdf)
- 📄 [Step 3: Collecting Data](docs/pdfs/Step_3_Collect_Data.pdf)
- 📄 [Step 4: Exploring Data](docs/pdfs/Step_4_Explore_Data.pdf)
- 📄 [Step 5: Extracting Segments](docs/pdfs/Step_5_Extract_Segments.pdf)
- 📄 [Step 6: Profiling Segments](docs/pdfs/Step_6_Profile_Segments.pdf)
- 📄 [Step 7: Describing Segments](docs/pdfs/Step_7_Describe_Segments.pdf)
- 📄 [Step 8: Selecting Targets](docs/pdfs/Step_8_Select_Targets.pdf)
- 📄 [Step 9: Customizing Marketing Mix](docs/pdfs/Step_9_Customize_Marketing_Mix.pdf)
- 📄 [Step 10: Evaluation & Monitoring](docs/pdfs/Step_10_Evaluation_Monitoring.pdf)

### Executive Presentation

- 🎥 [Complete Beamer Presentation (40+ slides)](docs/pdfs/Complete_Presentation.pdf)

### Code Documentation

API documentation available in `docs/api/`:
- [Clustering Module API](docs/api/clustering.md)
- [Validation Module API](docs/api/validation.md)
- [Profiling Module API](docs/api/profiling.md)

---

## 📈 Visualizations

### Key Figures Generated

1. **Segment Profile Plot**: Marker variables by segment
2. **Evaluation Matrix**: Like rating vs. visit frequency (bubble chart)
3. **Attractiveness Ranking**: Horizontal bar chart with scores
4. **Stability Analysis**: Bootstrap ARI distribution
5. **Implementation Roadmap**: 18-month Gantt chart
6. **Performance Dashboard**: Real-time KPI monitoring
7. **Alert Flowchart**: Decision tree for interventions

### Sample Output

```
# Generate all visualizations
python src/visualization.py --output outputs/figures/ --format png --dpi 300
```

---

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the repository**
2. **Create a feature branch** (`git checkout -b feature/AmazingFeature`)
3. **Commit your changes** (`git commit -m 'Add some AmazingFeature'`)
4. **Push to the branch** (`git push origin feature/AmazingFeature`)
5. **Open a Pull Request**

### Development Guidelines

- Follow PEP 8 style guide for Python code
- Include docstrings for all functions
- Add unit tests for new features
- Update documentation as needed
- Use meaningful commit messages

### Reporting Issues

Found a bug? Have a suggestion? Please [open an issue](https://github.com/yourusername/mcdonalds-market-segmentation/issues) with:
- Clear description of the problem
- Steps to reproduce
- Expected vs. actual behavior
- Screenshots (if applicable)

---

## 📄 License

This project is licensed under the **MIT License** - see the [LICENSE](LICENSE) file for details.

---


## 🙏 Acknowledgments

### References

- **Dolnicar, S., Grün, B., & Leisch, F. (2018).** *Market Segmentation Analysis: Understanding It, Doing It, and Making It Useful*. Springer.
- **Kotler, P., & Keller, K.L. (2016).** *Marketing Management*. 15th ed., Pearson Education.
- **Wedel, M., & Kamakura, W.A. (2000).** *Market Segmentation: Conceptual and Methodological Foundations*. 2nd ed., Kluwer.

### Data Source

- McDonald's consumer perception survey (anonymized)
- Original case study from Dolnicar et al. (2018)

### Tools & Libraries

- [scikit-learn](https://scikit-learn.org/) for machine learning
- [matplotlib](https://matplotlib.org/) & [seaborn](https://seaborn.pydata.org/) for visualization
- [LaTeX](https://www.latex-project.org/) for professional documentation

---

## ⭐ Star History

If you find this project useful, please consider giving it a star! ⭐

---

<div align="center">

**Made with ❤️ for Data Science & Marketing Analytics**

[⬆ Back to Top](#-mcdonalds-fast-food-market-segmentation-analysis)

</div>
```



