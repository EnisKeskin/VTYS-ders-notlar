
# <center>Açık/Kapalı Kaynak Kod İlişkisel VTYS Yazılımları Ve Mimarilerinin Karşılaştırmalı Analizleri</center>

# Açık Kaynak Kodlu Yazılım(Open Source)

- Açık kaynak  kodlu yazılım, kaynak kodu isteyen herkese açık olan yazılımlardır.
- Bu tür yazılımların ayırt edici özelliği kullanıcıya yazılımı değiştirme özgürlüğü sağlamasıdır.

- Açık kaynak kodlu yazılımlar;
- Uyarlanabilir,
- Sağlam,
- Hızlı,
- Güvenli,
- Yeni bir yazılım üretme biçimi, yeni iş modelleri sunmaktadır.

# Kapalı Kaynak Kodlu Yazılım(Closed Source)

- Açık kaynak alternatifleri artıyor olmasına rağmen, kişisel bilgisayarlar, özellikle masaüstü bilgisayarlar, üzerinde en çok kullanılan işletim sistemleri, kapalı kaynak olma eğilimindedir.

- Geliştirilme şansı yoktur, ücretlidir.

# AÇIK VE KAPALI KAYNAK YAZILIMLARIN AVANTAJLARI

| Open Source (Açık kaynak)                                                                                      | Closed Source (Kapalı kaynak)                                                          |
| -------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------- |
| Kodlar herkese açık olduğu için kullanıcı kendi isteğine göre değiştirip geliştirebilir.                       | Grafik kullanan uygulamarın daha performanslı çalışmasını sağlar                       |
| Geliştirdiğimiz yazılımı satıp maddi kazanç elde edebiliriz.                                                   | Bilgisayarımızın daha hızlı çalışmasını ve uygulamaların daha hızlı çalışmasını sağlar |
| Ücretsiz olması en büyük avantaj                                                                               | Görsel yönden gelişmiştir.                                                             |
| Virüs yok denecek kadar azdır                                                                                  | Kullanımı kolaydır                                                                     |
| İhtiyaç duyduğu donanı açısından da çok ucuzdur                                                                | Kodlar kapalı olduğu için güvenilirdir.                                                |
| Çok kapsamlı testlerden geçmemiş olması her an bir güvenlik açığı oluşma ihtimali vardır.                      | Kodları kapalı olduğu için geliştirmeye izin verilmiyor.                               |
| Henüz tüm ihtiyaçlara tam olarak cevap verememesi bir çok kullanıcının bu tarz sistemlere güvenini azaltmıştır | Ücretlidir                                                                             |
| Tecrübeli olmayanlar için kullanımı zordur                                                                     | Sitem çalışırken arka planda kullanıcıdan gizli işlemler gerçekleştirebilir.           |

# İlişkisel Veri Tabanı Yönetim Sistemleri

- ilişkisel veri tabanı, organize edilmiş verilerin tablolarda saklanması ve bu tablolar arasında kurulan bağ ile oluşan veri tabanı çeşididir.
- Tablolar satır ve sütunlardan oluşur, üzerinde verileri saklayabilir, ekleyebilir, silebilir ve güncelleyebiliriz.
- Her satır aynı sütunlara yani alanlara sahiptir.
- Her bir sütun o tabloda bulunması gereken ortak özellikleri yansıtır.
- Tablo üzerinde ki her bir satıra ise kayıt diyoruz
- Tablolar arasında kurulan ilişkiler ile verileri organize bir şekilde işlemek mümkün.
- **Veri Tekrarı (Data Redundancy)**: Aynı verilerin tekrarlanması önlenir.
- **Veri Tutarlılığı (Data Consistency)**: Personel tablosuna personelin bölümü yazıldığında sistem böyle bir bölümün Bölüm tablosunda olup olmadığını kontrol eder.
- **Veri Bütünlüğü (Data Integrity)**: Verinin farklı tablolarda ayrıldığı durumlarda, verilerin tümünün bir bütün olarak kullanılmasını sağlar.
- **Veri Güvenliği (Data Security)**: Yetkilendirme sistemi sayesinde hangi verilere kimin ulaşabileceğini belirleyerek verileri koruma altına alırız.
- **Veri Paylaşımı | Eş zamanlılık (Concurrency)**: Bir veri tabanına veri bütünlüğü ve tutarlılığı bozulmadan ağ üzerinden binlerce kullanıcı tarafından erişim sağlanabilir.
- **Veri Bağımsızlığı (Data Independence)**: Kullanıcıdan arka planda verilerin fiziksel alan üzerinde nasıl depolandığı yada ne tarz algoritmalar ile organize olduğunun gizlenmesidir.

# Transaction

- Transaction , daha küçük parçalara ayrılamayan en küçük işlem yığınına denir
- “Transaction”, prensip olarak ya bütün işlemleri gerçekleştirir ya da hiçbirini gerçekleştirmez. İşlemlerden biri dahi başarısız olursa, bu prensip nedeniyle hiçbir işlem olmamış kabul edilir;
- Bu işlemler sırasında veriler üzerindeki değişikliklerin de tutarlı olması, birbirlerini tamamlayıcı nitelik taşıması gerekir.
- Transaction çeşitleri 4 tanedir.
  - Begin Transaction
  - Save transaction
  - Rollback
  - Commit

# ACID (Atomicity,Consistency,Isolation,Durability)

- İlişkisel veritabanlarındaki Transaction için tanımlanmış özellik setidir.
- **Atomicity(Bütünlük)**: Transaction işlemini bir bütün olarak görür.
- **Consistency(Tutarlılık)**: Transaction işlemi sonucunda veritabanında ki verinin geçerli durumunun, bir sonraki geçerli duruma geçmesidir.
- **Isolation(izolasyon)**: Aynı anda birden fazla işlem gerçekleştirilmesini engeller.
- **Durability(Dayanıklılık)**: Transaction sırasında fiziksel veya işlemsel bir hata olması durumunda sistemin kendisini bir önceki geçerli veri durumuna döndürebilme kabiliyetidir.

# ACID Özet

- **A (Atomicity - Bölünemezlik)**
  - Tamamı veya hiçbiri
- **C (Consistency - Tutarlılık)**
  - İşlemlerin yarım bırakılmamasını garanti eder
- **I (Isolation - Yalıtım)**
  - Her işlem (ing transaction) diğerinden bağımsızdır
- **D - (Durability - Dayanıklılık)**
  - İşlenmiş veriler hiç bir zaman kaybolmaz

# Popüler Kapalı Kaynak Kod Veri Tabanı Sistemleri

- Microsoft SQL Server (MsSQL)
- Oracle

# Microsoft SQL Server (MsSQL)

- Performanslı bir şekilde çalıştırabilecek çok güçlü bir veri tabanı yönetim sistemidir.
- Database Engine kendi arasında iki gruba ayrılıyor.
- Birinci Grup Relational Engine diğeri ise Storage Enginedir

## DATABASE ENGINE

- **Relational Engine** :Sorguların optimizasyonu ve çalıştırılmasından sorumludur ve 3 bölümden oluşur.
  - **Command Parser** : Sorgu yazım hatalarına karşı denetler sorgu ağacını hazırlar.
  - **Query Optimizer** : Sorgularının execution planlarının hazırlanmasını sağlar. İlk aşaması Pre-Optimization denilen ve sorgunun karmaşıklığına göre kaç plan çıkarılacağına karar verildiği aşamadır.
  - **Query Executor** : Query i çalıştırır.madır.

## STORAGE ENGINE

- Veri tabanının fiziksel dosyalarından (Data ve Log)sorumlu olup bu dosyaların barındırıldığı yapının ( Storage System, Disk …) performansı , güvenli olması ve doğru barındırılmasından mesuldür.
- Genel anlamda I/O ile ilgili süreçleri kapsar. BACKUP,RESTORE, vb. süreçlerde Storage Engine tarafından yürütülmektedir.

<center><image src="./image/storeengine.gif" width="500" height="300"/></center>

# ORACLE

- İlişkisel Veritabanı Yönetim Sistemleri (Relational Database Management Systems - RDBMS) büyük miktarlardaki verilerin güvenli bir şekilde tutulabildiği, bilgilere hızlı erişim imkanlarının sağlandığı, bilgilerin bütünlük içerisinde tutulabildiği ve birden fazla kullanıcıya aynı anda bilgiye erişim imkanının sağlandığı programlardır.

## Oracle Database Server Yapısı

- Memory Birimleri
- Process Birimleri
- Depolama Birimleri

## 1. Oracle Memory Birimleri

- **System Global Area (SGA)**: SGA bir oracle instance için, data ve control bilgilerinin tutulduğu, bütün server ve processler tarafından kullanılan, paylaşımlı memory alanıdır.

- **Process Global Area (PGA)**: Bir oracle server veya background process başlatıldığında oluşturulan, paylaşımlı olmayan, herbir process in kendine ait alanının bulunduğu , data ve control bilgilerinin tutulduğu memory alanıdır.

### System Global Area (SGA) Memory Birimleri

- **Database Buffer Cache**: Database’den query'ler yardımıyla çekilen dataların tutulduğu yada saklandığı alandır.
- **Redo Log Buffer**: Instance crash olduğunda recover edilebilmesi için gerekli bilgilerin cache lendiği alandır
- **Shared Pool**: Database Userları tarafından paylaşılan çeşitli yapıların tutulduğu alandır
- **Large Pool**: Geniş memory alanı gerektiren, oracle Backup ve Recover gibi yada I/O prosesleri gibi işlemlerin yerleştirildiği alan olup, opsiyoneldir.
- **Java Pool**: Java Virtual Machine (JVM) deki dataların yada Sessionlara ait Java kodlarının tutulduğu alandır.
- **Streams Pool**: Oracle Streams Tarafından kullanılır

## 2. Oracle Process Birimleri

- **User Process**: Bir kullanıcı SQL\*PLUS gibi bir uygulama kullanarak oracle database ‘e bağlandığında Oracle Database Bu kullanıcının uygulamalarını çalıştırabilmesi için bir process oluşturur
- **Database Processler**: Oracle database tarafından oluşturulan processlerdir.
- **Database Writer Process (DBW)**: Daha önce bahsettiğimiz memory bölümü olan Database Buffer Cache içeriğini diske yazan process dir.
- **Log Writer Process (LGWR)**: Redolog Buffer daki verileri redolog file’ lara yazan processdir.
- **Checkpoint Process (CKPT)**: Chechkpoint bir tur system değiştirme numaraları saklayan data birimleridir.
- **System Monitor Process (SMON)**: Database in tutarsız bir şekilde kapanmasında recovery yapmak içindir.
- **Process Monitor Process (PMON)**: Bir kullanıcı process’ i fail olduğunda process recovery işlemini PMON yapar.
- **Recoverer Process (RECO)**: Dağınık database configurasyonları ile birlikte kullanılır.
- **Archiver Process (ARCn)**:  Redolog dosyalarını yedekler.ARCn processinin çalışması için database ARCHIVELOG MODE da olmalı ve Automaticarchiving enable olmalıdır.

## 3. Oracle Database Depolama Birimleri

**Control Files**: Database ile ilgili bilgilerin, control datalarının tutulduğu dosyalardır. 
**Data Files**: Kullanıcı ve uygulamalara ait dataların tutulduğu dosyalardır.
**Online RedoLog Files**: İnstance recovery dosyalarının tutulduğu filelerdir.
**Parameter File**: İnstance configurasyon bilgilerinin tutulduğu dosyadır.
**Password File**: Remote olarak db ye bağlanıp yönetimsel taskların gerçekleştirilmesine izin verir.
**Backup Files**:Database Recovery için kullanılır.
**Archived Redo Log Files**:Historik olarak data değişim bilgilerini tutar.Bu dosyalar ile birlikte backup dosyaları kullanılarak kayıp datalar recover edilebilir.
**Trace and Alert Files**: Her bir server ve background processlerin kayıtlarının tutulduğu, hataların yazıldığı dosyalardır. Bu dosyalardan faydalanılarak processler izlenebilir, sessionlar monitor edilebilir.

# İşlem Hataları

- İşlem başarısızlıkları durumunda, MS SQL Server bu işlem için gerçekleştirilen tüm işlemleri tersine çevirmek zorundadır.
- Bunun nedeni, kayıtları engelleyerek değişiklikleri zaten yapmış olmasıdır.
- Oracle ile bu değişiklik yapılmasına gerek yoktur, çünkü tüm değişiklikler orijinal kayıtlarda değil, bir kopyada yapılmıştır.

# Eşzamanlı Erişim ve Bekleme Süresi

- Yazma işlemi devam ederken, MS SQL Server'da hiçbir okuma izni yoktur ve bu okumak için bile uzun bir bekleme süresine neden olur .
- Yazım süreci Oracle'da devam ederken, kullanıcıların eski kopyayı güncellemeden hemen önce okumasına izin veriyor. Bu nedenle, Oracle'da daha kısa bekleme süresi var, ancak yazmanıza izin verilmiyor.

# Platform Desteği

- MS SQL Server yalnızca bir Windows platformunda çalıştırılabilir. Platform desteğinin eksikliği nedeniyle, farklı işletim sistemleri ile dünya çapında çalışan işletmeler için en uygun değildir.
- Oracle, UNIX, Windows, MVS ve VAX-VMS gibi çeşitli platformlarda çalıştırılabilir. İyi bir platform desteği sunar ve dolayısıyla farklı işletim sistemleri kullanan işletmelerde kullanılabilir.

# Sıralama, Önbelleğe Alma vb. İçin Bellek Ayırma

- MS SQL Server global bir bellek ayırma işlemini izler ve bu nedenle sıralama veya daha iyi performans için önbelleğe alma işlemi sırasında DBA tarafından değiştirilemez. Bu şekilde insan hatalarından kaçınılabilir.
- Oracle, performansı artıran dinamik bir bellek ayırma kullanıyor ancak performansını artırmak için DB'ye girdiğinizde insan hataları olasılığı yüksek.

# Tablo Bölme

- MS SQL Server, büyük tabloların daha fazla bölünmesine izin vermez, bu da verileri yönetmeyi zorlaştırır. Bununla birlikte, basitlik söz konusu olduğunda MS SQL Server ilk sırayı alıyor.
- Oracle, büyük tabloların bölümlerine izin verilerek daha kolay veri yönetimine yardımcı olur.

# Harici dosyaları bağlama

- MS SQL Server, harici dosyaları okumak veya yazmak için bağlantılı sunucuları kullanır; Oracle aynı şeyi yapmak için Java kullanıyor.
- Her ikisi de bu dosyaları birbirine bağlama seçeneğine sahiptir ve bu nedenle yalnızca yaklaşımlarının farklı olduğunu söyleyebiliriz.

# Arayüz

- Basit ve kullanıcı dostu arayüz gerçekten MS SQL Server ile ilişkili mükemmel bir özelliktir. Otomatik olarak istatistiksel veriler ve kendi kendine ayarlar tek başına oluşturur. Ayrıca, herkes büyük miktarda kaynak bulunduğundan MS SQL Server'ı kolayca öğrenebilir.
- Oracle kullanıcı arayüzü önceki ile aynı seviyede ancak işlemek ve öğrenmek biraz karmaşıktır.

# Sonuç: En İyi Kullanım

- MS SQL Server'ı Oracle ile karşılaştırdığımızda, eski SQL'in küçük veritabanları için en uygun olduğunu söyleyebiliriz. İşlemlerini beklemek için zamanınız varsa, daha büyük boyutlu veritabanları için sıkıcı zaman alan işlemler gerektirdiğinden ,dağıtmak en basit olanıdır.
- Aksi takdirde, Oracle ile birlikte devam edin çünkü kolaylıkla daha büyük bir veritabanını destekliyor.

# Popüler Açık Kaynak Kod Veri Tabanı Sistemleri

- **MySQL**
- **SQLite**
- **PostgreSQL**
- **Cubrid**
- **Firebird**

# MYSQL

- Kelime anlamı olarak incelendiği zaman MySQL, Structured Query Language (Yapılandırılmış Sorgulama Dili) SQL teknolojisini kullanan açık kaynak bir web yazılımıdır.
- Açık kaynak olarak geliştirilmesi nedeniyle hosting firmaları tarafından çok yüksek oranlarda kullanıma sahiptir.
- Güçlü bir veri tabanı yönetim sistemi olan MySQL, veri tabanı gerektiren hemen hemen her ortamda rahatlıkla kullanılabilir.
- Ama özellikle web sunucularında en çok kullanılan veri tabanıdır.

## MySQL Hangi Veri Tabanı Nesnelerini Desteklemektedir

- Tables (Tablo)
- Views (Görüntü) (Görüntüleme)
- Procedures (Prosedür/Yordam)
- Triggers
- Cursors

# MySQL ve SQL Server Arasındaki Farklılıklar

- Belirttiğimiz üzere, SQL Server en iyi .NET ile çalışmaktadır. Diğer yandan MySQL ise hemen hemen diğer tüm dillerle çalışabilir ancak başlıca PHP ile kullanılır.
- Syntax
- Sahipli yazılımların, açık kaynak yazılımlara karşı başlıca avantajı özel destek alıyor olmalarıdır.
- SQL Server, MySQL’in sunduğu çoklu depolama motorlarına karşın, Microsoft tarafından geliştirilen tekli depolama motoru kullanıyor.
- MySQL ile SQL Server arasındaki ciddi bir diğer fark ise MySQL’in sorgu uygulaması esnasında iptal şansı vermemesidir.
- MySQL ile SQL Server arasındaki güvenlik farklılıklarını karşılaştırırken yüzeyde bakılacak çok fazla bir şey yok.
- SQL Server’in aksine MySQL burada biraz öne geçiyor. Microsoft ,SQL Server’da çoklu veritabanı çalıştırabilmek için lisans satın almanızı istiyor.

# SQLite

- SQLite, dünyada en çok dağıtılan ve geliştiricilere kullanması için tavsiye edilen ve tamamen açık kaynak kodlarına sahip,  C ve C++ programlama dilleriyle kodlanmış, sunucu yazılımı ve yapılandırma gereksinimi olmayan, işlemsel ve ilişkisel bir SQL veritabanı motorudur.

## SQLite Mimarisi

- **SQLite, çalışacak bir sunucu gerektirmez.**
- SQLite veritabanı, veritabanına erişen uygulama ile entegre edilmiştir. Uygulamalar SQLite veritabanı ile etkileşime girer ve doğrudan diskte saklanan veritabanı dosyalarından yazabilir.

## SQLite Veri Erişim Bileşenleri (LiteDAC) Özellikleri

- **SQLite Şifreleme** - Verilerinizi yetkisiz erişime karşı korumak için, LiteDAC güçlü ve özelleştirilebilir bir SQLite Veritabanı Şifreleme motoru sağlar.
- **SQLite Özelliklerinin Geniş Kapsamı** - LiteDAC, en gelişmiş veritabanı işlevselliğine erişim sağlayarak, geliştiricilerin SQLite'nin tüm özelliklerini kullanmasına ve veritabanı uygulamalarını optimize etmesine olanak tanır.
- **Mobil Geliştirme** - LiteDAC kullanarak iOS ve Android mobil cihazlara yönelik Develompent, LiteDAC'ın mobil uygulamalarınızın masaüstü uygulamalarının yaptığı gibi SQLite veritabanıyla çalışmasına izin verdiği için daha da kolay hale geliyor.
- **Performans**- Tüm bileşenler ve kütüphaneler, yüksek performanslı, hafif veri erişim katmanları yazmanıza yardımcı olacak şekilde tasarlanmıştır, bu nedenle gelişmiş veri erişim algoritmaları ve optimizasyon teknikleri kullanırlar.

# PostgreSQL

- PostgreSQL, 15 yıldan fazla aktif gelişme ile Linux, UNIX (AIX, BSD, HP-UX, SGI IRIX, Mac OS X, Solaris, Tru64) ve Windows dahil olmak üzere tüm önemli işletim sistemlerinde çalışan bir diğer mükemmel açık kaynak seçeneğidir. PostgreSQL ayrıca tamamen ACID (Atomiklik,Tutarlılık, Isolasyon, Dayanıklılık) uyumludur.

## Artıları

- Özel veri türleri ve sorgulama yöntemleri oluşturun
- Çerçeve, kendi özel veri tiplerinin tanımını ve oluşturulmasını sağlar
- Saklanan prosedürleri, bir düzineden fazla programlama dilinde çalıştırır:
- Java, Perl, Python, Ruby, Tcl, C / C ++ ve kendi PL / pgSQL
- GiST (Genelleştirilmiş Arama Ağacı) sistemi
- Farklı sıralama ve arama algoritmalarını bir araya getirir:
- B-ağacı, B + -tree, R-ağacı, kısmi toplam ağaçlar ve sıralı B + -trees
- Postgres kodunu değiştirmeden daha fazla paralellik için CitusDB gibi uzantıların oluşturulması

# Eksiler

- MVCC sistemi düzenli "vakumlama" gerektirir
- Yüksek işlem oranı ortamlarında sorunlar
- Gelişim geniş topluluk tarafından yapılır
- İyileştirmeler için adil çabalar eklendi

# CUBRID

- CUBRID, karmaşık web hizmetleri büyük miktarlarda veri işlerken ve büyük eş zamanlı talepler üretirken yararlı olan, özellikle web uygulamaları için optimize edilmiş mükemmel bir ücretsiz ve açık kaynak seçeneğidir.

## Artılar

- Çoklu parçalı kilitleme
- Çevrimiçi yedekleme
- Geliştirme dilleri için GUI araçları ve sürücüleri:
- JDBC, PHP, Python, Perl ve Ruby.
- 7/24 çevrimiçi web servisi ile otomatik yerine çalışma özelliği
- Yatay / dikey ölçeklenebilirlik için doğal DB shard'ını destekler
- Büyük sistemler, verileri birden fazla veritabanı örneğine böler
- Veritabanı çoğaltma ve işlem tutarlılığı

## Eksiler

- Apple sistemleri ile çalışmaz
- Komut dosyası hata ayıklayıcı yok
- Kılavuz yalnızca İngilizce veya Korece gelir
- Forumlarındaki tartışmalar tarihlenebilir

# Firebird

- Bu ilişkisel veritabanı, 1981'den beri üretim sistemlerinde (çeşitli isimler altında) kullanılmıştır ve birçok ANSI SQL standardına sahiptir. Firebird Linux, Windows ve çeşitli Unix platformlarında çalışabiliyor.

## Artılar

- Gerçek zamanlı izleme için İzleme API'sı
- Windows güvenilir kimlik doğrulaması
- Dört desteklenen mimariler:
- SuperClassic, Klasik, SuperServer ve Gömülü
- Geliştirme araçlarının çeşitliliği:
- Ticari araçlar: FIBPlus ve IBObjects
- Veritabanını temizlemek için otomatik süpürme seçeneği
- Veri tabanı tetikleyicilerinden ve saklı yordamlardan olay bildirimleri
- Firebird’in büyük küresel topluluğu aracılığıyla ücretsiz destek

## Eksiler

- Entegre çoğaltma desteği dahil değildir (yalnızca eklenti olarak)
- Geçici tablolar ve diğer veritabanı sistemleriyle entegrasyon eksikliği
- Diğer OS çözümlerine kıyasla Windows-güvenilir kimlik doğrulaması yok

# <center>Bulut Bilişim (Cloud Computing)</center>

- Bulut bilişim teknolojisinin gelişmesi sayesinde, büyük verilerin internet üzerinde depolanabilirliği ve bu verilerin erişilebilirliği olanaklı hale gelmiştir.

- Bulut bilişim fikrinin temelleri 1950’li yıllarda atılmıştır. İnternet devlerinden olan **Amazon**, veri merkezlerini modernize ederek bulut bilişimin gelişmesinde anahtar bir rol oynayarak ilk gerçek bulut bilişim hizmeti olan Amazon S3’ün 2006 yılında hizmete girmesini sağladı.

- Günümüz teknolojisindeki mevcut cihazlarda kullanıcılar her geçen gün daha fazla kişisel veri (data) saklamak istediği için barındırma kapasitesi büyük sorunlara sebep olmaktadır.

- En düşük kapasiteli cihazla bile istenilen yerden istenildiği zaman her tür bilgiye, kişisel veriye ulaşmayı sağlıyor.

# Bulut Bilişim hizmet modelleri

- SaaS (Software as a Service); Yazılımı servis olarak sunma,
- PaaS (Platform as a Service); Platform hizmeti  ve
- IaaS (Infrastructure as a Service); Sunucu altyapı hizmeti.

<center><image src="./image/cchizmetmodeli.png" width="400" height="300"/></center>

<center><image src="./image/cchizmetmodeli2.png" width="400" height="300"/></center>

<center><image src="./image/cchizmetyapısı.png" /></center>

## Hizmet olarak yazılım (Software as a Service -SaaS)

- Hizmet olarak yazılım, yazılım uygulamalarını internet üzerinden isteğe bağlı olarak ve genellikle bir abonelik aracılığıyla dağıtma yöntemidir.
- **SaaS sayesinde bulut sağlayıcıları, yazılım uygulamalarını ve temel altyapıyı barındırıp yönetmenin yanı sıra yazılım yükseltmeleri ve güvenlik düzeltme eki uygulama gibi bakım işlerini de üstlenir.**

## Hizmet olarak platform (Platform as a Service -PaaS)

- Hizmet olarak platform, yazılım uygulamaları geliştirmek, test etmek, teslim etmek ve yönetmek üzere isteğe bağlı bir ortam sağlayan bulut bilgi işlem hizmetleri olarak tanımlanır.
- PaaS, geliştiricilerin web uygulamalarını veya mobil uygulamaları, geliştirme için gereken sunucular, depolama alanı, ağ ve veritabanlarından oluşan temel altyapıyı kurma ve yönetme endişesi taşımadan hızla oluşturmasını kolaylaştırmak üzere tasarlanmıştır.

## Hizmet Olarak Altyapı (Infrastructure as a Service -IaaS)

- Bulut bilgi işlem hizmetlerinin en temel kategorisidir. IaaS, bir bulut sağlayıcısından kullandıkça öde esasına dayalı olarak **BT altyapısı (sunucular ve sanal makineler (VM), depolama, ağ, işletim sistemleri) kiralamanıza olanak tanır.**

# Bulut Bilişim’ in Geliştirme Modelleri

- 4 ayrı çeşidi ile karşımıza çıkan bu teknoloji  farklı alanlarda,farklı biçimlerde kullanılmaya olanak sağlıyor.

<center><image src="./image/ccgelistirmemodeli.png" width="300" height="300"/></center>

<center><image src="./image/ccgelistirmemodeli2.png" width="500" height="300"/></center>

## Public Cloud (Genel Bulut)

- İnternet üzerindeki sunucular ile kurulan bir bulut teknolojisi.
- Küçük ve orta ölçekli şirketlerde kullanacağınız **kullandığınız kadar ödeme** yapılan  bu modele örnek olarak, elektronik postalar gösterilebilir.

## Private Cloud (Özel Bulut)

- Bilgileri önemli olan büyük şirketlerin tercih ettiği bir bulut teknolojisidir.
- Tüm bilgiler kurucunun elinin altındadır ve erişim **güvenliği  ve gizliliği** yüksektir.

## Hybrid Cloud (Melez Bulut)

- Public ve Private Cloud’un birleşiminden ortaya çıkan bulut teknolojisidir.
- Şirketlerin hacmine göre birleşim oranlarında farklılıklar görülebiliyor.

## Community Cloud (Topluluk Bulut)

- Birkaç şirket ile ortak kullanılan hizmetleri barındıran bulut teknolojisidir.
- Topluluk üyeleri uygulama ve verilere erişebilmektedir.

# Bulut Teknolojisi’nin Getirdiği Avantajlar

- Bulut bilişim sistemleri **API’ler ile hızlı kullanım** kolaylığı sağlıyor.
- Daha fazla depolama alanı, hızlı veri transferi ve bu yedekleme üzerinde maliyet tasarrufu yapabilme gibi bir takım olanaklar sağlıyor.
- Sürekli olarak artan verilerin arşivlenmesi, kullanıcıların yetki ve takibi gibi konuların oluşturduğu **alt yapı karmaşası ortadan kalkıyor.**
- Bulut teknolojisi yazılımları web tarayıcıları üzerinden çalıştığından, bilgisayar, tablet, akıllı telefon ve  Smart TV'ler de kullanılarak platform bağımlılığından koruyor.
- Bulut yazılım hizmetini veren şirketlerin  verilerinin tutulduğu serverları 7/24 yazılım ve donanımsal olarak güvenlik tedbirlerini aldıklarından dolayı ana bilgisayardan daha güvenlidir.
- **Kısaca; bulut bilişim çok daha ucuza, kurulum gerektirmeden, her yerden çalışmayı desteklen bir hizmettir.**

# Bulut Teknolojisi’nin Dezavantajları

- Bulut teknolojisi servisi kullanarak veri saklanması, kullanıcının verilerini riske atması bilgi güvenliğini ve kullanıcı gizliliğini sağlayamamaktadır. Güvenlik açıkları oldukça fazladır.
- Ülkelerin ekonomik durumlarından dolayı dijital bölünmeyi arttıracak, bu da uluslararası, politik ve ekonomik sorunlar doğuracaktır.
- En önemli sorun ise depolanan verilere ulaşılabilmesi için **internet bağlantısının olması** gerekmektedir.
- Hizmetlerinin gelişmesiyle birlikte donanımsal ve yazılımsal bakım ve tamir maliyetlerinin azalacak olması ve buna bağlı olarak da bu işi yapan Bilgi Teknolojisi (BT) uzmanlarının iş sahalarının daralması durumu da son dezavantajlardan birisidir.

# Bulut Bilişim Mimari Yapısı

- Bulut bilişim mimari yapısı her biri birbiri ile çok sıkı bağlı (ilintili) olmayan birçok bulut bileşenlerinden oluşur.

## Bilişimin Klasik Alt Yapısı

- İşletmelerdeki klasik Bilgi Teknolojileri altyapısında kullanıcıların çalıştığı bilgisayarlar, yazıcılar gibi cihazlar ile uygulama, bilgi ve servislerin üzerinde durduğu sunucular, depolama üniteleri, yedekleme sistemleri mevcuttur. -
- Bu sistem odalarını altyapı olarak besleyen jeneratörler, UPS cihazları, iklimlendirme aygıtları, yangın söndürme ve güvenlik için kamera ve erişim cihazları gerekmektedir.
- Bu BT altyapısının çıkacak problemlere karşı desteklenmesi, güvenlik önlemlerinin firma tarafından alınması, çalışan sistemin kesintisiz çalışabilmesi için izlenmesi, oluşabilecek hatalara karşı önceden uyarı sistemlerinin kurulması ve sürekli olarak yeni tehditlerin önüne geçme ve yeni fonksiyonları kullandırabilme adına güncellenmesi gerekmektedir.
- Ayrıca sistemlerin yedeklenmesi konusunda tüm sistemler için farklı lokasyonlar da yedekleme sistemlerinin kurulması gerekmektedir. Bu sistemlerin kurulması maliyeti artıran önemli bir faktördür.

## Bulut Bilişimin BT altyapısı

Klasik BT altyapısından farklı olarak Bulut Bilişim aşağıdaki şekilde bir yapı sunmakta, bu yapı ile

<center><image src="./image/ccaltyapı.png" width="300" height="300"/></center>

- Yedekli, hızlı ve kesintisiz bir altyapıya,
- Düzgün bir veri merkezi ortamında çalışan BT altyapısına,
- Bu veri merkezi içinde konumlandırılmış:

  - Mail, Sunucu, Hat Güvenlik Ürünlerine,
  - Arşivleme ve Yedekleme Çözümlerine,
  - Elektrik, UPS, Soğutma Sistemlerine,
  - Sunucu ve uygulamalara ve
  - Network alt yapısına sahip olunabilmekte.

- Bulut bilişim ile klasik BT altyapısı maliyet açısından karşılaştırıldığında aşağıdaki gibi bir oranlama ortaya çıkmaktadır.
- Bulut Bilişim ile işletme sahibi kendisi için bir kambur olan sistem odası bulundurma işleminden kurtulur.

## Bulut Bilişim Mimari Yapısı

- Bir bulut bilişim sistemi genel olarak ön taraf ve arka taraf olmak üzere iki kategoride değerlendirilir.

<center><image src="./image/ccmimariyapısı.png" width="400" height="300"/></center>

- Ön taraf, istemcinin bilgisayarını (veya bilgisayar ağını) ve bulut bilişim sistemine erişim için gerekli olan uygulamayı içerir.
- Protokoller denilen bir takım kuralları izler ve middleware denilen (ara bir yazılım) özel bir yazılım kullanır.
- Eğer bir bulut bilişim şirketi birçok istemciye sahip ise, depolama alanı için yüksek bir talep olması muhtemeldir

<center><image src="./image/ccmimariyapısıbackend.png" width="600" height="300"/></center>

# Bulut Teknolojisi Hizmeti Veren Platformlar

- Dropbox http://dropbox.com
- Google Drive http://drive.google.com
- SkyDrive https://skydrive.live.com
- Cloud https://cloud.google.com
- Yandex Disk http://disk.yandex.com
- Turkcell Akıllı Bulut http://turkcellakillibulut.com
- TTNETBulut http://ttnetbulutu.com
- UbuntuOne https://one.ubuntu.com
- Box http://box.com
- OneDrive
- ownCloud
- Slax Drive
- Mobile Me
- Ttnet Netdisk
- Mega
- Microsoft Azure

# 2020 yılının en iyi 10 bulut servis sağlayıcısı

1. Amazon Web Service
2. Microsoft Azure
3. Google Cloud
4. Alibaba Cloud
5. IBM Cloud
6. Oracle
7. Salesforce
8. SAP
9. Rackspace Cloud
10. VMWare

# <center>Big Data</center>

- Büyük veri. diskte çok fazla yer kaplayan veri.
- Geleneksel yöntem araçlarla işlenemeyen veri.

# Veri

- Bir ham (işlenmemiş) gerçek ya da enformasyon parçacığına verilen addır.

## Veri tipleri

- Yapılandırılmış Veri
  - Fatura
  - Ödemeler
- Yapılandırılmamış Veri

  - Tweetler
  - Reklam tıklama verileri

- Günümüzde 90% oranında yapılandırılmamış veri bulunmaktadır
- Günümüzde 10% oranında yapılandırılmış veri bulunmaktadır

# Bilgi çöplüğü

- Veri tabanlarında saklanamamasından ötürü bu veriler işlenemez ve sınıflandırılamaz bir hal aldı.
- Big data ile işlenmesi çok zor olan bu veri büyük boyutlara ulaşınca bilgi çöplüğü denildi.

# BİG DATA ORTAYA ÇIKIŞI ve amacı

- Bu çöplükten anlamlı verilerin de çıkabileceğini düşünen yazılım şirketleri, AR-GE çalışmalarını bu anlamda yürüterek Big Data olarak isimlendirdiğimiz olguyu ortaya çıkarttılar.
- Bilgi çöplüğü denilen çok büyük boyutlardaki verileri anlamlı ve işlenebilir bir hale getirmek

# Big data hedefleri

- Maliyet tasarrufu
- Zaman tasarrufu
- Yeni teklifler geliştirmek
- İş kararlarını desteklemek

# Büyük veri ne işe yarar?

- Şirketler müşterilerin gereksinimlerimi karşılamak ve onlara doğru hizmet yapabilmek için big datayı kullanmak istediler.
- Herkesin internete kolayca girebiliyor olması sebebiyle kullanıcıların her türlü bilgilerinin alınıp saklanması ve gerekli alanlarda kullanılması.

# Büyük verinin sektöre katkıları

- **İşletme**: Müşteri kişiselleştirme, müşteri kaybı sebeplerini belirleme, dağıtım ve lojistik optimizasyonu.
- **Teknoloji**: İşlem süresini azaltma, gerçek zamanlı analiz, kriz dönemlerinde hızlı cevap üretme, riskleri azaltmak için otomatik sistemler ile karar verme.
- **Sağlık**: Hastalık tespiti, seyrinin takibi ve sağlığı güçlendirmek için kişisel DNA analizi yapma.
- **Kamu Sektörü**: Verilere erişilebilirlik sağlayarak şeffaflık oluşturma, uygun ürün ve hizmetler için eylemlerin uyarlanması.
- **Perakende Satış**: Mağaza davranış analizi, çeşitlilik ve fiyat optimizasyonu, ürün yerleştirme tasarımı, performansı geliştirme, işçi geliri optimizasyonu.
- **Kişisel Konum Verileri**: Akıllı yönlendirme, coğrafi hedefli reklamcılık, acil müdahale.
- **Akıllı Şehirler**: Doğal kaynakların yönetilerek, sürdürülebilir ekonomik gelişmenin ve yüksek kaliteli yaşamın sağlanması.

# Big data aşamaları

- **Keşif**: elinizdeki verilerin tanımlanması, içeriğinin belirlenmesi, size ne gibi faydalar sağlayabileceği.
- **Üretim**: uygulamaları ölçeklendirerek üretim süreçlerine dahil etmek.

# Big data bileşenleri (3V to 5V)

- **Variety (çeşitlilik)**: Üretilen verinin yüzde 80’i yapısal değil ve her yeni üretilen teknoloji, farklı formatlarda veri üretebiliyor. Telefonlardan, tabletlerden, bütünleşik devrelerden gelen türlü çeşitlilikte veri tipi ile uğraşılması gerekiyor.
- **Velocity (hız)**: Büyük Veri’nin üretilme hızı çok yüksek ve gittikçe artıyor.
  Geometrik olarak büyüyen veri miktarına karşılık, işlenebilirliği arttırmak için hem donanımsal hem de yazılımsal olarak belli bir altyapıya ve hıza sahip olmak gerekiyor.
- **volume (veri büyüklüğü)**: IDC(international data corporation) istatistiklerine göre 2020’de ulaşılacak veri miktarı, 2009’un 44 katı olacak. Toplam bilişim harcamalarına karşın, çok büyük bir hızla veri artışı vardır.
- **Verification (doğrulama)/ veracity (gerçeklik)**: Oluşan bu bilgi yoğunluğu içerisinde verinin ‘güvenli’ olması son derece önemlidir.
- **Value (değer)**: büyük verinin değer yaratması en önemli bileşenlerinden biridir. Büyük verinin bütün bileşenleri ile birlikte veri üretim ve işleme işlemlerinden sonra kurum için değeri çok önemlidir.

# Big datanın yapılandırılması

- Elde ettiğimiz veriler yapısal değil, yani yapılandırılmak için bizi bekliyor. Bizim o veriyi en derinlere kadar inerek anlamlı bir şekilde yeryüzüne çıkarmamız ve bunun için de klasik yöntemlerden biraz daha farklı çözümler gerekiyor.

# VERİ DEPOLAMA

- Veri ve dosya depolama, bugün teknolojiye erişimi olan herkes için temel bir gereksinim.

# Bulut teknolojisi amacı

- Verileri bilgisayar, telefon, tablet gibi cihazlar yerine online bir platformda saklamak.
- Cihaz bozulduğunda kaybolan veriler.
- Cihazda depolama alanı sıkıntısı.
- Verilere kolay ve hızlı ulaşım.
- Veri güvenliği.

# Bulut bilişim faydaları

- Maliyetleri düşürür.
- Altyapı karmaşasını ortadan kaldırır.
- Çalışma alanını genişletir.
- Verileri korur.
- İstenilen zamanda bilgiye ulaşma imkanı verir.

# Big data ve bulut bilişim

- Son yıllarda verilerin, boyut, çeşitlilik ve karmaşıklık anlamında sürekli büyümesi ve büyümeye devam edecek olması, büyük veri konusunu bir sorun olmaktan çıkarıp bulut bilişimle birlikte bir çözüm odağı haline gelmesi sağlanmıştır.

# VTYS-BİG DATA VE BULUT İLİŞKİSİ

- Bulut Veritabanı kullanım şekillerinin artma gereksinimi bu alanda teknoloji ilerlemelerini sağlamaktadır.
- Bulut Veritabanı başlangıçta, müşteriye sadece veriyi okuma olanağı sağlamıştır.
- Ancak, müşterilerin taleplepleri üzerine,yazma sorgusu da yer aldı.
- Bu işlemler Web 2.0 teknolojisinin getirilmesi ile mümkün olmuştur.
- Bulut Veritabanında okuma isteklerinin sayısı hala yazma isteğin daha fazla olduğu görülmektedir.
- Ancak yakın zamanda okuma sayısıda Bulut Veritabanında artacaktır.
- Bu eğilim okuma ve yazma istekleri arasındaki boşlukları daralmaya başlamıştır.
- Büyük veri yönetimi sağlayan big data, verileri sanal bir sunucuda tutmamıza yarayan bulut bilişim ve verilerin dijital ortamda saklanmasını sağlayan veri tabanı birbirini destekleyen ve birbirinin önünü açan 3 teknolojidir.

# Nesnelerin interneti (Internet of things)

- Nesnelerin interneti, fiziksel nesnelerin birbirleriyle veya daha büyük sistemlerle bağlantılı olduğu iletişim ağıdır.
- Amerikan Federal Ticaret Komisyonu nesnelerin internetini "günlük kullanımımızda olan nesnelerin internete bağlanıp veri gönderip alması kabiliyeti" olarak tanımlamıştır

## NESNELERİN İNTERNETİNDE KONTROL EDİLECEK FAKTÖRLER

- Kişisel verilerin toplanmasını minimize etmek.

# Internet of things ve big data

- Nesnelerin interneti uygulamaları, sensörlerin tek tek erişilebilir olmasından başka, pek çok sensörün verisinin birleştirilerek değer üretilmesi amacıyla da kullanılmaktadır.
- Fiziksel ortamlardan akarak gelen yüksek miktardaki sensör verilerinin (data), yapılan değerlendirmelerin ardından bilgi (information) olarak operatörlere veya ilgili kişilere iletilmesi ya da verinin sistemler yardımıyla işlenerek bir faaliyet icra edilmesi sağlanmaktadır.

# HADOOP

- Hadoop, sıradan sunuculardan oluşan küme (cluster ) üzerinde büyük verileri işlemek amaçlı uygulamaları çalıştıran ve HDFS olarak adlandırılan bir dağıtık dosya sistemi ile Hadoop MapReduce özelliklerini bir getiren, Java ile geliştirilmiş açık kaynaklı bir kütüphanedir

## HDFS

- Hadoop içerisinde büyük verileri sakladığımız bileşene HDFS (Hadoop Distributed File System)denir.
- Büyük verileri HDFS sistemine yüklediğimiz zaman  , Hadoop bu verileri bloklara ayırır .
- Farklı bloklara ayrılan veriler Hadoop Cluster üzerinde farklı node lara dağılır
- Burada dikkat etmemiz gereken en önemli hususlardan bir tanesi her bir blok çoklanarak kaydedilmiştir

<center><image src="./image/hdfs.png" width="500" height="200"/></center>

- HDFS, NameNode ve DataNode süreçlerinden oluşmaktadır.
  - **NameNode**:
    - Ana süreç olarak blokların sunucular üzerindeki dağılımından, oluşturulmasından, silinmesinden, bir blokta sorun meydana geldiğinde yeniden oluşturulmasından ve her türlü dosya erişiminden sorumludur.
    - Kısacası HDFS üzerindeki tüm dosyalar hakkındaki bilgiler NameNode tarafından saklanır ve yönetilir.
    - **Her kümede yalnızca bir adet NameNode olabilir.**
  - **DataNode**:
    - DataNode ise işlevi blokları saklamak olan işçi süreçtir
    - Her DataNode **kendi yerel diskindeki veriden** sorumludur. Ayrıca diğer DataNode’lardaki verilerin yedeklerini de barındırır. DataNode’lar küme içerisinde birden fazla olabilir

# MAPREDUCE

- MapReduce HDFS üzerindeki büyük dosyaları verileri işleyebilmek amacıyla kullanılan bir yöntemdir.
- Dağıtık mimari üzerinde büyük boyutlu verinin hızlı biçimde analiz edilmesini sağlar.
- Fonksiyonel programlamadaki map ve reduce fonksiyonlarından esinlenerek geliştirilmiştir.
- MapReduce görevlerinde veri, bu iki fonksiyon tarafından işlenir.

<center><image src="./image/mapreduce.png"/></center>

- Map aşamasında, Hadoop sabit boyutlu parçalar halinde bir MapReduce taskı için veriyi küçük parçalara böler.
- Bu bölünmüş veriler splits/input splits olarak adlandırılır.
- Hadoop her split için bir map task oluşturur ve kullanıcı tanımlı map fonksiyonunu çalıştırır. Bu sayede bütün girdiyi işlemeye kıyasla, bölünmüş parçaları işlemek daha az zaman alır.
- Bu mimaride büyük miktardaki veri, kümede yer alan düğümler tarafından hızlı bir şekilde okunabilir ve aynı zamanda, kümede ne kadar çok düğüm varsa veri işleme hızı da o nispette artar.
- Map taskları çıktıyı HDFS’e değil local diske yazarlar çünkü map tasklarının oluşturduğu çıktı nihai değil ara çıktıdır.
- Reduce aşamasında, depolanmış ara çıktı, kullanıcı tanımlı reduce fonksiyonuna geçirilmek üzere birleştirilmek için ağ üzerinden reduce görevinin koştuğu düğüme aktarılır.
- Böylece nihai çıktı reduce taskları tarafından oluşturulur.
- Map-Reduce dağıtık mimari bazlı bir model olduğundan, map ve reduce görevlerinin diğerleriyle bir bağımlılığı yoktur, süreçler birbirinden bağımsız işlemektedir.
- Örnek olarak bir text dosyasının içerisindeki kelime sayısını bulan MapReduce programını inceleyelim . MapReduce şu adımlardan oluşacaktır

<center><image src="./image/mapreduceornek.png"/></center>

- **Spliting** : Veriler genellikle 64 veya 128 MB lık bloklara ayrılır .
  Mapping : Burada her bir kelime key(word) ve value(1) şeklinde bölümlere ayrılır
- **Shuffling** : Map işleminden çıkan sonuçları Reducer a yönlendirir . Amacımız word-count uygulaması oldugu için aynı kelime grubu aynı Reducer a yönlendirilir
- **Reducing** : Gelen sonuçlar üzerinden toplama işlemi yapılır ve sonuçlar istediğiniz kaynaklara yazılır
- **JobTracker**:
  - Yazılan MapReduce programının küme üzerinde dağıtılarak çalıştırılmasından sorumludur.
  - Ayrıca dağıtılan iş parçacıklarının çalışması sırasında oluşabilecek herhangi bir problemde o iş parçacığının sonlandırılması ya da yeniden başlatılması da JobTracker’ın sorumluluğundadır.
- **TaskTracker**:
  - DataNode’ların bulunduğu sunucularda çalışır ve JobTracker’dan tamamlanmak üzere iş parçacığı talep ede
  - JobTracker, NameNode’un yardımıyla DataNode’un lokal diskindeki veriye göre en uygun Map işini TaskTracker’a verir.

<center><image src="./image/hadoop.png"/></center>

<center><image src="./image/hadoop2.png"/></center>

## Avantajları

- **Çok büyük miktarda veriyi hızlıca saklama ve işleme yeteneği**. Veri hacmi ve çeşitliliği, özellikle sosyal medyadan ve Nesnelerin İnterneti'nden (IoT) sürekli olarak artmaktadır.
- **İşlem gücü**. Hadoop'un dağıtılmış bilgi işlem modeli, büyük verileri hızlı bir şekilde işler. Ne kadar çok hesaplama düğümü kullanırsanız, o kadar çok işlem gücünüz olur.
- **Hata toleransı**. Veri ve uygulama işleme donanım arızasına karşı korunur. Bir düğüm kapanırsa, dağıtılmış bilgisayarın başarısız olmadığından emin olmak için işler otomatik olarak diğer düğümlere yönlendirilir. Tüm verilerin birden fazla kopyası otomatik olarak saklanır.
- **Esneklik**. Geleneksel ilişkisel veritabanlarının aksine, saklamadan önce verileri önceden işlemek zorunda değilsiniz. İstediğiniz kadar veri depolayabilir ve daha sonra nasıl kullanacağınıza karar verebilirsiniz. Bu, metin, resim ve videolar gibi yapılandırılmamış verileri içerir.
- **Düşük maliyetli**. Açık kaynaklı çerçeve ücretsizdir ve büyük miktarda veriyi saklamak için emtia donanımını kullanır.
- **Ölçeklenebilirlik**. Yalnızca düğüm ekleyerek daha fazla veri işlemek için sisteminizi kolayca büyütebilirsiniz.
- **MapReduce programlama, tüm problemler için uygun değildir**
- **Tam teşekküllü veri yönetimi ve yönetişimi**. Hadoop'un veri yönetimi , veri temizleme, yönetişim ve meta veriler için kullanımı kolay, tam özellikli araçları yoktur.Özellikle veri eksikliği, veri kalitesi ve standardizasyon araçlarıdır.
- **Veri güvenliği**. Yeni araçlar ve teknolojiler ortaya çıksa da, bir başka zorluk da parçalanmış veri güvenliği sorunları etrafında yoğunlaşıyor.

# AMAZON WEB SERVİCES

- Amazon Web Servisleri (AWS), 2006 yılında kurulmuş olup,şirketlerin işlerini ölçeklendirmesi , büyütmesine yardımcı olan ; işlem gücü , veritabanı depolaması , içerik ulaştırma ve diğer fonksiyonel servisler sunan, 1 milyondan fazla müşterisi olan ve  Microsoft Azure ve Google Cloud Platform gibi IaaS, SaaS, PaaS and FaaS pazarında büyük rolü bir servis sağlayıcısıdır. Amazon, aralarında Shazam,Sportify ,Airbnb,Yelp,Ubisoft ,WIX’in yer aldığı ünlü teknolojilere hayat vermektedir.

- En fazla işlevsellik
- Müşteri ve çözüm ortaklarından oluşan en büyük topluluk
- En güvenli
- En hızlı inovasyon
- Kendini kanıtlamış operasyonel uzmanlık

# AMAZON WEB SERVİCES TARAFINDAN SUNULAN SERVİSLER NELERDİR?

- **İşleme ve yürütme (EC2)**: İşleme ve yürütme ihtiyacı için sanal sunucular sunar.Sunucuyu dinamik olarak ölçeklendirip ,performansı ve sunucu sağlığını korur.
- **Depolama (S3)**: Veri yedeklemesi , arşivleme ve analiz için ölçeklenebilir oranda depolama çözümlerini sunar.
- **Veritabanı ve veritabanı yönetimi** : Oracle,SQL Server,PostgreSQL ,MySQL,MariaDB ve Amazon Aurora gibi veritabanı yönetim seçeneklerini sunar.
- **Hibrit bulut**: Hibrit bulut teknoloji sayesinde kullanıcılar uygulamaları , veritabanları , sunucular ve verilerini herkese açık bulut sunuculara kolayca taşıyabilirler.
- **Ağ**: Çeşitli yük dengeleme araçlarını kullanarak ağ trafiğini sürekli kontrol altında tutabilirler.
- **Güvenlik ve yönetim**: AWS bulut sunucuların güvenliğini sağlamak adına kapsamlı araçlar sunuyor.Bu araçlarla adminler kullanıcıları ve kaynaklarını yönetebilme şansına sahipler.
- **Big Data yönetimi ve analiz**: Big Data’sını yönetmek isteyen şirket ve girişimler içinde amazon web servislerinin çeşitli çözümlerini sunar
- **Yapay Zeka**: AWS , AI gelişimi adına önemli teknoloji servisleri ile çözüm sunar.Makine öğrenimi teknolojisinden faydalanalarak kompleks algoritmalarını hayata geçirebilirler.
- **Mobil Geliştirme**: Mobil uygulama geliştiricileri , Amazon’u kullanarak kullanıcıların uygulamalarına erişmelerine yardımcı olabilir ve bildirimlerden haberdar olmasını sağlayabilirler

# AZURE

- Microsoft Azure hem açık çevre ortamlarından hem de internetten tüketilebilen çok çeşitli internet hizmetini sağlamakta olan bir bulut platformu hizmetidir.
- Microsoft online servis hizmetinin lansmanından sonra gelen bulut bilgi işlemi içine alan microsoftun ilk adımıdır.
- Bulut platformu web sunucularını barındırma,e-mail sunucusu oluşturma,veritabanı sunucusu, dosya depolama sunucusu,sanal makineler, kullanıcı dizinleri,web uygulamaları, mobil uygulamalar veya istenilen herhangi farklı servisler olarak hizmet edebilirler.

# AZURENİN SUNDUĞU ÇÖZÜMLER

- Tek bir mobil uygulama derlemesiyle farklı cihazlar kullanan tüm müşterilere ulaşılmasını sağlar
- Kişiselleştirilmiş,ölçeklenebilir ve güvenli bir alışveriş deneyimiyle müşterilere istediklerini sunar.
- Verileri ve kodları bulutta kullanımdayken korunmasını sağlar.
- Tüm geliştiriciler ve senaryolar için yapay zeka üretkenliğine sahiptir.
- Tüm platform uygulama oluşturma ve test etme sürecini basitleştirir ve hızlandırır.
- En önemlisi pahalıya mal olan iş kesintilerini önlemek için veri ve uygulamaları nerede depolandıklarından bağımsız olarak korur ve ihtiyacımız olan tüm verileri gerçek zamanlı olarak inceleyip mümkün olan en bilinçli kararları alır.
- Dağıtılmış kayıt defterlerinin kişilik gizliliğini , güvenliğini ve denetimini geliştirmek için nasıl kullanıldığını gösterir.
- Uygulamaların Azure’da veya Azure Stack’te çalıştırılacak olmasından bağımsız olarak geliştiricilerin aynı geliştirme ve dağıtıma yönetimini kullanılmasına olanak tanıyarak üretkenliği en üst düzeye çıkarır.

# GOOGLE CLOUD PLATFORM

- Google Cloud Platform, Google'ın son derece ölçeklenebilir ve güvenilir altyapısını kullanarak uygulamalar oluşturmanıza, test etmenize ve dağıtmanıza olanak tanır.

# GOOGLE CLOUD PLATFORM NE İŞE YARAR?

- Cloud Platform, web, mobil ve arka uç çözümleriniz için bilgi işlem, depolama ve uygulama hizmetleri sunar. Google Cloud Platform ile, yüksek seviyede çalışma süreleri ve optimize edilmiş yerel ağ performansı sunmayı amaçlayan dünya çapında bir yönetilen hizmet ağından faydalanılır. Kullanıcı tabanınız büyüdükçe Google Cloud Platform bu büyümenin yönetilmesini sağlar.

# TEMEL ÖZELLİKLER

- **Google'ın altyapısını kullanın**. Google'ın milisaniyeler içinde milyarlarca arama sonucu getirmesini sağlayan, ayda altı milyar saatlik YouTube videosu sunan, 425 milyon Gmail kullanıcısına depolama alanı sağlayan altyapısını kullanarak uygulamanızı oluşturun.
- **Ürününüze odaklanın**. Sistem yönetimi konusunda endişelenmeden uygulamanızı hızlıca geliştirin, dağıtın ve yineleyin. Google, uygulamanızı, veri tabanınızı ve depolama sunucularınızı yöneterek sizi bunlarla uğraşma zahmetinden kurtarır.
- **İhtiyacınız olan hizmetleri kullanın**. Google Cloud Platform, sanal makineler, yönetilen bir platform, blob depolama, blok halinde depolama, NoSQL veri tabanı, MySQL veri tabanı ve büyük veri analizi gibi uygulama mimarinizin ihtiyacı olan tüm hizmetleri sunar.
- **Milyonlarca kullanıcıya göre ölçekleyin**. Cloud Platform'da barındırılan uygulamalar, internet ölçeğindeki en zorlu iş yüklerinin üstesinden gelmek için otomatik olarak ölçek büyütebilir ve trafik hafiflediğinde ölçek küçültebilir. Yalnızca kullandığınız hizmetler için para ödersiniz.
- **Performansa güvenin**. Her milisaniyelik gecikme önemlidir. Google’ın bilgisayar altyapısı size tutarlı CPU, bellek ve disk performansı sunar. Ağımız ve kenar önbellek sunucularımız dünyanın her yerindeki kullanıcılarınıza hızlıca yanıt verir.
- **İhtiyacınız olan desteği alın**. Google, dünya çapındaki kullanıcı topluluğumuz, iş ortağı ekosistemimiz ve premium destek paketlerimizle, başlangıç ve büyüme aşamalarında size yardımcı olacak eksiksiz bir kaynak yelpazesi sunar.

# Google Cloud Platform Servisleri

<center><image src="./image/gcpservis.png"/></center>

# Storage (Depolama) Servisleri

- **Cloud SQL**, MySQL tabanlı bulutta çalışan SQL veritabanı depolama servisidir.
- **Cloud Datastore** veya **Cloud Bigtable**, SQL tabanlı olmayan (NoSQL) veritabanı depolama servisidir.
- **Cloud Storage tutarlı (consistent)**, ölçeklenebilir (scalable), büyük boyutlu dosya depolama için kullanılabilir. Bu depolamada da  üç seçenek bulunmaktadır.
- **GCE için kalıcı diskler (Persistent disks on Compute Engine)**  birincil öncelikli veri depolama alanı sunmaktadır. Eski tip mekanik Hard-Disk Tabanlı  ve Solid-State Persistent Disks (SSD) çeşitleri mevcuttur.

# Networking (Ağ ve İletişim) Servisleri

- **App Engine**; network altyapısını bizim yerimize yönetirken
- **Container Engine**; bu iş için Kubernetes modelini kullanırken
- **Compute Engine**; kullanmamız için bir dizi networking servisini bizlere sunmaktadır.
- Google Virtual Private Cloud (VPC)
- Google Cloud Load Balancing
- Content Delivery Network
- Google Cloud Interconnect
- Google Cloud DNS

# Big Data servisleri (Büyük Veri ) Servisleri

- Big Data servisleri elinizdeki mevcut büyük veriyi Google’ın bulut platformunda işleyerek ve sorgulayarak karmaşık sorularınıza hızlı cevaplar almanızı sağlar.
- **Google BigQuery**: Veri Analizi hizmeti sunmaktadır
- **Google Cloud Dataflow**: Yığın ve akışkan verileri işlemek için yönetilebilen servis ve SDK (Software Development Kit)’ler sağlar
- **Google Cloud Pub/Sub**: Eş zamanlı olmayan (asynchronous) bir mesajlaşma servisidir.

# Salesforce Crm

- Salesforce Müşteri Platformu, satış gücü otomasyonu, müşteri hizmet ve destek uygulamalarını, pazarlama otomasyonunu, iş ortakları yönetimini, iş zekası, uygulama geliştirme, Internet of Things (IoT ), entegrasyon ve bulut servislerini kapsamaktadır.
- Salesforce CRM tek bir ürün değil; şirketlerin büyümesine ve başarısına yardımcı olmak için müşteri, iş ortağı ve çalışanların arasında etkileşimleri yöneten kusursuz bir entegre çözümdür.

# Geçmişte Salesforce

- SaaS (software-as-a-service) olarak çalışacak bir yazılım geliştirmeye başladılar.
- İlk çözüm bir CRM paketiydi
- Ürün bulut tabanlı olunca, şirketlerin barındırma & bakım gibi giderleri olmayacaktı.
- Ürünün ismi Sales Cloud oldu. Bulut üzerinde çalışan bir “Müşteri Yönetim Sistemi” olarak kullanılabilecek bir üründü Sales Cloud.

# Salesforce’a Ait Ürünler

- Sales Cloud
- Service Cloud
- Marketing Cloud & Pardot
- Platform & App Cloud (Force.com & Heroku)
- Community Cloud
- Analytic Cloud (Wave)
- Financial Cloud
- Commerce Cloud
- Health Cloud
- IoT Cloud

# KARELPORT

- Bulut üzerinden hizmetler,fırsatlar ve sosyal paylaşım olanakları sunan online iş çevresidir
- Karelport her büyüklükte işletmeye sosyal iş ortamında ; bakım gerektirmeyen ölçeklenebilir bulut çözümlerinin yanı sıra katma değerli servisler , ürünler ve anlık fırsatları sosyal iş ağı ortamında sunan web sitesidir

# Karelport Amaçları

- Kurumsal iletişim sistemlerinin internet ortamında daha güvenli ve verimli çalışmasını sağlamak
- İletişim giderlerini azaltmak
- Çalışanların iş birliği ve paylaşımına uygun internet ortamı yaratmak
- Farklı sektörlerdeki çalışanların bilgi paylaşımı yapmasına olanak sağlamak
- Uygun servislerle küçük ve orta ölçekli işletmelerle teknolojik çözümler sunmak
- Yeni nesil teknolojileri kullanarak çalışanlara özel fırsatlar yaratmak

# Karelport Çözümleri

- Karelport’un sunduğu bulut bilişim çözümleri ; kurumsal kullanıcıların iş yapış biçimlerini kolaylaştırır.Tasarruf ve verimlilik sağlar.Yeni nesil internet uygulamalarını kapsar.
- Bulut bilişim çözümlerinde her işletmenin ihtiyaç duyabileceği farklı konulardaki çözümler her hangi bir işletme sabit yatırımı gerekmeden Karelport üzerinden kullanılabilir.
- Bu sayede işletme boyutundan bağımsız kurumsal çözümlerin kullanımına imkan tanınır.

# Karelport bulut bilişim çözümleri ile :

- Kurumsal iletişim sistemleri , internet ortamında daha güvenli ve verimli çalışır.
  İletişim maliyetleri azalır.
- Kurumsal satın alma maliyetleri azalır.
- Küçük ve orta ölçekli işletmelere ileri teknoloji ürünlere uygun maliyetlerle sunulur.
- Çalışma alanı genişler , kısaca her yerden her an çalışma desteklenir.
- Ürün veya çözüm ile ilgili kullanım tamamlandığında veya ihtiyaç değiştiğinde kolaylıkla vazgeçilir.

# Karelport kurumsal sosyal ağ platformu İLE:

- Kurumsal kimlik güvenle oluşturulur,yönetilir ve tüm karelport üyeleri ile paylaşılır.
- İşletmeye özel sağlam iş bağları kurulur.
- Farklı sektörlerdeki çalışanların bilgi paylaşımına olanak sağlanır.
- Pratik iş çözümleri ile verimlilik artışı sağlanır.
- Çalışanların iş birliği ve paylaşımına uygun internet ortamı yaratılır.

# Oracle Cloud

- Oracle Cloud, ister bulut ortamında ister şirket içinde işletme kullanıcılarının ve geliştiricilerinin iş yüklerini sorunsuzca maliyet etkili bir şekilde oluşturmasına , dağıtmasına ve yönetmesine olanak tanıyan eksiksiz ve entegre bulut servislerini sunarak dijital dünyada nasıl modernleştiğini , inovasyon sağladığını ve rekabet ettiğini yeniden tanımlar

# Oracle Cloud Özellikleri

- Eksiksiz
  - İşletmeler , karmaşıklığı azaltan eksiksiz teknoloji çözümlerine ihtiyaç duyar.
  - Sorunsuz bir deneyim sağlamak için hem tamamen entegre bulut katmanları hem de şirket içi platformlar isterler.
- Akıllı
  - Oracle yapay zeka , makine öğrenimi , sohbet robotları ve daha çok fazlası dahil gelişmekte olan teknolojilerin değerini anlamamıza yardımcı olur.
  - Artık gelişmekte olan teknolojilere ulaşmak daha basit , bu teknolojileri oluşturmak ve genişletmek daha kolay ve bu teknolojileri güvenli hale getirmek ve yönetmek daha da etkilidir.
- Açık
  - Oracle bulut serüveninizi nerede ve nasıl yaptığınıza ilişkin daha fazla seçenek sunar.
  - Teknoloji altyapıları genelinde mevcut beceri setlerinden yararlanılabilir hem Oracle olan hem de Oracle olmayan iş yüklerini çalıştırabilir ve üçüncü taraf uygulamaları Oracle uygulamaları ile bağlantılı hale getirebilirsiniz.
- Seçim
  - Seçenekler , bulut yolculuğunuzda önemlidir. Oracle ile özel bulutunuzda uygulamaları dağıtabilir ve yönetebilir ya da bunları genel buluta taşıyabilirsiniz.
  - Aynı zamanda belirli BT kaynaklarının Oracle Cloud’da çalıştığı ve diğerleri şirket içinde çalıştığı hibrit BT modelinde kullanabilirsiniz.
- Güvenli
  - Oracle güvenliği , şirket içi, özel ve genel bulut ortamınızı tüm açılardan savunan ve koruyan bir altyapı genelinde katmanlar ile bulut yolculuğunuzda destek sağlar.
  - Oracle , onaylanmamış uygulamalara görünürlük sağlar ve karmaşık siber saldırılara karşı korur.

# Azure Teknolojisi

- Microsoft'un açık kaynak bulut platformudur. Bilişim sektörüne sunduğu, bulut bilişim hizmetleri sağlayan Windows Server işletim sisteminin özelleştirilmiş bir üründür.
- Azure; işletim sistemi, programlama dili, veritabanı ve cihaz seçeneklerinin çoğunu destekler.
- JavaScript, Python, .NET, PHP, Java ve Node.js kullanarak uygulamalar oluşturabilirsiniz; iOS, Android ve Windows cihazlar için uygulamalar geliştirebilirsiniz.
- Verilerin saklanması ve verilerin yönetilmesi için **Microsoft Azure** teknolojisinde farklı teknolojiler kullanılır
- Bunlardan birisi **Microsoft Azure Virtual Machines** ile oluşturulan **SQL Server** veya diğer **DBMS** çalıştırılmasıdır.
- Burada NoSQL teknolojisinin kullanılması da mümkündür.
- Microsoft Azure bu iş içinde kullanıcılara üç farklı yöntem sunmuştur
- Bunlar **SQL Databases**, **Tables** ve **Blobs**'tur.

## Özellikler

- Kolay ölçeklendirilen
- .Net veya açık kaynak araçlarını kullanabilir
- Kullanım Kolaylığı
- Yüksek performans
- Geniş servis seçeneği
- Düşük maliyet

# Firebase

- Firebase, gerçek zamanlı uygulamalara güç sağlamak için tasarlanmış bir bulut hizmetidir.
- Paylaşılan bir veri yapısına erişmek için Firebase kütüphanesini uygulamanıza eklemeniz yeterlidir;
- Bu verilerde yaptığınız değişiklikler, Firebase bulutla ve milisaniye cinsinden diğer istemcilerle otomatik olarak senkronize edilir.

## Özellikleri

- Gerçek zamanlı
- Hızlı ve duyarlı
- Kolay kurulum
- JSON formatı
- Google tarafından desteklendi.
- Ücretsiz

<center><image src="./image/firebase.png"/></center>

# <center> NoSQL (Not only SQL) </center>

- Bu bilgiler ışığında yoğun okuma yazma gibi veritabanı işlemleri yapan organizasyonlar, performans ve esneklik gibi çeşitli ölçütler nedeniyle ilişkisel veritabanı yönetim sistemleri yerine farklı veritabanı tasarımları üzerinde durmaktadırlar.

- **“ACID”(Atomicity, Consistency, Isolation, Durability)kuralları bulunur. NoSQL sistemleri bu kuralların tamamına uymaz.**

## YATAY ÖLÇEKLEME ve DİKEY ÖLÇEKLEME

- **Yatay Ölçekleme**: Veritabanının Yatayda ölçeklenebilir olması (horizontally scalable, scale out) **ucuz ve çok sayıda makinenin** aynı anda kullanılması anlamına gelir. Yatay ölçeklenebilirlik sayesinde yedeklilik de performans artışı da sağlanabilir.
  - Cassandra
  - MongoDB
- **Dikey Ölçekleme**: Veritabanının Dikeyde ölçeklenebilir olması (dikey ölçeklenebilirlik, vertically scalable, scale up) bir tane çok güçlü aynı zamanda pahalı bir makine/donanım kullanılmasıdır. Dikey Ölçeklenebilir sistemlerde donanım kısıtları mevcuttur
  - MySQL-Amazon
  - RDS(Amazon Relational Database Service)

# İLİŞKİSEL VERİTABANI YÖNETİM SİSTEMLERİ

- TABLO
  - Veritabanına girilen veriler tablolarda tutulur.
  - Her bir tablo farklı yapılardaki veri gruplarına aittir.
  - Bu verilerin arasındaki ilişkilerin kurulduğu bir başka tablo daha olabilir.
- INDEKS
  - Tablolarda tutulan verilere daha hızlı erişim ve sorgulama yapılabilmesi için
    kullanılan nesneler ise indekslerdir.
- META-DATA
  - Her veritabanında, içerisinde oluşturulmuş nesneleri tutan sistem tabloları ve şemaları vardır, bunlara META-DATA denmektedir.
  - Stored Procedure
  - View
  - Triggers
  - Constraints
- Her ilişkisel veri tabanı kendi VTYS sistemine sahiptir.
- Veritabanı üzerindeki tüm yönetim işlemleri VTYS kullanılarak yapılır.
- İlişkisel OLTP veritabanlarında gerçek zamanlı operasyonel veriler tutulmaktadır.
- İlişkisel OLTP veritabanlarından sorgulama yapabilmek ve istenen kriterlere ait veri setlerini elde etmek için SQL Yapısal Sorgulama Dili kullanılır.
- Standart bir sorgulama komut kütüphanesi ANSI tarafından geliştirilmiştir
- Günümüzde bir çok veritabanı sistemi üreticisi ANSI-SQL komut setlerine ilave olarak, kendi veritabanına özgü ek komutlar içeren SQL komut setleri üretmiştir.
- Örneğin
  - PL/SQL
  - T-SQL.
- İlişkisel veritabanlarında tablolarda tutulan veriler sütun ve satır olmak üzere iki boyutludur.
- Bundan dolayı SQL ile yapılan sorgularda elde edilecek bilgi de iki boyutu geçemez
- Ancak günümüzde çok boyutlu karmaşık prosesler ve karar alma süreçleri karşısında bu yöntem yetersiz kalmıştır.
- Analiz süreçlerinde yalnızca belirli bir aşamaya kadar ihtiyaçları karşılamıştır.

# NoSQL BASE

- NoSQL; yatay ölçeklendirebilme, hız, dağıtık sistemlere uygunluk, verimlilik vb. özellikler açısından fark yaratsa da, birden fazla tablo üzerinde birlikte işlem yapıldığı durumlarda sorun oluşturabilmektedir.
- İlişkisel veritabanlarının kullandığı ACID işlemselliğine karşın NoSQL BASE (Basically Available, Soft state, Eventually consistent) akronimi kısaltması ile ifade edilir.
- **Basically Available (Kolay Ulaşılabilirlik)**: Veri erişim sorunlarını ortadan kaldırmak için kopyaları kullanır ve arta kalan herhangi bir paylaşılmış ya da bölümlenmiş veriyi birçok sunucudan alır.
- **Soft state(Esnek Durum)**: ACID mantığında veri tutarlılığının olmazsa olmaz bir gereklilik olduğu savunulurdu fakat NoSQL sistemler tutarsız ve süreksiz verilerin barınmasına da izin verir.
- **Eventually consistent (Eninde sonunda Tutarlı)**: Uygulamalar anlık tutarlılıkla ilgili olmasına rağmen, NoSQL sistemlerin gelecekte bir zamanda tutarlı olacağı farz edilir.
- ACID‟in zorunlu tuttuğu tutarlılık, NoSQL‟de tanımlanmayan bir zamanda tutarlılığın oluşacağı garanti edilir.

# NOSQL KULLANMA NEDENLERİ

- Değişken veri modeli ya da yapısı varsa,
- Veri bütünlüğü önemli değil ya da uygulama seviyesinde çözülmüşse,
- Mevcut ilişkisel modelin özellikle tablo birleştirme sorgularında getirdiği karmaşıklıktan kaçınmak üzere denormalizasyon işleminin yapılması gerektiği düşünülüyorsa,
- Mevcut sistem çoklu-nesne-hareketi (multi-object transaction) gerektirmeyen, daha çok her harekette bir nesne üzerinden işlem yapılıyorsa,
- Sistemin gereksinimleri sürekli değişkenlik gösteriyor ve bu değişiklikleri ilişkisel modele yansıtmak kayda değer kaynak maliyeti ortaya çıkarıyorsa,
- Mevcut sistemde aynı kayıtlar üzerinden okuma işlemi sık olarak gerçekleştiriliyor ve önbellek mekanizmasına ihtiyaç duyuluyorsa,
- Bulut bilişim servisleri ile organik bağlantıları vardır. Kolaylıkla bulut bilişimle birlikte kullanılabilir. Amazon gibi firmaların bu alanda çalışmaları bulunmaktadır.

# NoSQL Sistemleri nelerdir?

- **Döküman (Document) tabanlı**: Bu tip veri tabanları JSON yapısında kayıt yapar. Bu yapılarda sınırsız alan oluşturabilirsiniz. Hatta sınırsız alanların içine sınırsız alanlar ve onların da içine şeklinde devam edebilirsiniz.

  - Örnek sistemler:
    - MongoDB
    - CouchDB
    - Amazon Simple DB
    - Cassandra
    - HBase

- **Anahtar / Değer (Key / Value) tabanlı**: Bu sistemlerde anahtarlara karşılık gelen tek bir bilgi bulunur. Kolon yapısı yoktur.

  - Örnek sistemler:
    - MemcacheDB
    - Berkeley DB
    - Azure Table Storage

- **GRAPH(AĞ) tabanlı**: Bu sistemler diğerlerinden farklı olarak verilerin ilişkisini saklayan Graph Theory modelindeki sistemlerdir.

  - Örnek sistemler:
    - Neo4J
    - FlockDB

- **Kolon (Column) tabanlı**: Çok büyük verilerin tutulduğu dağıtık sistemler için uygundur. Veriler anahtar & değer ikilisi şeklinde saklanır fakat anahtar birden fazla kolona işaret etmektedir.
  - Örnek sistemler:
    - Cassandra
    - HBase

## Döküman (Document) tabanlı

- Doküman tabanlı veritabanlarının en önemli özelliği “esnek” olmalarıdır.
- Bir anahtara karşılık gelen veriler “doküman” adı verilen nesnelerde saklanırlar.
- Nesneler genellikle JSON formatındadır.
- Dokümanlar çok sayıda alan içerebilir ve her dokümanın yapısı birbirinden farklı olabilir.
- İlişkisel veritabanlarında bu tarz çok biçimli (polymorphic) veriler çok sayıda tabloya dağılmış olarak saklandığı için karmaşık sorgular gerektirmektedir.
- Doküman tabanlı veritabanları esnek yapısı ile bu ihtiyacı ortadan kaldırmaktadır.
- Doküman tabanlı veritabanları, içerik yönetim sistemleri, elektronik ticaret uygulamaları ve günlük (blog) siteleri gibi esnek veri yapısına ihtiyaç duyan uygulamalar için uygundur.

## Anahtar / Değer (Key / Value) tabanlı

- “Anahtar/Değer” tabanlı veritabanları, küçük ve çok sayıda okuma yazma işleminin yapıldığı uygulamalar için uygundur.
- Bir anahtara karşılık gelen veri genellikle boolean, integer gibi basit verilerdir.
- Bu tür veritabanları, önbellek (caching) yazılımları, alışveriş sepeti uygulamaları ve görüntü dosyalarının saklanması gibi uygulamalar için uygundur.

## AĞ (GRAPH) tabanlı

- Çizge tabanlı veritabanlarında veriler düğümler (**node**), ilişkiler (**edge**) ve özellikler (**properties**) şeklinde tutulurlar.
- Diğer veritabanı türlerinden farklı olarak veriler arasındaki ilişkiler de saklanabilir.
- Diğer NoSQL veritabanı türleri çok geniş kullanım alanına sahipken, çizge tabanlı veritabanlarının kullanım alanı daha kısıtlıdır.
- Çizge tabanlı veritabanları, BPM uygulamaları, sosyal ağ uygulamaları, kimlik ve erişim yönetimi uygulamaları ve tavsiye motorları gibi uygulamalar için uygundur.

## Kolon (Column) tabanlı

- Kolon tabanlı veritabanları, yüksek okuma yazma performansı ve yüksek erişilebilirlik (high availibity) için tasarlanmıştır.
- Birden çok sunucu üzerinde dağıtık olarak çalışırlar ve bu sayede tek bir sunucuda tutulamayacak kadar büyük verileri saklayabilirler.
- Yazma işleminde kesinti yaşanmaz fakat dağıtık yapısından dolayı kısa süreli veri tutarsızlığı (inconsistency) yaşanabilir.
- Bu özelliği tolere edemeyen uygulamalar için uygun değildir
- Kolon tabanlı veritabanları, içerik yönetim sistemleri, günlük (blog) uygulamaları, uygulama kayıtlarının (log) saklanması gibi uygulamalarda yaygın olarak kullanılmaktadır.

# NoSQL Sistemlerin Avantajları Nelerdir?

- NoSQL veritabanı sistemleri ilişkisel veritabanlarına göre yüksek erişilebilirlik imkanı sunarlar.
- NoSQL veritabanı sistemleri okuma ve yazma performansları göreceli olarak ilişkisel veritabanı sistemlerine göre daha performanslı olabilirler.
- NoSQL veritabanı sistemleri yatay olarak genişletilebilirler. Binlerce sunucu birarada küme olarak çalışabilir ve çok büyük veri üzerinde işlem yapabilirler.
- NoSQL veritabanı sistemleri esnek yapılarından dolayı programlama ve bakım anlamında kolaylık sağlarlar.
- NoSQLveritabanı sistemlerinde farklı özelliklere sahip birçok implementasyon arasından seçim yapma şansınız vardır.
- NoSQLveritabanı sistemleri birçok açık kaynak kodlu projelere ve bulut bilişim teknolojilerine uygun olduğu için maliyet olarak ilişkisel veritabanı yönetim sistemlerine göre daha avantajlıdır.

# NoSQL Sistemlerin Dezavantajları Nelerdir?

- İlişkisel veritabanı yönetim sistemlerini kullanan uygulamaların NoSql sistemlere taşınması başlangıçta zor olacaktır. Veri başarılı bir şekilde taşınsa bile bağlantıyı (join) kullanan kodlarda düzenlemelerin yapılması gerekecektir.
- İlişkisel veritabanı yönetim sistemlerindeki sorgu tabanlı veri erişimi yerine NoSQL sistemlerdeki anahtar tabanlı veri erişimi sağlamak gerekmektedir. Buna göre bir yapılandırmaya gidilmesi zaman alabilmektedir.
- İlişkisel veritabanı yönetim sistemlerindeki işlem hareketleri (transaction) kavramı, NoSQL veritabanı sistemlerinde bulunmadığı için veri kaybı söz konusu olabilmektedir.
- NoSQL veritabanı sistemleri veri güvenliği konusunda ilişkisel veritabanı yönetim sistemleri kadar gelişmiş özelliklere henüz sahip değiller. Bazı NoSQL projelerin dökümantasyon ve profesyonel destek konusunda eksikleri vardır.

# NoSQL Kullanım Yerleri

- NoSQL veri tabanları (fire&forget) prensibi ile çalışır.
- Bankacılık uygulamaları vb. için hiç uygun olmama sebebi de tam olarak budur.
- Buna göre veri, veritabanına gönderilir ve yazılıp yazılmadığı hakkında bilgi beklemeye gerek yoktur
- Fakat bankacılık gibi sektörlerde bu özellik bir işe yaramaz ve hatta çok risklidir.
- Bunun için neredeyse tüm finans firmaları ACID kurallarını uygulamaktadırlar.

# CAP TEOREMİ

- **Consistency(Tutarlılık)**: Brewer’a göre dağıtık bir veritabanı tutarlı olmalıdır.
  Bunun anlamı; herhangi bir veriye erişilmek istendiğinde mazeret kabul etmeksizin, her koşulda dağıtık parçalar üzerinden en son ve güncel verilere erişilmesi zorunludur.
- **Availability(KULLANILABİLİRLİK)**: Yine Brewer der ki; bir veritabanı her zaman veri kaydetmeye hazır olmak zorundadır.
  Dağıtık sistemler üzerinde çalışan bir veritabanı düşündüğünüzde sunuculardan biri ya da birkaçı arızalı bile olsa yine de erişilebilir ve kayıt ekleyip sorgulanabilir olması gerekir.
- **Partition Tolerance (Parçalanma Toleransı)**: Bir veritabanını hizmete sunan dağıtık sistemlerin birbiriyle iletişiminde sorun dahi yaşansa yine de veritabanı kayıt edilebilir olmalıdır.
- Malesef bir veritabanı sistemi bu 3 özelliğin tamamına sahip olamaz! İşte bu nedenle her bir veritabanı sistemi bir tercih yapmak zorunda, bu 3 temel özellikten birini göz ardı edeceksiniz. Peki hangisi ?
- Bize gereken şey her koşulda **erişilebilir olmak** ve yine **her koşul altında tutarlı** verilere sahip olmak ise **İlişkisel Veritabanı Yönetim Sistemleri** tercihimiz olmalı.
- Dağıtık veritabanı sistemimizin **verileri tutarlı yani her daim güncel olsun**, aynı zamanda da **dağıtık parçaların** birbirinden haberdar olmadığı durumda bile çalışsın istiyorsak **MongoDb** gibi **NoSQL** veritabanlarını kullanmamız gerekir.

<center><image src="./image/cap.png"/></center>

<center><image src="./image/cap2.png"/></center>

# KARŞILAŞTIRMALI ANALİZ

1. Esneklik

- Esneklik, NoSQL veritabanlarının en büyük artılarından birisi sayılabilir.
- İlişkisel veritabanlarının sınırları sabittir
- Belli sütunlar üzerinde ekleme çıkarma yapılabilir.
- Ama NoSQL veritabanlarında istenilen sütün eklenebilir, istenilen sütuna ise yazılmayabilir.
- Bu özellik, yazılımcı ve tasarımcı açısından genellikle bir avantaj gibi görünse dahi kimi zaman zorunlu olarak doldurulması gereken bir sütun gözden kaçabilir ve istenilen bilgilere ulaşılamayabilir.

2. Veri Bağlantıları - İişkisel Yönetim

- Burada İVTYS özelliği öne çıkarılabilir. NoSQL tarafında bu özellik yoktur ve uygulama seviyesinde çözümlenmelidir.

3. Performans

- Performans sonuçlarına bakıldığında MongoDb‟nin kayıt ekleme hızının MySQL‟e göre 3 kata yakın daha hızlı olduğu söylenebilir
- Kayıt okuma hızlarına bakıldığında ise sorgunun ilk çalıştırılmasında MySQL‟in MongoDB‟ye göre 3 kat daha hızlı olduğu söylenebilir.
- Güncelleme de MySQL in MongoDB ye göre farklı veri türlerinde daha hızlı işlem gerçekleştiğini görüyoruz.

4. Tutarlılık

- NoSQL sistemi üzerinde bilinen türde bir ilişki yapısı olmaması nedeniyle art arda bağlantıları olan işler yapıldığı zaman bütünsel işlem kavramı olmadığından oluşan bir hatadan dönmek son derece zor olabilir
- Ancak ilişkisel bir veritabanında yapılacak basit kontrollerle bu tutarlılık sağlanabilir

# OLTP ve OLAP Nedir?

- OLTP ve OLAP kavramları İlişkisel Veri Tabanı Sistemlerinde ve Veri Ambarı konularında sıkça rastladığımız kavramlardır.
- OLTP (On Line Transactional Processing) tipi sistemler organizasyonlarda kullanılan veri girişi, veri güncelleme, veri silme gibi işlemlere olanak tanıyan sistemlerdir.
- Günlük hayatta kullandığımız çoğu veri tabanı ve veri tabanına bağlı programlar OLTP tarzı işlem gören veri tabanlarıdır.
- İlişkisel veri tabanlarında kullanılmaktadır ve karmaşık ilişkiler bulunan büyük veriler için uygun değildir.
- **Büyük ve karmaşık veri tiplerinde en uygun sorgulama yöntemi için OLAP tipi sistemler kullanılmalıdır.**
- OLTP sistemlerde tablolar arasında ilişkiler oluşturulur, burada normalizasyon seviyesine dikkat edilmeli ve ayrıca ACID Prensiplerine göre işlem görülmelidir.
- Günümüzde işletmelerde yaygın olarak kullanılan ERP sistemleri (örn. SAP programı) kullanıcıları OLTP üzerinden işlem yapmaktadır.
- **OLTP türü sistemler, her gün çok sayıda işleme, girdi-çıktıya ve güncellemeye uygun sistemlerdir.**
- Fakat canlı sistemlerde karmaşık sorgulama işlemleri sistemde bir takım sorunlara ve yavaşlamalara yol açabilir.
- ERP, Kurumsal Kaynak Planlama anlamına gelen “Enterprise Resource Planning” kelimelerinden oluşmaktadır. ERP bir organizasyonun tüm veri ve proseslerinin tek bir noktada entegre edildiği bilgi sistemleridir.

## OLTP (On-line Transaction Processing)

- Çok sayıda kısa çevrimiçi işlem ile karakterize edilir (INSERT, UPDATE, DELETE)
- OLTP sistemlerinin ana vurgusu, çok hızlı sorgulama işlemine tabi tutulur, çoklu erişim ortamlarında veri bütünlüğünün korunması ve saniyedeki işlem sayısıyla ölçülen bir etkinliktir
- OLTP veritabanında detaylı ve güncel veriler vardır ve işlem veritabanlarını saklamak için kullanılan şema, varlık modeli (genellikle 3NF) 'dir.

## OLAP (On-line Analytical Processing)

- Nispeten düşük hacimli işlemlerle karakterize edilir.
- Sorgular genellikle çok karmaşıktır ve toplamaları içerir.
- OLAP sistemleri için bir yanıt süresi, bir etkinlik ölçüsüdür.
- OLAP uygulamaları, Veri Madenciliği teknikleri tarafından yaygın olarak kullanılmaktadır.
- OLAP veritabanında, çok boyutlu şemalarda (genellikle yıldız şeması) depolanmış, toplu, önceki veriler bulunur.

# Özet

- Günümüzde değişken ve büyük veri yapıları için NoSQL kullanılabilecek yegâne teknolojidir
- NoSQL veritabanları ilişkisel veri tabanlarına göre çok daha esnektir.
- Çeşitli açılardan iki veritabanı yaklaşımı göz önüne alındığında ikisinin de fark yarattığı ve ön plana çıktığı noktalar olduğu görülmektedir. Ancak bazı açılardan ilişkisel bir veritabanının kullanılmasının çok daha doğru olduğu görülmektedir.
- İnternet ortamında hızla artan veri yoğunluğu düşünüldüğünde geleceğin teknolojisi ilişkisel veri tabanları yerine NoSQL veri tabanı teknolojisi olabileceği düşünülmektedir.

# MongoDB

- MongoDB NoSql veri tabanı sistemlerinin Doküman tabanlı sistemlerinden biridir.
- Veriler JSON\BSON formatında saklanır.

# Peki JSON ve BSON nedir ?

- **JSON** verilerin XML benzeri formatta ama daha da sıkıştırılmış ve boyutu daha küçültülmüş halde tutulmasıdır.
- Böylelikle boyutun küçülmesinin yanında işlem hızı da daha iyi seviyede olmaktadır.
- **BSON** ise JSON verilerin encode edilmiş halidir yani bir kademe daha sıkıştırılmış hali olarak da düşünülebilir.
- MongoDB ye dönecek olursak MongoDB de veriler belirli ID’ler tanımlanarak tutulmaktadır ve bu sayede sorgulamalarda yüksek performans göstermektedir.
- Diğer NoSql sistemlere oranla daha zengin bir sorgulama diline sahiptir.
- MongoDB’de veriler Document’lar halinde Collection’lar içerisinde bulunur.
- Veriyapısı açısından İVTYS’lerle karşılaştırıldığında **collection tabloya, bir Document ise tablodaki bir satıra denk gelir** diyebiliriz.
- Veriler yatay ölçeklendirme ile yedeklenebildiği için kullanılabilirlik oranı oldukça yüksektir.
- MongoDB ölçeklenebilirliği sağlamak için **Master-Slave Replication** desteği sunuyor.
- Bu modelde yazma işlemleri master sunucuya yapılırken okuma işlemleri slave sunuculardan yapılarak ölçeklendirme sağlanıyor.
- MongoDB üzerindeki verileri işlemek için **MapReduce** desteği de sunuyor.
- Bu sayede büyük miktardaki veriyi kolay bir şekilde işlemek mümkün hale geliyor.
- MongoDB’nin en güzel özelliklerinden birisi de **Sharding**.
- Bu özellik sayesinde büyük miktardaki veri, sunucular arasında paylaştırılıp yükün dağıtılması sağlanabiliyor
- Replication özelliği ile birlikte kullanıldığında MongoDB NoSQL’in gücünü ortaya koyuyor.
- **Sorgu(query) Desteği**: Pekçok NoSQL çözümü veriye sadece anahtarlar(key) üzerinden erişme olanağı sağlarken, MongoDB istenilen alanlar ve belirli aralıklara(range query) göre, ayrıca düzenli ifadelerle(regular expression) de sorgulama imkanı sunuyor.
- **İkincil(secondary) index Desteği**: İstenilen alanlara göre sorgulama yanı sıra, bu alanları secondary index olarak tanımlayabilmek. Bu SQL de kullanılan non-clustered index olarak da düşünülebilir.

# MongoDB Altyapısı

- **Aggregation**
  - Dağınık halde bulunan verileri toplayıp gruplandırmak ve bunlar üzerinden gerekli işlemleri yapmak.
- **Map-Reduce Desteği**
  - Böl gönder, topla gönder
  - Burada kullanıcının sisteme yüklediği veriler mapperlar ile parçalara bölünür ve gerekli alanlara dağıtılır
  - Bu sayede işlemler daha hızlı yapılır ve sistemin her alanına aktarılan yük daha da azaltılmış olur
  - Sistem tarafından gerekli işlemler yapıldıktan sonra bu veriler Reducer’lar ile tekrar bir araya getirilir ve kullanıcıya aktarılır.
- **Data Models**
  - MongoDB’nin veri tutma biçimi SQLden farklı bir halde bulunmaktadır.
  - Bir dizi içerisinde string ve integer ifade bulunabilir. Bu özellikte İVTYS’lerden fark olarak düşünebileceğimiz bir özellik.
- **Replication**
  - MongoDB’nin herhangi bir server hatası durumunda kendini güvenceye alması.
  - VTYS sistemlerdeki Disaster Recovery’ler benzeri olarak da düşünülebilir.
  - Ana sunucunun her hangi bir sorunla karşılaşması tehlikesine karşın yedek sunucular ile verilerin yedeklenmesi ve ana sunucuda sorun gerçekleştiğinde yedek sunucunun ana sunucu görevini üstlenip veri kayıplarını engellemesi için gerekli bir özelliktir.
- **Master-Slave Replication Desteği**
  - Yazma ve okuma işlemlerini ayrı sunuculara yönlendirebilme.
  - Replication özelliğinin bir alt özelliği olarak da düşünülebilir.
  - Yine aynı şekilde ana sunucu ve yedek sunucular oluşturulabilir.
  - Burada ek olarak yazma ve okuma işlemleri ayrı sunuculardan yapılabilir.
  - Sunucular üzerindeki trafik ve yük azaltılacağından performans açısından önemli bir artış daha sağlanabilir.
- **Sharding Desteği**
  - Büyük ölçekli verilerin sunucular arasında paylaştırılması özelliği.
  - Bazen veriler çok büyük boyutlara ulaştığında tek bir sunucu artık bizim için yetersiz bir hal alabilir
  - Yeni sunucular ile yatay büyümeye giderek veriler bu sunuculara dağıtılır ve yük azaltılmış olur.

# MONGODB HANGİ DURUMLARDA KULLANILMALI?

- Yüksek okuma / yazma gerektiren yerlerde,
- Karmaşık sorgu ve analiz ihtiyacı varsa,
- Kullanıcı I/O, haber, duyuru verilerinde,
- Log verilerinde,
- Ürün, katalog verileri saklanmasında,
- Resim, video saklanmasında. (GridFS)

| SQL                                                                 | MongoDB                                                                       |
| ------------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| Database                                                            | Database                                                                      |
| Table                                                               | Collection                                                                    |
| Row                                                                 | document or BSON document                                                     |
| Column                                                              | Field                                                                         |
| Index                                                               | Index                                                                         |
| Table joins                                                         | embeded documents and linking                                                 |
| Primary key Spesify and unique or column combination as primary key | Primary key In MongoDB the primary key is automatically set to the \_id field |
| Aggregation (e.g group by)                                          | Aggregation framework                                                         |

# MongoDB Özellikleri

- Doküman Tabanlı veritabanı
  - JSON türevi (BSON) bir ofrmat kullanır
- Şemasız
- Performans
  - C++ da yazılmış
  - Index desteği
- Ölçeklenebilir
  - Replication
  - Auto-Sharding
- Ticari destekli (10gen)
  - Bolca döküman

# MongoDB DÖKÜMAN EKLEME

Var kayit = [{
"sicil": 2345,
"ad": "ayse okan",
"maas": 3000
},
{
"sicil": 1234,
"ad": "mahmut sarı",
"maas": 5000
}];
db.person.insert(kayit)

# MongoDB VERİTABANINI SORGULAMAK

db.person.find()

# Update ve Delete

db.person.update({"ad":"mahmut sarı"} ,{\$set:{‘maas':5500}}) <br>
db.person.remove({"sicil":"1234"})

# Karşılaştırma İfadeleri

- \$lt: Küçüktür
- \$gt: Büyüktür
- \$lte: Küçük Eşittir
- \$gte: Büyük Eşittir
- \$ne: Eşit Değildir

# CASSANDRA

- Cassandra da NoSql bir veri tabanı sistemi olup Facebook ve Apache tarafından geliştirilen açık kaynak kodlu bir veri tabanı sistemidir.
- Burada da veriler JSON ve XML olarak tutulmaktadır.
- Büyük dağıtık verilerin depolanması için MongoDB ve diğer NoSql veri tabanları gibi tercih edilen veri tabanı sistemlerinden biridir.

# COUCHDB

- Couchdb NoSQL tabanlı, verileri JSON formatında tutan , MapReduce indeksleri için JavaScript ve kendi API’si için HTTP kullanan, Erlang ile yazılmış open source bir veritabanı sistemidir.
- Bir ilişkisel veritabanı aksine CouchDB veri ve tablolar arasındaki, ilişkileri saklamaz. Bunun yerine her veritabanı bağımsız belgeler topluluğu oluşturur.
- Her doküman kendi veri ve kendi şemasını tutar ve böylece bir uygulama çoklu verilere ulaşabilir.
- Örneğin başka bir sunucudaki bir kişinin cep telefonunda saklanan verilere ulaşmak gibi.
- CouchDB kullanımı kolay olan ve tamamen Web i kucaklayan açık bir kaynaktır.
- CouchBase server, kalıcı veriyi hafıza gücüyle birleştirmiş son derece hızlı veri getirebilen update edebilen bir databasedir.
- **En temel özelliği hızdır.**
- Yazma/okuma işlemlerinde key/value API’sini kullanır.
- Kurulumu kolay ve elastik bir yapısı vardır.

# HBASE

- 2007 senesinde Powerset Firması tarafından geliştirilmeye başlandı.
- HDFS üzerinde çalışabilen NoSQL datastore
- Java ile yazılmış, Non-relational, Distributed (Dağıtık) sistem
- Yüksek boyutta veri saklayabilir.
- Yüksek «throughput» sağlar.
- BigData’da rastgele okuma ve yazma yapmanıza olanak sağlar.

# ANAHTAR DEĞER TABANLI VERİTABANI

- Anahtar & Değer ikililerinden (hash table) oluşan sistemdir.
- Kolon yapısı yoktur.
- Veriler JSON, boolean, integer gibi farklı formatında tutulabilir.
- Çok sayıdaki küçük veriler, okuma yazma işlemi yapılan uygulamalar için uygundur.
- Örnek sistemler: Riak, Redis, Voldemort, Memcache.
- Kullanıldığı uygulamalar: İçerik ön belleğe alma (özellkle büyük verileri idare etmek için) logolama, arşivleme, vb.
- Veri modülü: Anahtar-değer (Key - value)
- Artılar: Hızlı arama, verinin dağıtık olarak depolanması iyi
- Eksiler: Veri karmaşıklığında problem çıkar

## RİAK VERİTABANI

- Riak'ın key-value modelinin geleneksel ilişkisel veri tabanına kıyasla daha esnek ve daha hızlı geliştiği söylenir.
- Riak birçok uygulama için çok uygun olmasına rağmen, mevcut olan sorgu seçenekleri ve veri türleri açısından kaçınılmaz tradeofflar vardır.
- Bir key-value modeli ile, herhangi bir sütun veya satır kavramı yoktur, bu nedenle Riak'ın birleştirme işlemleri yoktur.
- Riak, ya doğrudan HTTP, protokol tamponları API'si ve çeşitli istemci kütüphaneleri aracılığıyla sorgulanabilir.
- Bununla birlikte, şu anda mevcut olan SQL veya SQL benzeri bir dil yoktur.
- Riak, veri çakışmaları meydana geldiğinde istatistiksel olarak az sayıda olayın tespit edilmesi ve çözümlenmesine yardımcı olan özellikler sunar.
- Bir okuma isteği yapıldığında, Riak bu nesne için tüm kopyaları arar.
- Varsayılan olarak, Riak, nesnenin vektör saatine bakarak belirlenen en güncel sürümü döndürür.

### Riak Sorgulama Seçenekleri

- Riak'ın aşağıdakileri içeren birkaç güçlü sorgulama seçeneği vardır:
  - **Riak Arama** : Apache Solr ile entegrasyon, Solr'un istemci sorgu API'ları için tam metin arama ve destek sağlar.
  - **İkincil Endeksler** : İkincil İndeksler (2i), geliştiricilere Riak'ta depolanan bir nesneyi bir veya daha fazla sorgu değeriyle etiketleme yeteneği verir. Dizinler tamsayılar veya dizeler olabilir ve tam eşlemeler veya değer aralıkları ile sorgulanabilir.
  - **MapReduce** : Geliştiriciler, belgelere etiketle filtre uygulamak, belgelerde kelimeleri saymak ve ilgili verilere bağlantılar çıkarmak gibi görevler için Riak MapReduce'dan yararlanabilir.

### Anahtar / Değer Eşleştirmeleri

- Aşağıdaki tablo genel uygulama türleri için anahtar / değer eşleştirmelerini göstermektedir:

**Başvuru Türü** **Anahtar** **Değer**

- Oturum, toplantı, celse Kullanıcı / Oturum Kimliği Oturum Verisi
- Reklâm Kampanya Kimliği Reklam İçeriği
- Kayıtlar tarih Log dosyası
- algılayıcı Tarih, Tarih / Saat Sensör Güncellemeleri
- Kullanıcı bilgisi Giriş, e-posta, UUID Kullanıcı Öznitelikleri
- içerik Başlık, Tamsayı Metin, JSON / XML / HTML Belgesi, Görüntüler vb.
- Verilerin Riak'ta düzenlenme şekli, okuma gibi erişim kalıpları dahil uygulamanın benzersiz ihtiyaçlarını dikkate almalıdır.

- Riak'ın sahip olduğu:
  - Değerin herhangi bir yapısal olmayan veri olduğu bir Anahtar / Değer modeli
  - Daha iyi kullanılabilirlik sağlayan daha fazla veri yedeklemesi
  - Nihai tutarlılık
  - Basitleştirilmiş sorgu yetenekleri
  - Riak Arama

### Riak 2.0 Veri Tipleri

- Sayaçlar: Riak 1.4'teki gibi
- Bayraklar: etkin / devre dışı
- Setleri: ikili değer koleksiyonları
- Kayıtlar: değerleri de ikili değer olarak adlandırılan ikili
- Haritalar: birden çok Veri Türünün iç içe geçmesini destekleyen - alanlardan oluşan bir koleksiyon

# REDIS VERİTABANI

- En basit haliyle Redis, key-value şeklinde tasarlanmış bir NoSQL veritabanıdır.
- Günümüzde kullanılan çoğu programlama dillerinde benzer key-value yapılarını bellekte bilgi saklamak için kullanıyoruz.
- Örneğin Java da Map yapılarında, ya da C#’ta Dictionary(sözlük) yapılarında key-value şeklinde yapılara rastlamak mümkün.
- Zaten Redis in açılımına baktığımızda da “Remote Dictionary Service(Uzak Sözlük Hizmeti)” olduğunu görüyoruz.

<center><image src="./image/redis.jpg"  height="500"/></center>

## Özellikleri

- Özellikle redis çok hızlı.
- Sitesinde paylaşılan banchmark’lara göre saniyede 100 bin operasyonu yürütebiliyor.
- Bunu nasıl yapıyor derseniz, sizin çalıştırdığınız tüm operasyonları bellekte çalıştırıyor ve size bellekteki veriyi dönüyor.
- Tüm veriyi bellekte tuttuğundan bu derece seri çalışabiliyor.
- Arzu edilirse, diske yazma seçenekleri de sunuyor.
- Herşeyi bellekte tuttuğunu söyledik. Bu durumda insanın aklına hemen çok fazla bellek kullanabileceği geliyorFakat, redis tek bir iş yapmaya ve bu işi iyi yapmaya odaklanmış.
- Redis, hiç bir veri barındırmazken bellekte sadece 1 mb yer kaplıyor.
- Eğer siz basit bir key-value eşlemesi, örneğin <String,String> şeklinde bir eşleme, tutmak isterseniz, bir millyon adedi bellekte sadece 100 mb yer kaplıyor.
- Yok ben bu kadar basit veriler tutmayacağım benim verilerim daha karmaşık derseniz, <Hash, Obj> şeklindeki verilerin (burada value alanındaki nesnemizin 5 kırılımı olduğunu varsayıyoruz) bir milyon adedi ise bellekte sadece 200mb yer kaplıyor.

## Avantajları

- Senkron çalıştığı için son derece hızlıdır.
- Birçok veri türünü destekler.
- Veriyi hem RAM üzerine hem de ayarlandığınız konfigürasyona göre disk üzerine kaydedebilir.
- Disk üzerine kayıt yaptığı için restart sonrasında aynı verilerle çalışmaya devam eder.
- Son derece aktif bir kullanıcı kitlesine sahiptir.
- Sharding, Cluster, Sentinel, Replication gibi birçok enterprise özelliklere sahiptir.
- Redis öntanımlı olarak 16 tane veritabanını destekler. Veritabanı sayısı, Redis konfigürasyonundan değiştirilebilir. Verilerinizi dilerseniz farklı veritabanlarında tutabilirsiniz.
- Redis ile oluşturduğunuz verilerin belirli bir süre sonra otomatik olarak silinmesini sağlayabilirsiniz.

## Dezavantajları

- Asenkron çalışmadığı için tek instance üzerinde, asenkron alternatiflerin eriştiği performansa erişemeyebilirsiniz.
- Veri boyutunuza göre RAM’e ihtiyacınız olur.
- Relational veritabanlarında olduğu gibi komplex sorguları desteklemez.
- Komplex sorgular için sorgu yapacaksanız, Redis yapısını düzgün kurgulamalısınız.
- Bir transaction hata alırsa geri dönüşü yoktur.

## Ne Kadar Hızlı

- İnternette Redis için yapılmış birçok benchmark bulabilirsiniz. - Kendi bilgisayarımda denediğimde saniyede 100.000 SET/GET, pipe özelliğini açtığımda saniyede 400.000 SET/GET komutu desteklediğini görmüştüm.
- Ancak göz önünde bulundurmamız gereken birkaç nokta var.
- Bu sadece bir tane Redis instancesinin değerleri.
- Birden fazla Redis instancesi oluşturup her birini işlemcinizin bir çekirdeğine ve farklı bir porta atayabilirsiniz.
- Eğer bu yetmiyorsa kolayca bir master-slave replikasyonu oluşturabilirsiniz.
- Bu da yetmiyorsa bir Redis cluster kullanabilirsiniz.
- Bu noktaya geleceğinizi hiç sanmıyorum ama bu da yetmiyorsa, consistent hashing özelliklerini kullanarak verilerinizi birden fazla parçaya bölüp shardlar veya partitionlar üzerinde tutabilirsiniz.

### Örnek

- Bir restorantta olduğunuzu hayal edin.
- Garsonluk yapıyorsunuz.
- Kocaman bir masanız var ve 1000 kişi aynı masaya rezervasyon yaptırmış.
- Müşterilerinizin herbirini siparişini veriyor.
- “Ben tavuk sote istiyorum.” “Ben köfte istiyorum.” Hepsini bir kağıda not edip mutfağın yolunu tutuyorsunuz.
- Redis asenkron çalışmadığı için tek garson var o da sizsiniz.
- 1000 kişiye yemeklerini en hızlı nasıl servis edersiniz?Mutfakta bir tane yemek servis arabasına koyabildiğiniz kadaryemek koyar, onu masaya iterek götürür, hepsini dağıtır ve gerigelirsiniz.
- Her defasında bir tane tabağı elinizde taşıyıp,masaya bırakıp, yenisini almak için mutfağa geri dönmezsiniz.

## Redis komutları

### Key Tanımlama

- Key ve Value atama: **SET KEY_NAME VALUE**
- Key değerini döndürme: **GET KEY_NAME**
- Key silme: **DEL KEY_NAME** -> Geri dönüş 0 ise silinmedi 1 ise silindi
- Key kontrol: **EXİSTS KEY_NAME** -> Geri dönüş 1 ise anahtar var 0 ise anahtar yok
- Key süre verme: **EXPİRE KEY_NAME TİME_IN_SECONDS** -> Geri dönüş 1 ise zaman ayarlandı 0 ise ayarlanmadı.
- Key süre verme: **PEXPİRE KEY_NAME TİME_IN_MILLISECONDS** -> Geri dönüş 1 ise zaman ayarlandı 0 ise ayarlanmadı.
- Key zamanını öğrenme: **TTL KEY_NAME** -> İnteger değer döner ise süresi -2 döner ise zamanı yoktur.
- Key kontrollü:**KEY \*** (tüm keyleri döner) - **KEY S**\* (s ile başlayan anahtar listesi)
- Rasgele key döndürme: **RANDOMKEY**
- Key yeniden isimlendirme: **RENAME KEY_NAME NEW_KEY_NAME**
- Veri tipi: TYPE KEY_NAME
- Birden fazla Key ekleme: **MSET KEY_NAME1 VALUE1 KEY_NAME2 VALUE2**
- Birden fazla Key çağırma: **MGET KEY_NAME1 VALUE1 KEY_NAME2 VALUE2**
- Key'de ki verinin istenilen kısmı: **GETRANGE KEY_NAME START END**
- Key'de ki verinin istenilen kısma ekleme: **SETRANGE KEY_NAME START END**
- Key'de ki verinin uzunluğu: **STRLEN KEY_NAME**
- HASHES veri tipi
  - HASHES veri ekleme: **HSET KEY_NAME INDEX VALUE** (index olarak ekler)
  - HASHES veri çağırma: **HGET KEY_NAME INDEX**
  - HASHES tümünü çağırma: **HGETALL KEY_NAME**
- SETS Veri Tipi
  - SETS veri ekleme: **SADD KEY_NAME VALUE** (oto index oluşturu)
  - SETS veri çekme: **smembers KEY_NAME**
- SORTED SETS veri tipi
  - SORTES SETS veri ekleme: **ZADD KEY_NAME INDEX VALUE**
  - SORTES SETS veri çekme: **ZRANGE KEY_NAME START END**
- Liste Veri tipi
  - Liste Veri ekleme: **LPUSH KEY_NAME VALUE**
  - Liste Veri çekme: **LRANGE KEY_NAME START END**
  - Liste Veri silme: **LPOP KEY_NAME**

# MEMCACHE VERİTABANI

- Memcached ücretsiz ve açık kaynak, yüksek performanslı, dağıtılmış bellek nesne önbellekleme sistemidir.
- Doğası gereği geneldir, ancak anahtar değer deposu olduğu için özellikle veritabanı yükünü hafifleterek dinamik web uygulamalarını hızlandırmak için kullanışlıdır.
- Memcached php ve veritabanı istekleri arasında uygulanabilir ve veritabanı sorgunuzun sonucunu RAM'de belirli bir süre için saklar.
- Yapılandırmada Memcached'in kullanabileceği RAM'i ayırabilirsiniz.
- Doğru şekilde uygulandığında, bu durum veritabanı trafiğinizi büyük ölçüde azaltabilir (bazı durumlarda% 95'den fazla) ve web mağazanızı hızlandırabilir.

## Özellikleri

- Önbellek üzerinde gerçekleştirilen değişiklikler veritabanına yansıtılmaz.
- Daha önceden verilerinizi önbelleğe aldınız ve veritabanında değişiklik yaptınız.
- Önbellekte depolanan veriler silinmedikçe veritabanındaki yeni değerler görüntülenemez.
- Sonuçların önbelleğe alınmasındaki başlıca nedenler hız ve veritabanı trafiğinin azaltılmasıdır.
- Varsayılan ayarları değiştirilmediği sürece Memcache ile en fazla 1MB büyüklüğünde veriyi önbeleğe alabilirsiniz.
- Daha yüksek boyutlardaki veriler otomatik olarak kırpılır.
- Önbelleğe alınan veri için bir takma isim tanımlanır.
- Belirtilen takma isim en fazla 250 karakterden oluşmalıdır.
- Genellikle veritabanı sorgularında -SQL sözcüğü md5() fonksiyonu ile şifrelenerek anahtar kelime olarak kullanılır.
- Tüm komutlar olabildiğince hızlı ve kilit dostu olmak için uygulanır.
- Bu, tüm kullanım durumları için deterministik sorgu hızlarına izin verir.
- Yavaş makinelerde sorgular 1 ms'nin altında çalışmalıdır.
- Yüksek uç sunucular, işlem hacminde saniyede milyonlarca tuşa hizmet verebilir.

## Nerelerde Kullanılır

- Genellikle büyük çaplı ve veritabanından yoğun bilgi sorgulama gerektiren projelerde kullanılır.
- Bunun aksine, yazılımcının tercihine bağlı olarak her türlü projede kullanılabilir.
- Fakat sakınılması gereken önemli bir nokta var.
- Veritabanı üzerinde sıklıkla değişikliklerin yapıldığı bölümlerde önbellek işleminin kullanılması hatalı sonuçların görüntülenmesine neden olabilir.
- Bu nedenle, yoğun güncelleme gerektirmeyen bölümlerde kullanılması tavsiye edilir.

## Nasıl Çalışır

- Memcached bir geliştirici aracıdır, bir "kod hızlandırıcı" değil, veritabanı ara katman yazılımıdır.
- Memcached'ı kullanmak için indirdiğiniz veya satın aldığınız bir uygulamayı kurmaya çalışıyorsanız, uygulamanızın belgelerini okuyun.
- Bu wiki ve topluluk size yardım edemeyecektir.

## Tasarım felsefesi

- **Basit Anahtar / Değerli Mağaza**
  - Sunucu, verilerinizin neye benzediğini umursamıyor.
  - Öğeler bir anahtar, bir son kullanma süresi, isteğe bağlı bayraklar ve ham verilerden oluşur.
  - Veri yapılarını anlamıyor; önceden serileştirilmiş verileri yüklemelisiniz.
  - Bazı komutlar (incr / decr) temel veriler üzerinde çalışabilir, ancak basit bir şekilde.
- **İstemcide Mantık Yarısı, Sunucunun Yarısı**
  - "Memcached bir uygulama" kısmen bir istemcidedir ve kısmen bir sunucudadır.
  - İstemciler, bir sunucu için hangi sunucunun okuyacağını veya yazılacağını, bir sunucuyla iletişim kuramadığında ne yapılacağını seçer.
  - Sunucular öğeleri nasıl depolayacağını ve getirdiğini anlar.
  - Hafızayı ne zaman tahliye edip yeniden kullanacaklarını da yönetirler.
- **Sunucuların Birbirinden Bağlantıları Kesilir**
  - Memcached sunucuları birbirinden habersiz.
  - Herhangi bir karışma yoktur, senkronizasyon yok, yayın yok, çoğaltma yok.
  - Sunucuları eklemek mevcut belleği artırır.
  - İstemcinin doğrudan sahibi olduğu sunucudaki verileri sildiği veya üzerine yazdığı için önbellek geçersiz kılma basitleştirilir.

# Kolon Mimarisi Neden Tasarlanmıştır?

- Kolon tabanlı veritabanları, yüksek okuma yazma
  performansı ve yüksek erişilebilirlik (high availibity) için
  tasarlanmıştır.

- ->?JSON(JavaScript Object Notation)?

<center><image src="./image/kolon.png" width="500" height="300"/></center>

- **Satır anahtarı**: Her satırın, o satır için benzersiz bir tanımlayıcı olan benzersiz bir anahtarı vardır.
- **Sütun**:Her sütun bir ad, bir değer ve zaman damgası içerir.
- **Ad**: Bu, ad / değer çiftinin adıdır.
- **Değer**: Bu, ad / değer çiftinin değeridir.
- **Zaman Damgası**: Bu, verilerin eklendiği tarihi ve saati sağlar. Bu, verilerin en yeni sürümünü belirlemek için kullanılabilir.

<center><image src="./image/kolon1.png" width="500" height="300"/></center>

- Bir sütun ailesi birden çok satırdan oluşur.
- Her satır, diğer satırlara farklı sayıda sütun içerebilir.
- Sütunlar diğer satırlardaki sütunlarla eşleşmek zorunda değildir (yani farklı sütun adlarına, veri türlerine vb. Sahip olabilirler)

## Nasıl çalışır?

- Birden çok sunucu üzerinde dağıtık olarak çalışırlar ve bu sayede tek bir sunucuda tutulamayacak kadar büyük verileri saklayabilirler.
- Yazma işleminde kesinti yaşanmaz fakat dağıtık yapısından dolayı kısa süreli veri tutarsızlığı (inconsistency) yaşanabilir.
- Bu özelliği tolere edemeyen uygulamalar için uygun değildir.
- Değer/Anahtar tabanlı veritabanları gibi veriye anahtar üzerinden erişim sağlarlar.
- Doküman tabanlı sistemler gibi verinin tüm alanlarından sorgulama yapmak mümkün değildir.
- Bu grupta yer alan Cassandra veritabanı geniş ikincil index ve özel veri tipleri (set, map, list, tüple, …) desteği ile çok farklı sorgu modellerine destek verebilmektedir.

## Kullanım Alanları

- Kolon tabanlı veritabanları, içerik yönetim sistemleri, günlük (blog) uygulamaları, uygulama kayıtlarının (log) saklanması gibi uygulamalarda yaygın olarak kullanılmaktadır.

# Cassandra

- Cassandra, Java ile geliştirilmiş, açık kaynak(open source), nosql veritabanı tipidir.
- Verilerimiz RDBMS’deki gibi tablolarda tutulmuyor, onun yerine JSON ya da XML formatında column base yapısını kullanarak kaydediliyor.
- Column base derken Cassandra bir kaç farklı sunucuda üzerinde dağıtık şekilde çalışabildiği için verileri yatay olarak ölçekleyebiliyoruz.
- Ana makineye bağlı sunucular üzerine kurulu değil.Bu yapı, sunucu istemci mantığıyla değil de peer to peer (eşler arası) mantığıyla çalışıyor.
- Bütün makineler eşit, makinelerden biri çöktüğünde sistem durup diğer makinelerin çalışmasını etkilemiyor.. Bu da kullanımımızı kolaylaştırıyor.
- Hız açısından önemli bir veritabanı olduğundan genelde hızlı arama yapılan ve veritabanları büyük olan servislerin tercihi oluyor.

### Cassandra-cli

- **CREATE TABLE** :
  - create column family User with comparator = UTF8Type;
  - update column family User with column_metadata =[{column_name: first, validation_class: UTF8Type},{column_name: last, validation_class: UTF8Type},{column_name:class,validation_class: UTF8Type,index_type: KEYS}];
- **INSERT** :
  - assume User keys as utf8;
  - set User[‘ying’][‘first’] = ‘Enes’;
  - set User[‘ying’][‘last’] = ‘Fatih’;
  - set User[‘ying’][‘class’] = ‘3’;
- **DESCRIBE** :describe;
- **GET** : get User[‘ying’];

### MySQL karşılaştırması

Cassandra > MySQL read and write

# APACHE HBASE

- 2007 senesinde Powerset Firması tarafından Java dili ile geliştirilmeye başlandı.
- Milyarlarca satır Milyonlarca kolondan oluşabilen ve Hadoop üzerinde inanılmaz iyi olan bir NOSQL çözümüdür.
- Apache Hbase %100 open source HDFS storage kullanabilen çok hızlı performansa sahip , çökmesi zor Fault toleransı olan bir NOSQL çözümüdür.
- Yüksek boyutta veri saklayabilir (TB/PB).
- Büyük veri (bigdata) de rastgele okuma ve yazma yapmanıza olanak sağlar.
- Eğer random ve real time data access istiyorsanız Hbase düşünmeniz gereken bir seçenektir.
- Hbase bir Cloumn oriented databasedir. Yani amacınız 5 milyar kayıt içerisinde kolon bazında en büyük 50 taneyi bulmaksa doğru yerdesiniz demektir.
- Bu tarz databaselerde Key değeri birçok parçadan oluşabilir, yani key vatandaşlık numarası yada abone numarası demek doğru olmaz.
- Key Column Family,rowid,Column qualifer ve timestampdan oluşur.
- Value ise bu Keyin döndürdüğü değerdir.

### Örnek Tablo oluşturma

- **hbase> create ‘table1’, {NAME => ‘family1’, VERSIONS => 5}** burada table1 tek kolon familysinde oluşturuldu.
- **hbase> create ‘sosyal’, {NAME => ‘facebook’},{NAME => ‘twitter’}, {NAME => ‘instagram’}** Burada Sosyal isimli tabloda facebook CF si Twitter CFsi ve Instagram CF oluşturuldu.

# Graf Tabanlı NoSQL Veribanı

## Graf Nedir?

- Graph teorisi, matematik branşlarından birisidir.
- Temel olarak yapısı, noktalar ve bu noktaları birleştiren yollar ile ilgilidir.
- Graph teorisi, noktaların birbirleri ile olan ilişkilerini ve ilişkinin noktaya göre yapısını ele alır.
- Çizge, graf, ağ, çizit…
- Bir dizi düğüm ve bunları birbirine bağlayan ilişkilerdir.
- Graflar varlıkları düğümler olarak gösterir
- Bu varlıkların dünyayla nasıl ilişki kurduklarını gösterir
- Geniş bir kullanım alanına sahip
- Her türlü senaryoyu modellememizi sağlar
- Esnek bir yapıya sahip
- Düğümler, ilişkiler ve özelliklerden oluşur
- Kullanıldığı alanlar:
  - Bilgisayar ağları, navigasyonlar, şehirlerarası mesafe hesaplama, yol haritası çıkarma, elektronik devreler, şebeke yapıları, soyağaçları vb.

<center><image src="./image/graf.png"/></center>

- G=(V,E)
  - G : Graf
  - V : Düğüm (Node)
  - E : Ara-çizgi (Edge)
- V= {A,B,C,D}
- E={[AB],[AC],[AD],[CD]}
- Düğümler ve çizgiler özelliklere sahip olabilir

## Graf Veritabanları

- 7yBir graph veritabanı düğümler, kenarlar ve özelliklerle beraber graph yapılarını kullanarak veriyi sunar ve saklar.
- Tanımsal olarak bir graph veritabanı, indissiz yakınlık (index-free adjacency) sağlayan bir veri saklama sistemidir.
- Graph veritabanları graph teorisine dayalıdır ve düğümler, özellikler ve kenarlar içerirler.
- Graf tabanlı veritabanlarında veriler düğümler (node), ilişkiler (edge) ve özellikler (properties) şeklinde tutulurlar.
- Diğer veritabanı türlerinden farklı olarak veriler arasındaki ilişkiler de saklanabilir.

<center><image src="./image/graf1.png"/></center>

## Düğümler

- Düğümler, nesneye yönelik programcıların aşina olduğu objelere
  çok benzemektedir.
- Düğümler insan, iş, hesap gibi takip edilmek istenen varlıkları temsil eder.
  - Örneğin, eğer “wikipedia” düğümlerden biriyse, “web sitesi” veya “referans materyali” gibi özelliklere bağlanabileceği gibi düğümün hangi özelliklerinin veritabanı ile uyumlu olacağına bağlı olarak, “‘w’ ile başlayan kelimeler” gibi özelliklere de bağlanabilir.

## Ara-çizgiler (İlişkiler)

- Ara-çizgiler düğümleri düğümlere veya düğümleri özelliklere bağlayan çizgilerdir ve iki taraf arasındaki ilişkiyi temsil eder.
- Önemli bilginin çoğu çizgilerde tutulur.
- Birisi düğümlerin, özelliklerin ve çizgilerin bağlantılarını incelediği zaman anlamlı örüntüler ortaya çıkar.

## Özellikleri

- Karmaşık aramalarda daha iyi performans
- Esnek bir yapıya sahip
- Agile uygulama pratikleri ile uyumlu
- Veriler arasındaki ilişkiler ve bu ilişkilerin özellikleri üzerinden sorgulama imkânı sunar.

## İlişkisel Veritabanı Kavramlarına Karşılık Graf Tabanlı Veritabanı Kavramları

| Tablolar            | Graflar                |
| ------------------- | ---------------------- |
| Satırlar            | Düğümler               |
| Kolonlar ve Veriler | Özellikler ve Değerler |
| Kısıtlayıcılar      | ilişkiler              |
| Joinler             | Traversallar           |

## Graf Veritabanları

- GraphDB
- GraphQL
- neo4j
- Infinite Graph
- Dgraph
- Cayley

## GraphDB

- Ücretsizdir.
- Ontotext tarafından oluşturulan yüksek performanslı bir veri tabanıdır.
- Java'da uygulanır ve RDF4J için bir Depolama ve Çıkarım Katmanı (SAIL) olarak paketlenir.
- Yükleme, muhakeme ve sorgu değerlendirmesi büyük ontolojilere ve bilgi tabanlarına karşı bile hızlı ilerlemektedir .
- W3C standartlarına uygunluk , performans, genişletilebilir, ölçeklenebilir, yüksek kullanılabilirlik kümesi, etkileyici, zengin ve esnek veri modeli.
- GraphDB en çok semantik bağlam ve veri kalitesinin önemli olduğu yüksek model karmaşıklığı olan senaryolarda kullanılır.

## Neo4j

- Kurumsal ve gelişmiş sürümler için GPLv3 Topluluk Sürümü, ticari ve AGPLv 3, ve öğrenciler içinde ücretsiz kullanım seçenekleri mevcuttur.
- Son derece ölçeklenebilir açık kaynak, ACID'i destekler, kurumsal dağıtımlar için yüksek kullanılabilirlikli kümelenmeye sahiptir ve tam işlem desteği ve görsel düğüm bağlantı grafik kâşifi içeren web tabanlı bir yönetim aracıyla birlikte gelir.
- Yerleşik REST web API arayüzünü kullanarak birçok programlama dilinden erişilebilir.
- Ocak 2017 itibarıyla kullanımda olan en popüler graf veritabanıdır.
- Neo4j adının sonundaki ‘j’ harfinden çıkarım yapabileceğimiz üzere Java ile yazılmıştır.
- Neo4j’deki veri yapısı temel iki kavram üzerine oturtulmuştur; düğümler ve bağlantılar.
- Düğümler verileri, bağlantılar ise düğümler arasındaki ilişkileri gösterir.
- Herhangi bir düğümün veya bağlantının birden fazla özelliği olabilir.

## FlureeDB

- Ücretsizdir.
- Blockchain destekli uygulamalara olanak veren graph veri tabanıdır.
- ACID ile uyumludur.
- Dağıtılmış defter uygulamaları için üretilmiştir.

# NEO4J TEMEL SORGULAR

1. Create(n) -> Tek düğüm oluşturma
2. Create(n)(m) -> Birden fazla düğüm oluşturma
3. Create(n:insan{ad:"Enis"}) -> İçerisinde Enis adını bulunduran n adet instan düğümü oluşturur
4. Match(n) Return n -> Tüm düğüm ve ilişkileri yazdırma
5. Match(n) Detach Delete n -> Tüm düğüm ve ilişkileri silme
6. Match(n:insan{name:"Enis"}) SET n.name="Sedat" Return n -> ismi "Enis" olan düğümleri getirdi ve bu düğümlerin isimleri "Sedat" olarak güncelledi

## İlişki Kurma

- Yönetmen grafında Quentin Tarantino adlı düğüm ile Filmler grafındaki Pulp Fiction adlı düğüm ile ilişki kurma

MATCH (n : Yonetmen { name : " Quentin Tarantino "}),(b : Filmler { name : "Pulp Fiction"})

MERGE (n)-[:YONETMEN]->(b)

MATCH (n : Yonetmen { name : " Quentin Tarantino "}),(b : Filmler { name : "Pulp Fiction"})

CREATE (n)-[:YONETMEN]->(b)

## İLİŞKİ SORGUSU

- İsmi Enis KESKİN olan düğümün ARKADAŞ ilişkisini gösteren sorgu

MATCH (n : Kisiler {name : "Enis KESKİN"})-[r : ARKADAŞ]->(c : Kisiler) RETURN n , c

## WHERE KOMUTU

- Filmler grafındaki tüm düğümlerdeki yıl özelliğine bakılarak 2000 yılından önce yapılan düğümler gösterilmiştir.

MATCH ( n : Filmler ) WHERE n.yil<2000 RETURN n

## ORDER BY KOMUTU

- Filmler grafındaki tüm düğümlerin yıl özelliğine bakarak küçükten büyüğe sıralanması yapılır.

MATCH (n : Filmler) RETURN n.name, n.yil ORDER BY n.yil

## COUNT KOMUTU

- Enis KESKİN’in arkadaş sayısını bulan sorgu.

MATCH (n:Kisiler{name:"Enis KESKİN"})-[:ARKADAŞ]->(c:Kisiler) RETURN c,COUNT(\*) as ARKADASSAYISI

## Çeşitli Örnekler

- Kişilerin Özcan ÖZYURT ile olan öğretmen ilişkisini sorgulama.
  - MATCH (c:Kisiler)-[r:ÖĞRETMEN]->(n:Ogretmenler{name:"Özcan ÖZYURT"}) RETURN c,n
- Enis KESKİN kişisinin favori filmlerini getirir.
  - MATCH (c:Kisiler {name: "Enis KESKİN"})-[r:FAVORİ]->(n:Filmler) RETURN c,n
- Enis KESKİN kişisinin tüm ilişkileri
  - MATCH (c:Kisiler {name: "Enis KESKİN"})-[ ]->(n) RETURN c,n
- Araba grafına audi düğümünün eklenmesi
  - CREATE (n:Araba{name:"Audi"}) RETURN n
- Özcan ÖZYURT düğümü ile Araba grafındaki Mercedes düğümü arasında detaylı ilişki kurma
  - CREATE (b:Ogretmenler{name:"Özcan ÖZYURT"})-[:SAHİP{yil:2019}]->(n:Araba{name:"Mercedes"}) RETURN b,n
- Enis KESKİN ile Yaşar KURT arasındaki arkadaşlık ilişkisinin silinmesi
  - MATCH (n:Kisiler{name:"Enis KESKİN"})-[r:ARKADAŞ]->(b:Kisiler{name:"Yaşar KURT"}) DELETE r
- Enis KESKİN’in arkadaşlarının arkadaşlarını bulan sorgu.
  - MATCH (n:Kisiler{name:"Enis KESKİN"})-[:ARKADAŞ]->(c:Kisiler)-[:ARKADAŞ]->(f:Kisiler) RETURN f