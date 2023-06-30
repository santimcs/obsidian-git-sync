mysql -u root -p
use portfolio_development;
describe buys;

/* Select buys with active status by name*
SELECT name,date,price,qty,status FROM buys B JOIN stocks T ON stock_id = T.id WHERE T.name='ORI' AND status = 'Active' ORDER BY name ASC;

/* Select latest buys with active status by name*
SELECT name,date,price,qty,status FROM buys B JOIN stocks T ON stock_id = T.id WHERE  status = 'Active' ORDER BY name ASC LIMIT 10;

/* Select Sales Data */
SELECT name, S.date, B.date, S. price, B.price, qty, days, profit, percent  from sells S JOIN buys B ON S.buy_id = B.id JOIN stocks T ON B.stock_id = T.id WHERE T.name='TFFIF' ORDER BY S.date DESC;

/* Select Buy Data */
SELECT name, B.date, B.price, qty, status FROM buys B JOIN stocks T ON B.stock_id = T.id WHERE T.name='ICHI'  AND status = 'Active' ORDER BY B.date DESC;