Linked List: Arama sonuçlarını saklamak için kullanacağız. Arama sonuçları her dork sorgusuyla birlikte bir listeye eklenecek.
Stack: Kullanıcıların önceki aramalarına gidip geri dönmeleri için kullanılacak.
Queue: Arama geçmişini sırasıyla saklayacağız.
Graph: Belirli konuların ve dosya türlerinin ilişkilerini modellemek için kullanılacak.
Array: Kullanıcıların seçebileceği dosya türlerini saklayacak.


Linked List Yapısı

class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
Node sınıfı: Bir bağlı listenin her bir elemanını (düğümünü) temsil eder.
data: Bu düğümde saklanan veriyi temsil eder (örneğin bir string veya sayı).
next: Bu, bir sonraki düğümün referansını tutar. Başlangıçta None (boş) olur çünkü bir düğüm tek başına oluşturulmuş olabilir.

class LinkedList:
    def __init__(self):
        self.head = None
LinkedList sınıfı: Bağlı listenin kendisini temsil eder. Bu sınıf, düğümleri eklemek, silmek veya görüntülemek gibi işlemleri yönetir.
head: Listenin ilk elemanını (başlangıç düğümünü) tutar. Başlangıçta None olur, yani liste boştur.

def append(self, data):
    new_node = Node(data)
    if not self.head:
        self.head = new_node
    else:
        last = self.head
        while last.next:
            last = last.next
        last.next = new_node
append fonksiyonu: Listeye yeni bir düğüm ekler.
new_node: Yeni bir Node nesnesi yaratılır, içine veriler (data) eklenir.
Eğer listenin başı (head) None ise, yani liste boşsa, bu yeni düğüm listenin başı olur.
Eğer liste boş değilse, listenin sonuna kadar gidilir (while döngüsü ile) ve son düğümün next referansı yeni düğüme bağlanır.

def display(self):
    current = self.head
    while current:
        print(current.data)
        current = current.next
display fonksiyonu: Listeyi ekrana yazdırır.
current değişkeni listeyi dolaşmak için kullanılır.
while current: döngüsü, listenin sonuna kadar giderek her düğümdeki veriyi (data) yazdırır.
Stack Yapısı (Yığın)

class Stack:
    def __init__(self):
        self.stack = []
Stack sınıfı: Yığın veri yapısını temsil eder. Yığın, son giren ilk çıkar (LIFO - Last In First Out) prensibine dayanır.
stack: Boş bir liste ile başlar ve bu liste yığının verilerini tutar.

def push(self, item):
    self.stack.append(item)
push fonksiyonu: Yığına bir eleman ekler. Listeye append() ile eleman eklenir.

def pop(self):
    if not self.is_empty():
        return self.stack.pop()
pop fonksiyonu: Yığından bir eleman çıkarır.
is_empty() fonksiyonu ile yığının boş olup olmadığı kontrol edilir. Eğer boş değilse, pop() ile son eklenen eleman çıkarılır ve döndürülür.

def is_empty(self):
    return len(self.stack) == 0
is_empty fonksiyonu: Yığının boş olup olmadığını kontrol eder. Eğer yığının uzunluğu sıfırsa, yığın boştur.
Queue Yapısı (Kuyruk)

class Queue:
    def __init__(self):
        self.queue = []
Queue sınıfı: Kuyruk veri yapısını temsil eder. Kuyruk, ilk giren ilk çıkar (FIFO - First In First Out) prensibine dayanır.
queue: Boş bir liste ile başlar ve bu liste kuyruğun verilerini tutar.

def enqueue(self, item):
    self.queue.append(item)
enqueue fonksiyonu: Kuyruğa bir eleman ekler. Listeye append() ile eleman eklenir.

def dequeue(self):
    if not self.is_empty():
        return self.queue.pop(0)
dequeue fonksiyonu: Kuyruktan bir eleman çıkarır.
is_empty() fonksiyonu ile kuyruğun boş olup olmadığı kontrol edilir. Eğer boş değilse, pop(0) ile kuyruktaki ilk eleman çıkarılır ve döndürülür.

def is_empty(self):
    return len(self.queue) == 0
is_empty fonksiyonu: Kuyruğun boş olup olmadığını kontrol eder. Eğer kuyruğun uzunluğu sıfırsa, kuyruk boştur.
Graph Yapısı (Graf)

class Graph:
    def __init__(self):
        self.graph = {}
Graph sınıfı: Graf veri yapısını temsil eder. Graf, düğümler (node) ve bu düğümler arasındaki bağlantılardan oluşur.
graph: Bir sözlük (dictionary) olarak başlar, bu sözlükte anahtarlar (düğümler) ve değerler (bu düğümle bağlantılı olan diğer düğümler) tutulur.

def add_edge(self, topic, file_type):
    if topic not in self.graph:
        self.graph[topic] = []
    self.graph[topic].append(file_type)
add_edge fonksiyonu: İki düğüm arasındaki kenarı (bağlantıyı) ekler.
Eğer verilen topic (konu) henüz grafda yoksa, yeni bir liste oluşturulur. Ardından, file_type bu listeye eklenir.

def get_edges(self, topic):
    return self.graph.get(topic, [])
get_edges fonksiyonu: Belirtilen bir topic için bağlantılı olan tüm file_type değerlerini döndürür. Eğer o topic grafda yoksa, boş bir liste döndürür.
Dosya Türleri (Array)

class FileTypes:
    def __init__(self):
        self.file_types = ["HTML", "PDF", "Word", "PNG"]
FileTypes sınıfı: Desteklenen dosya türlerini saklar.
file_types: Bu liste, kullanıcıların seçebileceği dosya türlerini tutar. Başlangıçta "HTML", "PDF", "Word", "PNG" türleri tanımlanmış.

def get_file_types(self):
    return self.file_types
get_file_types fonksiyonu: file_types listesindeki tüm dosya türlerini döndürür.
Özet
Bu kodda, LinkedList, Stack, Queue, Graph ve FileTypes sınıflarının her biri kendi başına bir veri yapısını ve işlevini temsil eder. Bağlantılı liste, yığın, kuyruk, graf ve dosya türleriyle ilgili temel işlemleri (ekleme, çıkarma, sorgulama) gerçekleştirebileceğiniz işlevler sağlar.
