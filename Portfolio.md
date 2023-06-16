mysql -u root -p
use portfolio_development;
describe buys;

SELECT name, date,price, qty, status FROM buys B JOIN stocks T ON B.stock_id = T.id WHERE T.name='GVREIT' AND status = 'Active' ORDER BY price ASC;

SELECT name, S.date, B.date, S. price, B.price, qty, days, profit, percent  from sells S JOIN buys B ON S.buy_id = B.id JOIN stocks T ON B.stock_id = T.id WHERE T.name='KTC' ORDER BY S.date DESC;

SELECT name, B.date, B.price, qtyFROM buys B JOIN stocks T ON B.stock_id = T.id WHERE T.name='KTC' ORDER BY B.date DESC;