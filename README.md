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























Here’s a neatly organized syntax reference for Exploratory Data Analysis (EDA) in Python, covering various statistical metrics, graphical representations, and data preprocessing techniques.

### EDA

#### First Moment Business Decision
**Mean**
```python
mean_value = data['column_name'].mean()
```
*Calculates the average value of a numerical column, providing a central measure of the dataset.*

**Mode**
```python
mode_value = data['column_name'].mode()[0]
```
*Identifies the most frequently occurring value in a dataset, useful for categorical data.*

**Median**
```python
median_value = data['column_name'].median()
```
*Determines the middle value of a dataset, offering a robust measure against outliers.*

---

#### Second Moment Business Decision (Measure of Dispersion)
**Standard Deviation**
```python
std_dev = data['column_name'].std()
```
*Measures the amount of variation or dispersion of a set of values.*

**Variance**
```python
variance = data['column_name'].var()
```
*Quantifies the degree to which values deviate from the mean, highlighting variability.*

**Range**
```python
range_value = data['column_name'].max() - data['column_name'].min()
```
*Calculates the difference between the maximum and minimum values, indicating spread.*

---

#### Third Moment Business Decision
**Skewness**
```python
skewness = data['column_name'].skew()
```
*Measures the asymmetry of the probability distribution of a real-valued random variable.*

---

#### Fourth Moment Business Decision
**Kurtosis**
```python
kurtosis = data['column_name'].kurtosis()
```
*Measures the "tailedness" of the probability distribution, indicating the presence of outliers.*

---

### Graphical Representation

#### Univariate Graphs
**Histogram**
```python
import matplotlib.pyplot as plt
data['column_name'].hist()
plt.title('Histogram')
plt.xlabel('Values')
plt.ylabel('Frequency')
plt.show()
```
*Visualizes the distribution of a single variable, highlighting frequency of values.*

**Box Plot**
```python
data.boxplot(column='column_name')
plt.title('Box Plot')
plt.show()
```
*Displays the summary of a dataset’s distribution, highlighting median, quartiles, and outliers.*

---

#### Bivariate Graphs
**Scatter Plot**
```python
plt.scatter(data['column_x'], data['column_y'])
plt.title('Scatter Plot')
plt.xlabel('X-axis')
plt.ylabel('Y-axis')
plt.show()
```
*Shows the relationship between two variables, revealing correlations.*

**Pair Plot**
```python
import seaborn as sns
sns.pairplot(data)
plt.show()
```
*Displays pairwise relationships in a dataset, useful for multivariate analysis.*

---

#### Multivariate Graphs
**Heatmap**
```python
import seaborn as sns
correlation_matrix = data.corr()
sns.heatmap(correlation_matrix, annot=True, cmap='coolwarm')
plt.title('Heatmap of Correlations')
plt.show()
```
*Visualizes the correlation between multiple variables in a matrix format, indicating strength and direction of relationships.*

---

### Data Preprocessing Techniques

#### Typecasting
```python
data['column_name'] = data['column_name'].astype('int')
```
*Changes the datatype of a column to a specified type (e.g., from float to int).*

---

#### Handling Duplicates
```python
data = data.drop_duplicates()
```
*Removes duplicate rows from the dataset to ensure data integrity.*

---

#### Outlier Treatment
**Z-Score Method**
```python
from scipy import stats
data = data[(np.abs(stats.zscore(data['column_name'])) < 3)]
```
*Removes outliers by filtering based on Z-scores beyond a specified threshold.*

**IQR Method (Interquartile Range)**
```python
Q1 = data['column_name'].quantile(0.25)
Q3 = data['column_name'].quantile(0.75)
IQR = Q3 - Q1
data = data[(data['column_name'] >= (Q1 - 1.5 * IQR)) & (data['column_name'] <= (Q3 + 1.5 * IQR))]
```
*Identifies and removes outliers based on the interquartile range.*

---

**Winsorization**
```python
from scipy.stats import mstats
data['column_name'] = mstats.winsorize(data['column_name'], limits=[0.05, 0.05])
```
*Replaces extreme values with the nearest value within a specified percentile range.*

**Trimming**
```python
data = data[(data['column_name'] > lower_bound) & (data['column_name'] < upper_bound)]
```
*Removes outliers by specifying lower and upper bounds.*

---

#### Zero and Near Zero Variance
```python
from sklearn.feature_selection import VarianceThreshold
selector = VarianceThreshold(threshold=0.01)  # 1% variance threshold
data = selector.fit_transform(data)
```
*Removes features with low variance, which provide little to no information.*

---

#### Discretization
**Binarization**
```python
from sklearn.preprocessing import Binarizer
scaler = Binarizer(threshold=0.0)
data['binarized'] = scaler.fit_transform(data[['column_name']])
```
*Converts numerical features into binary variables based on a threshold.*

**Binning**
```python
data['binned'] = pd.cut(data['column_name'], bins=5)
```
*Divides continuous data into discrete bins, making analysis easier.*

---

#### Dummy Variable Creation
**One Hot Encoding**
```python
data = pd.get_dummies(data, columns=['categorical_column'], drop_first=True)
```
*Converts categorical variables into binary columns, allowing for easier modeling.*

**Label Encoding**
```python
from sklearn.preprocessing import LabelEncoder
le = LabelEncoder()
data['encoded'] = le.fit_transform(data['categorical_column'])
```
*Converts categorical labels into numeric values, preserving order.*

---

**Dummy Coding Scheme**
```python
data = pd.get_dummies(data, columns=['categorical_column'], drop_first=False)
```
*Creates dummy variables for categorical features without dropping the first category.*

**Effect Coding Scheme**
```python
data = pd.get_dummies(data, columns=['categorical_column'], drop_first=True)
data['effect_coded'] = data['categorical_column'] - data['categorical_column'].mean()
```
*Represents categorical variables as effects, centering around the mean.*

**Feature Hashing Scheme**
```python
from sklearn.feature_extraction import FeatureHasher
h = FeatureHasher(n_features=10, input_type='string')
hashed_features = h.transform(data['categorical_column'].astype(str))
```
*Transforms categorical variables into a fixed number of features using hashing.*

---

#### Handling Missing Values
**Imputation**
```python
from sklearn.impute import SimpleImputer
imputer = SimpleImputer(strategy='mean')
data['column_name'] = imputer.fit_transform(data[['column_name']])
```
*Fills missing values using a specified strategy (e.g., mean, median).*

---

#### Transformation
**Log Transformation**
```python
data['log_transformed'] = np.log(data['column_name'])
```
*Reduces skewness and stabilizes variance by applying logarithm.*

**Square Root Transformation**
```python
data['sqrt_transformed'] = np.sqrt(data['column_name'])
```
*Similar to log transformation, it reduces skewness and can improve normality.*

**Reciprocal Transformation**
```python
data['reciprocal_transformed'] = 1 / data['column_name']
```
*Inverts values, effectively treating very high values as low and vice versa.*

---

#### Feature Scaling
**Standardization**
```python
from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
data[['scaled_column']] = scaler.fit_transform(data[['column_name']])
```
*Rescales features to have a mean of 0 and a standard deviation of 1.*

**Min-Max Scaling**
```python
from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
data[['scaled_column']] = scaler.fit_transform(data[['column_name']])
```
*Rescales features to a fixed range (usually 0 to 1), preserving relationships.*

---

This concise syntax guide should provide a solid foundation for performing EDA and various preprocessing techniques in Python. Let me know if you need further elaboration on any specific topic!
