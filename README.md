# Google Dork Search with Data Structures  

Bu proje, kullanıcıların belirli dosya türlerine sahip içerikleri Google'da aramalarını sağlayan bir web uygulamasıdır. Kullanıcıların girdileriyle Google Dork sorguları oluşturulur ve ilgili dosyalar aranır. Arama işlemleri, temel veri yapıları (LinkedList, Stack, Queue, Graph) ile simüle edilmiştir.  

## Özellikler  
- Kullanıcı, belirli bir konu ve dosya türü seçerek Google Dork sorgusu oluşturabilir.  
- Oluşturulan sorgular, **LinkedList**, **Stack**, **Queue**, ve **Graph** veri yapılarıyla işlenir.  
- Sonuçlar, seçilen dosya türlerine göre filtrelenerek görüntülenir.  
- Web uygulaması **Python Django** framework'ü ile geliştirilmiştir.  
- Kullanıcı, arama sorgularının sonuçlarını web arayüzü üzerinden görebilir.  

## Teknolojiler  
Proje aşağıdaki teknolojiler kullanılarak geliştirilmiştir:  
- **Python 3.x**  
- **Django 5.x**  
- **HTML / CSS**  
- **JavaScript** (isteğe bağlı)  

---

## Kurulum  

### 1. Python ve Django Yükleyin  
Proje, Python 3 ve Django 5.x sürümünde çalışmaktadır. Gerekli yazılımları yüklemek için:  
- Python 3'ü [buradan indirin](https://www.python.org/downloads/).  
- Django'yu yüklemek için:  
  ```bash
  pip install django

### 2. Proje Dosyalarını İndirin
 ```bash
git clone https://github.com/username/google_dork.git  
cd google_dork
```
### 3. Gerekli Bağımlılıkları Yükleyin
```bash
pip install -r requirements.txt  
```
### 4. Veritabanı Migrasyonlarını Çalıştırın
```bash
python manage.py migrate  
```
### 6. Sunucuyu Başlatın
```bash
python manage.py runserver  
```
### Tarayıcınızda http://127.0.0.1:8000/ adresine giderek uygulamayı başlatabilirsiniz.

### Kullanım
Topic (Konu): Aramak istediğiniz terimi yazın.
File Type (Dosya Türü): HTML, PDF, Word, PNG vb. formatlardan birini seçin.
Search: Butonuna tıklayın.
Google Dork sorgusu oluşturularak sonuçlar ekranda listelenecektir.

Veri Yapıları
1. LinkedList (Bağlantılı Liste)
Kullanıcı sorguları bağlantılı liste içinde saklanır.
Her yeni sorgu listeye eklenir.
2. Stack (Yığın)
En son eklenen sorgu ilk çıkar.
Push ve pop işlemleri ile veriler eklenip çıkarılır.
3. Queue (Kuyruk)
İlk giren ilk çıkar (FIFO) prensibine dayanır.
Kullanıcı sorguları kuyruğa eklenir ve sırayla işlenir.
4. Graph (Graf)
Konular ve dosya türleri arasındaki ilişkiler graf yapısında gösterilir.
Her konu, bağlı dosya türlerini gösterecek şekilde grafa eklenir.
