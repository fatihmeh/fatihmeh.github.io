---
layout: post
title: Zeki Müren de bizi görecek mi?
date: 2019-07-03
lang: TR
---


*İlk olarak Teknoseyir.com'da yayınlanmıştır.*


[https://teknoseyir.com/blog/zeki-muren-de-bizi-gorecek-mi](https://teknoseyir.com/blog/zeki-muren-de-bizi-gorecek-mi)
<br>
<br>
<hr>
<br>
Online gizliliğimizi korumak adına yapmaya çalıştığımız şeylerin ne kadarı etkili olduğu hakkında bir yazı hazırladım. Çoğunlukla web odaklı konulardan bahsediyorum ve geliştirici olmadığım için bu yapıları entegre etmenin olumlu-olumsuz değerlendirmesini yapamıyorum. Burada maliyet, performans, güvenlik gibi birçok faktör işin içinde, tez yazılabilecek mevzular bunlar. Bir noktaya kadar insanlar kendilerinden alınan bilgiler için hassas davranabiliyorlar. Fakat göz göre göre yapılmıyorsa ardından giden olmayacaktır.
<br>
<br>
Yazdığım her şey kendi fikirlerim çerçevesindedir. Eksik veya yanlış bilgi varsa düzeltmekten çekinmeyin lütfen.
<br>
<br>
### Bizi takip edenlerin izlediği yollar
<br>
1- <ins>Fingerprinting</ins> (1)(2)(3)
<br>
*Her bir tarayıcının veya cihazın web erişiminde bir kimliği mevcut. PC gibi karmaşık platformlar kullanıcıların kullanım tarzıyla değiştiği için sahip oldukları kimlik de değişiyor. Hepsini maddelemek yerine ⋅⋅⋅ ekran görüntüsü koydum. Javascript çalışır halde olduğu takdirde(kapatmak internette gezememek demek) yüklü font listesine kadar ulaşabilme ihtimali kimlik tanımlamasına karşı durmayı baya zorlaştırıyor.*
<br>
<br>
![](https://teknoseyir.com/wp-content/uploads/2019/05/63b5d4660c75003.png)
<br>
*Figür 1*
<br>
<br>
2- <ins>IP tanımlaması</ins> (İnternete çıkış adresiniz vpn'siz kabak gibi ortada)
<br>
<br>
3- <ins>Webrtc ile bağlı olduğumuz ağ içinde cihazımızın lokal tanımlaması (192.168.1.50 gibi)</ins>
<br>
*Kendinize özenle bir alan oluşturmuş olsanız bile lokal ip adresiniz açıkta kalabiliyor doğru uygulamaları kullanmazsanız(Chrome).*
<br>
<br>
4- <ins>Profillendirme (Her tuş basımının takibi, sitelere erişme sıklığı vb.)</ins>(4)
<br>
*Yapay zeka resim çizebillecek konuma geldi ve gerekli bilgiler verildiğinde kişileri eriştiği adresler ve nicesi neticesinde rahatlıkla bulabilir diye tahmin ediyorum. Yapay zeka veya başka bir yöntem olabilir bu.*
<br>
<br>
![](https://teknoseyir.com/wp-content/uploads/2019/05/cba60b01bc99d97.png)
<br>
*Figür 2*(5)
<br>
<br>
<br>
### Masaüstü platformda gizliliğe ulaşmak için izlediğimiz yollar
<br>
1- <ins>Vpn</ins>
<br>
*Log tutmayan(6) , kill switch özelliği olan, ortak surveillance ağına ait olmayan (Fourteen Eyes(7)) bir vpn ile tarayıcı kimliğini koruyabildiğiniz durumda işe yarar. Eklentilerle parmak izi göz önünde olan, Webrtc kapatılamayan Dns sızdırmasına sebep olan tarayıcılar(Chrome) veya mobil platformlarda tam yetkinlik sağlamıyor. Örneğin Teknoseyir'e kullanıcı girşi yapmadan Vpn bağlı ve bağlı olmadan girince aynı olan bilgiler karşılaştırılarak hedef bulunabilir.*
<br>
<br>
2- <ins>Sadece tarayıcı tabanlı koruma</ins>
<br>
*Ağ kimiliğinizi saklamadığınız müddetçe kısıtlı miktarda işe yarar. Data toplayan şirketlerin özel hedefleri var mı yok mu bilmediğimiz için veri yığınları arasında ne kadar önem arz ettiğiniz bir soru işareti. Çoğunluğun kanıksadığı bir durum olsaydı gizlilk bu yöntem daha çok öneme sahip olurdu ve işe yarardı.*
<br>
<br>
2.a- <ins>Do not track</ins>
<br>
*Bazı siteler tarayıcıdan giden "beni takip etme" isteğini görüyor ve ona göre davranıyor. Fakat bu anlayış pek yaygın değil ve korunmaktan çok göze batan bir hareket olduğu için tercih edilmiyor.*
<br>
<br>
2.b- <ins>Eklentiler, engelleyiciler</ins>
<br>
*Ublock origin, Noscript, Privacy badger, User-Agent Switcher, CanvasBlocker gibi(8). Ağ kimliği açık olduğu sürece bir noktaya kadar işe yarar.*
<br>
<br>
2.c- <ins>Site izolasyonu (Firefox containers eklentisi, bazı özel ayarlar gibi.)</ins>(3)(9) 
<br>
<br>
2.d- <ins>Fingerprint datasına erişimi engellemek veya gerçek bilgileri değiştirmek</ins>(1)(2)
<br>
*Engellemektense yanlış bilgiler göndermek daha etkili gözüküyor.*
<br>
<br>
2.e- <ins>Javascript kapatmak veya her siteye özel erişimler ayarlamak</ins>(1)(2)
<br>
*Noscript gibi eklentiler ile güvendiğiniz adreslere erişim verebilirsiniz. Bir yerden sonra uğraşmak sıkıyor insanı.*
<br>
<br>
2.f- <ins>Özel ayarlar</ins> (10)
<br>
*Firefox tarayıcısının özelleştirilebilir ayarları ile sitelerin erişebildikleri bilgileri kısıtlamak mümkün. Elbette istediği bilgilere erişemeyen siteler buna göre bir profillendirme de yapabilir.*
<br>
<br>
3- <ins>Tor</ins>
<br>
*Fingerprint'e izin vermeyen, köprü(ara-bağlantı) kullanarak bağlantı sağlayan ve çoğu platformda olan bir uygulama. Ulaşılan köprülerin yetkili birimlerce oluşturulduğu ve kontrol edildiği durumlar söz konusu illegal olayları takip etmek için.*(11)
<br>
<br>
4- <ins>Özgür yazılım</ins> (12)
<br>
<br>
<br>
### Yaygın olarak yaptığımız konfigürasyonlar
<br>
1- <ins>Vpn kulanmadan tarayıcı ile her türlü bilgiyi korumaya çalışmak</ins>
<br>
*Data yığınları arasına girmemiş oluyorsunuz belki ama IP adresiniz görünür kalıyor.*
<br>
<br>
2- <ins>Vpn ile bağlantı sağlayarak fakat özelleştirilmiş tarayıcı kullanmak</ins>
<br>
*Servis sağlayıcılardan gizlenmek için ideal.*
<br>
<br>
3- <ins>Tor</ins>
<br>
*Gizlilik açısından en garanti bağlantı tipi olarak gösteriliyor fakat çok yavaş hızlar sunuyor.*
<br>
<br>
<br>
### Peki sonra?
<br>
Özelleştirilmiş reklamlar ile kişisel ilgilerimizin takip edildiğini biliyoruz. Sosyal medyalarda toplanan bilgi ile sosyal, siyasi tercihlerimize kadar yüksek doğruluk oranına sahip tahminlerde de bulunabildiklerini biliyoruz. Kendimiz hakkında yapamayacağımız yorumlar yapmaları da söz konusu(13). Bizi imite edecek çoğu bilgiye sahipler aslında.
<br>
<br>
Dünya simulasyonu yapılması mümkün mü acaba bu kadar veriyle?(14). Kişiye özel haberleri ne zaman görmeye başlarız? Bizi yönlendirmeye başladılar mı?(15)(16)
<br>
<br>
<br>
<br>
**Kaynakça**
<br>
1- [https://panopticlick.eff.org/privacy](https://panopticlick.eff.org/privacy)
<br>
2- [https://panopticlick.eff.org/about](https://panopticlick.eff.org/about)
<br>
3- [https://www.privacytools.io/browsers/](https://www.privacytools.io/browsers/)
<br>
4- [https://www.eff.org/deeplinks/2009/09/what-information-personally-identifiable](https://www.eff.org/deeplinks/2009/09/what-information-personally-identifiable)
<br>
5- [https://www.theguardian.com/technology/2018/mar/17/facebook-cambridge-analytica-kogan-data-algorithm](https://www.theguardian.com/technology/2018/mar/17/facebook-cambridge-analytica-kogan-data-algorithm)
<br>
6- [https://thatoneprivacysite.net/](https://thatoneprivacysite.net/)
<br>
7- [https://protonvpn.com/blog/5-eyes-global-surveillance/](https://protonvpn.com/blog/5-eyes-global-surveillance/)
<br>
8- [https://www.privacytools.io/browsers/#addons](https://www.privacytools.io/browsers/#addons)
<br>
9- [https://www.mozilla.org/tr/firefox/facebookcontainer/](https://www.mozilla.org/tr/firefox/facebookcontainer/)
<br>
10- [https://www.privacytools.io/browsers/#about_config](https://www.privacytools.io/browsers/#about_config)
<br>
11- [https://bridges.torproject.org/](https://bridges.torproject.org/)
<br>
12- [https://prism-break.org/tr/all/](https://prism-break.org/tr/all/)
<br>
13- [https://www.nytimes.com/2019/04/21/opinion/computational-inference.html](https://www.nytimes.com/2019/04/21/opinion/computational-inference.html)
<br>
14- [https://www.scientificamerican.com/article/are-we-living-in-a-computer-simulation](https://www.scientificamerican.com/article/are-we-living-in-a-computer-simulation)
<br>
15- [https://www.theguardian.com/news/2019/may/23/what-happened-when-i-met-my-islamophobic-troll](https://www.theguardian.com/news/2019/may/23/what-happened-when-i-met-my-islamophobic-troll)
<br>
16- [https://www.nytimes.com/2018/03/10/opinion/sunday/youtube-politics-radical.html?rref=collection%2Fcolumn%2Fzeynep-tufekci](https://www.nytimes.com/2018/03/10/opinion/sunday/youtube-politics-radical.html?rref=collection%2Fcolumn%2Fzeynep-tufekci)
