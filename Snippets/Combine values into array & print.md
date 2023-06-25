
	array = pd.Series([p1cost, p1profit, p1pct])
	array = array.map('฿{:,.2f}'.format)
	for value in array:
	    print(f"The value is: {value}")



[[Format single float variable]]