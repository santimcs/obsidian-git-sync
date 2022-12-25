		import pandas as pd
	
		# Create a sample DataFrame
		df = pd.DataFrame({'A': [1, 2, 3, 4, 5],
		                   'B': [6, 7, 8, 9, 10]})
		
		print(df)
		
		# Drop the second and third rows
		df.drop([1, 2], inplace=True)
		
		print(df)



	   A   B
	0  1   6
	1  2   7
	2  3   8
	3  4   9
	4  5  10
	   A   B
	0  1   6
	3  4   9
	4  5  10


#rows