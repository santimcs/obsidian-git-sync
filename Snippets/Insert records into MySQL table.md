  
	sqlIns = """
	INSERT INTO buy (name, date, volbuy, price, volsell, volbal, active, dividend, period, grade)
	VALUES (%s, %s, %s, %s, %s, %s, %s, %s, %s, %s)
	"""
	print(sqlIns)
	
	rp = const.execute(sqlIns, rcd)
	rp.rowcount