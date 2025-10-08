# Savcı Sigorta - Kurumsal Web Sitesi

Modern, responsive ve profesyonel bir sigorta acente web sitesi.

## 🎨 Özellikler

- **Modern Tasarım**: Siyah ve kırmızı renk temasıyla profesyonel görünüm
- **Tam Responsive**: Tüm cihazlarda (mobil, tablet, desktop) mükemmel görüntüleme
- **Animasyonlu İçerik**: Scroll animasyonları ve geçiş efektleri
- **İnteraktif Öğeler**: Hover efektleri ve kullanıcı etkileşimleri
- **İletişim Formu**: Doğrulama özellikli form sistemi
- **Performans Optimizasyonu**: Hızlı yükleme ve akıcı performans
- **SEO Uyumlu**: Arama motorları için optimize edilmiş yapı

## 📋 Bölümler

1. **Ana Sayfa (Hero)**: Çarpıcı giriş bölümü
2. **İstatistikler**: Şirket başarılarını gösteren sayaç animasyonları
3. **Hizmetler**: 8 farklı sigorta hizmeti kartları
4. **Hakkımızda**: Şirket bilgileri ve özellikler
5. **Referanslar**: Müşteri yorumları
6. **İletişim**: Bilgi kartları ve iletişim formu
7. **Footer**: Sosyal medya ve site haritası

## 🚀 Kullanılan Teknolojiler

- **HTML5**: Semantic ve modern HTML yapısı
- **CSS3**: 
  - CSS Grid ve Flexbox
  - Animasyonlar ve geçişler
  - Gradient'ler ve efektler
  - Responsive Media Queries
- **JavaScript (Vanilla)**:
  - Intersection Observer API
  - Smooth scroll
  - Form validasyonu
  - Counter animasyonları
  - Mobile menu toggle
- **Font Awesome**: İkonlar için

## 📦 Kurulum

1. Projeyi bilgisayarınıza indirin veya klonlayın:
```bash
git clone [repository-url]
```

2. Proje klasörüne gidin:
```bash
cd "Savcı Sigorta"
```

3. `index.html` dosyasını bir web tarayıcısında açın veya bir local server kullanın:

### Local Server Seçenekleri:

**Python ile:**
```bash
# Python 3
python -m http.server 8000

# Python 2
python -m SimpleHTTPServer 8000
```

**Node.js ile (http-server):**
```bash
npx http-server -p 8000
```

**VS Code Live Server:**
- VS Code'da Live Server eklentisini yükleyin
- index.html dosyasına sağ tıklayıp "Open with Live Server" seçeneğini seçin

4. Tarayıcınızda `http://localhost:8000` adresine gidin

## 📁 Dosya Yapısı

```
Savcı Sigorta/
│
├── index.html          # Ana HTML dosyası
├── styles.css          # Tüm CSS stilleri
├── script.js           # JavaScript fonksiyonları
└── README.md           # Proje dokümantasyonu
```

## 🎯 Özelleştirme

### Renk Teması Değiştirme

`styles.css` dosyasındaki CSS değişkenlerini düzenleyin:

```css
:root {
    --primary-color: #DC143C;      /* Ana kırmızı renk */
    --secondary-color: #8B0000;    /* Koyu kırmızı */
    --dark-color: #0a0a0a;         /* Ana siyah */
    --light-dark: #1a1a1a;         /* Açık siyah */
}
```

### İletişim Bilgilerini Güncelleme

`index.html` dosyasında iletişim bölümünü bulun ve bilgilerinizi girin:

```html
<!-- Telefon -->
<p>+90 212 XXX XX XX</p>

<!-- E-posta -->
<p>info@savcisigorta.com</p>

<!-- Adres -->
<p>Merkez Mahallesi, Atatürk Caddesi No:123</p>
```

### Logo ve Görsel Ekleme

Şu anda görsel placeholder'lar kullanılmaktadır. Gerçek görseller eklemek için:

1. Görselleri bir `images/` klasörüne koyun
2. HTML'de placeholder div'leri `<img>` etiketleriyle değiştirin
3. Lazy loading için `data-src` attribute'u kullanın

## 📱 Responsive Breakpoint'ler

- **Desktop**: 1200px ve üzeri
- **Tablet**: 768px - 1199px
- **Mobile**: 767px ve altı
- **Small Mobile**: 480px ve altı

## ✨ JavaScript Özellikleri

- **Scroll Animasyonları**: Elementler görünüme girdiğinde animate olur
- **Sayaç Animasyonları**: İstatistik sayıları yukarı doğru sayar
- **Sticky Navbar**: Scroll'da navbar küçülür ve sabitlenir
- **Active Link**: Hangi bölümde olduğunuzu gösterir
- **Smooth Scroll**: Yumuşak sayfa geçişleri
- **Form Validasyonu**: Gerçek zamanlı form kontrolü
- **Mobile Menu**: Hamburger menü sistemi
- **Scroll to Top**: Sayfanın başına dön butonu

## 🔧 Tarayıcı Desteği

- Chrome (son 2 versiyon)
- Firefox (son 2 versiyon)
- Safari (son 2 versiyon)
- Edge (son 2 versiyon)
- Opera (son 2 versiyon)

## 📈 Performans İpuçları

1. **Görselleri Optimize Edin**: WebP formatı kullanın
2. **CDN Kullanın**: Font Awesome için CDN aktif
3. **Minify Edin**: Production için CSS ve JS dosyalarını minify edin
4. **Caching**: Browser caching ayarlarını yapın
5. **Lazy Loading**: Görseller için lazy loading kullanın

## 🎨 Tasarım Özellikleri

### Renk Paleti
- **Primary Red**: `#DC143C` - Dikkat çekici vurgular
- **Dark Red**: `#8B0000` - Gradient'ler ve gölgeler
- **Black**: `#0a0a0a` - Ana arka plan
- **Light Black**: `#1a1a1a` - Kartlar ve bölümler
- **White**: `#ffffff` - Metin
- **Gray**: `#cccccc` - İkincil metin

### Typography
- Font Family: Segoe UI, Tahoma, Geneva, Verdana, sans-serif
- Başlıklar: Bold, büyük boyutlar
- Paragraflar: Normal ağırlık, okunabilir satır yüksekliği

### Animasyonlar
- Fade In Up: Elementler aşağıdan yukarı belirir
- Bounce: Scroll down ikonu zıplar
- Shine: Placeholder görselde parlama efekti
- Hover: Tüm interaktif elementlerde hover efektleri

## 📞 Form Entegrasyonu

Şu anda form sadece console'a yazdırıyor. Backend entegrasyonu için:

### Option 1: FormSpree
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

### Option 2: EmailJS
```javascript
// script.js içinde emailjs entegrasyonu
emailjs.send("service_id", "template_id", formData);
```

### Option 3: Kendi Backend'iniz
```javascript
fetch('/api/contact', {
    method: 'POST',
    headers: {'Content-Type': 'application/json'},
    body: JSON.stringify(formData)
});
```

## 🔒 Güvenlik

- Form validasyonu aktif
- XSS koruması için input sanitization önerilir
- HTTPS kullanımı önerilir
- CORS ayarlarını backend'de yapın

## 📝 Yapılacaklar (İsteğe Bağlı)

- [ ] Gerçek görseller ekleyin
- [ ] Backend/API entegrasyonu
- [ ] Blog bölümü ekleyin
- [ ] Çoklu dil desteği
- [ ] PWA (Progressive Web App) yapın
- [ ] Google Analytics entegrasyonu
- [ ] Live chat widget
- [ ] Online poliçe teklif formu
- [ ] Admin paneli

## 🤝 Katkıda Bulunma

1. Fork edin
2. Feature branch oluşturun (`git checkout -b feature/AmazingFeature`)
3. Değişikliklerinizi commit edin (`git commit -m 'Add some AmazingFeature'`)
4. Branch'inizi push edin (`git push origin feature/AmazingFeature`)
5. Pull Request açın

## 📄 Lisans

Bu proje MIT lisansı altındadır.

## 👨‍💻 Geliştirici

Savcı Sigorta için özel olarak geliştirilmiştir.

## 📞 Destek

Herhangi bir sorun veya öneriniz için iletişime geçin:
- E-posta: info@savcisigorta.com
- Telefon: +90 212 XXX XX XX

---

**Not**: Bu proje production'a almadan önce:
1. Tüm placeholder bilgileri gerçek bilgilerle değiştirin
2. Logo ve görselleri ekleyin
3. SEO meta tag'lerini optimize edin
4. Analytics kodlarını ekleyin
5. SSL sertifikası edinin
6. Güvenlik önlemlerini alın
7. Form backend'ini kurun
8. Test edin (mobil, tablet, desktop)
9. Performans testleri yapın
10. Tarayıcı uyumluluğunu kontrol edin

## 🎉 Teşekkürler

Bu web sitesini kullandığınız için teşekkür ederiz!

