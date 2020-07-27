
```python
df = pd.read_csv('raw-data/mt-combined.csv', dtype={'NAICSCode':str})
naics = pd.read_csv('raw-data/naics-6-digit-codes.csv',dtype={'naics':str})
df = df.merge(naics, left_on='NAICSCode', right_on='naics')
df.to_csv('mt-ppp-loans.csv', index=False)

```