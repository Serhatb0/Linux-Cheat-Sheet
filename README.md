# npm run prod > /dev/null 2>&1 &

This command runs the npm run prod command in the background and redirects all standard output (stdout) to /dev/null. The 2>&1 statement directs the standard error output (stderr) to standard output (stdout). So no output will appear in the terminal.

# lsof -i :4321

Show Applications Running on port 4231 , if we want more than one we can sepaarete them witg , for Example :   lsof -i :4321 , 5321

# sudo tail -f /var/log/nginx/access.log

Nginx Loglarına Bakma:
Nginx, gelen isteklerin bir günlüğünü tutar. Bu günlük dosyalarını kontrol ederek hangi portlara gelen istekleri görebilirsiniz. Günlük dosyaları genellikle /var/log/nginx/ dizininde bulunur. 



# sudo nano /etc/nginx/sites-available/default

Nginx Konfigürasyonu:
Nginx'in varsayılan konfigürasyon dosyasını düzenlemek için bir metin düzenleyici kullanabilirsiniz.


# sudo nginx -t
Yapılandırmanın Geçerli Olmasını Sağlama

# sudo systemctl restart nginx
Nginx'i Yeniden Başlatma
