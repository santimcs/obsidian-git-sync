
	import pandas as pd
	import sidetable
	my_dictionary  = {
	        'A':['One','One','One','Two','Two','Two','Three','Three','Three'],
	        'B':[1,2,-2,4,5,6,7,8,9]               
	}
	my_df = pd.DataFrame(my_dictionary)
		
	my_df.stb.freq(["A"], value="B")

	```
			A	B	percent	cumulative_B	cumulative_percent
	0	Three	24	60.0	24	60.0
	1 Two	    15	37.5	39	97.5
	2	One  	1	2.5	    40	100.0
	```




[Medium](https://towardsdatascience.com/pandas-sidetable-simplifies-the-exploratory-data-analysis-process-417b42eebed6)

