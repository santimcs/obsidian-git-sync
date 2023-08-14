	aadf.rename(columns={'price_x':'tdy_price','price_y':'avg_price',
	                   'qty_x':'tdy_qty','qty_y':'avg_qty'},inplace=True)
	                   
	dividend.columns = dividend.columns.str.lower()


[[Move columns]]

[[Export DF to CSV Files]]

[Medium](https://medium.com/@shouke.wei/convenient-methods-to-rename-columns-of-dataset-with-pandas-in-python-389af50782f)