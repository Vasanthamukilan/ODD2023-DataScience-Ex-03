# EX-03 UNIVARIATE ANALYSIS
## Aim:
To read the given data and perform the univariate analysis with different types of plots.
## Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.
## Algorithm:
- Step 1: Read the given data.
- Step 2: Get the information about the data.
- Step 3: Remove the null values from the data.
- Step 4: Mention the datatypes from the data.
- Step 5: Count the values from the data.
- Step 6: Do plots like boxplots,countplot,distribution plot,histogram plot.
## Program:
```
Developed By: VASANTHAMUKILAN M
Register Number: 212222230167
```
- Diabetes.csv
```Python 
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
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
- Output(diabetes.csv) :<br>
![ds_3_1](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/943c889b-5bd7-495d-8e8e-71eb75a4a938)
![ex_3_2](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/f81d2e1d-0a09-492f-862e-c58c7da60f17)
![exp_3_3](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/9a46d62d-c593-4708-b3fe-4d4863837330)
![exp_3_4](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/648e1d87-1838-4b6b-af2e-ff26667f3941)
![exp_3_5](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/f5c2abd0-9825-4f47-9bcb-c097132b37e4)
![exp_3_6](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/c5b8585a-0102-44e8-8fca-aca3019d0c89)
![exp_3_7](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/e6dc8b7b-24c4-497e-b2d4-c9a6082ba5f0)
![exp_3_8](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/09dd6657-4728-4a26-8eca-bf87cf5ea60b)
- SuperStore.csv:

```Python
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
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
![exp_3_9](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/81c0f75f-70d4-41d7-ba4f-4b9d44559f5b)
![exp_3_10](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/2050a727-ed45-41d4-b1b7-53ddfcd4a943)
![exp_3_11](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/cafdfcf7-e31f-4813-8bc9-dcc489e12d33)
![exp_3_12](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/fd9993ee-14da-4efc-a4f4-176098430470)
![exp_3_13](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/73bc8d15-f735-49fa-a173-990a19fece2d)
![exp_3_14](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/46bd12f4-722b-49a5-a48b-2868f51a577c)
![exp_3_15](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/dba867f2-cfae-419b-a805-1bb059bf6223)
![exp_3_16](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/3024a004-4d62-4353-aa6a-b2f2eb4dda10)
- employeesal.csv:
```Python
import pandas as pd
import seaborn as sns
import numpy as np
from scipy import stats
from google.colab import files
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
![exp_3_17](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/8e318cf7-9a65-4aa7-b9c7-c9180f3f4a56)
![exp_3_18](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/2af26692-82fd-4ce7-b057-f11e692e32d8)
![exp_3_20](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/146a9ae0-5d24-4a37-aec8-ec37ee2ce7e3)
![exp_3_21](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/e9f07d34-ce4e-45e8-a4c0-3fdb0e602439)
![exp_3_22](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/4c7024b3-8b78-4e11-9839-7de23f41cf3b)
![exp_3_23](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/d80d7fdf-0e1f-4b94-83cc-54a77b3d0ce4)
![exp_3_24](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/7c309add-e970-4450-8286-a82e47068336)
![exp_3_25](https://github.com/Vasanthamukilan/ODD2023-DataScience-Ex-03/assets/119559694/a33ff6e3-94e3-4454-9594-202ec701611b)
## Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.
