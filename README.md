Google Dork Dosya Arama Web Uygulaması

Genel Bakış

Bu proje, Python ve Django kullanılarak geliştirilen bir web uygulamasıdır. Kullanıcılar, belirli bir konu ve dosya türü seçerek Google Dork tarzında arama sorguları oluşturabilir ve özel veri yapıları kullanarak veri işlemlerini simüle edebilir.

Özellikler

Belirtilen dosya türlerinde (ör. PDF, Word, PNG, HTML) Google Dork tarzı aramalar yapma.

Aşağıdaki veri yapılarıyla simüle edilmiş veri işlemleri:

Bağlı Liste (Linked List)

Yığın (Stack)

Kuyruk (Queue)

Grafik (Graph)

Etkileşimli ve duyarlı bir kullanıcı arayüzü.

Gereksinimler

Aşağıdaki yazılımların kurulu olduğundan emin olun:

Python 3.9 veya üstü

Django 5.1.3

Kurulum

Projeyi klonlayın ve proje dizinine gidin:

git clone https://github.com/username/google_dork.git
cd google_dork

Gerekli Python paketlerini yükleyin:

pip install -r requirements.txt

Veritabanı migrasyonlarını uygulayın:

python manage.py migrate

Statik dosyaları toplayın:

python manage.py collectstatic

Geliştirme sunucusunu başlatın:

python manage.py runserver

Tarayıcınızı açın ve şu adrese gidin:
http://127.0.0.1:8000/

Kullanım

Ana sayfada bir konu girin ve açılır menüden bir dosya türü seçin.

"Ara" düğmesine tıklayarak sorguyu oluşturun ve çalıştırın.

Oluşturulan sorgu görüntülenecek ve yeni bir tarayıcı sekmesinde açılacaktır.

Kullanılan Veri Yapıları

Bağlı Liste (Linked List): Arama sonuçlarını yönetir.

Yığın (Stack): LIFO düzeninde arama sorgularını depolar.

Kuyruk (Queue): FIFO düzeninde arama sorgularını yönetir.

Grafik (Graph): Konular ve dosya türleri arasındaki ilişkileri temsil eder.

Dosya Yapısı

data_structures.py: Bağlı liste, yığın, kuyruk ve grafik implementasyonlarını içerir.

views.py: Kullanıcı girdilerini işleme ve sorgu oluşturma mantığını yönetir.

templates/: Web arayüzü için HTML şablonlarını içerir.

static/: Stil dosyaları ve diğer statik dosyaları içerir.
