# nginx


- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo apt update && sudo apt install nginx -y</button> Install Nginx
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl start nginx && sudo systemctl enable nginx</button> Start Nginx
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo chmod o+rx /home/danny &&
sudo chmod o+rx /home/danny/Documents &&
sudo chmod o+rx /home/danny/Documents/Projects &&
sudo chmod -R 755 /home/danny/Documents/Projects/website</button> give permission
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo chown -R danny:www-data /home/danny/Documents/Projects/website</button> change owner
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo nano /etc/nginx/sites-available/website</button> create nginx config
- <button onclick="navigator.clipboard.writeText(this.innerText)">server {
    listen 8004;
    server_name localhost;

    root /home/danny/Documents/Projects/website;
    index index.html;

    location / {
        try_files $uri $uri/ =404;
    }
}</button> nginx config input
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo ln -s /etc/nginx/sites-available/website /etc/nginx/sites-enabled/</button> Enable the site
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo nginx -t</button> Test config
- <button onclick="navigator.clipboard.writeText(this.innerText)">sudo systemctl restart nginx</button> Restart Nginx
- <button onclick="navigator.clipboard.writeText(this.innerText)">http://localhost:8004</button> Open in browser 


