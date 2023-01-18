
1. Get percent parameter from terminal
2. Do while true
	1. For each line from stocks-all.csv
	2. Store input line to array in
	4. Read from "http://classic.settrade.com/C04_01_stock_quote_p1.jsp?txtSymbol=#{stock_name}&ssoPageId=9&selectPage=1"
	5. Read tag H1 which will get 4 elements
		1. constant `settrade`
		2. latest price
		3. amount change
		4. percent change
		5. Save last three elements
		6.  Calculate spreads between latest price & target
	6. If order active status <= input parameter, display to screen

3. Press ctrl-C to exit