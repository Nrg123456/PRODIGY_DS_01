# PRODIGY_DS_01
import pandas as pd
import matplotlib.pyplot as plt
import seaborn as sns
# dataset with age and gender
data = {
    'Age': [23, 45, 31, 22, 35, 42, 28, 31, 36, 27, 40],
    'Gender': ['Male', 'Female', 'Male', 'Female', 'Male', 'Female', 'Female', 'Male', 'Female', 'Female', 'Male']
}
df = pd.DataFrame(data)
# Count of each gender
gender_counts = df['Gender'].value_counts()

# Plot bar chart
sns.barplot(x=gender_counts.index, y=gender_counts.values)
plt.title('Distribution of Gender')
plt.xlabel('Gender')
plt.ylabel('Count')
plt.show()
# Plot histogram
plt.hist(df['Age'], bins=5, color='skyblue', edgecolor='black')
plt.title('Distribution of Age')
plt.xlabel('Age')
plt.ylabel('Frequency')
plt.show()
