
	sql = """
	SELECT date, amount, C.name AS item, G.name AS kind, strftime("%m", date) as Month 
	FROM transactions T 
	JOIN categories C ON category_id = C.id 
	JOIN groups G ON group_id = G.id 
	WHERE strftime('%Y', date) = '2022'
	"""
	
	monthly = df.groupby("Month")
	monthly.sum().style.format(format_dict)

[Medium](https://medium.com/gitconnected/how-to-use-groupby-effectively-as-a-data-scientist-9e1d931e1619)