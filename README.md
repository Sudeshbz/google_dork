Google Dork Search with Data Structures
Bu proje, kullanıcıların belirli dosya türlerine sahip içerikleri Google'da aramalarını sağlayan bir web uygulamasıdır. Projede, kullanıcının girdiği konu ve dosya türüne göre Google Dork sorgusu oluşturulur ve ilgili dosyaların araması yapılır. Ayrıca, projede temel veri yapıları (LinkedList, Stack, Queue, Graph) kullanılarak arama işlemleri simüle edilmiştir.

Özellikler
Kullanıcı, belirli bir konu ve dosya türü seçerek Google Dork sorgusu oluşturabilir.
Oluşturulan sorgular, LinkedList, Stack, Queue, ve Graph gibi temel veri yapıları kullanılarak işlenir.
Google Dork sorgusu sonucu, dosya türlerine göre ilgili içerikler aranır.
Web uygulaması, Python Django framework'ü ile geliştirilmiştir.
Kullanıcı arama sorgusunun sonuçlarını ekranda görebilir.
Teknolojiler
Python 3.x
Django 5.x
HTML / CSS
JavaScript (isteğe bağlı)
Kurulum
1. Python ve Django Yükleyin
Proje Python 3 ve Django 5.x sürümü ile çalışmaktadır. İlk olarak Python ve Django'nun bilgisayarınızda yüklü olduğundan emin olun. Eğer yüklü değilse, aşağıdaki komutları kullanarak yükleyebilirsiniz:

bash
Kodu kopyala
# Python 3'ü yükleyin
https://www.python.org/downloads/

# Django'yu yükleyin
pip install django
2. Proje Dosyalarını İndirin
Proje dosyalarını bilgisayarınıza indirerek ilgili dizine geçin.

bash
Kodu kopyala
git clone https://github.com/username/google_dork.git
cd google_dork
3. Gerekli Bağımlılıkları Yükleyin
Proje dizininde aşağıdaki komutları kullanarak gerekli bağımlılıkları yükleyin:

bash
Kodu kopyala
pip install -r requirements.txt
4. Veritabanı Migrasyonlarını Çalıştırın
Veritabanı yapısını oluşturmak için aşağıdaki komutları çalıştırın:

bash
Kodu kopyala
python manage.py migrate
5. Statik Dosyaları Toplayın
CSS ve diğer statik dosyaları toplamak için aşağıdaki komutu çalıştırın:

bash
Kodu kopyala
python manage.py collectstatic
6. Sunucuyu Başlatın
Geliştirme sunucusunu başlatmak için şu komutu çalıştırın:

bash
Kodu kopyala
python manage.py runserver
Tarayıcınızda http://127.0.0.1:8000/ adresine giderek uygulamayı kullanabilirsiniz.

Kullanım
Web uygulamasına giriş yapın.
Topic (Konu) kısmına aramak istediğiniz terimi yazın.
File Type (Dosya Türü) kısmından aramak istediğiniz dosya türünü seçin (HTML, PDF, Word, PNG vb.).
"Search" butonuna tıklayarak aramayı başlatın.
Google Dork sorgusu sonucu oluşturulacak ve ilgili dosyalar listelenecektir.
Veri Yapıları
Projede şu veri yapıları kullanılmaktadır:

1. LinkedList (Bağlantılı Liste)
Kullanıcı tarafından yapılan arama sorguları, bağlantılı liste içinde saklanır.
Listeye her yeni sorgu eklenir.
2. Stack (Yığın)
Yığın, en son eklenen sorgunun ilk önce çıkarılacağı şekilde çalışır.
Yığının push ve pop fonksiyonları ile veriler eklenip çıkarılabilir.
3. Queue (Kuyruk)
Kuyruk veri yapısı, ilk giren ilk çıkar (FIFO) prensibine dayanır.
Kullanıcı sorguları kuyruğa eklenir ve sırayla işlenir.
4. Graph (Graf)
Graf, konular ve dosya türleri arasındaki ilişkileri göstermek için kullanılır.
Her konu, ona bağlı olan dosya türlerini göstermek için graf yapısına eklenir.
