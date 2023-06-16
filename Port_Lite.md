
cd\ruby\port_lite\db

sqlite3 development.sqlite3
.separator " "
.schema sales

SELECT trade, name, qty ,price, active, reason, market FROM orders WHERE active = 2 ORDER BY trade, name;
SELECT trade, name, qty ,price, active, reason, market FROM orders WHERE name = 'GVREIT';

UPDATE orders SET active = 2, price = 7.5 WHERE name = 'JASIF';
UPDATE orders SET trade = 'S', active = 2, price = 52.50, reason = '5pct' WHERE name = 'KTC';



SELECT name,fm_date,to_date,fm_price,to_price,max_price,min_price,pct,days,ttl_spread FROM sales WHERE to_date = '2023-06-14' AND name= "AWC";

SELECT name,fm_date,to_date,fm_price,to_price,ttl_spread,days,max_price,min_price,pct FROM sales WHERE pct<=-5.00 AND to_date='2023-06-15' ORDER BY pct ASC;

SELECT name, fm_date,to_date,fm_price,to_price,ttl_spread,days,max_price,min_price,pct FROM sales WHERE pct>=5.00 AND to_date='2023-06-15' ORDER BY pct DESC;

DELETE FROM orders WHERE name = 'TFFIF';

.quit