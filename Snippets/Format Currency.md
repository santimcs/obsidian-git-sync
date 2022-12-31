
	import pandas as pd
	
	# Create a sample DataFrame with a float column
	df = pd.DataFrame({'x': [123.4567, 345.678, 567.89]})
	
	# Define a formatting function that converts a float to a string with two decimal places
	def to_currency(x):
	    return '${:,.2f}'.format(x)
	
	# Apply the formatting function to the float column
	df['x'] = df['x'].apply(to_currency)
	
	print(df)

	df['x'] = df['x'].map('${:,.2f}'.format)
	print(df)


[[Format PortLite]]
