

	osd_path = "\\Users\\User\\OneDrive\\Documents\\obsidian-git-sync\\Data\\"
	
	file_name = '5-day-average.csv'
	data_file = data_path + file_name
	output_file = csv_path + file_name
	box_file = box_path + file_name
	one_file = one_path + file_name
	osd_file = osd_path + file_name
	
	df[colu].sort_values(["prc_pct"], ascending=False).to_csv(data_file, index=False)
	df[colu].sort_values(["prc_pct"], ascending=False).to_csv(output_file, index=False)
	df[colu].sort_values(["prc_pct"], ascending=False).to_csv(box_file, index=False)
	df[colu].sort_values(["prc_pct"], ascending=False).to_csv(one_file, index=False)
	df[colu].sort_values(["prc_pct"], ascending=False).to_csv(osd_file, index=False)


[[Convert stock names to string for use in SQL IN criteria]]

[[Export DF to table in database to update data with SQL]]

[[How to Read Dataset from GitHub]]

