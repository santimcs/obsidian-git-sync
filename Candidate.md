
1. Get spread parameter
2. Do while true
	1. For each line from orders.csv
	2. Bypass first line, which is header
	3. Store input line to array in
	4. Read from "http://classic.settrade.com/C04_01_stock_quote_p1.jsp?txtSymbol=#{stock_name}&ssoPageId=9&selectPage=1"
	5. Read tag H1 which will get 4 elements
		1. constant `settrade`
		2. latest price
		3. amount change
		4. percent change
		5. Save last three elements
		6.  Calculate spreads between latest price & target
	6. If spread <= input parameter, display to screen

3. Press ctrl-C to exit
	

