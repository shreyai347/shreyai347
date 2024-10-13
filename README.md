# 👋 Hello there!

Welcome to my GitHub profile! I'm **Shreya** ✨, a passionate data enthusiast eager to uncover insights and tell stories through data analysis.

## 🔍 About Me
- 👀 I’m interested in **Data Insights**: I love diving deep into datasets to extract meaningful patterns and trends. 📊
- 🌱 Currently learning in **Bangalore, Karnataka**: Exploring the tech hub of India while honing my data skills! 🚀
  
## 🛠️ Tech Stack
Here's a glimpse of the technologies I'm working with:
- 📈 **Data Science** 
- 🤖 **Machine Learning** 
- 🧠 **Deep Learning** 
- 🗣️ **NLP (Natural Language Processing)** 
- 🐍 **Python** 
- 🔍 **Exploratory Data Analysis (EDA)** 
- 🗄️ **SQL** 
- 📊 **Power BI** 
- 📝 **Jupyter/Google Colab** 
- 🌐 **Flask** 

## 🌟 Fun Fact
I believe data is like a treasure chest; the more you dig, the more you discover! 🏴‍☠️💎

## 📫 Let's Connect
I’d love to connect with fellow data enthusiasts, so feel free to reach out to me! 🤝

- ✉️ Email: [shreyashreya2322@gmail.com](mailto:shreyashreya2322@gmail.com)
- 🔗 LinkedIn: [Shreya Nagarbawdi](https://www.linkedin.com/in/shreya-nagarbawdi-a7749a24a/)

## ⚡ Fun Fact
When I'm not analyzing data,  I'm hanging out with friends ☕ and watching series!🏞️
around Bangalore! 

Thank you for visiting my profile. Let's embark on this data journey together! 🎉






Sure! Here are additional univariate and bivariate graphs in Python, along with one-line descriptions for each.

### Univariate Graphs

#### 1. **Bar Plot**
```python
data['categorical_column'].value_counts().plot(kind='bar')
plt.title('Bar Plot')
plt.xlabel('Categories')
plt.ylabel('Frequency')
plt.show()
```
*Displays the frequency of categories in a categorical variable, making it easy to compare counts.*

#### 2. **Density Plot**
```python
import seaborn as sns
sns.kdeplot(data['column_name'], shade=True)
plt.title('Density Plot')
plt.xlabel('Values')
plt.ylabel('Density')
plt.show()
```
*Visualizes the distribution of a continuous variable, showing the probability density function.*

#### 3. **Violin Plot**
```python
sns.violinplot(x=data['categorical_column'], y=data['column_name'])
plt.title('Violin Plot')
plt.show()
```
*Combines box plots and density plots, providing insights into the distribution of a continuous variable across different categories.*

#### 4. **QQ Plot (Quantile-Quantile Plot)**
```python
import statsmodels.api as sm
sm.qqplot(data['column_name'], line='s')
plt.title('QQ Plot')
plt.show()
```
*Assesses whether a dataset follows a given distribution, typically a normal distribution.*

#### 5. **Count Plot**
```python
sns.countplot(data=data, x='categorical_column')
plt.title('Count Plot')
plt.show()
```
*Visualizes the count of observations in each categorical bin, similar to a bar plot but specifically for counts.*

### Bivariate Graphs

#### 1. **Line Plot**
```python
plt.plot(data['date_column'], data['value_column'])
plt.title('Line Plot')
plt.xlabel('Date')
plt.ylabel('Values')
plt.show()
```
*Shows the relationship between two continuous variables over time, highlighting trends.*

#### 2. **Bubble Plot**
```python
plt.scatter(data['column_x'], data['column_y'], s=data['size_column']*10, alpha=0.5)
plt.title('Bubble Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
*Extends scatter plots by including a third dimension through the size of the bubbles, representing additional data.*

#### 3. **Hexbin Plot**
```python
plt.hexbin(data['column_x'], data['column_y'], gridsize=30, cmap='Blues')
plt.colorbar()
plt.title('Hexbin Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
*Visualizes the relationship between two continuous variables using hexagons, useful for large datasets to indicate density.*

#### 4. **Facet Grid**
```python
g = sns.FacetGrid(data, col='categorical_column')
g.map(sns.scatterplot, 'column_x', 'column_y')
plt.show()
```
*Displays the relationship between two variables across different levels of a categorical variable, enabling comparative analysis.*

#### 5. **Heatmap for Categorical vs. Numerical**
```python
sns.heatmap(data.pivot_table(values='numerical_column', index='categorical_column', columns='another_categorical_column'), annot=True, cmap='coolwarm')
plt.title('Heatmap for Categorical vs. Numerical')
plt.show()
```
*Visualizes the mean (or other aggregates) of a numerical variable across different categories, indicating patterns or trends.*

### Summary

These graphs will help you analyze and visualize the relationships and distributions within your data, providing valuable insights during the exploratory data analysis (EDA) process. If you need further details or additional graphs, feel free to ask!
