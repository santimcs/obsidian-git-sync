
	sqlUpd = """
	UPDATE stocks
	  SET
	    market = (SELECT filter_all.market_x FROM filter_all 
	    WHERE filter_all.name = stocks.name)
	"""
	rp = conlite.execute(sqlUpd)
	rp.rowcount

#sql_updates