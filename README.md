# Data-science.mini.project
# DATA ANALYSIS
# AIM:

To Perform Data Analysis on the given dataset and save the data to a file.

# Explanation

Data analytics is important because it helps businesses optimize their performance.Implementing it into the business model means companies can help reduce costs by identifying more efficient ways of doing business and by storing large amounts of data

# ALGORITHM
# STEP 1
Read the given Data

# STEP 2
Clean the Data Set using Data Cleaning Process

# STEP 3
Apply Feature generation and selection techniques to all the features of the data set

# STEP 4
Apply data visualization techniques to identify the patterns of the data.

# CODE:

```

import pandas as pd
import numpy as np
import matplotlib.pyplot as plt
import seaborn as sns
df=pd.read_csv("/content/ds_salaries.csv",encoding="ISO-8859-1")
dfdf.isnull()
df.info()
df.describe()
sns.lineplot(x="work_year",y="salary",data=df,marker='o')
plt.title("work_year vs salary")
plt.xticks(rotation = 90)
plt.show()

sns.barplot(x="work_year",y="salary",data=df)
plt.xticks(rotation = 90)
plt.show()
df.shape
df1 = df[(df.salary>= 60)]
df1.shape

plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
plt.figure(figsize=(30,8))
states=df1.loc[:,["job_title","salary"]]
states=states.groupby(by=["job_title"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("job_title")
plt.ylabel=("salary")
plt.show()
sns.lineplot(x="company_size",y="salary",data=df)
plt.show()
states=df.loc[:,["work_year","salary"]]
states=states.groupby(by=["work_year"]).sum().sort_values(by="salary")
sns.barplot(x=states.index,y="salary",data=states)
plt.xticks(rotation = 90)
plt.xlabel=("work_year")
plt.ylabel=("salary")
plt.show()
df.groupby(['work_year']).sum().plot(kind='pie', y='salary',figsize=(6,9),pctdistance=1.7,labeldistance=1.2)
df["work_year"].corr(df["salary"])
df_corr = df.copy()
df_corr = df_corr[["work_year","salary"]]
df_corr.corr()
sns.pairplot(df_corr, kind="scatter")
plt.show()
grouped_data = df.groupby('employment_type')[['work_year', 'salary']].mean()
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
ax.bar(grouped_data.index, grouped_data['work_year'], label='work_year')
ax.bar(grouped_data.index, grouped_data['salary'], bottom=grouped_data['work_year'], label='salary')
ax.set_xlabel('employment_title')
ax.set_ylabel('Value')
ax.legend()
plt.show()
grouped_data = df.groupby(['job_title', 'company_size'])[['work_year', 'salary']].mean()
pivot_data = grouped_data.reset_index().pivot(index='job_title', columns='company_size', values=['work_year', 'salary'])
# Create a bar chart of the grouped data
fig, ax = plt.subplots()
pivot_data.plot(kind='bar', ax=ax)
ax.set_xlabel('job_title')
ax.set_ylabel('Value')
plt.legend(title='company_size')
plt.show()

```

# OUTPUT:

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/057920fc-6996-4e90-8816-0855883e270b)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/37d8731e-9f91-42e8-8a9c-9b066c721158)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/118bcf66-d479-43ca-bb61-cde153c98b14)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/a613500d-54be-41f5-bfb6-299b572c19da)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/ede0b8e1-03da-4c62-a2e1-dccadf0846eb)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/6eaf7818-1ad1-4bdb-85f6-11d3a74f4668)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/ebe60605-d3db-4ac6-b4bd-416f4765a1aa)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/9b199fbc-2b4e-460f-a385-1a32f632ea55)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/cdbe4917-6f0a-45fd-916b-bdfcdc826120)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/6e610be3-bb38-4111-b1e4-6b2e575487d8)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/3fe49fec-7e71-4396-916e-dba5aa0eeeeb)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/112525a6-27bb-4ae8-b609-e018d052cea4)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/cd5b896b-fc96-4968-ad0d-230c45f6ea4c)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/b18e912e-2610-466f-b9c6-4322d5c734a8)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/aae400b0-c87f-4066-a362-34e28594c110)

![image](https://github.com/premalatha-sureshbabu/Data-science.mini.project/assets/120620842/18f2ef95-955f-4826-8c26-563ac485829d)


# Result:

Thus, Data analysis is performed on the given dataset and save the data to a file

