
3. Kontrol Yapıları
Swift programlama dilinde, programın akışını kontrol etmek için çeşitli yapılar kullanılır. Bu yapılar, programın belirli koşullara göre farklı komutlar yürütmesini sağlar. Aşağıda, Swift'in kontrol yapıları detaylı bir şekilde açıklanmıştır.

3.1 If ve Else
Swift'te if ve else ifadeleri, belirli bir koşulun doğru olup olmadığını kontrol etmek için kullanılır. Koşul doğru ise if bloğu içindeki kodlar, yanlış ise else bloğu içindeki kodlar çalıştırılır.

Örnek Kullanım:
swift
Copy code
var yas = 20
if yas >= 18 {
    print("Reşit.")
} else {
    print("Reşit değil.")
}
3.2 Guard
guard ifadesi, if ifadesine benzer bir şekilde koşulları kontrol eder, ancak bir koşulun doğru olmadığı durumlarda erken çıkış sağlamak için kullanılır. guard'ın her zaman bir else bloğu olmalıdır, bu blok koşul yanlış olduğunda çalıştırılır.

Örnek Kullanım:
swift
Copy code
func kullaniciDogrula(kullaniciAdi: String?) {
    guard let kullaniciAdi = kullaniciAdi else {
        print("Kullanıcı adı girilmemiş.")
        return
    }
    print("Kullanıcı adı: \(kullaniciAdi)")
}
3.3 Switch
switch ifadesi, bir değişkenin birden fazla olası durumunu kontrol etmek için kullanılır. Her durum case anahtar kelimesi ile belirtilir ve switch ifadesi değişkenin değerine göre uygun case bloğunu çalıştırır.

Örnek Kullanım:
swift
Copy code
let meyve = "elma"
switch meyve {
case "muz":
    print("Bu bir muz.")
case "elma":
    print("Bu bir elma.")
default:
    print("Tanınmayan meyve.")
}
3.4 For-in Döngüsü
for-in döngüsü, bir koleksiyon (dizi, sözlük, aralık vs.) üzerinde yineleme yapmak için kullanılır. Her yinelemede koleksiyondan bir eleman alınır ve döngü içindeki kodlar bu eleman ile çalıştırılır.

Örnek Kullanım:
swift
Copy code
let sayilar = [1, 2, 3, 4, 5]
for sayi in sayilar {
    print(sayi)
}
3.5 While Döngüsü
while döngüsü, belirli bir koşul doğru olduğu sürece yürütülür. Koşul yanlış olduğunda döngü sona erer.

Örnek Kullanım:
swift
Copy code
var sayi = 5
while sayi > 0 {
    print(sayi)
    sayi -= 1
}
3.6 Repeat-While Döngüsü
repeat-while döngüsü, while döngüsüne benzer, ancak koşul döngünün sonunda kontrol edilir. Bu, döngü içindeki kodların en az bir kez çalıştırılmasını garanti eder.

Örnek Kullanım:
swift
Copy code
var counter = 5
repeat {
    print(counter)
    counter -= 1
} while counter > 0
3.7 Break ve Continue
break ifadesi, içinde bulunduğu döngüyü veya switch ifadesini derhal sonlandırır. continue ifadesi ise, döngünün mevcut yinelemesini sonlandırır ve döngünün bir sonraki yinelemesine geçer.

Örnek Kullanım:
swift
Copy code
for i in 1...10 {
    if i == 5 {
        break
    }
    print(i)
}

for i in 1...10 {
    if i % 2 == 0 {
        continue
    }
    print(i)
}
Swift'in kontrol yapıları, program akışını yönlendirmede esneklik ve güç sağlar. Uygun yapıları kullanarak, kodunuzu daha okunabilir, etkili ve hata yapma olasılığını azaltacak şekilde düzenleyebilirsiniz. Bu yapıların her birinin doğru kullanımı, Swift programlama becerilerinizi geliştirmenize yardımcı olacaktır.
