# ODD2023-DataScience-Ex-03
#   EX-03 UNIVARIATE ANALYSIS


Aim:

To read the given data and perform the univariate analysis with different types of plots.
Explanation:

Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
Algorithm:

    Step1: Read the given data.
    Step2: Get the information about the data.
    Step3: Remove the null values from the data.
    Step4: Mention the datatypes from the data.
    Step5: Count the values from the data.
    Step6: Do plots like boxplots,countplot,distribution plot,histogram plot.

Program:

Developed By: MOHAMED ASIL.M
Register Number: 212222230080

  - Diabetes.csv 
```
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('diabetes.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x="Glucose",data=df)
Glucose_q1 = df['Glucose'].quantile(0.25)
Glucose_q3 = df['Glucose'].quantile(0.75)
Glucose_IQR = Glucose_q3 - Glucose_q1
Glucose_low = Glucose_q1 - 1.5 * Glucose_IQR
Glucose_high = Glucose_q3 + 1.5 * Glucose_IQR
df=df[((df['Glucose']>=Glucose_low)&(df['Glucose']<=Glucose_high))]
sns.countplot(x="Glucose",data=df)
sns.distplot(df['Glucose'])
sns.histplot(x="Glucose",data=df)
```
   - Output(diabetes.csv) :
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/ebc04d23-67fa-434a-98a0-53baa3f3a7ff)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/4ea41da8-d381-4caa-a635-ba37cbe7a880)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/fd41b934-be8c-4cc3-a9a3-2b220f1d68a5)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/857d30f2-09c7-4613-8b4c-e3e390c60c53)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/3e74511a-c1e5-443a-b7eb-3c5d258119eb)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/d6607df4-89c2-4c8d-b32b-d75a52b056d1)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/df3cdef0-37f3-427a-a654-78f3cab1ec0d)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/dae9e190-a62a-4ef0-a064-2152cc0c0f96)


```
- SuperStore.csv:
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('SuperStore.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
df['Postal Code']=df['Postal Code'].fillna(method='ffill')
sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x="Postal Code",data=df)
```
   - Output(SuperStore.csv) :
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/37a8a78b-6ee0-47ae-8146-af155ff31b2c)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/60d080fc-cbce-4ab4-af9a-862548a60c52)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/439245a4-a31c-4f1d-acbc-b2726453da6a)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/f5f1b8f3-ea28-4679-8983-7c077412523d)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/dbeed09c-2ed9-4d89-93df-81ac241f6be7)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/8e6bc619-028c-40ba-9fe4-ab1f7c78f550)
   - ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/0de8dfc0-e8ac-458c-9ece-10b3fea81e5e)
   - 






```
employeesal.csv:
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
uploaded=files.upload()
df=pd.read_csv('employeesal.csv')
df.head()
df.describe()
df.isnull().sum()
df.info()
sns.boxplot(x='Experience_Years',data=df)
sns.countplot(x="Experience_Years",data=df)
sns.distplot(df['Experience_Years'])
sns.histplot(x="Experience_Years",data=df)
```
- Output(employeesal.csv) :
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/14ffcf03-9dd5-4133-b625-23efe14d54c2)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/e3a63ea8-b1dc-4fe6-ad23-1ecb5ed41213)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/2cfcb920-032c-416b-9de2-4e6c031708f4)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/b42a4972-e699-4763-a67b-bf8556018b0b)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/cf43f01e-f70a-4c8f-a7ba-ffe4273d582d)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/f651ca9b-7f9e-46a8-9660-26b42bd3387d)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/4c0a1e99-0129-4b33-af03-321542d272d1)
- ![image](https://github.com/Asilsathik/ODD2023-DataScience-Ex-03/assets/119476247/12d2fbf7-1314-419b-818b-a1ed6289b1d2)


Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.
