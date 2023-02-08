	importPrice.bat
	
	mysqlimport --ignore-lines=1 --fields-terminated-by=',' --fields-enclosed-by='"' --lines-terminated-by='\n' -u <username> -p <database_name> <file.csv>


[[DL _Nite2 Batch]]

#price