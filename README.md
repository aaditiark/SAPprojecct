

import numpy as np # linear algebra
import pandas as pd # data processing, CSV file I/O (e.g. pd.read_csv)


import os
for dirname, _, filenames in os.walk('/kaggle/input'):
    for filename in filenames:
        print(os.path.join(dirname, filename))
import pandas as pd
import seaborn as sns
sns.set(color_codes=True)
df = pd.read_csv('Customer Call List.csv')
df.head()
df.info()
df.describe()
df.isna()
df.isna().sum()
df.shape
df.hist()
df.Address.value_counts().plot(kind='pie')
df.Last_Name.value_counts().plot(kind= 'bar') 
import matplotlib.pyplot as plt
%matplotlib inline
# %matplotlib notebook
plt.hist(df.Address);
plt.boxplot(df.CustomerID);
sns.scatterplot(data=df, x="Address",y="Last_Name");
x=[1,2,3]
y=[3,4,5]
plt.plot(x,y)
plt.show()
plt.plot(x,y,'b+')
plt.show()
plt.plot(x,y,'b--')
plt.show()
sns.heatmap(df.corr(numeric_only=True))
plt.show()
sns.heatmap(df.corr(numeric_only=True),annot=True)
plt.show()
