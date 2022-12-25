	filters = [
	   (df.market.str.contains('SET50')),
	   (df.market.str.contains('SET100')),
	   (df.market.str.contains('mai'))]
	values = ['SET50','SET100','mai']
	df["mrkt"] = np.select(filters, values, default='SET999')
	
	df["mrkt"].value_counts()


#filters 