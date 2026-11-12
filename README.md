# borcumne.com.tr — web sitesi

Premium tasarımlı statik site: yalnız HTML, CSS, kendi sunucusunda barındırılan yazı tipleri (Fraunces, Inter) ve görseller. JavaScript, çerez, analiz veya reklam yok (gizlilik politikasıyla uyumlu). Her barındırmada çalışır.

| Adres | Dosya | App Store Connect'te |
|---|---|---|
| https://borcumne.com.tr/ | `index.html` | Pazarlama adresi |
| https://borcumne.com.tr/gizlilik/ | `gizlilik/index.html` | Gizlilik politikası adresi |
| https://borcumne.com.tr/destek/ | `destek/index.html` | Destek adresi |
| https://borcumne.com.tr/kosullar/ | `kosullar/index.html` | (isteğe bağlı) Kullanım koşulları |
| https://borcumne.com.tr/rehber/ | `rehber/index.html` + 20 yazı | — |

## Yükleme

**A. Alan adını aldığın firmada hosting varsa (cPanel/Plesk):** Dosya Yöneticisi'nde `public_html` klasörüne bu klasörün **içindekileri** (index.html, stil.css, fonts/, img/, rehber/, gizlilik/, destek/, kosullar/, 404.html, robots.txt, sitemap.xml) yükle. SSL (Let's Encrypt) açık olsun; adres https ile açılmalı.

**B. Hosting yoksa (ücretsiz): Cloudflare Pages veya Netlify**
1. Hesap aç, "Deploy manually / Upload" seç, `borcumne-site.zip` dosyasını sürükle.
2. "Custom domain" bölümüne `borcumne.com.tr` ve `www.borcumne.com.tr` yaz.
3. Alan adını aldığın firmanın DNS panelinde, servisin gösterdiği kayıtları ekle (genellikle `www` için CNAME, kök alan adı için A/ALIAS kaydı). SSL kendiliğinden açılır.

## Yüklemeden önce
- `destek@borcumne.com.tr` posta kutusunu aç (alan adı firmasında e-posta yönlendirmesi de olur). Bu adres sitede, uygulamanın gizlilik ekranında ve App Store'da kullanılıyor.
- Gizlilik politikası ve kullanım koşulları taslak; hukuki gözden geçirme önerilir (S-04, S-37). Değişirse uygulamadaki metin de (`apps/mobile/lib/ui/screens/privacy.dart`) aynı şekilde güncellenmeli.
- Uygulama App Store'a çıkınca ana sayfadaki "Yakında App Store'da" düğmesi uygulama bağlantısıyla değiştirilir.

## Rehber (20 yazı)
- Yazılar `rehber/<konu>/index.html`; her birinde grafik (satır içi SVG), "Kısaca" kutusu, uyarı notu ve ilgili yazılar var. Paylaşım görselleri `rehber/img/01–20.png`.
- Rakamlar `docs/FINANCIAL_RULES.md`'deki kaynaklara dayanır (erişim 06.11.2026). TCMB faiz tavanları veya BDDK asgari ödeme oranları değişirse ilgili yazılar güncellenmeli: 1, 2, 3, 4, 5, 11, 16, 17.
- Site bir üretici betikle oluşturuldu (repoda `website/_kaynak/`); metin düzeltmesi küçükse doğrudan HTML'de yapılabilir.
