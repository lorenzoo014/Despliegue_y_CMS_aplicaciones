**Explicacion del paso 7**
Aclaración sudo es una instrucción que corresponde con "Super User DO" para referirse al administrador
                1. sudo apt update
                2. sudo apt install nginx
                        Para crear un nuevo archivo de host virtual voy a utilizar el editor "nano"
                3. sudo nano /etc/nginx/sites-available/example.com.conf
        Luego establece las directivas de Nginx para que reenvíe las solicitudes a Apache agregando el siguiente server {...} y bloques de location:
                4. server {
                                listen      80;
                                server_name example.com www.example.com;
                                index       index.php;
                                root        /var/www/example.com/public    # fallback for index.php
                                location / {
                                try_files $uri $uri/ /index.php?$query_string;
                                }location /blog {
                                proxy_pass http://blog.domain.com;proxy_http_version#Habróa que ubicarlo en la paguina correspondiente                 1.1;
                                proxy_cache_bypass                 $http_upgrade;

                                # Proxy headers
                                proxy_set_header Upgrade           $http_upgrade;
                                proxy_set_header Connection        "upgrade";
                                proxy_set_header Host              $host;
                                proxy_set_header X-Real-IP         $remote_addr;
                                proxy_set_header X-Forwarded-For   $proxy_add_x_forwarded_for;
                                proxy_set_header X-Forwarded-Proto $scheme;
                                proxy_set_header X-Forwarded-Host  $host;
                                proxy_set_header X-Forwarded-Port  $server_port;

                                # Proxy timeouts
                                proxy_connect_timeout              60s;
                                proxy_send_timeout                 60s;
                                proxy_read_timeout                 60s;
                                }
                5.Guarda el archivo en el host virtual:
                        sudo ln -s /etc/nginx/sites-available/example.com.conf /etc/nginx/sites-enabled/example.com.conf
                6. Prueba gnix -->sudo nginx -t