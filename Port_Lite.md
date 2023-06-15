
cd\\ruby\\port_lite\\db

sqlite3 development.sqlite3

select * from orders where name = 'CPNREIT';
update orders set active = 1 where name = 'CPNREIT';
update orders set trade = 'S', active = 2, price = 52.50 where name = 'KTC';

.schema sales

SELECT name,fm_date,to_date,fm_price,to_price,max_price,min_price,pct,days,ttl_spread FROM sales WHERE to_date = '2023-06-14' AND name= "AWC";

.quit