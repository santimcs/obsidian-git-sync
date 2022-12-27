	
	df['created_at'] = pd.to_datetime(df['created_at'])
	df['updated_at'] = pd.to_datetime(df['updated_at'])
	df['shares'] = df['shares'].astype('int64')

[[Drop Columns]]

#dates 

[Medium](https://medium.com/towards-data-science/4-python-pandas-functions-that-serve-better-with-dictionaries-bbfcc6c39fa5)