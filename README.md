This is the task 1 data cleaning that i have done on the dataset
1.I have done the following things:
2.Extracted the file fron the zip folder
3.uploaded it in Google colab
4.used pd.read_csv method to read the file
5.data.head--- to see the data
6.data.isnull().sum()---- to see the no of null data in each column
7.data.info()---- to see the information on the data
8.data.dropna()--- to drop the nan values (if all the values in the raw are null)
9.data.duplicated().sum()---to see the no of duplicate values in each column
10.data.columns---to see the column names
11.data['column_name'].unique()--- to see the values in the columns . I have applied this method to other columns to see the unique data
12.data.dtypes---- to see a summary of the datatypes of different colulmns
13.data['column_name'].apply(type).value_counts()--- to check if there are mixed data types in columns. I have applied this method to other columns also
14.data[data['column_name].apply(lambda x: isinstance(x, float))]----- to check what are the float datatypes present in each columns
15.data['column_name'] = data['column_name'].fillna('missing').astype(str)----- to fill the data into a single datatype(mostly str) and to replace NAN with missing values
16.data['date_added'] = pd.to_datetime(data['date_added'], errors='coerce')------to convert the date into datetime foemat
17.data['date_added'] = data['date_added'].dt.strftime('%d-%m-%Y')--- to convert the date into date-month-year format
