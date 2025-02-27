# Hotel-Booking-Data-Analysis
# Aleena Riaz
#SU92-BSAIM-F24-158-158

# Hotel Booking Analysis

## Steps to Reproduce

### Step 1: Load the Dataset
```python
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns

# Suppress warnings
import warnings
warnings.filterwarnings('ignore')

# Load the dataset
df = pd.read_csv('hotel_booking.csv')
```

### Step 2: Explore and Clean Data
- Check for missing values:
  ```python
  df.isnull().sum()
  ```
- Drop or fill missing values based on data relevance.

### Step 3: Perform Exploratory Data Analysis (EDA)
- **Visualization of Booking Trends**
```python
sns.countplot(x='hotel', data=df)
plt.title('Bookings per Hotel Type')
plt.show()
```
- **Analyzing Lead Time:**
```python
plt.figure(figsize=(10, 6))
sns.histplot(df['lead_time'], bins=50, kde=True)
plt.title('Lead Time Distribution')
plt.xlabel('Lead Time (days)')
plt.show()
```

### Step 4: Extract Key Insights
Conduct deeper analysis on:
- Cancellation rates.
- Guest demographics (country, special requests).
- Seasonal trends.
