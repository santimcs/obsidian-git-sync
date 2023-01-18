
1. Get spread parameter
2. Do while true
	1. For each line from orders.csv
	2. Bypass first line, which is header
	3. Store input line to array in
	4. Read from "http://classic.settrade.com/C04_01_stock_quote_p1.jsp?txtSymbol=#{stock_name}&ssoPageId=9&selectPage=1"