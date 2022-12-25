	filter_all.to_sql('filter_all', engine1, if_exists='replace')
	
	sql = '''
	UPDATE stocks
	  SET
	    market = (SELECT filter_all.market_x FROM filter_all WHERE filter_all.name = stocks.name)
	'''
	rp = conlite.execute(sql)
	rp.rowcount

[[Insert records into SQLite table]]