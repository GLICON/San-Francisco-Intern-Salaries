import pandas as pd
import matplotlib.pyplot as plt

# Load the CSV data
try:
    df = pd.read_csv('cleaned_salaries.csv')
except FileNotFoundError:
    print("Error: 'cleaned_salaries.csv' not found. Please check the file path.")
    exit(1)

# Validate required columns
required_cols = ['year', 'job_title', 'agency', 'total_pay']
if not all(col in df.columns for col in required_cols):
    print(f"Error: Missing required columns. Expected: {required_cols}, Found: {list(df.columns)}")
    exit(1)

# Check if total_pay is numeric
if not pd.api.types.is_numeric_dtype(df['total_pay']):
    print("Error: 'total_pay' column must be numeric.")
    exit(1)

# Define exact job titles to match (case-sensitive)
job_titles = ['PERSONNEL ANALYST', 'Personnel analyst', 'ADMINISTRATIVE ANALYST', 'Administrative analyst']

# Filter for San Francisco agency and exact job titles
df_filtered = df[(df['agency'] == 'San Francisco') & (df['job_title'].isin(job_titles))]

# Check if filtered data is empty
if df_filtered.empty:
    print("Error: No data found for the specified job titles and agency.")
    exit(1)

# Verify which job titles were found
found_titles = df_filtered['job_title'].unique()
missing_titles = [job for job in job_titles if job not in found_titles]
if missing_titles:
    print(f"Warning: The following job titles were not found in the data: {missing_titles}")

# Group by year and job_title, calculate mean total_pay
average_pay = df_filtered.groupby(['year', 'job_title'])['total_pay'].mean().reset_index()

# Pivot the data for visualization
pivot_table = average_pay.pivot_table(index='year', columns='job_title', values='total_pay')

# Display the aggregated results
print("Average Total Pay (Excluding Benefits) by Job Title and Year:")
print(pivot_table)

# Data Visualization
plt.figure(figsize=(12, 6))

# Plot a line for each job title
for job in pivot_table.columns:
    plt.plot(pivot_table.index, pivot_table[job], marker='o', markersize=8, linewidth=2, label=job)

# Customize the plot
plt.title('Average Total Pay (Excluding Benefits) for Administrative and Personnel Analysts in San Francisco', fontsize=14, pad=20)
plt.xlabel('Year', fontsize=12)
plt.ylabel('Average Total Pay ($)', fontsize=12)
plt.grid(True, linestyle='-', alpha=0.7)
plt.legend(title='Job Title', fontsize=10)
plt.xticks(pivot_table.index, rotation=45, fontsize=10)
plt.yticks(fontsize=10)

# Adjust layout to prevent clipping
plt.tight_layout()

# Show the plot
plt.show()

# The salaries trend Analysis
print("\nTrend Analysis:")
for job in job_titles:
    if job in pivot_table.columns:
        print(f"\n{job}:")
        years = pivot_table.index
        pays = pivot_table[job].dropna()
        if len(pays) > 1:
            trend = []
            for i in range(1, len(pays)):
                change = pays.iloc[i] - pays.iloc[i-1]
                trend.append(f"From {int(years[i-1])} to {int(years[i])}: {'increased' if change > 0 else 'decreased'} by ${abs(change):,.2f}")
            print("\n".join(trend))
        else:
            print("Not enough data points to determine trend.")
