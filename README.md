# SQLtask
Patika.dev SQL tasks

--1) film tablosunda bulunan title ve description sütunlarındaki verileri sıralayınız.

SELECT title,description FROM film;

-- 2) film tablosunda bulunan tüm sütunlardaki verileri film uzunluğu (length) 60 dan büyük VE 75 ten küçük olma koşullarıyla sıralayınız.

SELECT * FROM film where film.length>60 AND film.length<75

-- 3) film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99 VE replacement_cost 12.99 VEYA 28.99 olma koşullarıyla sıralayınız.

SELECT * FROM film WHERE rental_rate=0.99 AND replacement.cost=12.99 OR replacement.cost=28.99

-- 4) customer tablosunda bulunan first_name sütunundaki değeri 'Mary' olan müşterinin last_name sütunundaki değeri nedir?

SELECT last_name FROM customer where first_name="Mary"

-- 5) film tablosundaki uzunluğu(length) 50 ten büyük OLMAYIP aynı zamanda rental_rate değeri 2.99 veya 4.99 OLMAYAN verileri sıralayınız.

SELECT * FROM film WHERE NOT length>50 AND NOT (rental_rate = 2.99 OR rental_rate = 4.99)

---------------------------------------------------------------------------------------------------------------------------------------------------------------------


--1.film tablosunda bulunan tüm sütunlardaki verileri replacement cost değeri 12.99 dan büyük eşit ve 16.99 küçük olma koşuluyla sıralayınız ( BETWEEN - AND yapısını kullanınız.)
Select * from film 
Where  replacement_cost Between 12.99 AND 16.99 ;
--2..actor tablosunda bulunan first_name ve last_name sütunlardaki verileri first_name 'Penelope' veya 'Nick' veya 'Ed' değerleri olması koşuluyla sıralayınız. ( IN operatörünü kullanınız.)
Select first_name, last_name From actor
Where first_name In('Penelope','Nick','Ed' );
--3.film tablosunda bulunan tüm sütunlardaki verileri rental_rate 0.99, 2.99, 4.99 VE replacement_cost 12.99, 15.99, 28.99 olma koşullarıyla sıralayınız. ( IN operatörünü kullanınız.)
Select * from film 
Where rental_rate  In(0.99, 2.99, 4.99) And  replacement_cost In (12.99, 15.99, 28.99 );
