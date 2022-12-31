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
-----------------------------------------------------------------------
SELECT * FROM film
WHERE rental_rate=4.99 AND rental_duration=3 AND replacement_cost > 20;
BURDAKİ ÖRNEĞİ ŞÖYLE DÜŞÜNELİM İLK RENTAL_RATE'İ 4.99 OLAN SONRA RENTAL_DURATİON'U 3 OLAN VE SONRA RELACEMENT_CONST'U 20'DEN BÜYÜK OLANLARI GETİR DİYORUZ.
-----------------------------------------------------------------------
SELECT * FROM film
WHERE replacement_cost < 17 AND replacement_cost > 20;
BU TARZ SORGUMUZDA HATA ALACAĞIZDIR NEDENİ Replacement_cost HEM 17'DEN KÜÇÜK OLUP 20'DEN BÜYÜK OLMASI İMKANSIZ OLDUGU İÇİN HATA DÖNECEKTİR.
ANCAK OR YAZDIGIMIZ ZAMAN HEM 17 DEN KÜÇÜK OLANLAR HEM DE 20'DEN BÜYÜK OLANLAR GELİR
-----------------------------------------------------------------------
SELECT * FROM film
WHERE NOT  (rental_rate=4.99 AND replacement_cost=20.99);
BU SORGUMUZDA RENTAL_RATE'DE 4.99 VE REPLACEMENT_COST'TA 20.99 U GÖRÜRÜZ BUNUN NEDENİ BİZ BUNLASRI PARANTEZ İÇERİSNE ALDIK VE BAŞLARINA NOT DEDİK YANİ (rental_rate=4.99 VE replacement_cost=20.99)'İ OLANLARI GETİRME DİYORUZ.
-----------------------------------------------------------------------
SELECT * FROM film
WHERE NOT (NOT(rental_rate=4.99 AND replacement_cost=20.99));
BU SORGUMUZDA İSE BİZE 4.99 VE 20.99 OLANLARI GETİRİR NEDENİ 2 ADET NOT KULLANDIGIMIZ İÇİN BİRBİRLERİNİN TÜMLEYENLERİ OLUP SORGU İÇERİSİNDEKİLE GETİR DEMEK OLUYOR.YANİ İÇERİDE Kİ 2 NOT BİRBİRİNİ YOK EDER.
-----------------------------------------------------------------------
SELECT * FROM film
WHERE NOT length > 110; uzunlugu 110'dan küçük olanları getirir.
SELECT * FROM film
WHERE NOT NOT length > 110; oldugu zaman ise dediğimiz gibi uzunlugu 110'dan büyük olanları getiriyor.
-----------------------------------------------------------------------
SELECT * FROM actor
WHERE first_name='Penelope' AND last_name='Monroe'
OR first_name='Joe' AND last_name='Swank';

BİZ HER OR KULLANDIGIMIZ ZAMAN SANKİ BAŞTAN YENİ BİR FİLTRELEME BAŞLAMIŞ GİBİ DÜŞÜNECEĞİZ O NEDENLE ÖNCEKİLERE DİKKAT ETMEZ VE AYNI ZAMANDA GİDİP JOE'YU GETİRİR.
![image](https://user-images.githubusercontent.com/66878884/175505407-e26f7954-a11a-4a6d-8e9d-11940b2bfeca.png)
BİLEREK LAST_NAME'İ YANLIŞ YAZDIMIZ ZAMAN SADECE PENELOPE'Yİ GETİRİR BİZE.
![image](https://user-images.githubusercontent.com/66878884/175505426-e4e285c2-0eac-44c0-a854-b094cac34f93.png)

-----------------------------------------------------------------------
SELECT * FROM actor
WHERE first_name='Penelope' AND last_name='Monroe' 
AND last_name='Swanks' OR first_name='Joe'
BU KOŞULDA PENELOPE'YE BAKAR SONRA LAST_NAME'E BAKAR VE SONRA BİR SONRAKİ AND'E BAKAR VE OLMADIGI İÇİN BİZİM SORGUMUZ OR'A GEÇER VE YALNZICA İLK İSMİ JOE'OLANI GETİRİR.


![image](https://user-images.githubusercontent.com/66878884/175505875-7e62b01e-33d0-44dc-b990-a6df9148fea3.png)






![image](https://user-images.githubusercontent.com/66878884/175494882-c25dfa05-84d1-4173-af30-80ae1b93b43e.png)


<hr>


					             BETWEEN ve IN
BETWEEN
Aşağıdaki sorgumuzda AND mantıksal operatörü yardımıyla film tablosunda bulunan verilerimizi uzunluğu 140 tan küçük eşit VE 100 den büyük eşit olmak üzere sıralıyoruz.

SELECT * 
FROM film
WHERE length >= 100 AND length <= 140;
Burada temel olarak yaptığımız belirli aralıkta bulunan verileri sıralamak. Bunun BETWEEN ... AND yapısını kullanarak da yapabiliriz.

BETWEEN AND Söz Dizimi
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <koşul>;

BETWEEN Örnek Kullanım
SELECT *
FROM film
WHERE length BETWEEN 100 AND 140; -- WHERE length >= 100 AND length <= 140 ifadesi ile aynı sonucu verir.
Burada dikkat edilmesi gereken nokta 100 ve 140 sınır değerleri aralığa dahildir.

IN
Şöyle bir senaryo düşünelim, yine film tablosundan uzunluğu 30, 60, 90 veya 120 dakikaya eşit olan verileri sıralayalım.

SELECT * 
FROM film
WHERE length = 30 OR length = 60 OR length = 90 OR length = 120;
sorgusuyla verileri aldık ancak burada şöyle bir sorunumuz var peki 4 farklı değer için değil 14 farklı değer için bu sorgumuzu gerçekleştirmek için 14 ayrı OR mantıksal operatörü kullanmamız gerekirdi. Bunun yerine istenilen değerleri liste haline geitip IN anahtar kelimesiyle kullanabiliriz.

--------------------------------------------
SELECT title,length FROM film
WHERE length NOT BETWEEN 90 AND 120;
Bize 90 ile 120 sınırları aralıgındaki filmleri getiriyordu fakat başına NOT koyduğumuz için 90 ile 120 dk arasındaki filmleri çıkarıp o halde bize getiriyor fakat 90 ile 120 DAHİL DEĞİLDİR!! Çünkü 90 ile 120 BETWEEN yapısına dahildir bunu unutmayın !!!
length < 90 OR length >120 çıktısı gelir bize.
--------------------------------------------
SELECT rental_rate,replacement_cost FROM film
WHERE (rental_rate BETWEEN 2 AND 4) AND 
(replacement_cost BETWEEN 10 AND 20)
rental_rate imiz 2 ile 4 arasında ve replacement_cost değerimizin de 10-20 arasında olduğunu istediğimiz sorgu.
--------------------------------------------
<hr>


					           IN Söz Dizimi
IN: ANAHTAR KELİMİSİNDE BİZ ORDA VERDİĞİMİZ DEĞERLERE BAKARIZ ÖRNEĞİN (40,50) BİZE SADECE 40 VE 50 OLANLARI GETİRİR.
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <sütun_adı> IN (değer1, değer2, ...);
IN Örnek Kullanım
SELECT *
FROM film
WHERE length IN (30,60,90,120);

--------------------------------------------
SELECT length FROM film
WHERE length IN (40,50,60)
Uzunlugu 40,50,60 olanları getiririz.Tekli olarakta sorgumuzu yapabiliriz.
SELECT length FROM film
WHERE length = 40 OR length=50 OR length =60; ile aynı sonuçları verir syntaxları farklıdır.
--------------------------------------------
SELECT * FROM film
WHERE replacement_cost IN (10.99,12.99,16.99)
--------------------------------------------
SELECT * FROM film
WHERE replacement_cost NOT IN (10.99,12.99,16.99)
10.99,12.99,16.99'ların dahil olamdıgı replacement_costları bizlere getirir.
--------------------------------------------

<hr>


						         LIKE ve ILIKE
						   
Aşağıdaki sorgumuzda actor tablomuzda bulunan tüm sütunlardaki verileri first_name sütununda ki değeri 'Penelope' olmak üzere getiriyoruz.

SELECT *
FROM actor
WHERE first_name = 'Penelope';
Ancak bizler bazı durumlarda bu şekilde tam eşleşme değil belirli şablonlara uyan koşulların sağlanmasını isteriz. Örneğin aşağıdaki sorgumuzda first_name sütunun 'Penelope' değerine eşit olmasını değil, ilk harfin 'P' olması koşulunu sağlar. Bunun için LIKE operatörünü kullanırız.

SELECT *
FROM actor
WHERE first_name LIKE 'P%';
Burada kullanılan % karakteri sıfır, bir veya daha fazla karakteri temsil eder ve Wildcard olarak isimlendirilir. Bir diğer wildcard karakteri _ karakteridir ve bir karakteri temsil eder.

LIKE Söz Dizimi
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
WHERE <sütun_adı> LIKE <şablon>;
ILIKE operatörü LIKE operatörünün case - insensitive versiyonudur.


% : Valcard işareti anlamına gelir ya herhangi bir karakter yoktur ya da birden fazla karakter için yer tututcu işlevi görür.
LIKE: Büyük küçük(case-sensivity) hassasiyeti vardır.
~~ : İşaretide LIKE anlamına gelir.
ILIKE: Case-sensivity hassasiyeti yoktur.
~ ~ * : BİRLEŞİK ŞEKİLDE YAZILIR VE ANLAMI ILIKE ANLAMINA GELİR.

! : NOT ANLAMINA GELİR.

WHERE first_name LIKE 'M%' M ile başlayan isimleri bize getirir 'MA%' diyip te sınır koyabiliriz herhangi bir sınır yoktur bir de '%y' kullanımı vardır buda son harfi arar yani burda son harfi 'y' olanları ara diyoruz.
 
--------------------------------------------
SELECT * FROM customer
WHERE first_name LIKE 'M%'
M ile baslayan tüm isimleri almamıza yarar.
--------------------------------------------
SELECT * FROM actor 
WHERE first_name LIKE 'A%y';
BAş harfi A ile başlıyor ortada ya hiç karakter olmayacak ya da 1'den fazla karakter olacaktır diyip son harfini'de y ile bitiriyoruz bize bunları sağlayan sorguları getiriyor.
--------------------------------------------
SELECT * FROM customer 
WHERE first_name LIKE 'A%' AND last_name LIKE 'A%';
İlk ismin ve son ismin baş harfları A ile başlayanları sıralar.
--------------------------------------------
SELECT * FROM customer 
WHERE first_name NOT LIKE 'D%n' 
NOT ile kullanılabilir ve böyle kullanıldıgı zaman bize baş harfi D son harfi n olanların haricindekileri listeler.
--------------------------------------------
SELECT * FROM customer 
WHERE first_name LIKE 'J_an';
Kullandığımız underscore(_) bize tek karakter için yer tutucu görevini sağlar.(Jean,Joan,Juan) gibi çıktılar verir.
--------------------------------------------
SELECT * FROM customer 
WHERE first_name LIKE 'J_' ;
Bu kes ise TEK BİR KARAKTERİ KAPSADIĞI İÇİN Jo yu getirir.DİKKAT EDİLMESİ GEREKEN BİR NOKTA ÇOK KARIŞTIRILABİLİYOR.
--------------------------------------------
SELECT * FROM customer 
WHERE first_name LIKE 'J%n' ;
Burda ise J ile başlayan n ile sonlanan tüm isimleri getirir.
--------------------------------------------
SELECT * FROM actor
WHERE first_name !~ ~* 'B%' 
BAŞ HARFİ KÜÇÜK B İLE BAŞLAYANLRI LİSTELER.
--------------------------------------------

				 DISTINCT ve COUNT
DISTINCT(Unique-Benzersiz): Farklı ifadaeleri görmek için kullanırız.
Şimdiye kadar yaptığımız SQL sorgularında genellikle verileri belirli koşullar altında sıraladık. Dikkat ettiyseniz bir çok durumda aynı sütün içerisinde birbirinin aynı olan veriler ile karşılaştık. Örneğin dvdrental veritabanı içerisinde bulunan film tablosundaki replacement_cost, rental_rate gibi sütunlar birbirini tekrar eden verilerden oluşmaktadır. Bazı durumlarda bir sütun içerisinde bulunan farklı değerleri görmek isteriz.

SELECT DISTINCT rental_rate 
FROM film;
sorgusu bize rental_rate sütununda bulunan birinden farklı 2.99, 0.99, 4.99 verilerini gösterir.
Yani rantel_rate 3 ader farklı veri barındırıyormuş içerisinde.

SELECT DISTINCT Söz Dizimi
SELECT DISTINCT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>;
COUNT
COUNT aggregate fonksiyonu ilgili sorgu sonucunda oluşan veri sayısını bildirir. Aşağıdaki sorguda ismi 'Penelope' olan aktörleri sıralıyoruz.
--------------------------------------------
SELECT DISTINCT City,Country FROM Customers;
w3school'da örnekleri yaparken böyle bir öenk yaptıgımız zaman bize 
![image](https://user-images.githubusercontent.com/66878884/175759585-ad194efd-8a1a-4a68-875c-02a6116fe5b8.png)
bu şekil bir döndü döndürüyor burda 1'den fazla Germany olması hata oldugu anlamına gelmiyor biz 2 sütunu 1 olarak düşüneceğiz, devam eden ikili verilerin diğerlerinden farklı oldugunu düşüneceğiz.
--------------------------------------------

SELECT * 
FROM actor
WHERE first_name = 'Penelope';
ancak veri sayısını bulmak istersek COUNT fonksiyonunu kullanırız.
--------------------------------------------
Count: biz ilk olarak ne yapıyoruz verileri listeliyoruz ve sonrasında belirli bir filterelemden geçiyoruz ve Count bize bu filtremizin yani şartlarımızı sağlayan veri sayısını döner bize. 
SELECT COUNT(*)
FROM actor
WHERE first_name = 'Penelope';
Yukarıda da belirttiğimiz gibi COUNT fonksiyonu ile sorgu sonucunda ortaya verileri sayıyoruz. Bu nedenle COUNT(*) veya COUNT(sütun_adı) aynı sonucu verir.
--------------------------------------------
Normal kullanımda 4 adet Penelope kullanıcısının oldugu dönüyor.
![image](https://user-images.githubusercontent.com/66878884/175759685-85c083cc-4cd7-4505-b213-1ebc0465a3bc.png)

Count ile kullandığımızda Penelope isimli kaç adet kullanıcı olduğunu dönüyor.
![image](https://user-images.githubusercontent.com/66878884/175759673-edd4b7f1-e0d5-4639-872c-b7bab317125c.png)
Burda Count(*) yazmamızın sebebi Count aynı length()'inde oldugu gibi bir fonksiyon olduğu içindir.
--------------------------------------------

BENİM BİRBİEİNDEN FARKLI KAÇ TANE first_name'imimiz var bu seneryoyu doğrulayan fonksiyonumuz
SELECT COUNT(DISTINCT first_name) FROM actor;D
ÇIKTISIDA;
![image](https://user-images.githubusercontent.com/66878884/175759832-7294f0d3-dd3d-4741-9187-adacd8b55089.png)
--------------------------------------------
SELECT COUNT(DISTINCT length) FROM film;
ilk olarak uzunlugu istediğimiz için length'i yazarız sonra birbirinden farklı olamsını istediğimiz için DISTINCT'i kullanıyoruz fakat tek başlarına kullanılması bizim istediğimiz sonucu vermeyecektir bundan dolayı onları bize bu (DISTINCT length) filtrelemyi sağlayan kaç adet oldugunu öğrenmek için COUNT(DISTINCT length)parantezine alıp işlemimizi yaparız.
Birbirinden uzunlukları farklı kaç tane filmimizin oldugunu öğrenmek için kullanırız ve çıktısı ;
![image](https://user-images.githubusercontent.com/66878884/175759896-5f391e04-ef72-4e21-8e96-c76e706f6b77.png)
Count kullanmadan olan çıktısı 
--------------------------------------------
Uzayıp gidiyor kaç adet olduguna göre.
![image](https://user-images.githubusercontent.com/66878884/175759952-d80a52e3-ab5f-4669-abdb-88fbf90903e6.png)
--------------------------------------------



				PSQL ve Uygulama I
PSQL


PSQL ile PostgreSQL'e bağlanmak.
psql -U <kullanıcı_adı>
Kullanıcıya ait şifreyi girdikten sonra varsayılan veritabanı postgres'e bağlanıyor.
postgres=#
Bulunan veritabanlarını listelemek için:
\l veya \list
![image](https://user-images.githubusercontent.com/66878884/175762741-8ad836fd-29c2-4798-95a3-d2c6b3146237.png)
--------------------------------------------
Bizim örneğimizde dvdrental veritabanına bağlanacağız.
\c dvdrental veya \connect dvdrental
![image](https://user-images.githubusercontent.com/66878884/175762738-5fadf14f-ba4b-43e7-96df-1953d61380de.png)
--------------------------------------------
Bağlanılan dvdrental veritabanında bulunan tabloları listelemek için:
\dt
![image](https://user-images.githubusercontent.com/66878884/175762728-6b292dff-0b4a-4bef-afd6-a1b2b86c0be6.png)
--------------------------------------------
Herhangi bir tablonun sütunlarını ve tablo detaylarını görmek için:
\d <tablo_adı>
![image](https://user-images.githubusercontent.com/66878884/175762762-3c671297-93fa-4396-bca4-4b4f8612f6bf.png)
--------------------------------------------
Örnek Sorgu Senaryoları
SELECT * FROM actors WHERE first_name='Penelope';
![image](https://user-images.githubusercontent.com/66878884/175762811-eeac6058-3cba-485b-bf61-48a1a94a41ae.png)

TERMİNAL EKRANIMIZDA ; KULLANMAK ZORUNDAYIZ!!!!
ŞUNDAN DOLAYI GÖSTERMİŞ OLDUGUM ÖRNEKTE dvrental=# İŞARETİ İLE SORGUMUZU YAPTIK VE SONUNA ; KOYDUGUMUZDA SORGUNUN BİTTİĞİNİ VE BİZE CEVAP DÖNMESİ GEREKTİĞİNİ ANLAR FAKAT BİR EĞER Kİ BİRDEN ÇOK SATIRDA SORGUMUZU YAPACAKSAK EĞER O ZAMAN ; KOYMAYIZ VE dvdrental-# ŞEKLİNE DÖNÜŞÜR VE BURDA BİZE SEN SORGUNU YAZDIN FAKAT BİTİRMEDİN DER VE BİZ ALT SATIRDAN DA pgAdmin SAYFASINDA YAPTIGIMIZ GİBİ SORGUMUZU YAPABİLİRİZ. 
PSQL, PostgreSQL ile birlikte gelen terminal tabanlı bir kullanıcı arayüzüdür. PSQL sayesinde komut satırında sorgular yazıp, sonuçlarını görebiliriz. Aşağıda temel PSQL komutlarının ilk bölümünü bulabilirsiniz.
![image](https://user-images.githubusercontent.com/66878884/175762906-d9926b54-926d-4901-9f24-26758d548b08.png)

--------------------------------------------
FARKLI SATIRLARA YAZIP GÖSTERİM ŞEKLİ. SONDA ; KOYMAMIZIN NEDENİ İLLA Kİ ; SON SATIRDA OLACAK DİYE BİR KAİDE YOK ÖYLE BİR DURUMDA YOK SORGUYU BİTİREMEK İÇİN UZATMAMAK VE 2.3. VS. DİĞER SATIRLARDA ; KOYMAZSAK DEVAM EDEBİLECEĞİMİZİ GÖRMEMİZ İÇİNDİ.
![image](https://user-images.githubusercontent.com/66878884/175762969-f7232bf1-1095-473c-83f5-66d80b387256.png)

--------------------------------------------

customer tablosunda bulunan first_name değeri ve last_name değeri 'A' karakteri ile başlayan verileri sıralayınız.
SELECT * 
FROM customer
WHERE first_name LIKE 'A%' AND last_name LIKE 'A%';
![image](https://user-images.githubusercontent.com/66878884/175763025-5f6b713e-3d88-415b-93a1-088f5f63f38a.png)

film tablosunda bulunan ve uzunluğu 80 ile 120 arasında bulunan ve aynı zamanda rental_rate değeri 0.99 veya 2.99 olan verileri sıralayınız.
SELECT * 
FROM film
WHERE (length BETWEEN 80 AND 120) AND (rental_rate IN (0.99, 2.99));
PSQL terminal ekranından çıkmak için:
\q

--------------------------------------------

ilk ismi A ile son ismi G ile başlasın sayısını yakalamak için

![image](https://user-images.githubusercontent.com/66878884/175763083-dcb5002a-7225-47e5-8079-94596dfd556a.png)

--------------------------------------------




![image](https://user-images.githubusercontent.com/66878884/175763170-60d530d2-a53d-4825-8161-894e20a4d781.png)


--------------------------------------------
İsminden en az 2 tane a olsun 100dk'dan daha uzun replacement_cost 15'ten büyük 25'ten küçük rental_rate 2.99
SELECT * FROM film
WHERE (title ILIKE ('%a%a%')) AND (length > 100) AND (replacement_cost > 15 AND replacement_cost < 25) AND rental_rate=2.99;
![image](https://user-images.githubusercontent.com/66878884/175764122-a1cdb0b2-e4fe-4338-a12d-94ecc5c6d2d4.png)
--------------------------------------------
T ile Başlayan filmlerin kaç farklı dakikaya sahip uzunlukları vardır.
kaç farklı derken kaç tane olacagını bulacağımız için COUNT
kaç farklı dakikaya derken ise unique var DISTINCT kullanacağız

SELECT COUNT(DISTINCT length) FROM film
WHERE title LIKE 'T%';
![image](https://user-images.githubusercontent.com/66878884/175764229-537722fb-5dbf-454e-a4fa-de1c6a788089.png)
--------------------------------------------

<hr>

					ORDER BY
ORDER BY anahtar kelimesi sayesinde bizler verilerimizi herhangi bir sütunda bulunan değerlere göre azalan veya artan bir şekilde sıralayabiliriz.
SIRALAMA İŞLEMLERİNDE KULLANIRIZ. İLK OLARAK KOŞULLARIMIZI BELİRTİR DEVAMINDA SIRALAMASINI NASIL YAPACAĞIMIZI BELİRTİRİZ.

ORDER BY Söz Dizimi
SELECT <sütun_adı>, <sütun_adı>, ...
FROM <tablo_adı>
ORDER BY <sütun_adı>, <sütun_adı>, ... ASC|DESC;
ORDER BY Örnek Kullanım
SELECT *
FROM film
ORDER BY title (ASC);
Bu sorgumuzda dvdrental veritabanında bulunan film tablosundaki tüm sütunları title sütununda bulunan verilere göre artan (ASC) şeklinde sıralıyoruz.

ASC sıralama varsayılan olduğu için ayrı bir şekilde yazılması zorunluluğu yoktur ancak sorguyu belirginleştirmesi açısından genelde yazılır.

SELECT *
FROM film
ORDER BY title ASC length DESC;
Sıralama birden fazla sütuna göre de yapılabilir. Yukarıdaki örneğimizde sıralama title sütununa göre artan length sütununa göre azalan şeklinde yapılıyor.
ASC:AZALANDAN ARTANA
DESC:ARTANDAN AZALANA DOGRU SIRALAR.
SELECT *
FROM film
WHERE title LIKE 'A%'
ORDER BY title ASC length DESC;
Yukarıdaki örneğimizde de gördüğümüz gibi sıralama işlemi, koşuldan sonra yazılır.
--------------------------------------------
SELECT * FROM film
ORDER BY title;
Sıralı şekilde listelememize yarar. A-Z'ye doğr
SELECT * FROM film
ORDER BY title ASC; Aynı kullanımdır ASC yazmadıgımız zaman yukarıda default olarak ASC olarak alır ve sıralı şekilde listeler.
SELECT * FROM film
ORDER BY title DESC;
DESC: İSE AZALAN ŞEKİLDE YANİ Z-A'YA DOĞRU SIRALAR.
![image](https://user-images.githubusercontent.com/66878884/175765892-0e1baddc-e5e2-4dd0-806e-02a0f583fccb.png)

--------------------------------------------
SELECT title,length FROM film
ORDER BY length DESC;
Burdaki order'ı sıralamayı azalana göre yaparız

![image](https://user-images.githubusercontent.com/66878884/175766002-9a7deb65-071f-44b3-a670-c7b7ea5aa9f7.png)

--------------------------------------------

ÖNCELİKLE RANTEL_RATE'E GÖRE ARTAN,LENGTH'E GÖRE AZALAN ŞEKİLDE SIRALAMA
SELECT title,rental_rate,length FROM film
ORDER BY rental_rate ASC, length DESC; 

![image](https://user-images.githubusercontent.com/66878884/175766068-344f9a6d-4756-4fda-94bb-d0fcdad37057.png)

--------------------------------------------
YALNIZCA A İLE BAŞLAYAN, RENTAL_RATE'E GÖRE ARTAN LENGTH'E GÖRE AZALAN.

SELECT title,rental_rate,length FROM film
WHERE title LIKE 'A%'
ORDER BY rental_rate ASC, length DESC; 

![image](https://user-images.githubusercontent.com/66878884/175766108-2c2ca48b-b201-482b-8100-e4c9f55ad229.png)
--------------------------------------------

RATİNG'İ G YE EŞİT OLAN FİLMLERİ UZUNLUKLARINA GÖRE ARTACAK ŞEKİLDE SIRALAMA.
SELECT * FROM film
WHERE rating = 'G'
ORDER BY length DESC;
![image](https://user-images.githubusercontent.com/66878884/175766188-9e8bfa2e-dd22-482e-822e-4e8e404efa7b.png)

--------------------------------------------

<hr>



						LIMIT ve OFFSET
LIMIT
Şimdiye kadar yaptığımız SQL sorgularında genellikle verilerin tamamını belirli koşullar altında sıraladık. Bazı durumlarda ise koşullarımızı sağlayan verilerin tamamını değil belirli sayıda olanlarını sıralamak isteriz, bunun için LIMIT anahtar kelimesini kullanırız.

-> ÖNCE KOŞULLARIMIZA GÖRE VERİLERİ ALIYORUZ SINRA VERİLERİ SIRALIYORUZ SONRA DA KAÇ TANE VERİ GÖRMEK İSTİYORSAK LİMİT ANAHTARI ATIYORUZ.


Şöyle bir senaryo üzerine düşünelim. dvdrental veritabanında bulunan film tablosundan B ile başlayan filmleri uzunluklarına göre en uzun olan 10 filmi sıralayalım.

SELECT *
FROM film
WHERE title LIKE 'B%'
ORDER BY length DESC
LIMIT 10;
Yukarıdaki sorgumuzda da görmüş olduğunuz gibi önce koşullamayı, sonra gruplamayı en son ise LIMIT kullanarak istediğimiz veri sayısını belirttik.

--------------------------------------------
SELECT * FROM film
LIMIT 20
20 tane film verisini getirir bize.
--------------------------------------------
SELECT * FROM film
WHERE rental_rate=4.99 
ORDER BY length
LIMIT 20;
rental_rate'i 4.99 olan lengthleri azalandan başlatarak 20 adet listemizi getirir.
--------------------------------------------
SELECT * FROM film
WHERE replacement_cost = 14.99 AND rental_rate=0.99
UZUNLUKLARI EN UZUNDAN EN KISAYA (AZALAN) sıralamamız lazım VE DESC yazıyoruz SONRA LIMITIMIZI GİRİYORUZ
VE EN UZUN 7 FILMI ALMAK İÇİN LIMITLIYORUZ.
ORDER BY length DESC
LIMIT 10;

![image](https://user-images.githubusercontent.com/66878884/175768438-53e2b86d-edc8-40c6-9d86-c08be8832afe.png)
--------------------------------------------
OFFSET
Bazı durumlarda sonuç olarak gördüğümüz veri grubu içerisinden bazılarını "pass" geçmek isteriz. Yukarıdaki senaryomuzu tekrar düşünelim, dvdrental veritabanında bulunan film tablosundan B ile başlayan filmleri uzunluklarına göre sıralayalım ancak en uzun 6 filmi "pass" geçelim ve sonrasındaki 4 filmi sıralayalım. Bu durumda LIMIT 4 ve OFFSET 6 olacak.
WHERE title LIKE 'B%'
ORDER BY length DESC
SELECT *
FROM film
OFFSET 6
LIMIT 4;
--------------------------------------------
SELECT * FROM country
ORDER BY 6
LIMIT 4;
ilk 6 veriyi geçip sonrasında belirlediğimiz 4 verisi gelir.
![image](https://user-images.githubusercontent.com/66878884/175768491-1c773642-e55d-4cde-8e73-c8d2e83531f1.png)
--------------------------------------------


<hr>


				Aggregate Fonksiyonlar - MIN, MAX, SUM, AVG
Aggregate fonksiyonları yardımıyla bizler veri kümelerimizden sonuçlar(genel veriler) çıkarabiliriz. Ne demek istiyorum? Şu senaryoları düşünelim.

Toplam kaç adet müşterimiz var?
Elimizde bulunan filmlerin ortalama uzunluğu nedir?
Bu şekilde belirli veri kümelerinden tek bir sonuç çıkarmak için aggregate fonksiyonları kullanırız.

Örnek Kullanımlar
AVG fonksiyonunu kullandığımız sayısal değerlerden oluşan sütunun ortalama değerini alırız.

SELECT AVG(length) 
FROM film;
sorgusu sayesinde film tablosunda bulunan length sütunundaki değerlerin ortalamasını alırız. SUM fonksiyonunu kullandığımız sayısal değerlerden oluşan sütunun toplam değerini alırız.

SELECT SUM(length) 
FROM film;
sorgusu sayesinde film tablosunda bulunan length sütunundaki değerlerin toplamını alırız. MAX fonksiyonunu kullandığımız sayısal değerlerden oluşan sütunun en yüksek değerini alırız.

SELECT MAX(length) 
FROM film;
sorgusu sayesinde film tablosunda bulunan length sütunundaki değerlerin en yüksek değerini alırız. MIN fonksiyonunu kullandığımız sayısal değerlerden oluşan sütunun en düşük değerini alırız.

SELECT MIN(length) 
FROM film;
sorgusu sayesinde film tablosunda bulunan length sütunundaki değerlerin en düşük değerini alırız.


--------------------------------------------
ACABA TOPLAMDA KAÇ VERİMİZ VAR ?
SELECT COUNT(*) FROM film;
--------------------------------------------
EN YÜKSEK REPLECAMENT_COST'UMUZ NEDİR ?
Bu şekilde EN YÜKSEK gibi MAX'I kullanacağız
SELECT MAX(replacement_cost) FROM film
![image](https://user-images.githubusercontent.com/66878884/175772540-19bf7ede-9134-4758-b2df-cbb4b78951da.png)
--------------------------------------------
EN DÜŞÜK REPLECAMENT_COST'UMUZ NEDİR ?
SELECT MIN(replacement_cost) FROM film
![image](https://user-images.githubusercontent.com/66878884/175772551-4a80769c-50a3-4c57-9208-4d5ea382fa4d.png)
--------------------------------------------
ACABA FİlMLERİMİZİN ORTALAMASI NEDİR ?
SELECT AVG(length) FROM film
![image](https://user-images.githubusercontent.com/66878884/175772584-564a76e3-8353-49fe-83a4-e6f7066f2973.png)
ONDALIK KISMINDA GEREKSİZ ŞEKİLDE SIFIRLAR VAR ONLARI KALDIRMAK İÇİN;
SELECT ROUND(AVG(length),3) FROM film
TÜM FİLMLERİN UZUNLUKLARININ ORTALAMASINI .'DAN SONRA 3 ONDALIK ŞEKLİNDE BİZİM BELİRTTİĞİMİZ GİBİ GETİRİR.
ROUND(HANGİ DEĞERİ ROUND ETMEK İSTİYORSAK O DEĞER(LENGTH),KAÇ KARAKTERE KADAR YUVARLAYACAGIMIZI YAZARIZ)
![image](https://user-images.githubusercontent.com/66878884/175772672-1348bfa3-b7df-44bf-af51-edb39fb274f1.png)
--------------------------------------------
SUM
RENTAL_RATE'LERIN TOPLAMI
SELECT SUM(rental_rate) FROM film
![image](https://user-images.githubusercontent.com/66878884/175772703-b4f6971b-5100-452e-8be8-e242f6d34e04.png)
--------------------------------------------
SELECT MAX(length),MIN(length),SUM(replacement_cost) FROM film
EN UZUN FİLMİMİZİ,EN KISA FİLMİMİZİ,REPLACEMENT_COST'LARIN TOPLMAI
![image](https://user-images.githubusercontent.com/66878884/175772747-861733aa-f0af-497c-b836-6b4a91720272.png)
--------------------------------------------
BENİM RANTEL_RATE ORANIM 0.99 OLAN EN UZUN FİLMİ BULMA ?
SELECT MAX(length) FROM film
WHERE rental_rate=0.99
![image](https://user-images.githubusercontent.com/66878884/175772780-bedcf9aa-44b1-4d8f-a425-42fcd4aa0921.png)

--------------------------------------------
HER FARKLI RANTEL_RATE DEĞERİ İÇİN O RANTEL RANTE'E AİT EN UZUN FİLMİ BULMA

--------------------------------------------
<hr>


							GROUP BY
Bizler şimdiye kadar olan sorgularımızın tamamında sorguları yaparken genel veri kümesinin tamamı üzerine düşündük, ancak bazı durumlarda aynı sonuçları veri kümesinin içerisinde bulunan farklı gruplarda da bulmak isteyebiliriz. Senaryomuzu şu şekilde düşünelim, dvdrental veritabanında rental_rate sütununda bizim 3 farklı değerimiz var (0.99, 2.99, 4.99). Biz bu 3 farklı değer için en uzun filmi bulmaya çalışalım.

![image](https://user-images.githubusercontent.com/66878884/175775977-dc17fdc4-f300-4d02-928f-94fa4ff06537.png)


SELECT MAX(length) 
FROM film
WHERE rental_rate = 0.99;
SELECT MAX(length) 
FROM film
WHERE rental_rate = 2.99;
SELECT MAX(length) 
FROM film
WHERE rental_rate = 4.99;
İstediğimiz sonuçları elde ediyoruz ancak şöyle bir sorunumuz var 3 farklı değer yerine 30 farklı değer olsaydı? İşte bu şekilde senaryolar için yani verileri gruplama için GROUP BY anahtar kelimesi kullanılır.

GROUP BY Söz Dizimi
SELECT <sütun_adı>, <sütun_adı>, ... (veya aggregate func)
FROM <tablo_adı>
GROUP BY <sütun_adı>, <sütun_adı>, ...

Burada şuna dikkat etmemiz gerekir, SELECT anahtar kelimesinde bulunan sütunların GROUP BY anahtar kelimesi içerisinde bulunması gerekir.

GROUP BY Örnek Kullanım
Yukarıdaki senaryomuzu GROUP BY anahtar kelimesini kullanarak gerçekleştirelim. Dikkat ettiğiniz üzere SELECT ile kullanılan rental_rate sütunu GROUP BY satırında da kullanılmıştır.

SELECT rental_rate, MAX(length) 
FROM film
GROUP BY rental_rate;
![image](https://user-images.githubusercontent.com/66878884/175776152-9b227442-7e11-4e2f-b669-50d2c6c9e44a.png)

--------------------------------------------
SELECT rental_rate,COUNT(*) FROM film
GROUP BY rental_rate
![image](https://user-images.githubusercontent.com/66878884/175776175-7c1b455c-5a21-4103-bae1-2d1c4efaeafe.png)
--------------------------------------------
SELECT rental_rate,title,COUNT(*) FROM film
GROUP BY rental_rate
BİZLER 2 ADET DEĞİŞKEN YAZABİLİRİZ YA GROUP BY 'DA KULLANILAN SÜTUN İSMİ YA DA aggregate FONKSİYON YAZABİLİRİZ.
BİZ 3.DEĞİŞENİ (TİTLE) YAZDIGIMIZDA İSE BİZE AŞAĞIDA Kİ GROUP BY HATASINI VERİR. title sütununu görmek istiyorsan burda ki group by ifadesinde de bulunmak zorundadır diyor. 
![image](https://user-images.githubusercontent.com/66878884/175776216-ddcc5151-53f2-406f-95fb-ff0816c90484.png)

--------------------------------------------
SELECT rating,COUNT(*) FROM film
GROUP BY rating;

-- Her bir Rating için bu ratinglere karşılık gelen toplam kaç filmimizin oldugunu bulma
-- Film sayımızı COUNT'tan ubluyoruz ve grouplamamızı bir alttan satırdan yapıcaz
![image](https://user-images.githubusercontent.com/66878884/175776386-ef4786fb-69a8-4803-8baa-76797e42e549.png)

--------------------------------------------
SELECT replacement_cost,MIN(length) FROM film
GROUP BY replacement_cost;
-- Her bir replacement_cost ifadesine karşılık gelen en kısa filmimimizi bulma
![image](https://user-images.githubusercontent.com/66878884/175776436-a41b05a1-9749-43c3-81df-214a09ef24bd.png)


--------------------------------------------
SELECT replacement_cost,rental_rate,MIN(length) FROM film
GROUP BY replacement_cost,rental_rate;
-- replacement_cost ' U 14.99 REPTAL_RATE'İ 2.99 OLAN EN KISA FİLM 61DK DİYOR
![image](https://user-images.githubusercontent.com/66878884/175776529-47f76dce-4fb6-4601-be3f-9e6d79af05a3.png)
-- Toplam 63 tane tablo geliyor bize ben artık rental_rate'in 3 değer aldıgını biliyorum ve bu su demek oluyor demek ki unique olarak 21 tane tablomuz var aynı değerde

SELECT COUNT(DISTINCT replacement_cost) FROM film;
Sorugumuz ile 
![image](https://user-images.githubusercontent.com/66878884/175776626-973568f3-4e13-4fd2-b3e2-9bde814e5910.png)
sonucumuz gelir.
--------------------------------------------
MANTGIMIZ İLK VERİLERİ SIRALARI SONRA ONLARI GRUPLAR SONRASINDA O GURUPLADIUKLARIMIZI SIRALIYORUZ.
ONDAN DOLAYI ORDER BY - GROUP'TAN SONRA SIRALANIR.
SELECT replacement_cost,rental_rate,MIN(length) FROM film
GROUP BY replacement_cost,rental_rate
ORDER BY replacement_cost, rental_rate DESC;
replacement_cost'u artana göre rental_rate'i azalana göre sıralar.
![image](https://user-images.githubusercontent.com/66878884/175776706-7e9f4d7b-b736-4a98-850d-8f65635f3f9e.png)

<hr>

						HAVING
HAVING anahtar kelimesi sayesinde gruplandırılmış verilere koşullar ekleyebiliriz. Hemen aklımıza WHERE anahtar kelimesi geldi değil mi? Ancak WHERE anahtar kelimesi ile biz satır bazlı koşullar verebiliyoruz.

HAVING:GRUP BAZLI FİLTRE UYGULAR.
WHERE: SATIR BAZLI FİLTRE UYGULAR ARALARINDA Kİ EN BÜYÜK FARK BUDUR.

Şöyle bir senaryomuz olsun. Her bir rental_rate oranına karşılık gelen film sayısını bulalım. Bunu GROUP BY ile gerçekleştirebiliriz. Ancak bu kez 1 adım öteye gidip şöyle bir koşul ekleyelim toplam film sayısı 325 ten fazla olan rental_rate oranlarını görelim. Bu durumda GROUP BY ile elde ettiğimiz toplam film sayılarına koşul eklememiz gerekir.

--------------------------------------------
FİLM SAYISI 325'TEN BÜYÜK OLAN RANTEL_RATELERİ GETİRİR.
HAVING İLE GRUPLANMIŞ VERİLERE KOŞUL VERDİK.
SELECT rental_rate, COUNT(*) FROM film
GROUP BY rental_rate
HAVING COUNT(*) > 325;
--------------------------------------------
--KAÇ TANE SATIŞ YAPILDI.
SELECT COUNT(*) FROM payment
--------------------------------------------
--çalışanlara göre gruplayıp her bir çalışan kaçar tane satış yapmış.
SELECT staff_id,COUNT(*) FROM payment
 GROUP BY staff_id;
--------------------------------------------
--Toplam satısı 7300'den büyük olan çalışanı getirme
SELECT staff_id,COUNT(*) FROM payment
 GROUP BY staff_id
HAVING COUNT(*) > 7300
--------------------------------------------
--Toplamda 100'den daha fazla satıs yapan customer_id leri görme
SELECT customer_id,SUM(amount) FROM payment
GROUP BY customer_id
HAVING SUM(amount) > 100
ORDER BY SUM(amount) // bunu koyarak aratak sıralama işlemini yaparız.
--------------------------------------------

<hr>

						ALIAS (AS)
AS anahtar kelimesi sayesinde sorgular sonucu oluşturduğumuz sanal tablo ve sütunlara geçici isimler verebiliriz.

ALIAS SÜTUN KULLANIMI

SELECT <sütun_adı> AS <geçici_ad>
FROM <tablo_adı>;
ALIAS TABLO KULLANIMI

SELECT <sütun_adı>, <sütun_adı>...
FROM <tablo_adı> AS <geçici_ad>;



--------------------------------------------
SELECT first_name AS isim,last_name AS soyisim FROM actor
YALNIZCA SIRALADIGIMIZ VERİLERİN SÜTUNLARININ İSİMLERİNİ DEĞİŞTİRİYORUZ.GERÇEKTE DEĞİŞMEZ.O SORGU İÇERİSİNDE BİZE GÖRE DAHA ANLAMLI SIRALIYORUZ.
YENİ OLUŞTURACAĞIMIZ TABLOYA 1 DEN FAZLA FAZLA KELİME VEYA KARAKTER VERECEK OLURSAK O ZAMAN "" İÇERİSİNE ALMAMIZ LAZIM.
TEK VERİDĞİMİZ ZAMAN "" İÇERİSİNE ALMAYA GEREK YOK.
SELECT first_name  isim,last_name  soyisim FROM actor AYNI SONUCU ALIRIZ AS ' İ KOYUP KOYAMAMK ÖNEMLİ DEĞİL.
![image](https://user-images.githubusercontent.com/66878884/175781461-65889350-841d-4496-b94c-25a09219a2a8.png)
--------------------------------------------
SELECT first_name "isim test",last_name "soyisim test" FROM actor

![image](https://user-images.githubusercontent.com/66878884/175781577-d34dfac1-b149-4664-b09c-d7050d6c9308.png)

--------------------------------------------
<hr>

					CONTACT
SÜTUNLARI BİRLEŞTİRMEYE YARAR KARAKTERLERİ YAN YANA YAZMAMIZDA BİZE YARDIMCI OLUR.
--------------------------------------------
SELECT  CONCAT(first_name, ' ', last_name) AS "İsim ve Soyisim" FROM actor
![image](https://user-images.githubusercontent.com/66878884/175781696-d137cd61-1099-4789-beaa-a7cedaba2317.png)

--------------------------------------------

--------------------------------------------

<hr>

			Tablo Oluşturmak ve Silmek (CREATE - DROP)
Tablo Oluşturmak - CREATE
SQL ile yeni bir tablo oluşturmak için CREATE anahtar kelimesi kullanılır. Tablo oluştururken sonrasında daha detaylı konuşacağımız 3 önemli başlık daha vardır.

Sütunlara verilecek isim, sütunların veri tipi ve varsa sütunlarda bulunan kısıtlama yapıları.

Tablo Oluşturmak - CREATE Söz Dizimi
CREATE TABLE <tablo_adı> (
    <sütun_adı> <veri_tip> (kısıtlama_adı>,
    <sütun_adı> <veri_tip> (kısıtlama_adı>,
   ....
);
--------------------------------------------
Tablo Oluşturmak - CREATE Örnek Kullanım
author isminde bir tablo oluşturalım, id, first_name, last_name, email, birthday sütunları olsun. Veri tipleri ve kısıtlama yapılarıyla ilgili sonrasında detaylı olarak konuşacağız.

CREATE TABLE author (
  id SERIAL PRIMARY KEY,
  first_name VARCHAR(50) NOT NULL,
  last_name VARCHAR(50) NOT NULL,
  email VARCHAR(100)
  birthday DATE
);--------------------------------------------
Tablo Silmek - DROP
Oluşturduğumuz tabloları silmek için DROP anahtar kelimesi kullanılır.

Tablo Silmek - DROP Söz Dizimi
DROP TABLE (IF EXISTS) <tablo_adı>;
Burada IF EXISTS yapısını kullanarak yanlış tablo ismi yazımı durumunda hata mesajı almayı önleriz.

Tablo Silmek - DROP Örnek Kullanım
"test" isimli tablomuzu silmek istersek;

DROP TABLE IF EXISTS test;
--------------------------------------------

Sütunların 3 temel özelliği olur;
-- CREATE TABLE <table_name> (
--     <column_name> <data_type> <constraint>,
--     ...
--     <column_name> <data_type> <constraint>;
-- )
1.Sütun ismi <sütun_adı>
2.Data type <veri_tip>: ilgili sütuna koymak sitediğimiz veri tipidir.(numeric,string,tarih.vs)
3.<constraint>(ksııtlamaadi):Sütuna yerleştireceğimiz verinin özelliklerini veririz.Primary key,null vs.
--------------------------------------------
	

CREATE TABLE author(
--     Serial numeric ifade verir.Aynı zamanda otomomatik olarak artmasını sağlar verilerin.
--  PRIMARY KEY:TAblomuzda bulunacak her bir satır için benzersiz tanımlayıcı verir.
    id SERIAL PRIMARY KEY
--     VARCHAR(50 50 karaktere kadar string kabul ediyor.
--     NOT NULL BUradaki kısım boş olamaz tanımlaması.
    first_name VARCHAR(50) NOT NULL,
    last_name VARCHAR(50) NOT NULL,
    email VARCHAR(100),
    birthday DATE 
)
--------------------------------------------
INSERT INTO author (id,first_name,last_name,birthday
	tablolarımıza sütunların eklemnmesini yapıyoruz
	fakat burda bizim id'yi yazmamıza gerek yok Çünkü onu serüal olarak tanımladıgımız için otomatik olarak kendisi artarak gidecektir numaraları.

)
INSERT INTO author (first_name,last_name,email,birthday)
VALUES  
    ('Haruki','Murakami','haruki@gmail.com','1948-11-06'),
    ('Sabahattin','Ali','sabahattin@gmail.com','1955-08-06'),
    ('Sabahattin','Ali','sabahattin@gmail.com','1955-08-06'),
    ('Sabahattin','Ali','sabahattin@gmail.com','1955-08-06'),
    ('Sabahattin','Ali','sabahattin@gmail.com','1955-08-06');

--------------------------------------------
YENİ BİR TABLO OLUSTURUYORUZ FAKAT ŞABLON OLARAK LIKE AUTHOR DİYEREK ONUN ŞABLONUNU KULLANACAGIMIZI BELİRTİYORUZ.
	VERİLERİ ALMIYORUZ YALNIZCA TABLO ŞABLONUNU ALIYORUZ !
CREATE TABLE author2 (LIKE author)
	
--------------------------------------------
FARKLI TABLODA Kİ VERİLERİ ALMA
INSERT INTO author2 İLK OLARAK NEREYE INSERT EDİLECEĞİNİ SONRA NERDEN SELECT EDECEĞİMİZİ SEÇİYORUZ

INSERT INTO author2
SELECT * FROM author BU şekil kullanımda tüm verileri alıyoruz 
	,ANCAK

DİYELİM Kİ SEBAHATTIN ALİYİ ALMAK İSTİYORUZ SADECE
	
INSERT INTO author2
SELECT * FROM author
WHERE first_name = 'Sabahattin';

![image](https://user-images.githubusercontent.com/66878884/175804367-7f8c951b-ebd3-47d4-a970-9fe9bec0d1fd.png)

-------------------------------------------- 
CREATE TABLE author3 AS 
SELECT * FROM author; DİYEREK AUTHOR3 ADINDA YENİ BİR TABLO OLUSTUURP İÇİNDE Kİ TÜM VERİERİ ÇEKMEMİZE YARAR.

--------------------------------------------
TABLOYU SİLMEK
DROP TABLE IF EXISTS atuhor2 GENEL TABLOYU SİLMEK İÇİN.
--------------------------------------------

<hr>
--------------------------------------------
	
	
	
	Tablo Verilerini Güncellemek (UPDATE - DELETE)
Bir tabloda bulunan verileri güncellemek veya silmek için öncelikle örnek bir tablo oluşturup içine 5 date veri yerleştireceğim.

Bunun için Mockaroo benzeri servisleri kullanabiliriz. Aşağıdaki örnek tablo oluşturma ve veri girme komutlarını bulabilirsiniz.

CREATE TABLE my_apps (
	id INT,
	name VARCHAR(50),
	price VARCHAR(50)
);
INSERT INTO my_apps (id, name, price) values (1, 'Ronstring', '$0.96');
INSERT INTO my_apps (id, name, price) values (2, 'Duobam', '$3.44');
INSERT INTO my_apps (id, name, price) values (3, 'Tresom', '$2.21');
INSERT INTO my_apps (id, name, price) values (4, 'Redhold', '$2.52');
INSERT INTO my_apps (id, name, price) values (5, 'Y-find', '$9.14');

UPDATE
UPDATE anahtar kelimesi sayesinde tablomuzda bulunan verileri güncelleyebiliriz.

UPDATE Söz Dizimi
UPDATE <tablo_adı>
SET <sütun_adı> = değer, 
    <sütun_adı> = değer,
    ----
WHERE <koşul_adı>;
UPDATE Örnek Kullanım
my_apps tablosunda bulunan ve id 2' ye eşit olan verimizin name sütunundaki degerini 'Mayak' price sütunundaki değerini '$5.22' ile değiştirelim.

UPDATE my_apps
SET name = 'Mayak',
	price = '$5.22'
WHERE id = 2;
DELETE
DELETE anahtar kelimesi sayesinde tablomuzda bulunan verileri silebiliriz.

DELETE Söz Dizimi
DELETE FROM <tablo_adı>
WHERE <koşul_adı>;
DELETE Örnek Kullanım
my_apps tablosunda bulunan name sütunundaki verisi 'Tresom' olan satırı silelim.

DELETE FROM my_apps
WHERE name = 'Tresom';

--------------------------------------------
-- id'si 10 olan yazaramızı yeni bir yazarla değiştirme seneryosu
-- Güncelleme yapacağımız VeriTabanını seçiyoruz.
UPDATE author
-- İlk olarak değiştirmek istediğim sütun ismini yazacağım fakat
-- id otomatik olarak veriliyor bunu değiştirmeyeceğiz ve aynı zamanda o id'de olan yazarı değiştirmek istiyoruz.
SET first_name = 'Furkan',
last_name = 'Tasdemir',
email='furkan.com',
birthday = '1997-06-06'
-- eğer ki yukarıda ki gibi direkt güncellersek verilerin tamamamını değiştiririz biz bunu istemiyoruz.
-- Tek bi veriyi değiştirmek istiyoruz.
WHERE id = 10	
Bu değişikliği POSTGRESQL tablonun sonunda gösterir.
![image](https://user-images.githubusercontent.com/66878884/176409900-5c2dd079-26b3-4426-a956-f05501621537.png)
        
--------------------------------------------
-- İlk isminin baş harfleri V ile başlayan yazarların 
-- ismini değiştirme seneryosu

UPDATE author
SET first_name = 'XXXX',
last_name='YYYY'
WHERE first_name LIKE 'V%'            
            
--------------------------------------------
Yaptıgımız işlemleri Updateyken de görebiliriz bunun için RETURNİNG anahtar kelimesini kullanırız yani
-- İSmi odetta olan arkadaşımızın soyismini UPDATET seklinde değiştireceğiz
UPDATE author
SET last_name = 'UPDATE'
WHERE first_name = 'Trev'
-- BU değişiklik yaptıgımız satırın geri gelmesini istiyoruz bu nedenle
RETURNING *;
![image](https://user-images.githubusercontent.com/66878884/176412115-075177eb-1bb4-44f4-8052-eba0e661cd7c.png)
--------------------------------------------
Verileri silmek içinde DELETE anahtar kelimesi kullanılır.
DELETE FROM <table_name>
WHERE condition	    
--------------------------------------------	
-- id'si 6 olan veriyi silme
DELETE FROM author
WHERE id=6;	
--------------------------------------------	
	
	
	
	
	
	
	
	
	
	

--------------------------------------------
/*primery key: Bizim için birinci lanahtar ol. çevrilir. SAtırdı bulşunan veriyi diğer verilerden ayrıstırmak içindir.
foreign key:Genelde başka bir tabloda ki başka bir satıra referans verir.Bunlar yardımıyla başka tabloların satırlarına/primary keylerine faydalarınız/referans verebiliriz.
VErileri tekrar edebilir ondan dolayı integer yaparız.Tekrar edebilir buda aynı isimde yazar olabilir veya aynı yazarın farklı kitapları olabilir.
*/

/*CREATE TABLE book (
	id SERIAL PRIMARY KEY,/*int bir veri tipidir SERIAL +1 ol. artar */  /*PRIMARY KEY:Birincil ol yani birinci satırda olan satırları diğer satırlardan ayır */
	title VARCHAR(100) NOT NULL, /*NOT NULL:Burda kitabin baslıgının bos olmasını istemiyoruz demektir. VARCHAR(100)'lede 1-100 arasında olacaıgın söylüyoruz.'*/
	page_number INTEGER NOT NULL,
	inventory_id INTEGER REFERENCES inventory(inventory_id)/*FOREIGN key ler ilişki kuracagı için genelde ilişki kuracagı veri tabanının adına göre yaparız*/
);*/

/*select * from book*/

-- insert into book (id,title,page_number,inventory_id)values(1,'Furkan',6,55) ekleyecegiiz veriler.
select * from book


----------------------------------
	    POSTRESQL'DE 21 FARKLI VERİ TİPİ VARDIR -> POSTGRESQL (KULLANILAN VERSİYON) DATA TYPES YAZARAK DOC.'U GÖRÜNTÜLEYEBİLİRİZ.
	    
![image](https://user-images.githubusercontent.com/66878884/210126120-eec6437e-4336-4b17-8b8b-8b916b2f6fc4.png)

	    
---------------------------------
 ![image](https://user-images.githubusercontent.com/66878884/210126361-591d69de-a88c-4172-9e37-63fc46046bdb.png)

---------------------------------
![image](https://user-images.githubusercontent.com/66878884/210126429-df4aa02d-9626-44d2-b194-ce6d62e2b1d5.png)
---------------------------------
![image](https://user-images.githubusercontent.com/66878884/210126451-6042572b-9efc-4d97-9df9-53f710309676.png)  
---------------------------------	    
![image](https://user-images.githubusercontent.com/66878884/210126460-0a28fd90-3b21-477c-8f11-6cedba0c1740.png)
---------------------------------	    
![image](https://user-images.githubusercontent.com/66878884/210126463-e5e61755-6843-412c-b281-1bcc32ea7a1d.png)
---------------------------------
![image](https://user-images.githubusercontent.com/66878884/210126473-66644061-f59f-4d12-8fae-b10d6019f16c.png)
---------------------------------
![image](https://user-images.githubusercontent.com/66878884/210126480-43ecb15d-eb1c-4bfd-af18-2e0ec52dd301.png)
---------------------------------

------------------------------------------------- CHAR TYPES ------------------------------------------------
![image](https://user-images.githubusercontent.com/66878884/210126969-be7b9e1f-6104-4190-8a57-94a1d690ec9a.png)

-- -- CHARACTER TYPES
-- -- CHAR:Bizim belirtmiş oldugumuz kadar kapsa 10.olarak belirtsek bile 3 kelimelik şey yazsakta kendini 10'a göre ayarlar.
-- -- VARCHAR:bizim belirtmiş oldugumuz değer kadar yer kaplar 10 ol. belirsek bile diyelim ki aşağıda ki gibi 5 kelimelik bir şey yazdıgımızda kendini 5'e göre ayarlar.
-- --Herhangi bir sınırlama yapmadan bunu yazarsak içeriği kadar kapsar.
-- -- SELECT ('Lorem'::CHAR(10))
-- -- SELECT ('Lorem ipsum dolor sit amet'::CHAR(10));
-- -- SELECT ('Lorem'::VARCHAR(10));
-- -- SELECT ('Lorem ipsum dolor sit amet'::VARCHAR(10));
-- -- SELECT ('Lorem ipsum dolor sit amet'::VARCHAR);
-- -- SELECT ('Lorem'::TEXT);
-- -- SELECT ('Lorem'::CHAR(10));
-- SELECT ('Lorem ipsum dolor sit ame'::TEXT);

--BOOLEAN TYPES
-- SELECT (true,'yes','t',1) TRUE
-- SELECT (false,'no','f',0) FALSE
-- SELECT ('no'::BOOLEAN) 
-- SELECT (1::BOOLEN) 
-- SELECT ('f'::BOOLEN) 
-- SELECT (true::BOOLEN) 
-- SELECT (NULL::BOOLEN) 


--DATE TIME TYPES
-- SELECT ('1980-12-03' :: DATE)
-- SELECT ('DEC-03-1980' :: DATE)
-- SELECT ('DEC 03 1980' :: DATE)
-- SELECT ('1980 December 03')

-- SELECT ('03:44' :: TIME)
-- SELECT ('03:44 AM' :: TIME)
-- SELECT ('03:44 PM' :: TIME)
-- SELECT ('03:44:11' :: TIME)
SELECT ('02:16' :: TIME WITH TIME ZONE)--Zaman dilimiyle beraber getirir.+0... ol zmana getirir UTC'ye göre universal cordinatet time'a göre
-- SELECT ('1980 December 03 02:16:08' :: TIMESTAMP)--Zaman ve tarihi beraber getirir.

	    
 -------------------------------------------------NOT NULL AND AFTER ------------------------------------------------
 -- NOT NULL : Bir sütunumuzda devamlı olarak veri olmasını istiyoruz hiçbir türlü null değerini istemiyorsak eğer kullanırız.
--EĞER Kİ BU TANIMLAMALARI TABLOMUZ OLUSTUKTAN SONRA YAPMAK AKLIMIZA GELDİYSE ALTER KOMUTUNU KULLANIRIZ VE TANIMLAMALARIMIZI YAPARIZ.
LTER ve NOT NULL


NOT NULL
Birçok durumda bizler herhangi bir sütuna yazılacak olan verilere belirli kısıtlamalar getirmek isteriz. Örneğin yaş sütünunda sadece sayısal verilerin olmasını isteriz ya da kullanıcı adı sütununda bilinmeyen (NULL) değerlerin olasını istemeyiz. Bu gibi durumlarda ilgili sütunda CONSTRAINT kısıtlama yapıları kullanılır.
NULL bilinmeyen veri anlamındadır. Boş string veya 0 verilerinden farklıdır. Şu şekilde bir senaryo düşünelim bir kullanıcının email hesabı yoksa buradaki veriyi boş string şeklinde düşünebiliriz. Acak eğer kullanıcının maili var ancak ne olduğunu bilmiyorsak bu durumda o veri NULL (bilinmeyen) olarak tanımlanabilir.


NOT NULL Kullanımı
Employees şeklinde bir tablomuzu oluşturalım. Tablodaki first_name ve last_name sütunlarında bilinmeyen veri istemiyoruz, bu sütunlarda NOT NULL kısıtlama yapısı kullanabiliriz.

CREATE TABLE Employees (
    id SERIAL PRIMARY KEY,
    first_name VARCHAR(100) NOT NULL,
    last_name VARCHAR(100) NOT NULL,
    age INTEGER
);

ALTER ve NOT NULL

ALTER anahtar kelimesini varolan bir tabloda değişiklik yapmak için kullanılır. Aşağıdaki senaryoda bir sütuna NOT NULL kısıtlaması vermek için aşağıdaki söz dizimi yapısı kullanılır.

ALTER TABLE <tablo_adı>
ALTER COLUMN <sütun_adı>
SET NOT NULL;
	  
![image](https://user-images.githubusercontent.com/66878884/210127981-1248900c-4680-4069-a666-8be66b6f2ee2.png)
	    
	    
	    

![image](https://user-images.githubusercontent.com/66878884/210128053-674c549f-812f-4c36-8a16-a8eefe9acfb5.png)
ALTER KOMUTUNDAN SONRA BÖYLE BİR HATA ALIRIZ BURDA BİZE SEN USERNAME SÜTUNUN NOT NULL YAPMAYA CALISIYORSUN ANCAK BURADA NULL İFADELER VAR, NULL İFADESİ OLAN BİR SÜTUNU SEN NOTNULL'A ÇEVİREMEZSİN HATASI VERİYOR BİZLERE. BU HATADAN KURTULMA FARKLI SENARYOLARDA FARKLI ŞEKİLLERDE YAPILIR, SAYISAL BİR TABLO OLSAYDI ANORMAL BİR DEĞER VERİLEREK YAPILIYOR YAŞİ SÜTUNU OLSAYDI 999 GİBİ DEĞERLER VERİLİYOR Kİ BUNUN EKSTREM BİR DURUM OLDUGU BELLİ OLSUN İSTEDİĞİMİZ İÇİN.BİZ BURADA NULL OLAN SATIRLARI SİLEREK BU HATADAN KURTULACAĞIZ.

![image](https://user-images.githubusercontent.com/66878884/210128148-9d849190-aa53-498b-9d06-e7a0d71a4b64.png)
VE DELETE 0 ŞEKLİNDE BİR DÖNÜŞ ALDIK. HERHANGİ BİR ŞEKİLDE BİR SATIR SİLİNMEDİ BURDA = DEĞİL IS KULLANMAMIZ GEREKLİDİR.

![image](https://user-images.githubusercontent.com/66878884/210128164-06cf5187-379a-466f-bb28-72044861dccb.png)
VE BAŞARIYLA SİLDİK.
	    
![image](https://user-images.githubusercontent.com/66878884/210128187-4fb970bd-19b5-4f8b-877c-838887a50805.png)
 TABLOMUZU SADECE NULL OLMAYAN İFADELERE SAHİP ARTIK ŞİMDİ GİDİP TEKRARDAN ;
	    
![image](https://user-images.githubusercontent.com/66878884/210128201-1ce04fb7-cf56-4346-ba9c-66b156757449.png)
BAŞARILI ŞEKİLDE DÖNÜŞÜMÜZÜ ALDIK.
	    
![image](https://user-images.githubusercontent.com/66878884/210128218-ec3c8493-b553-4b03-b9f5-4fc3b6f88efe.png)
DEĞERİ NULL OLAN BİR VERİ GİRMEK İSTEDİĞİMİZ ZAMAN BİZE BU HATAYI VERİR.
	    
![image](https://user-images.githubusercontent.com/66878884/210128262-201f44fa-18ce-4504-b208-0d865b2be6d2.png)
BOŞ BİR DEĞER BİZİM İÇİN NULL DEĞER DEĞİLDİR DEĞER KOYMADIGIMIZ ZAMAN 0 OL. TANIMLARIZ VE NULL DEMEK DEĞİLDİR BURASI.



---------------------------------------------------- UNIQUE ----------------------------------------------------
UNIQUE
UNIQUE kısıtlaması ile uyguladığımız sütundaki verilerin birbirlerinden farklı benzersiz olmalarını isteriz. PRIMARY KEY kısıtlaması kendiliğinden UNIQUE kısıtlamasına sahiptir.

NOT NULL kısıtlamasında olduğu gibi tablo oluştururken veya ALTER komutu ile beraber tablo oluştuktan sonra da kullanabiliriz.

UNIQUE Kullanımı
Employees şeklinde bir tablomuzu oluşturalım. Tablodaki email sütununda bulunan verileri UNIQUE olarak belirlemek istersek.

CREATE TABLE Employees (
    ---
    emaile VARCHAR(100) UNIQUE,
    ----
);

ALTER ve UNIQUE

ALTER TABLE <tablo_adı>
ADD UNIQUE <sütun_adı>


Bu arada herhangi bir sütuna UNIQUE kısıtlaması getirirsek ve öncesinde UNIQUE olmayan verileri kaldrmamız gerekir.



![image](https://user-images.githubusercontent.com/66878884/210128415-a8ddf980-109c-491a-834d-534600e43d00.png)
AYNEN NOT NULL KISITLAMASINDA OLAN HATASINDA OLDUGU GİBİ BURDA DA O HATAYI ALIRIZ UNİQUE OLMAYAN VERİLERİ BİLDİRİR.
	    
![image](https://user-images.githubusercontent.com/66878884/210128494-f3a4ceb1-9805-46df-8e1d-26c85a30d910.png)
DİREKT TANIMLI OLAN MAİLLERİMİZE GELİP ÇİFT TIKLADINTAN SONRA -> DEĞİŞTİRİP -> F6 İLE KAYIT EDİP DEĞİŞİKLİĞİ YAPARIZ .
	    
![image](https://user-images.githubusercontent.com/66878884/210128639-c6911227-652c-4476-bd06-afd2d39c0637.png)



---------------------------------------------------- CHECK ----------------------------------------------------
 CHECK
CHECK kısıtlaması ile uyguladığımız sütundaki verilere belirli koşullar verebiliriz. Örneğin age (yaş) olarak belirlediğimiz bir sütuna negatif değerler verebiliriz veya web portaline üye olan kullanıcıların yaşlarının 18 yaşından büyük olması gibi kendi senaryolarımıza uygun başka kıstlamalar da vermek isteyebiliriz.

CHECK kısıtlamasını da tablo oluştururken veya ALTER komutu ile beraber tablo oluştuktan sonra kullanabiliriz.

CHECK Kullanımı
Employees şeklinde bir tablomuzu oluşturalım. Tablodaki age sütununda bulunan verilerin 18'e eşit veya büyük olmasını istiyoruz.

CREATE TABLE Employees (
    ---
    age INTEGER CHECK (age>=18)
    ----
);
ALTER ve CHECK
ALTER TABLE <tablo_adı>
ADD CHECK (age>=18)


-- INSERT INTO users(username,email,age)
-- VALUES 
-- 	('gamer3','gamer5@gmail.com',-22);
	
-- SELECT * FROM users;

-- CHECK KISITLAMALARINI 2 ŞEKİLDE YAPABİLİRİZ;
-- 1-YA TABLOYU OLUŞTURURKEN 
-- 2-YA DA TABLODA DEĞİŞİKLİK YAPARKEN.

ALTER TABLE users
ADD CHECK (age >18)

![image](https://user-images.githubusercontent.com/66878884/210130143-f4433bdc-5c2a-4be0-b03c-119a62719c54.png)
BU ŞEKİLDE HATA ALIYORUZ BU DA YUKARIDA Kİ HATALARIMIZ GİBİ BİZE UYMAYAN VERİLERİN OLDUĞUNU BELİRTİYOR.
![image](https://user-images.githubusercontent.com/66878884/210130162-f22dc862-3bbd-4716-a396-f28003f9d060.png)

![image](https://user-images.githubusercontent.com/66878884/210130191-d76bce1b-c687-4ace-b091-df5998a01c23.png)
BU ŞEKİLDE SİLEREK TABLOMUZU DÜZENLİYORUZ.
	    ![image](https://user-images.githubusercontent.com/66878884/210130213-44a2a7c3-05e3-4bb0-88a8-6364066c456c.png)

	    
![image](https://user-images.githubusercontent.com/66878884/210130235-85f494de-a0c7-40b9-86de-882c6384d007.png)
YAPTIGIMIZ TANIMLANIN DOĞRULUĞUNU BURADA GÖRÜYORUZ BURDA USER TABLOSUNDA Kİ users_age_check'in KISITLMASINA KARŞI GELİYORSUN DİYOR VE -'Yİ POZİTİF BİR DEĞERE DÖNEREK TABLOMUZA EKLEYEBİLİYORUZ.
	    
![image](https://user-images.githubusercontent.com/66878884/210130269-84e75a23-fd7d-4729-b99e-b62946f0d68c.png)
	    
CREATE TABLE products(
product_no integer,
name text,
price numeric CHECK (price > 0),
discounted_price numeric CHECK (discounted_price > 0),
CHECK (price > discounted_price)-- ayrı bir CHECK daha koyarak PRİCE'IN İNDİRİM YAPILMIŞ FİYATTAN DAHA BÜYÜK OLMAK ZORUNDADIR DİYE FARKLI BİR CHEK KULLANDIK.
);
	    ![image](https://user-images.githubusercontent.com/66878884/210130425-28cdce53-dbc5-4fd7-ba39-af5073d9a21c.png)
YANLIS KARSILASTIRMA YAPTIGIMIZ İÇİN BİZE KARŞI GELİYOR. - DEĞER VERSEKTE BİZE HATA VERİR.
	    
![image](https://user-images.githubusercontent.com/66878884/210130439-8411a63c-33dd-433a-9195-d048b9daae19.png)
DOĞRU ŞEKİLDE YAPTIGIMIZDA BİZİ BU TABLO KARŞILAR.
	    

	    

 -------------------------------------------------INNER JOIN ------------------------------------------------

JOIN Kavramı (Birleştirme)


Veraitabanları çoğunlukla birbiri ile ilşkili olan tablolardan oluşur. Bu birbiri ile ilişkili olan tablardaki verileri farklı JOIN yapıları kullanarak sanal olarak birleştirip daha anlamlı veriler haline getirebiliriz.



INNER JOIN


INNER JOIN yapısı sayesinde birbiriyle ilişkili olan tabloların birbiriyle eşleşen (kesişen) verilerini sıralayabiliriz. Senaryomuzda kitapları gösterdiğimiz book tablosu ve yazarları gösterdiğimiz author tablosu var, author tablosunun id sütunuyla book tablosunun author_id sütunlarında bulunan veriler sayesinde her iki tabloya ait bilgilerden daha anlamlı sonuçları elde edebiliriz.



Aşağıdaki SQL sorgusunda kitap isimlerini yazar isim ve soyisimler ile birlikte gösterebiliriz.



SELECT book.title, author.first_name, author.last_name
FROM book
JOIN author ON author.id = book.author_id;


Yukarıdaki sorgumuzda tablolar arasındaki eşleşmeyi author.id ve book.author_id sütunları yardımıyla yapıyoruz.



Inner Join



Yukarıdaki görselimizde de gördüğümüz üzere INNER JOIN tablolar arasındaki eşleşen (kesişen) verileri sıralar. Bundan dolayı INNER JOIN yapısı simetriktir, author - book tablolarının yerlerinin değiştirilmesi sonucu etkilemez.
            ![image](https://user-images.githubusercontent.com/66878884/210132492-aac4169b-8d61-4766-bb53-705db369fd84.png)



INNER JOIN Söz Dizimi


SELECT <sütun_adı>, <sütun_adı> ...
FROM <tablo1_adı>
INNER JOIN <tablo2_adı>
ON <tablo1_adı>.<sütun_adı> = <tablo2_adı>.<sütun_adı>;
q

Buradaki tablo1 "left table", tablo2 "right table" olarak da adlandırılır.


	    
![image](https://user-images.githubusercontent.com/66878884/210132382-a2432fb9-5901-4e2a-8288-c7d9726833b3.png)
![image](https://user-images.githubusercontent.com/66878884/210132428-e40997f3-60b5-4b1b-af07-6082056d56d1.png)
![image](https://user-images.githubusercontent.com/66878884/210132483-e1dc0c64-9382-4a64-9bf9-8538047fb3f9.png)
AYNI SONUCU ALIRIZ

 -------------------------------------------------LEFT JOIN ------------------------------------------------



LEFT JOIN yapısındaki tablo birleştirmesinde, birleştirme işlemi tablo 1 (soldaki tablo) üzerinden gerçekleştirilir. Senaryomuzu şu şekilde düşünelim eğer tablo 1 olarak book tablosunu aldığımızda öncelikle book tablosundaki ilgili sütundaki tüm verileri alacağız, sonrasında bu verilerin eşleştiği ilgili tablo 2 sütunundaki verileri alacağız. Tablo 1 de olup Tablo 2 de olmayan veriler için NULL değeri kullanılır.



Aşağıdaki SQL sorgusunda kitap isimlerinin tamamını alıyoruz, sonrasında bu kitap isimleriyle eşleşebilen yazar isimlerini alıyoruz. Kitap isimlerine karşılık olmayan yazarlar için NULL değeri alıyoruz.



SELECT book.title, author.first_name, author.last_name
FROM book
LEFT JOIN author
ON author.id = book.author_id;


Yukarıdaki sorgumuz sonucunda göreceğimiz gibi kitapların yazar bilgisine sahip değilse NULL değerlerini alırız.
            ![image](https://user-images.githubusercontent.com/66878884/210132859-c26c1275-08f3-4ba6-acd4-ef92b6184799.png)


Left Join



Yukarıdaki görselimizde de gördüğümüz üzere LEFT JOIN tablolar arasındaki eşleşmeyi tablo 1 (soldaki tablo) üzerinden belirlenir.



LEFT JOIN Söz Dizimi


SELECT <sütun_adı>, <sütun_adı> ...
FROM <tablo1_adı>
LEFT JOIN <tablo2_adı>
ON <tablo1_adı>.<sütun_adı> = <tablo2_adı>.<sütun_adı>;


Buradaki tablo1 "left table", tablo2 "right table" olarak da adlandırılır.
            
 -------------------------------------------------RIGHT JOIN ------------------------------------------------
RIGHT JOIN yapısındaki tablo birleştirmesinde, birleştirme işlemi tablo 2 (sağdaki tablo) üzerinden gerçekleştirilir. Senaryomuzu şu şekilde düşünelim eğer tablo 2 olarak author tablosunu aldığımızda öncelikle author tablosundaki ilgili sütundaki tüm verileri alacağız, sonrasında bu verilerin eşleştiği ilgili tablo 1 sütunundaki verileri alacağız. Tablo 2 de olup Tablo 1 de olmayan veriler için NULL değeri kullanılır.



Aşağıdaki SQL sorgusunda yazar isim ve soyisim bilgilerinin tamamını alıyoruz, sonrasında eşleşebilen kitap isimlerini alıyoruz. Yazar bilgilerine karşılık olmayan kitap isimleri için NULL değeri alıyoruz.



SELECT book.title, author.first_name, author.last_name
FROM book
RIGHT JOIN author
ON author.id = book.author_id;


Yukarıdaki sorgumuz sonucunda göreceğimiz gibi yazarlara ait olmayan kitaplar NULL değerlerini alırız.
            ![image](https://user-images.githubusercontent.com/66878884/210132872-e8348949-c2fe-4ec3-aa3b-621f30f1b643.png)




Right Join



Yukarıdaki görselimizde de gördüğümüz üzere LEFT JOIN tablolar arasındaki eşleşmeyi tablo 1 (soldaki tablo) üzerinden belirlenir.



RIGHT JOIN Söz Dizimi


SELECT <sütun_adı>, <sütun_adı> ...
FROM <tablo1_adı>
RIGHT JOIN <tablo2_adı>
ON <tablo1_adı>.<sütun_adı> = <tablo2_adı>.<sütun_adı>;


Buradaki tablo1 "left table", tablo2 "right table" olarak da adlandırılır.

 -------------------------------------------------FULL JOIN ------------------------------------------------



FULL JOIN
Full JOIN yapısındaki tablo birleştirmesinde, birleştirme işlemi her iki tablo üzerinden gerçekleştirilir. Senaryomuzu şu şekilde düşünelim eğer tablo 1 olarak book tablosunu aldığımızda öncelikle book tablosundaki ilgili sütundaki tüm verileri alacağız, sonrasında tablo 2 deki ilgili sütunlardan tüm verileri alacağız. Tablo 1 de olup Tablo 2 de olmayan ve Tablo 2 de olup Tablo 1 de olmayan veriler için NULL değeri kullanılır.

Aşağıdaki SQL sorgusunda kitap isimlerinin tamamını alıyoruz, sonrasında yazar isimlerini alıyoruz. Eşleşemeyen veriler için NULL değeri alıyoruz.

SELECT book.title, author.first_name, author.last_name
FROM book
FULL JOIN author
ON author.id = book.author_id;
Yukarıdaki sorgumuz sonucunda göreceğimiz gibi kitapların yazar bilgisine sahip değilse NULL değerlerini alırız, yazarlar kitap bilgisine sahip değilse orada da NULL değerlerini alırız.

Full Join

Yukarıdaki görselimizde de gördüğümüz üzere FULL JOIN tablolar arasındaki birleştirmeyi her iki tablo üzerinden belirlenir.

FULL JOIN Söz Dizimi
SELECT <sütun_adı>, <sütun_adı> ...
FROM <tablo1_adı>
FULL JOIN <tablo2_adı>
ON <tablo1_adı>.<sütun_adı> = <tablo2_adı>.<sütun_adı>;
Buradaki tablo1 "left table", tablo2 "right table" olarak da adlandırılır.


 -------------------------------------------------FULL JOIN ------------------------------------------------
UNION operatörü sayesinde farklı SELECT sorgularıyla oluşan sonuçları tek bir sonuç kümesi haline getiririz.



UNION Kullanımı


bookstore veritabanında iki adet sorgu yapıyoruz. İlk sorgumuzda sayfa sayısı en fazla olan 5 kitabı, ikinci sorgumuzda ise isme göre 5 kitabı sıralıyoruz. UNION anahtar kelimesi sayesinde bu iki sorguyu da birleştirebiliriz.



(
SELECT * 
FROM book
ORDER BY title
LIMIT 5
)
UNION
(
SELECT * 
FROM book
ORDER BY page_number DESC
LIMIT 5
);


UNION operatörü kullanılacağı sorguların, sütun sayıları eşit olmalıdır ve sütunlardaki veri tipleri eşleşmelidir.



UNION Söz Dizimi


SELECT <sütun_adı>, <sütun_adı>...
FROM <table1>
UNION
SELECT <sütun_adı>, <sütun_adı>...
FROM <table2>

UNION ALL


UNION operatörü bize birleşik veriler içerisindeki tekrar edenleri göstermez. Tekrar edenleri görmek için UNION ALL kullanırız.
            
            
            
            
            
  -------------------------------------------------INTERSECT ve EXCEPT ------------------------------------------------
           
   INTERSECT operatörü sayesinde farklı SELECT sorgularıyla oluşan sonuçların kesişen verilerini tek bir sonuç kümesi haline getiririz.



INTERSECT Kullanımı


bookstore veritabanında iki adet sorgu yapıyoruz. İlk sorgumuzda sayfa sayısı en fazla olan 5 kitabı, ikinci sorgumuzda ise isme göre 5 kitabı sıralıyoruz. INTERSECT anahtar kelimesi sayesinde bu iki sorgu sonucunda oluşan veri kümelerinden kesişen verileri tek bir sonuçta birleştiririz.



(
SELECT * 
FROM book
ORDER BY title
LIMIT 5
)
INTERSECT
(
SELECT * 
FROM book
ORDER BY page_number DESC
LIMIT 5
);


INTERSECT operatörü kullanılacağı sorguların, sütun sayıları eşit olmalıdır ve sütunlardaki veri tipleri eşleşmelidir.



INTERSECT Söz Dizimi


SELECT <sütun_adı>, <sütun_adı>...
FROM <table1>
INTERSECT
SELECT <sütun_adı>, <sütun_adı>...
FROM <table2>

INTERSECT ALL


INTERSECT operatörü bize kesişen veriler içerisindeki tekrar edenleri göstermez. Tekrar edenleri görmek için INTERSECT ALL kullanırız.



EXCEPT Kullanımı


bookstore veritabanında iki adet sorgu yapıyoruz. İlk sorgumuzda sayfa sayısı en fazla olan 5 kitabı, ikinci sorgumuzda ise isme göre 5 kitabı sıralıyoruz. EXCEPT anahtar kelimesi sayesinde ilk sorguda olup ancak ikinci sorguda olmayan verileri gösterir.



(
SELECT * 
FROM book
ORDER BY title
LIMIT 5
)
EXCEPT
(
SELECT * 
FROM book
ORDER BY page_number DESC
LIMIT 5
);


EXCEPT operatörü kullanılacağı sorguların, sütun sayıları eşit olmalıdır ve sütunlardaki veri tipleri eşleşmelidir.


EXCEPT Söz Dizimi


SELECT <sütun_adı>, <sütun_adı>...
FROM <table1>
EXCEPT
SELECT <sütun_adı>, <sütun_adı>...
FROM <table2>

EXCEPT ALL


EXCEPT operatörü bize ilk sorguda olan ancak ikinci sorguda olmayan veriler içerisindeki tekrar edenleri göstermez. Tekrar edenleri görmek için EXCEPT ALL kullanırız.         
            
            
            
  -------------------------------------------------ALT SORGU ------------------------------------------------
            
  Alt Sorgular (Subqueries)


Bir sorgu içerisinde, o sorgunun ihtiyaç duyduğu veri veya verileri getiren sorgulardır.



Alt Sorgu Kullanımı


bookstore veritabanında "Gülün Adı" isimli kitabımızın sayfa sayısı 466 dır. Bu kitaptan daha fazla sayıda sayfası bulunan kitapları aşağıdaki sorgu yardımıyla sıralayabiliriz.



SELECT *
FROM book
WHERE page_number > 466;


Ancak yukarıdaki sorgumuzda şöyle bir sorun var. 466 ifade statik bir ifade ve biz bu değeri bilmiyor olabiliriz. Bu nedenle buradaki 466 rakamını aşağıdaki sorgu yardımıyla bulabiliriz.



SELECT page_number
FROM book
WHERE title = 'Gülün Adı'


İşte bu ikinci sorgumuz ilk sorgumuzda bir alt sorgu görevi görebilir. Her iki sorguyu da birleştirelim.



SELECT *
FROM book
WHERE page_number >
(
SELECT page_number
FROM book
WHERE title = 'Gülün Adı'
);          
            
            
            
            
  ------------------------------------------------- Any ve All Operatörleri  -------------------------------------------------


Any ve All operatörleri alt sorugularda sıklıkla kullanılır ve tek bir sütunda bulunan bir değerle bir değer dizisinin karşılaştırılmasını sağlar.



ANY Operatörü


Alt sorgudan gelen herhangi bir değer koşulu sağlaması durumunda TRUE olarak ilgili değerin koşu sağlamasını sağlar. bookstore veritabanında yapmış olduğumuz aşağıdaki sorguyu inceleyelim.



SELECT first_name, last_name
FROM author
WHERE id = ANY
(
  SELECT id
  FROM book
  WHERE title = 'Abe Lincoln in Illinois' OR title = 'Saving Shiloh'
)


Yukarıda görmüş olduğunuz gibi alt sorgudan gelebilecek potansiye iki id değeri var, bu id değerinin her ikisi de birbirinden bağımsız olarak ana sorgudaki id sütununda bulunan değerler ile eşleştiği için sorgu sonucunda oluşan sana tabloda id değeri 4 ve 5 olan yazarlara ait first_name ve last_name değerlerini göreceğiz.



ALL Operatörü


Alt sorgudan gelen tüm değerlerin koşulu sağlaması durumunda TRUE olarak döner.

bookstore veritabanındaki yine aynı sorguyu inceleyelim.



SELECT first_name, last_name
FROM author
WHERE id = ALL
(
  SELECT id
  FROM book
  WHERE title = 'Abe Lincoln in Illinois' OR title = 'Saving Shiloh'
)


Burada ne söylemiştik alt sorgu tarafından 4 ve 5 id leri gelecek burada eştlik olduğu için aynı anda 4 ve 5 in bu şulu sağlaması olanaksız olduğu için herhangi bir değer dönülmeyecektir.           
            
            
     ------------------------------------------------- ALT SORGULAR VE JOIN KULLANIMI  -------------------------------------------------         
            
    Alt Sorgular ve JOIN Kullanımı


Altsorgular ve JOIN kavramları birlikte çok sık kullanılırlar. Aşağıdaki iki senaryoda bu iki yapıyı birlikte kullanacağız.



İlk senaryomuz: bookstore veri tabanında kitap sayfası sayısı ortalama kitap sayfası sayısından fazla olan kitapların isimlerini, bu kitapların yazarlarına ait isim ve soyisim bilgileriyle birlikte sıralayınız.



SELECT author.first_name, author.last_name, book.title
FROM author
INNER JOIN book ON book.author_id = author.id
WHERE page_number >
(
  SELECT AVG(page_number) FROM book
);



Yukarıdaki sorgumuzda kitaplara ait yazar bilgilerini JOIN kullanarak elde ediyoruz. Ortalama sayfa sayısını da alt sorgudan getiriyoruz.



İkinci senaryomuz: dvdrental veritabanında en uzun filmlerin isimlerini aktör isim ve soyisimleriyle birlikte sıralayalım.



SELECT actor.first_name, actor.last_name, film.title
FROM actor
JOIN film_actor ON film_actor.actor_id = actor.actor_id
JOIN film ON film.film_id = film_actor.film_id
WHERE film.length =
(
  SELECT MAX(length)  FROM film
)



Burada da görmüş olduğumuz gibi film lerin aktör bilgilerini ikili JOIN yapısı kullanarak elde ediyoruz. En uzun film süresini de alt sorgudan getiriyoruz.        

