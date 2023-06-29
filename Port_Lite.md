
cd\ruby\port_lite\db

sqlite3 development.sqlite3
.separator " "
.schema sales

/* Select Order, Consensus by Name */
SELECT trade, O.name, qty ,price, qty*price AS amount, active, reason, market, target, max, min, buy, hold, sell FROM orders O JOIN consensus C ON O.name  = C.name WHERE O.name = 'DIF';

/* Select Order, Consensus by Active */
SELECT trade, O.name, qty ,price, qty*price AS amount, active, reason, market, target, max, min, buy, hold, sell FROM orders O JOIN consensus C ON O.name  = C.name WHERE active = 2 ORDER BY trade, C.name;

/* Select Order by Name */
SELECT trade, name, qty ,price, active, reason, market FROM orders WHERE name = 'AWC';

SELECT name,fm_date,to_date,fm_price,to_price,max_price,min_price,pct,days,ttl_spread FROM sales WHERE to_date = '2023-06-14' AND name= "AWC";
/* Select Prospective Buy stocks */
SELECT name,fm_date,to_date,fm_price,to_price,ttl_spread,days,max_price,min_price,pct FROM sales WHERE pct<=-5.00 AND to_date='2023-06-16' ORDER BY pct ASC;
/* Select Prospective Sell stocks */
SELECT name, fm_date,to_date,fm_price,to_price,ttl_spread,days,max_price,min_price,pct FROM sales WHERE pct>=5.00 AND to_date='2023-06-16' ORDER BY pct DESC;

UPDATE orders SET active = 1 WHERE name = 'AWC';
UPDATE orders SET active = 2, price = 11 WHERE name = 'WHART';
UPDATE orders SET trade ='B', active = 2, price = 10.6, reason = '5pct' WHERE name = 'DIF';

DELETE FROM orders WHERE name = 'TFFIF';

/* Consensus */
SELECT * FROM consensus WHERE name = 'GVREIT';
INSERT INTO consensus VALUES ('GVREIT',9.1,9.1,9.1,0,0,0);

.quit