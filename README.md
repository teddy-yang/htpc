# htpc

1. PLEX will have to be installed natively and configured to use your <PATH TO MEDIA FILES> as Libraries

2. Your domain will need to be transferred to cloudflare if it's not already hosted there. For CLOUDFLARE DDNS Docker - refer to: https://hub.docker.com/r/oznu/cloudflare-ddns/

3. Add your domain and local static IP (it will need to be configured manually on your router and have portfowarding set up for port 80 and 443) to haproxy.cfg in the config folder

4. Configure Jackett, Radarr, Sonarr and qBitTorrent accordingly via <SERVICE>.<YOUR DOMAIN> urls

5. This repo uses docker-compose, so cd into the repo directory in your terminal and execute '$ docker-compose up -d'