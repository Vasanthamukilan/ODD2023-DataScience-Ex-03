# ODD2023-DataScience
# Ex-03 Univariate Analysis
# Aim:
To read the given data and perform the univariate analysis with different types of plots.

# Explanation:
Univariate analysis is basically the simplest form to analyze data. Uni means one and this means that the data has only one kind of variable. The major reason for univariate analysis is to use the data to describe. The analysis will take data, summarise it, and then find some pattern in the data.

# Algorithm:
### Step1:
Read the given data.

### Step2:
Get the information about the data.

### Step3:
Remove the null values from the data.

### Step4:
Mention the datatypes from the data.

### Step5:
Count the values from the data.

### Step6:
Do plots like boxplots,countplot,distribution plot,histogram plot.

# Program:
DEVELOPED BY :Vasanthamukilan M

REGISTER NO :212222230167

## SUPERSTORE.CSV
```
import pandas as pd
import numpy as np
import seaborn as sns

df=pd.read_csv('superstore.csv')
df

df.head()
df.info()
df.describe()
df.isnull().sum()

df.dtypes

df['Postal Code'].value_counts()

sns.boxplot(x='Postal Code', data=df)
sns.countplot(x='Postal Code',data=df)
sns.distplot(df["Postal Code"])
sns.histplot(x='Postal Code',data=df)
```
## DIABETES.CSV:
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
## EMPLOYEESAL.CSV
```
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
# OUTPUT:
# SUPERSTORE.CSV:

![272515924-dab07356-02d3-482c-925d-f71090f0c8e5](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/c3ed9ded-d972-4f6d-9fe0-02be9cb93e54)



![272516004-c4bb4ae5-4e51-4b9a-a5f0-b3014cb648ec](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/c8174ab9-1aee-48b7-bfc0-23a5263850bb)


![272516081-6199aaf4-0268-4535-b4c4-3a6ef42b9141](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/809e69ee-da1b-46bc-8b2a-c37c90dffdb5)



![272516138-ae5c0f59-20eb-4944-af48-1dd2e95b9072](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/cb27fb7c-65d7-43c1-9470-f485d0e6bf2b)


![272516201-a5a98935-3097-4af6-8003-ac9d510c8fc2](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/79fad7a6-5f6d-4aa0-b844-5a1f51cb5dc5)



![272516284-49c3e822-cc10-4006-9bf1-67b01ac6456f](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/49366ff6-ee13-48e7-ae6f-fc31b06da4bd)


![272516402-04e3240c-4cad-4560-81f5-da78765ee284](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/0c3e63b3-e8ef-415d-8fc1-399a4bff8856)


![272516480-44f74bb3-d204-4f6a-8cb8-66405adad5a1](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/4ca2b799-f1ec-4920-8afe-f3bbf9f5d94c)


![272516557-fd880d66-572b-4ee2-9076-f87314fb9b16](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/03bf88f7-3b29-4c75-bdea-ea5aa046aef4)




![272516754-2b383bc1-a9cd-4daf-90ba-94123fbe416b](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/d4f0c7dc-ff1e-438b-aad3-7e7327e2e3fd)


![272516818-07e83a45-f8f1-4378-a4a0-f2c37a44d935](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/c515d754-f075-42d7-b5b0-d603a861e54c)

# DIABETES.CSV

![272159225-1d3b12f6-7b20-4d55-bc5b-aa87020d5b89](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/d45e6459-5adf-4ef0-81a3-6bd4364091a7)

![272159241-fa9b48c9-50b2-4c7d-a41b-7dd97ccbeffa](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/98512a37-e4db-419d-9fe7-a1bd636b530f)

![272159261-df172427-658f-4dab-a2e1-4a8ff56c8639](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/706ed497-b59b-4c69-87ce-e05ca3a734db)

![272159283-a079d5b0-5e56-4a79-8b82-b23e79c26f2d](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/a8e10c82-c6e6-42d1-9cd8-eb564b868a22)

![272159299-6b8f321b-1b0b-4ef6-b1a3-15ccdb51d5f9](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/1c2faa26-961d-4622-a5ba-edbef68e94aa)

![272159332-40ca042e-5c75-42e0-8786-c26c54039280](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/b08ae918-b4a6-41ff-bbf5-23db5eb36ff8)

![272159352-c275a6cf-0d5e-4783-b4cc-5bd5999d1a07](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/317efdf1-a7c8-45b6-b033-28e15fba1ecf)

# EMPLOYEESAL.CSV:
![272162113-3c6aa2b1-a2c9-4e5c-b244-c1fd7b95de74](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/2abc376b-a481-4884-b18d-0f81f3aa5054)

![272162136-50535ce5-798d-4689-a510-8b64542272e2](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/374e1837-5a41-45a5-916a-9d8489f21bf3)

![272162126-7d5f1c67-e2ec-403f-908b-bba9fc6a1923](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/580ed8dd-7cc0-4a8f-bf41-a8fa07a19e03)

![272162150-d33eeccd-9096-470d-852f-1d7d5e76b979](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/e4feeb08-1284-4eec-a4e8-3df56cc30b52)

![272162162-73f32d4e-4fbc-46c7-bd18-18cc201e5998](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/ab63a7c7-479f-4808-bedf-d8be35dd1538)

![272162171-bbdeff51-b108-4786-9223-8f6e825262a7](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/28b74c82-8dbc-40e1-b6e9-7a1a7a4e62bd)

![272162189-9506c400-a405-424e-bbd8-5fc0417c3572](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/9f52bb1d-9512-43ad-ae84-aaf1d3af0443)

![272162201-e574c9ed-8fdb-4f37-ad51-d8294e17a846](https://github.com/KRISHNARAJ-D/ODD2023-DataScience-Ex-03/assets/119559695/c886ebf6-ca55-495d-beb8-eea2b2dec00e)



# Result:
Thus we have read the given data and performed the univariate analysis with different types of plots.
