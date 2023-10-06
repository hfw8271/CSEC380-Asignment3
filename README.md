# CSEC380-Asignment3
This is for Web App Security, building 3 docker containers, a DVWA, nginx reverse proxy w/ ssl, and a modsecurity nginx container

Intended for use on linux Ubuntu distro, other distros may require other commands to work but the docker containers will work the same.

How to use:

1) install this repository, keep all files in the same directory
2) run, sudo apt-get update
3) run, sudo apt-get install docker
4) run, sudo apt-get install docker-compose
5) run, sudo docker-compose up -d

6) Congrats now all docker containers should be running, to verify run, sudo docker ps and all three containers should be listed

7) to access DVWA via the nginx ssl reverse proxy, open firefox (or your browser) and go to "https://localhost" this will connect you to the DVWA via the nginx ssl reverse proxy
8) to access DVWA via the modsecurity reverse proxy, open firefox (or your browser) and go to "http://localhost" this will connect you to the DVWA via the modsecurity reverse proxy
