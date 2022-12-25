
	import pandas as pd
	
	# create a date object
	date = pd.to_datetime('2022-06-15')
	
	# find the beginning of the month for the given date
	month_start = date.to_period('M').start_time
	month_end = date.to_period('M').end_time
	
	print(f'Month start: {month_start}')
	print(f'Month end: {month_end}')

#dates 