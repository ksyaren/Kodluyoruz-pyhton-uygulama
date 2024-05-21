# Öklid Mesafesi Hesaplama Programı
Bu Python programı, iki boyutlu uzaydaki noktalar arasındaki Öklid mesafelerini hesaplar ve minimum mesafeyi bulur.

![Alt metin](https://lh7-us.googleusercontent.com/nPfCm5iIpBSZ046cFX6_nigXzWzp5ZEy5IqwCyf0Tw4DH8eeDhjz9bX05y0pT03gurzg6dulaObb7-o7wuevBBySG1xCIzkkM91EqqgDvFKPJc_V40bbT3Se9qt4EDBreCLOlugrMdBbvDVnr79vzo4)

## Öklid Mesafesi Hesaplama: 
İki nokta arasındaki Öklid mesafesini hesaplar.
## Mesafe Listesi Oluşturma: 
Bir liste içindeki tüm nokta çiftleri arasındaki mesafeleri hesaplar.
## Minimum Mesafe Bulma: 
Hesaplanan mesafeler arasındaki en küçük mesafeyi bulur ve ekrana yazdırır.


## Kod Açıklaması
Program dört ana bölümden oluşmaktadır:

Öklid Mesafesi Hesaplayan Fonksiyon:

import math

def euclideanDistance(point1, point2):
    return math.sqrt((point2[0] - point1[0])**2 + (point2[1] - point1[1])**2)
    
- euclideanDistance fonksiyonu, iki nokta arasındaki Öklid mesafesini hesaplar. math.sqrt fonksiyonunu kullanarak mesafenin karekökünü alır.

## Noktaların Tanımlanması:

points = [(1, 2), (4, 6), (7, 8), (2, 1), (9, 3)]

- points adında bir liste oluşturulmuş ve bu liste, iki boyutlu uzaydaki noktaları temsil eden demetleri (tuple) içerir.

## Mesafelerin Hesaplanması:

distances = []
for i in range(len(points)):
    for j in range(i + 1, len(points)):
        distance = euclideanDistance(points[i], points[j])
        distances.append(distance)
        
- Bu bölümde, points listesindeki her nokta çifti arasındaki mesafeler hesaplanır ve distances adındaki listeye eklenir.

## Minimum Mesafenin Bulunması:
min_distance = min(distances)
print(f"Minimum mesafe: {min_distance}")

- distances listesinden minimum mesafe bulunur ve ekrana yazdırılır.
