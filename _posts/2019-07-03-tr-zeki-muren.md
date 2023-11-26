---
layout: post
title: Zeki Müren de bizi görecek mi?
date: 2019-07-03
lang: TR
excerpt: Çevrimiçi hareketlerinizden kimliğinizin nasıl profillendirildiği ve detayları.
category: self legacy
---


Online gizliliğimizi korumak adına aldığımız aksiyonların ne kadarı etkili olduğu hakkında bir yazı hazırladım. Çoğunlukla web odaklı konulardan bahsediyorum ve geliştirici olmadığım için bu yapıları entegre etmenin olumlu-olumsuz değerlendirmesini yapamıyorum. Burada maliyet, performans, güvenlik gibi birçok faktör işin içinde, tez yazılabilecek mevzular bunlar. Bir noktaya kadar insanlar kendilerinden alınan bilgiler için hassas davranabiliyorlar. Fakat göz göre göre yapılmıyorsa ardından giden olmayacaktır.


<hr>


### Bizi takip edenlerin izlediği yollar

1- **Fingerprinting** *(1)(2)(3)*

*Her bir tarayıcının veya cihazın web erişiminde bir kimliği mevcut. PC gibi karmaşık platformlar kullanıcıların kullanım tarzıyla değiştiği için sahip oldukları kimlik de değişiyor. Hepsini maddelemek yerine ekran görüntüsü ekledim. Javascript çalışır halde olduğu takdirde(kapatmak internette gezememek demek) yüklü font listesine kadar ulaşabilme ihtimali kimlik tanımlamasına karşı durmayı ciddi anlamda zorlaştırıyor.*

![](/assets/figur-1.png){:class="img-responsive"}
*Figür 1*


2- **IP tanımlaması** (İnternete çıkış adresiniz vpn'siz kabak gibi ortada)


3- **Webrtc ile bağlı olduğumuz ağ içinde cihazımızın lokal tanımlaması** (192.168.1.50 gibi)

*Kendinize özenle bir alan oluşturmuş olsanız bile lokal ip adresiniz açıkta kalabiliyor doğru uygulamaları kullanmazsanız(Chrome).*


4- **Profillendirme** (Her tuş basımının takibi, sitelere erişme sıklığı vb.) *(4)*

*Yapay zeka resim çizebillecek konuma geldi ve gerekli bilgiler verildiğinde kişileri eriştiği adresler ve nicesi neticesinde rahatlıkla bulabilir diye tahmin ediyorum. Yapay zeka veya başka bir yöntem olabilir bu.*

![](/assets/figur-2.png){:class="img-responsive"}
*Figür 2 (5)*


<hr>


### Masaüstü platformda gizliliğe ulaşmak için izlediğimiz yollar

1- **Vpn**

*Log tutmayan (6), kill switch özelliği olan, ortak surveillance ağına ait olmayan (Fourteen Eyes*(7)*) bir vpn ile tarayıcı kimliğini koruyabildiğiniz durumda işe yarar. Eklentilerle parmak izi göz önünde olan, Webrtc kapatılamayan Dns sızdırmasına sebep olan tarayıcılar(Chrome) veya mobil platformlarda tam yetkinlik sağlamıyor. Örneğin bir siteye kullanıcı girşi yapmadan, Vpn bağlı ve bağlı olmadan girince aynı olan bilgiler karşılaştırılarak hedef bulunabilir.*


2- **Sadece tarayıcı tabanlı koruma**

*Ağ kimiliğinizi saklamadığınız müddetçe kısıtlı miktarda işe yarar. Data toplayan şirketlerin özel hedefleri var mı yok mu bilmediğimiz için veri yığınları arasında ne kadar önem arz ettiğiniz bir soru işareti. Çoğunluğun kanıksadığı bir durum olsaydı gizlilk bu yöntem daha çok öneme sahip olurdu ve işe yarardı.*


2.a- **Do not track**

*Bazı siteler tarayıcıdan giden "beni takip etme" isteğini görüyor ve ona göre davranıyor. Fakat bu anlayış pek yaygın değil ve korunmaktan çok göze batan bir hareket olduğu için tercih edilmiyor.*


2.b- **Eklentiler, engelleyiciler**

*Ublock origin, Noscript, Privacy badger, User-Agent Switcher, CanvasBlocker gibi *(8)*. Ağ kimliği açık olduğu sürece bir noktaya kadar işe yarar.*


2.c- **Site izolasyonu** (Firefox containers eklentisi, bazı özel ayarlar gibi.) *(3)(9)*


2.d- **Fingerprint datasına erişimi engellemek veya gerçek bilgileri değiştirmek** *(1)(2)*

*Engellemektense yanlış bilgiler göndermek daha etkili gözüküyor.*


2.e- **Javascript kapatmak veya her siteye özel erişimler ayarlamak** *(1)(2)*

*Noscript gibi eklentiler ile güvendiğiniz adreslere erişim verebilirsiniz. Bir yerden sonra uğraşmak sıkıyor insanı.*


2.f- **Özel ayarlar** *(10)*

*Firefox tarayıcısının özelleştirilebilir ayarları ile sitelerin erişebildikleri bilgileri kısıtlamak mümkün. Elbette istediği bilgilere erişemeyen siteler buna göre bir profillendirme de yapabilir.*

2.g- **Obfuscation** *(17)(18)*

*Online ortama aktardığımız verilerimizi karşı tarafın kullanamaması için gerçek dışı tıklamalar ile şaşırtma yöntemidir. Sadece aramalarda veya reklam tıklamlarında değil, cloud olarak yüklenilen her türlü trafik için yapılması ile ideal bir yöntem olabilir.*

3- **Tor**

*Fingerprint'e izin vermeyen, köprü(ara-bağlantı) kullanarak bağlantı sağlayan ve çoğu platformda olan bir uygulama. Ulaşılan köprülerin yetkili birimlerce oluşturulduğu ve kontrol edildiği durumlar söz konusu illegal olayları takip etmek için.(11)*


4- **Özgür yazılım** *(12)*


<hr>


### Yaygın olarak yaptığımız konfigürasyonlar

1- **Vpn kulanmadan tarayıcı ile her türlü bilgiyi korumaya çalışmak veya obfuscation**

*Data yığınları arasına girmemiş oluyorsunuz belki ama IP adresiniz görünür kalıyor. Şaşırtma(obfuscation) yöntemi ile toplanılan bilgilerin kullanılamaz hale getirilmesi işe yarayabilir.*


2- **Vpn ile bağlantı sağlayarak fakat özelleştirilmiş tarayıcı kullanmak**

*Servis sağlayıcılardan gizlenmek için ideal.*


3- **Tor**

*Gizlilik açısından en garanti bağlantı tipi olarak gösteriliyor fakat çok yavaş hızlar sunuyor.*


<hr>


### Peki sonra?

Özelleştirilmiş reklamlar ile kişisel ilgilerimizin takip edildiğini biliyoruz. Sosyal medyalarda toplanan bilgi ile sosyal, siyasi tercihlerimize kadar yüksek doğruluk oranına sahip tahminlerde de bulunabildiklerini biliyoruz. Kendimiz hakkında yapamayacağımız yorumlar yapmaları da söz konusu *(13)*. Bizi imite edecek çoğu bilgiye sahipler aslında.


Dünya simulasyonu yapılması mümkün mü acaba bu kadar veriyle? *(14)*. Kişiye özel haberleri ne zaman görmeye başlarız? Bizi yönlendirmeye başladılar mı? *(15)(16)*


<hr>


**Kaynakça**

1- [panopticlick.eff.org/privacy](https://panopticlick.eff.org/privacy){:target="_blank"}

2- [panopticlick.eff.org/about](https://panopticlick.eff.org/about){:target="_blank"}

3- [privacytools.io/browsers/](https://www.privacytools.io/browsers/){:target="_blank"}

4- [eff.org/.../what-information-personally-identifiable](https://www.eff.org/deeplinks/2009/09/what-information-personally-identifiable){:target="_blank"}

5- [theguardian.com/.../facebook-cambridge-analytica-kogan-data-algorithm](https://www.theguardian.com/technology/2018/mar/17/facebook-cambridge-analytica-kogan-data-algorithm){:target="_blank"}

6- [thatoneprivacysite.net/](https://thatoneprivacysite.net/){:target="_blank"}

7- [protonvpn.com/blog/5-eyes-global-surveillance/](https://protonvpn.com/blog/5-eyes-global-surveillance/){:target="_blank"}

8- [privacytools.io/browsers/#addons](https://www.privacytools.io/browsers/#addons){:target="_blank"}

9- [mozilla.org/tr/firefox/facebookcontainer/](https://www.mozilla.org/tr/firefox/facebookcontainer/){:target="_blank"}

10- [privacytools.io/browsers/#about_config](https://www.privacytools.io/browsers/#about_config){:target="_blank"}

11- [bridges.torproject.org/](https://bridges.torproject.org/){:target="_blank"}

12- [prism-break.org/tr/all/](https://prism-break.org/tr/all/){:target="_blank"}

13- [nytimes.com/.../computational-inference.html](https://www.nytimes.com/2019/04/21/opinion/computational-inference.html){:target="_blank"}

14- [scientificamerican.com/.../are-we-living-in-a-computer-simulation](https://www.scientificamerican.com/article/are-we-living-in-a-computer-simulation){:target="_blank"}

15- [theguardian.com/.../what-happened-when-i-met-my-islamophobic-troll](https://www.theguardian.com/news/2019/may/23/what-happened-when-i-met-my-islamophobic-troll){:target="_blank"}

16- [nytimes.com/.../youtube-politics-radical.html](https://www.nytimes.com/2018/03/10/opinion/sunday/youtube-politics-radical.html){:target="_blank"}

17- [https://adnauseam.io/](https://adnauseam.io/){:target="_blank"}

18- [http://trackmenot.io/.../trackmenot2009.pdf](http://trackmenot.io/resources/trackmenot2009.pdf){:target="_blank"}


<hr>


[Medium.com](https://link.medium.com/7QouqDIp32){:target="_blank"} üzerinde de erişilebilir.
