mysqTo open a MySQL database using the command line in XAMPP, follow these steps:

1. Open XAMPP Control Panel.
2. Start the MySQL module by clicking on the ‘Start’ button next to it.
3. Click on the ‘Shell’ button in XAMPP Control Panel to open a command-line interface.
4. Connect to MySQL by entering the following command:

```bash
mysql -u root -p
```

	5. USE stock;
	6. SELECT COUNT(*) from price;
	7. describe dividend; #to display structure
	8.  SELECT YEAR(date) AS year,
	    ROUND(AVG(price), 2) AS avg
		FROM price
		 WHERE name = 'STA'
		GROUP BY YEAR(date)
		ORDER BY YEAR(date) DESC;
