# BACKEND
VERİ
Ölçüm, sayım, deney, gözlem veya araştırma sonucuyla elde edilen ham bilgilerdir.

VERİTABANI
Verilerin organize bir şekilde depolanmasını sağlayan sistemlerdir.

Düzenli verilere sahip olursak;
İleriye yönelik geliştirici kararlar verebiliriz.
Hatalarımızı daha kolay çözeriz.
Geleceğe yönelik başarılı tahminlerde bulunabiliriz.
Peki, gelelim kritik soruya. Bizler örneğin EXCEL benzeri yazılımlar sayesinde verilerimizi saklayabiliriz.
 Neden bir veritabanına ihtiyaç duyalım?

Veritabanı sayesinde sütunlarda bulunacak verilerin aynı veri tipinde olmasını garanti ederiz.
Veritabanları sayesinde çok büyük boyutlu veri kümeleriyle daha kolay çalışırız.
Çoklu kullanıcı yönetimi için veri tabanları daha uygundur.
Veritabanları başka yazılım ve uygulamalarla daha kolay çalışır.




Veritabanı Yönetim Sistemi (DBMS)
Veritabanı verilerimizi organize bir şekilde depolamımızı sağlayan yapılardı. 
İşte bu veritabanımızı oluşturmamızı, yönetmemizi ve SQL yardımıyla gerekli gördüğümüz sorguları
 yapmamızı sağlayan yazılımlara Database Management System veritabanı yönetim sistemi adı verilir.

Bizler SQL sorguları sayesinde veritabanımız üzerinde yapmak istediğimiz 
işlemler veritabanı yönetim sistemi yazılımı aracılığıyla yaparız.

DBMS(DATA BASE MANEGAMENT SISTEM)(VERİ-VERİ TABANI- VERİ TABANI YÖNETİM SİSTEMİ)

TEMELDE BİR DBMS'İN 2 ADET TEMEL FONKSİYONU VARDIR.
1-VERİLERİ OLUŞTURMAMIZI SAĞLAR
2-O VERİLER İLE TEMEL MANİPÜLASYONLARI(CREAT-READ-DELETE-UPDATE)(CRUT DENIR KISACA.) YAPMAMIZI YARAR.
*MEMNUN KALMADIĞIMIZ VEYA FAZLADAN OALRAK GÖRDÜĞÜMÜZ VERİ TABANLARINI ALIP BAŞKA BİR DBMS ÜZERİNE KOYABİLİRİZ.


Yukarıdaki şekilde de gördüğümüz üzere farklı kaynaklardan gelen sorgular DBMS yazılımı sayesinde farklı veritabanlarında kullanılır. 
Genel kullanım olarak bizler pratikte veri, veritabanı ve veritabanı yönetim sisteminin tamamını 
VERİTABANI olarak adlandırmak şekilde bir eğilimimiz vardır.

Farklı ihtiyaçlara göre çeşitli veritabanı yönetim sistemleri bulunur. Temel veritabanı yönetim sistemleri:

Temel Veritabanı Yönetim Sistemleri
Hiyerarşik Veritabanı
Ağ Veritabanı
İlişkisel Veritabanı (RDBMS)(SQLITE-ORACLE-POSTGRESQL-SQLSERVER-SQLAZIRE-MYSQL)
-VERİLER BİRBİRLERİ İLE İLİŞKİLİ TABLOLARDA SAKLANIRLAR.
-SÜTUNLAR VE SATIRLARDAN OLUSUR.
--------*SÜTUNLAR:SAKLANAN VERİ-VERİLERİN VERİ TİPLERİ İLE İLGİLİ BİLGİLER VERİR BİZLERE.
--------*SATIRLAR:O ANKİ BAKILAN TABLANONUN İSMİ-TANIMI-YILI-UZUNLUGU VS VS GİBİ O ÖRNEKLEM İÇERİSİNDE  BİZE VERİLERİ GETİRİR.

Nesneye Yönelik Veritabanı
İlişkisel Veritabanı Yönetim Sistemleri
İlişkisel veritabanı yönetim sistemlerinde veriler satır ve sütunlarında oluşan tablolarda tutulur. 
Her sütunda aynı tür verilerin tutulması sebebiyle yüksek bir veri tutarlılığına sahiptir.

				                      SQL (Structured Query Language) Nedir?
SQL Türkçe ifadesiyle yapılandırılmış sorgu dili anlamına gelmektedir. Biz SQL sayesinde verilerimizin bulunduğu veritabanı ile iletişime geçeriz.4.nesil programlama dili olarakta ifade edilir
(giderek makine dilinden insan diline yaklaşıldıgını ifade eder.).

Daha önce de konuştuğumuz gibi veritabanı yönetim sitemi (DBMS) veritabanını barındıran bir yazılım. 
Bizler bu yazılım üzerinden verilerimiz için yapmak istediğimiz sorguları SQL dili standartlarına uygun olarak yazmak durumundayız.

Bir Programlama dili olarak SQL
SQL üzerine konuşulurken ilk olarak şu soru akla gelir. SQL bir programlama dili midir? 
Evet, SQL ilişkisel veritabanı yönetim sistemleri ile ilişki kurmamızı sağlayan bir declarative bildirimsel bir programlama dilidir.

Bildirimsel Yaklaşım
Aşağıdaki örnek bir SQL sorgusu bulabilirsiniz.

SELECT title FROM book
WHERE page_number > 200;
Yukarıdaki sorgumuzda, veritabanındaki book tablosundan sayfa sayısı 200 den daha fazla olan kitapları görmek istiyoruz.
 Burada biz işin sonuç kısmıyla ilgileniyoruz. SQL, DBMS ile nasıl çalışır, arka tarafta yapılan işlemin bizim açımızdan önemi yoktur. 
Bundan dolayı SQL declarative yani bildirimsel, beyan edici bir yaklaşıma sahiptir.

Dördüncü Nesil Programlama Dili
SQL daha az kod yazarak ve daha çok belirli şablonlar kullanan bir programlama dili olarak dördüncü nesil bir programlama dilidir.
 Yapılması istenen işlemin her basamağının ayrıca kodlanmasına gerek duyulmaz.

--IMPERATIVE PROGRAMMIN(EMREDİCİ-ZORUNLU KILICIDIR): BİZİM İÇİN ÖNEMLİ OLANI İŞLEMLERİN NASIL OLDUGUDUR.NELERIN YAPILACAGI AŞAMA AŞAMA YAZILMIŞTIR.
var numbers=[1,2,3,4,5]
var doubled=[]
for(var i=0;i<numbers.lenght;i++){
var newNumbers = numbers[i] * 2
doubled.push(newNumbers)
}
console.write(doubled)=>[2,4,6,8,10]

--DECLARATIVE PROPGRAMMING(BEYAN EDİCİ):AŞAMA AŞAMA NE YAPILACAGI SÖYLENMİYORDUR.ÖENMLİ OLAN SONUÇTA NE OLACAĞIDIR.
var numbers = [1,2,3,4,5]
var doubled=numbers.map(function(n)){
return n * 2
}
console.log(doubled) =>[2,4,6,8,10]


psql -U postgres bu kod ile terminalde psql dosyamızın .bin klasörüne gidip çalıştırıyoruz ve diyoruz ki postgres kullanıcısı ile veri tbanına ulaşmaya çalışacağımızı diyoruz.
şifremizide girdikten sonra
postgres=# geldikten sonra biz artık veritabanı ile iletişimizi kurduk anlamına geliyor.



							               SELECT
Sorgu (Query)
SQL komutlarını içeren sorgu cümleleridir.

Üzerine ilk konuşacağımız SQL komutu SELECT komutudur. SELECT en çok kullanılan
 SQL komutudur ve veritabanından belirtilen sütunlardaki verileri çekmemizi sağlar.
 Ayrıca SELECT komutunu çoğunlukla diğer SQL komutlarıyla birlikte kullanırız.

SELECT Söz Dizimi
SELECT <sütun_adı>, <sütun_adı>, ... FROM <tablo_adı>;
Eğer tablodaki tüm sütunlardaki verileri çekmek istersek asteriks * karakterinden faydalanırız.

SELECT * FROM <tablo_adı>;
SQL komutlarının büyük harf - küçük harf duyarlılıkları yoktur. (Case Insensitive)
Aşağıdaki sorguların tamamı aynı sonucu verir.

SELECT <sütun_adı>, <sütun_adı>, ...FROM <tablo_adı>;

select <sütun_adı>, <sütun_adı>, ...from <tablo_adı>;

Select <sütun_adı>, <sütun_adı>, ...From <tablo_adı>;
Ancak biz bu çalışmalarımız boyunca yazdığımız SQL komutlarının daha kolay anlaşılması açısından SELECT örneğinde olduğu gibi büyük harflerden oluşan yazımı kullanacağız.

SELECT Örnek Kullanım
SELECT first_name, last_name FROM actor;
Bu sorgumuzda dvdrental veritabanında bulunan actor tablosundaki first_name ve last_name sütunlarında bulunan verileri çekiyoruz.


SELECT title from film; diye yazdıgımız kodlar bizim sql statement olarak bildirilir.Biz query (sorgu) deriz.
title,description gibi birden fazla da sorgularımızı yapabiliriz.
*: tablodaki tüm sütunları getirir. 

SELECT- bir veritabanından veri çıkarır
UPDATE- bir veritabanındaki verileri günceller
DELETE- veri tabanından verileri siler
INSERT INTO- bir veritabanına yeni veriler ekler
CREATE DATABASE- yeni bir veritabanı oluşturur
ALTER DATABASE- bir veritabanını değiştirir
CREATE TABLE- yeni bir tablo oluşturur
ALTER TABLE- bir tabloyu değiştirir
DROP TABLE- bir tabloyu siler
CREATE INDEX- bir dizin oluşturur (arama anahtarı)
DROP INDEX- bir dizini siler



WHERE ve Karşılaştırma Operatörleri
WHERE
SELECT komutu ile yaptığımız çalışmalarda bizler tüm sütunların veya ilgili sütunlarda bulunan verilerin tamamını çekmek isteriz. Çoğu durumda ise verilerin tamamını değil belirli koşulları sağlayan verileri görmek isteriz. Bunun için WHERE anahtar kelimesini kullanırız.

WHERE Söz Dizimi
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <koşul>;
Eğer tablodaki tüm sütunlardaki verileri çekmek istersek asteriks * karakterinden faydalanırız.

SELECT *
FROM <tablo_adı>;
WHERE Örnek Kullanım
SELECT title, replacement_cost
FROM film
WHERE replacement_cost = 14.99;
Bu sorgumuzda dvdrental veritabanında bulunan film tablosundaki title ve replacement_cost sütunlarında bulunan verileri çekiyoruz ancak bu kez tüm verileri değil replacement_cost = 14.99 koşulunu sağlayan verileri alıyoruz.

SELECT * FROM film WHERE replacement_cost =12.99;
//Yukarıdaki örneğimizde biz diyoruz ki film içerisindeki tüm verileri seç ve replacement_cost!u 12.99
olan verileri döndür diyoruz.

SELECT * FROM actor
WHERE first_name='Penelope';
//first_name in değeri string olduğu için SQL'de stringleri '' içerisine yazarız.


Söz dizimi olarak SQL boşlukları yok sayarak ilerler bizler daha kolay şekilde okunmasını sağlamak için
SELECT * FROM film diyerek ilk seçiçi kısmımızı oluşturduktan sonra diğer sorgumuzu alta yazarız
WHERE rental_rate=0.99;
Postgresql dizinleri ilk olarak FROM'dan okumaya başlar. Hangi verileri çekicem diyerek yani FROM film gibi o satırdan başlar. Sonra Bu verileri çekmemdeki koşulum nedir diye bakar WHERE rental_rate=0.99 en son da SELECT
ile istenen sütunları bize getirir.


Karşılaştırma Operatörleri
Yukarıda da bahsettiğimiz üzere WHERE anahtar kelimesi koşul ile birlikte çalışır. Aşağıda SQL ile birlikte kullanılan karşılaştırma operatörlerini görebilirsiniz.
**
SELECT * FROM film 
WHERE length > 90;
**
SELECT * FROM film 
WHERE rental_rate <= 1 ;
**
SELECT * FROM film 
WHERE rental_rate != 1 ;
--Aynı Kullanım--
SELECT * FROM film 
WHERE rental_rate <> 4.99 ;
**



![image](https://user-images.githubusercontent.com/66878884/175478137-55039ac0-a48c-4932-a4e6-0403b95a61e3.png)
<hr>



				WHERE ve Mantıksal Operatörler
Geçen çalışmamızda WHERE anahtar kelimesi ve karşılaştırma operatörleri üzerine konuştuk. Karşılaştırma operatörleri sayesinde koşulumuzu belirtiyorduk ancak çoğu durumda biz birden fazla koşulu gerçekleştirme isteriz bunun için mantıksal operatörlerden faydalanırız.

Mantıksal Operatörler
Yukarıda da bahsettiğimiz üzere WHERE anahtar kelimesi koşul ile birlikte çalışır. Aşağıda SQL ile birlikte kullanılan karşılaştırma operatörlerini görebilirsiniz.

Örnek Kullanım
SELECT *
FROM actor 
WHERE first_name = 'Penelope' AND last_name = 'Monroe' ;
Bu sorgumuzda dvdrental veritabanında bulunan actor tablosundaki tüm sütunlarında bulunan verileri çekiyoruz ancak bu kez iki koşulumuz var. AND operatörünün true sonucu dönmesi için bu iki koşulumuzun da sağlanması gerekiyor. Sıralanacak verilerin first_name sütunundaki değeri 'Penelope' ve last_name sütunundaki değerinin 'Monroe' olması gerekmektedir.

SELECT *
FROM actor 
WHERE first_name = 'Penelope' OR first_name = 'Bob' ;
Bu sorgumuzda dvdrental veritabanında bulunan actor tablosundaki tüm sütunlarında bulunan verileri çekiyoruz ancak bu kez iki koşulumuz var. OR operatörünün true sonucu dönmesi için bu iki koşulumuzunda herhangi birinin sağlanması yeterlidir. Sıralanacak verilerin first_name sütunundaki değeri 'Penelope' veya 'Bob' olması gerekmektedir.

SELECT *
FROM film 
WHERE NOT rental_rate = 4.99 ;
Bu sorgumuzda dvdrental veritabanında bulunan film tablosundaki tüm sütunlarında bulunan verileri çekiyoruz ancak bu kez koşulumuzu NOT yani değil mantıksal operatörü yardımıyla oluşturmuşuz. NOT operatörü bize verilerin hangi koşul dışı olduğunu gösterir. Örneğimizin senaryosu; Film tablomuzda bulunan tüm sütunlardaki verileri sıralayacağız ancak bu verilerin rental_rate sütununda bulunan değerleri 4.99' a eşit OLMAYACAK!

SELECT *
FROM film 
WHERE NOT (rental_rate = 4.99 OR rental_rate = 2.99)
Mantıksal operatörleri sıklıkla birlikte kullanırız. Yukarıdaki örneğimizde sıralayacağımız verilerin rental_rate sütunlarında bulunan değerlerinin 4.99 veya 2.99 olmamasını istiyoruz.


--> AND: AND OPERATÖRÜ HEM ÖNÜNDEKİ VE HEM DE BİR ARKADASINDA Kİ SORGUNUN DOĞRU OLMASI DURUMUNDA BİZE İLGİLİ DURUMU 
DÖNER.

-->OR: OR OPERATÖRÜNDE İLK KOSULDAN VEYA İKİNCİ KOSULDAN HERHANGİ BİRİ DOĞRU OLDUGU ZAAMAN TRUE DÖNER VE BİZE SONUCU GETİRİR.
--------------------------------------------------------------------
SELECT first_name,last_name FROM actor
WHERE first_name = 'Penelope' OR first_name='bob';

SELECT first_name,last_name FROM actor
WHERE first_name = 'Penelope' OR first_name='Bob';

YUKARIDAKİ İKİ SORGUDA AYNI GÖRÜNEBİLİR FAKAT DEĞER SORGULARINDA CASE SENSIVITY OLABİLİR VE TABLOMUZDA Bob İSMİ VAR FAKAT bob İSMİ YOK İSE BİZE İLK SORGUDA FIRST NAME'I bob OLAN BULAMADIĞI İÇİN DÖNDÜRMEZ FAKAT Bob ŞEKLİNDE ARATTIĞIMIZDA EŞLESEN 1 DEĞER OLDUGU İÇİN BİZE HEM Penelope hem de Bob DEĞERLERİNİN SONUÇLARINI GETİRİR.
----------------------------------------------------------------------
SELECT * FROM film
WHERE rental_rate=4.99 AND length >90;
-----------------------------------------------------------------------
SELECT * FROM film
WHERE rental_rate=4.99 AND rental_rate=2.99;
BU SORUDA BİZ KİRALAMA ORANI 4.99 VE KİRALAMA ORANI 2.99'U GETİR DİYORUZ SANKİ HEM 4.99 HEM DE 2.99'A SAHİP OLACAKMIŞ GİBİDİR VE BİZE HERHANGİ BİR VERİ DÖNMEZ.
AND YERİNE OR DEDİĞİMİZ ZAMAN 1.KOŞUL 2.KOŞUL VEYA HER İKİSİDE DOĞRU OLDUGU İÇİN OLDUGU İÇİN BİZE SONUÇLARI GETİRECEKTİR.


![image](https://user-images.githubusercontent.com/66878884/175494882-c25dfa05-84d1-4173-af30-80ae1b93b43e.png)






























