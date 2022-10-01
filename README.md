# htpc

1. PLEX will have to be installed natively and configured to use your [PATH TO MEDIA FILES] as Libraries

2. Your domain will need to be transferred to cloudflare if it's not already hosted there. For CLOUDFLARE DDNS Docker - refer to: https://hub.docker.com/r/oznu/cloudflare-ddns/

3. This setup uses cloudflare proxy so you will need to generate a Origin Certificate and copy it into config/haproxy/origin-server.pem and turn on Full(strict) mode in SSL/TLS for your domain - refer to: https://developers.cloudflare.com/ssl/origin-configuration/origin-ca/

4. Add your domain and local static IP (it will need to be configured manually on your router and have portfowarding set up for port 80 and 443) to haproxy.cfg in the config folder

5. Configure Jackett, Radarr, Sonarr, qBitTorrent and Portainer accordingly via [SERVICE].[YOUR DOMAIN] urls. Default backend will be your plex server.

6. This repo uses docker-compose. Change all neccesary sections in docker-compose.yml (adding VPN username/passowords, adding domain API key and domain name and etc.) then cd into the repo directory in your terminal and execute '$ docker-compose up -d'