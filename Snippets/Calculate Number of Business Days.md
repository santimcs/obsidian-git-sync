			# For each row in the DataFrame, generate a series of dates between the start and end dates
			df['dates'] = df.apply(lambda x: pd.date_range(x['fm_date'], x['to_date']), axis=1)
			
			# For each row in the DataFrame, select only the business days (Monday through Friday) from the series of dates
			df['business_days'] = df['dates'].apply(lambda x: x[x.isin(pd.date_range(x.min(), x.max(), freq='B'))])
			
			# For each row in the DataFrame, count the number of business days between the start and end dates
			df['bdays'] = df['business_days'].apply(lambda x: len(x))


#dates 
