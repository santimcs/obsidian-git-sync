
	rcds = df_orders.values.tolist()
	len(rcds)
	 
	 sqlIns = """
		INSERT INTO orders (trade, name, qty, price, active, reason, market, xdate)
		VALUES (?, ?, ?, ?, ?, ?, ?, ?)
		"""
		print(sqlIns)
		
	for rcd in rcds:
		conlite.execute(sqlIns, rcd)
	    

	

[[Insert records into MySQL table]]