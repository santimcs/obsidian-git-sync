1. Output to summary.csv
	1. Output header to output file
	2. Print header columns to screen
2. Input file is filtered price records
3. For each input row
	1. If 1st records, save values
	2. from 2nd record onward
		1.  If group break
			Derived values
			Output row
			Save values
		 2. If same group
			 1. Compare prices to get trend
			 2. If trend changes
				 1. Derived values
				 2. Output row
				 3. Save values
	3.  Do every row
		1. Save row to previous row
		2. Accumulate total qty
		3. Check and keep max & min prices
		