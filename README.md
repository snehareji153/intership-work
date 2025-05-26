This is the task 1 data cleaning that i have done on the dataset
I have done the following things:
Extracted the file fron the zip folder
uploaded it in Google colab
used pd.read_csv method to read the file
data.head--- to see the data
data.isnull().sum()---- to see the no of null data in each column
data.info()---- to see the information on the data
data.dropna()--- to drop the nan values (if all the values in the raw are null)
data.duplicated().sum()---to see the no of duplicate values in each column
data.columns---to see the column names
data['column_name'].unique()--- to see the values in the columns . I have applied this method to other columns to see the unique data
data.dtypes---- to see a summary of the datatypes of different colulmns
data['column_name'].apply(type).value_counts()--- to check if there are mixed data types in columns. I have applied this method to other columns also
data[data['column_name].apply(lambda x: isinstance(x, float))]----- to check what are the float datatypes present in each columns
data['column_name'] = data['column_name'].fillna('missing').astype(str)----- to fill the data into a single datatype(mostly str) and to replace NAN with missing values
data['date_added'] = pd.to_datetime(data['date_added'], errors='coerce')------to convert the date into datetime foemat
data['date_added'] = data['date_added'].dt.strftime('%d-%m-%Y')--- to convert the date into date-month-year format
