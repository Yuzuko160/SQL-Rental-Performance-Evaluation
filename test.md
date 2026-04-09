USE sakila;
SELECT customer.customer_id, first_name, rental_id
FROM customer
JOIN rental USING(customer_id);

-- 列出每位顧客的編號、名字以及租借的訂單編號
-- 若是要顯示出的欄位在兩張表都有，前面要加上資料表名稱
SELECT c.customer_id, c.first_name, r.rental_id
FROM customer c
JOIN rental r
ON c.customer_id = r.customer_id;

-- 列出每位顧客的編號以及他們租借的編號alter
-- LEFT JOIN 會將左邊表格的所有資料都加入到查詢結果中
-- 如果左邊表格的某個紀錄在右邊表格中找不到匹配的紀錄，則結果將包含NULL值
SELECT c.customer_id, r.rental_id
FROM customer c
LEFT JOIN rental r
ON c.customer_id = r.customer_id;

-- 列出每位顧客的編號以及他們租借的編號
-- RIGHT JOIN 會將右邊表格的所有資料都加入到查詢結果中
-- 如果右邊表格的某個記錄在左邊表格中找不到匹配的紀錄, 則結果將包含NULL值
SELECT c.customer_id, r.rental_id
FROM customer c
RIGHT JOIN rental r
ON c.customer_id = r.customer_id;

-- OUTER JOIN
-- 列出每位顧客的編號以及他們租借的編號
SELECT c.customer_id, r.rental_id
FROM customer c
LEFT JOIN rental r
ON c.customer_id = r.customer_id;

-- 等於
SELECT c.customer_id, r.rental_id
FROM rental r
RIGHT JOIN customer c
ON c.customer_id = r.customer_id;

-- OUTER JOIN的反一邊
-- 列出每位顧客的編號以及他們租借的編號
SELECT c.customer_id, r.rental_id
FROM customer c
RIGHT JOIN rental r
ON c.customer_id = r.customer_id;

-- 等於
SELECT c.customer_id, r.rental_id
FROM rental r
LEFT JOIN customer c
ON c.customer_id = r.customer_id;

-- INNER JOIN - CROSS 交叉連接
-- 列出每部影片的編號以及所屬的類別名稱
-- 不指定任何條件，將兩個資料表中所有的可能排列組合出來
SELECT film_category.film_id, category.name
FROM film_category
CROSS JOIN category;

-- INNER JOIN - NATURAL
-- 兩張資料表之間同名的欄位會被自動結合在一起
-- 列出每部影片的編號以及所屬的類別名稱
SELECT category_id, film_id
FROM film_category
NATURAL JOIN category;


