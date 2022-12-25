	# Get the column names in their current order.  
	new_order = cars.columns.to_list()# Remove price from the list.  
	new_order.remove('price')# Place price at the beginning of the list.  
	new_order.insert(0, 'price')# Redefine the data frame with the new column order.  
	cars = cars[new_order]

[Medium](https://medium.com/towards-data-science/moving-pandas-columns-around-c0fad1043d3a)