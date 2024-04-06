###  This command runs the npm run prod command in the background and redirects all standard output (stdout) to /dev/null. The 2>&1 statement directs the standard error output (stderr) to standard output (stdout). So no output will appear in the terminal.
```
npm run prod > /dev/null 2>&1 &
```


### Show Applications Running on port 4231 , if we want more than one we can sepaarete them witg , for Example :   lsof -i :4321 , 5321
```
lsof -i :4321
```


### Nginx, gelen isteklerin bir günlüğünü tutar. Bu günlük dosyalarını kontrol ederek hangi portlara gelen istekleri görebilirsiniz. Günlük dosyaları genellikle /var/log/nginx/ dizininde bulunur. 
```
 sudo tail -f /var/log/nginx/access.log
```




### Nginx'in varsayılan konfigürasyon dosyasını düzenlemek için bir metin düzenleyici kullanabilirsiniz.
```
sudo nano /etc/nginx/sites-available/default
```



### Yapılandırmanın Geçerli Olmasını Sağlama
```
 sudo nginx -t
```


### Nginx'i Yeniden Başlatma
```
 sudo systemctl restart nginx
```



### gizli dosyalrı gosterir
```
ls -a
```



### sudo apt install certbot && sudo certbot certonly --standalone -d your_domain.com
Ücretsiz bir SSL sertifikası oluşturmak için Let's Encrypt'in sunduğu Certbot'u kullanabilirsiniz. Certbot, hızlı ve kolay bir şekilde SSL sertifikası almanıza ve yapılandırmanıza yardımcı olur. Ubuntu'da Certbot'u kullanarak SSL sertifikası oluşturmak için aşağıdaki adımları izleyebilirsiniz
```
server {
    listen 443 ssl;
    server_name your_domain.com;
    ssl_certificate /etc/letsencrypt/live/your_domain.com/fullchain.pem;
    ssl_certificate_key /etc/letsencrypt/live/your_domain.com/privkey.pem;
    location / {
        proxy_pass http://localhost:3000;
        proxy_http_version 1.1;
        proxy_set_header Upgrade $http_upgrade;
        proxy_set_header Connection 'upgrade';
        proxy_set_header Host $host;
        proxy_cache_bypass $http_upgrade;
    }
}

```
