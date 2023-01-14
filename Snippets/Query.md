
	# Set a variable  
	min_age = 30  
	  
	# Use the variable in the query function  
	df_filtered = df.query('age > @min_age')  
	  
	# View the filtered DataFrame  
	print(df_filtered)

[Medium](https://medium.com/towardsdev/harness-the-power-of-the-pandas-query-function-2e964331f370)