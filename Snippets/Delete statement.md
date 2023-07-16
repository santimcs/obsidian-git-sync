
	sqlDel = """
	DELETE FROM profits
	WHERE name in (%s)"""
	sqlDel = sqlDel % in_p
	print(sqlDel)
	
	rp = conmy.execute(sqlDel)
	rp.rowcount