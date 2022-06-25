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








































































