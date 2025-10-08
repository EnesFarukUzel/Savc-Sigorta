# Domain ve DNS Ayarları

## Domain Satın Alma

### Önerilen Domain Sağlayıcıları
1. **Natro** - 80-120 TL/yıl
2. **Hostinger** - 60-90 TL/yıl
3. **Turhost** - 70-100 TL/yıl

## DNS Ayarları

### Kendi Sunucunuz İçin DNS Ayarları

#### 1. A Record Ayarları
```
Type: A
Name: @
Value: YOUR_SERVER_IP
TTL: 3600

Type: A
Name: www
Value: YOUR_SERVER_IP
TTL: 3600
```

#### 2. CNAME Record (İsteğe Bağlı)
```
Type: CNAME
Name: savcisigorta
Value: yourdomain.com
TTL: 3600
```

### 3. MX Record (Email İçin)
```
Type: MX
Name: @
Value: mail.yourdomain.com
Priority: 10
TTL: 3600
```

## Port Yönlendirme (Router)

### Router Ayarları
1. **Router'a giriş yapın** (192.168.1.1)
2. **Port Forwarding** bölümüne gidin
3. **Aşağıdaki ayarları ekleyin:**

```
Port 80 -> 192.168.1.XXX (Bilgisayar IP'si)
Port 443 -> 192.168.1.XXX (Bilgisayar IP'si)
Port 22 -> 192.168.1.XXX (SSH için)
```

### Dinamik IP Sorunu
```bash
# No-IP veya DuckDNS kullanın
# Ücretsiz dinamik DNS servisi
# Otomatik IP güncelleme
```

## SSL Sertifikası

### Let's Encrypt (Ücretsiz)
```bash
# Certbot kurulumu
sudo apt install certbot -y

# SSL sertifikası alın
sudo certbot certonly --standalone -d yourdomain.com

# Nginx konfigürasyonu
sudo nano /etc/nginx/sites-available/default
```

### Nginx SSL Konfigürasyonu
```nginx
server {
    listen 80;
    server_name yourdomain.com www.yourdomain.com;
    return 301 https://$server_name$request_uri;
}

server {
    listen 443 ssl;
    server_name yourdomain.com www.yourdomain.com;
    
    ssl_certificate /etc/letsencrypt/live/yourdomain.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/yourdomain.com/privkey.pem;
    
    root /var/www/html;
    index index.html;
    
    location / {
        try_files $uri $uri/ =404;
    }
}
```

## Güvenlik Ayarları

### Firewall Kurulumu
```bash
# UFW kurulumu
sudo apt install ufw -y

# Firewall ayarları
sudo ufw default deny incoming
sudo ufw default allow outgoing
sudo ufw allow ssh
sudo ufw allow 80
sudo ufw allow 443
sudo ufw enable
```

### Fail2ban Kurulumu
```bash
# Fail2ban kurulumu
sudo apt install fail2ban -y

# Konfigürasyon
sudo nano /etc/fail2ban/jail.local
```

## Yedekleme Stratejisi

### Otomatik Yedekleme
```bash
# Crontab ile günlük yedekleme
0 2 * * * tar -czf /backup/website-$(date +\%Y\%m\%d).tar.gz /var/www/html/
```

### Cloud Yedekleme
```bash
# Google Drive, Dropbox veya OneDrive
# rclone ile otomatik yedekleme
```

## Performans Optimizasyonu

### Nginx Optimizasyonu
```nginx
# Gzip sıkıştırma
gzip on;
gzip_types text/plain text/css application/json application/javascript text/xml application/xml;

# Cache ayarları
location ~* \.(jpg|jpeg|png|gif|ico|css|js)$ {
    expires 1y;
    add_header Cache-Control "public, immutable";
}
```

## Monitoring ve Loglar

### Log Takibi
```bash
# Nginx logları
tail -f /var/log/nginx/access.log
tail -f /var/log/nginx/error.log

# Sistem logları
journalctl -u nginx -f
```

### Uptime Monitoring
```bash
# Uptime Robot (ücretsiz)
# Pingdom (ücretli)
# StatusCake (ücretsiz)
```
