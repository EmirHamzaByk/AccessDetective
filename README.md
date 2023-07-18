# AccessDetective
 
Bu Python kodu, bir hedef URL üzerinde belirli bir liste içinde bulunan olası yönetici panellerini kontrol etmek için kullanılır. İşleyişini aşağıda açıklıyorum:

İlk olarak, kullanıcıdan hedef URL'yi girmesi istenir.

Ardından, bir sayacı ve sonuçları kaydetmek için "AdminPanel.txt" adında bir dosyayı tanımlarız.

Daha sonra, bir liste oluşturulur. Bu liste, potansiyel yönetici paneli adreslerini içerir.

"liste" üzerinde döngü başlatılır ve her bir öğe için aşağıdaki adımlar gerçekleştirilir:

**A. **Hedef URL ile "birles" adında bir tam URL oluşturulur.

**B.** requests.get() yöntemi kullanılarak ilgili URL'ye bir istek gönderilir ve yanıt alınır.

**C.** Yanıt durum kodu (status_code) kontrol edilir:
Eğer 200 ise, bir yönetici paneli bulunduğu sonucuna varılır. Bu durumda, sonuç hem ekrana yazdırılır hem de "AdminPanel.txt" dosyasına eklenir.

Eğer 403 ise, erişimin engellendiği sonucuna varılır ve ilgili URL ekrana yazdırılır.

Eğer 404 ise, bir yönetici paneli bulunamadığı sonucuna varılır ve ilgili URL ekrana yazdırılır.

**D.** Her bir istek için sayacı güncelleriz.

Son olarak, sayacın değerine göre sonuçları ekrana ve "AdminPanel.txt" dosyasına yazdırırız.
Bu kodun iki versiyonu vardır. Birincisi, "**lite**" versiyonunda istekler tek tek denendiği için daha yavaş olabilir. Diğer sürümde ise bütün istekler tek seferde denendiği için daha hızlı olabilir. Hangi versiyonu kullanmak istediğinizi seçebilirsiniz.
