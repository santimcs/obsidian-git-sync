
	import pandas as pd
	import sidetable
	my_dictionary  = {
	        'A':['One','One','One','Two','Two','Two','Three','Three','Three'],
	        'B':[1,2,-2,4,5,6,7,8,9]               
	}
	my_df = pd.DataFrame(my_dictionary)
		
	my_df.stb.freq(["A"], value="B")



[Medium](https://towardsdatascience.com/pandas-sidetable-simplifies-the-exploratory-data-analysis-process-417b42eebed6)

