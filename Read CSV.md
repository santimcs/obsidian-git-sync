
	file_name   = 'orders-log.csv'
	input_file = data_path + file_name
	#col_names   = ['trade','name','spreads','reason','market','qty','target_price','set_price','chg_amt','chg_pct','active']
	df_log = pd.read_csv(input_file, sep=',',  index_col=None)
	df_log