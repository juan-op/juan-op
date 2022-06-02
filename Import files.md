# Import files

## Text file
```python
file = open('filename', mode='r' / 'w') # 'r' is to read / 'w' is to write
text = file.read()
file.close()
```
It is best practice to use the context manager to open the file, this way there is no need to close the file.

```python
with open('filename', 'r') as file:
    file.read()
```

## Flat file
### [NumPy](inkdrop://note/I-4nbwyon)
```python
data = np.loadtxt('filename', delimiter=',',
                  skiprows=1, 
                  usecols=[a, b],
                  dtype=str).
```
```python
data = np.genfromtxt('filename', delimiter=',',
                     names=True,
                     dtype=None)
```
```python
data = np.recfromcsv('filename.csv')
```

### [pandas](inkdrop://note/fPNX08JlK)
```python
df = pd.read_csv('filename.csv',
                 sep=',',
                 comment='',
                 na_values=['']
                 nrows=1,
                 header=None)
```

## Excel
```python
data = pd.ExcelFile('filename.xlsx')

data.sheet_names # to get the sheet names of the file

df = data.parse('nameofthesheet',
                skiprows=[a],
                names=[''],
                usecols=[b]
               
               ) # to load a sheet into a DataFrame
///
df = data.parse(0) # you can also use the index number of the sheet
```

## Pickle
A python native file type, used for serializing Python object structures (converting objects to bytestream).
```python
import pickle

with open('filename.pkl', 'rb') as file: # 'rb' to read as binary 
    d = pickle.load(file)
```
## SAS
```python
from sas7bdat import SAS7BDAT

with SAS7BDAT('filename.sas7bdat') as file:
    df_sas = file.to_data_frame()
```

## Stata
```python
data = pd.read_stata('filename.dta')
```
