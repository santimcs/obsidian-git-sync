
	sql = """
	SELECT date, amount, C.name AS item, G.name AS kind, strftime("%m", date) as Month 
	FROM transactions T 
	JOIN categories C ON category_id = C.id 
	JOIN groups G ON group_id = G.id 
	WHERE strftime('%Y', date) = '2022'
	"""

	sales.groupby("product_group", as_index=False).agg(  
	avg_price = ("price","mean")  
	)

	sales.groupby("product_group", as_index=False).agg(  
	avg_price = ("price","mean"),  
	avg_stock_qty = ("stock_qty","mean")  
	)


	monthly = df.groupby("Month")
	monthly.sum().style.format(format_dict)

[Medium](https://medium.com/gitconnected/how-to-use-groupby-effectively-as-a-data-scientist-9e1d931e1619)

[Medium2](https://medium.com/towards-data-science/all-pandas-groupby-you-should-know-for-grouping-data-and-performing-operations-2a8ec1327b5)