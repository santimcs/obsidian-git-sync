	
	df['created_at'] = pd.to_datetime(df['created_at'])
	df['updated_at'] = pd.to_datetime(df['updated_at'])
	df['shares'] = df['shares'].astype('int64')

[[Drop Columns]]

#dates 