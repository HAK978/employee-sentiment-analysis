# Employee Sentiment Analysis - Project Summary

## Overview

This project analyzes employee sentiment from 2,191 email messages collected from 10 employees at Enron Corporation during 2010-2011. The analysis uses large language model (LLM) based sentiment classification, statistical methods, and predictive modeling to identify engagement patterns, top performers, and flight risk employees.

---

## Top 3 Positive Employees

Employees with the highest normalized sentiment scores (2010-2011):

1. **eric.bass@enron.com** - Score: 0.0714
2. **sally.beck@enron.com** - Score: 0.0529
3. **lydia.delgado@enron.com** - Score: 0.0352

---

## Top 3 Negative Employees

Employees with the lowest normalized sentiment scores (2010-2011):

1. **john.arnold@enron.com** - Score: -0.0117
2. **patti.thompson@enron.com** - Score: -0.0044
3. **kayne.coulter@enron.com** - Score: 0.0057

---

## Flight Risk Identification

**Employees flagged as flight risk** (4+ negative emails within 30-day rolling window):

- **sally.beck@enron.com**: 4 negative emails in 10 days (August 15-25, 2011)

---

## Key Insights

### Sentiment Distribution
- **Neutral**: 1,898 emails (86.7%)
- **Positive**: 174 emails (7.9%)
- **Negative**: 119 emails (5.4%)

The high proportion of neutral communications reflects typical professional workplace patterns where most emails are informational or procedural.

### Communication Patterns
- **Positive-to-Negative Ratio**: 1.45:1 (moderately healthy)
- **Average Emails per Employee**: 219.1
- **Most Active**: Lydia Delgado (284 emails)
- **Least Active**: Kayne Coulter (174 emails)

### Temporal Insights
- Most employees maintain stable sentiment over time
- Sally Beck experienced an acute crisis in August 2011 despite overall positive performance
- Email volume does not strongly correlate with sentiment quality

---

## Recommendations

### Immediate Actions
1. **Investigate Sally Beck's August 2011 Crisis**: Conduct one-on-one meeting to understand the issues behind the negative communication cluster
2. **Monitor Declining Employees**: Provide support to john.arnold@enron.com and patti.thompson@enron.com
3. **Recognize Top Performers**: Acknowledge eric.bass@enron.com, sally.beck@enron.com, and lydia.delgado@enron.com

### Strategic Initiatives
1. **Implement Real-Time Monitoring**: Deploy sentiment analysis for continuous communication pattern tracking
2. **Early Intervention Protocol**: Establish procedures for reaching out when negative clusters are detected
3. **Increase Positive Communication**: Address the low positive email rate (7.9%) through recognition programs
4. **Regular Check-ins**: Implement monthly sentiment reviews to identify trends and emerging issues

### Preventive Measures
1. Provide additional support during high-stress periods
2. Create formal channels for escalating concerns
3. Develop training on positive communication practices
4. Continue longitudinal tracking to validate interventions

---

## Project Deliverables

### Code Files
- `employee_sentiment_analysis_complete.ipynb` - Main analysis notebook with all tasks
- All supporting data processing and analysis code

### Reports
- `Employee_Sentiment_Analysis_Report.tex` - Comprehensive LaTeX report

### Data Files
- `test_labeled.csv` - Complete dataset with sentiment labels

### Visualizations
All visualizations are stored in the `visualizations/` folder:

**Exploratory Data Analysis:**
- `viz_1_sentiment_distribution.png` - Overall sentiment distribution (bar chart and pie chart)
- `viz_2_individual_trajectories.png` - Individual employee sentiment over time
- `viz_3_company_trend.png` - Monthly email volume by sentiment (stacked bar chart)
- `viz_4_cumulative_trajectories.png` - Cumulative sentiment paths by employee
- `viz_5_sentiment_heatmap.png` - Employee × month sentiment heatmap
- `viz_6_employee_scores.png` - Overall employee sentiment scores

**Predictive Modeling:**
- `task6_actual_vs_predicted.png` - Model performance (actual vs predicted with residuals)

---

## Methodology

**Sentiment Labeling**: Qwen 2.5 72B Instruct LLM

**Scoring System**:
- Positive: +1
- Negative: -1
- Neutral: 0
- Normalized Score = (Positive - Negative) / Total Emails

**Flight Risk Criteria**: 4+ negative emails within any 30-day rolling window (irrespective of month boundaries)

**Predictive Modeling**: Linear regression model (R² = 1.0000) analyzing relationship between message characteristics and monthly sentiment


