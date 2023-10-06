# CSEC380-Asignment3
This is for Web App Security, building 3 docker containers, a DVWA, nginx reverse proxy w/ SSL, and a ModSecurity nginx container

Intended for use on Linux Ubuntu distro, other distros may require other commands to work but the docker containers will work the same.

How to use:

1) install this repository, and keep all files in the same directory
2) run, sudo apt-get update
3) run, sudo apt-get install docker
4) run, sudo apt-get install docker-compose
5) run, sudo docker-compose up -d

6) Congrats now all docker containers should be running, to verify run, sudo docker ps, and all three containers should be listed

7) to access DVWA via the nginx SSL reverse proxy, open Firefox (or your browser) and go to "https://localhost" This will connect you to the DVWA via the nginx SSL reverse proxy
8) to access DVWA via the ModSecurity reverse proxy, open Firefox (or your browser) and go to "http://localhost" This will connect you to the DVWA via the ModSecurity reverse proxy



Other notes:
This environment is intended for a class, please do not use this in a real-world environment
SSL cert and key are provided here, for better security it is recommended to self-sign your own keys (steps below) or get your keys signed by a trusted certificate authority

self-signed SSL: keys:
1) sudo apt-get update
2) sudo apt-get install openssl
3) sudo openssl genpkey -algorithm RSA -out SERVER.key -aes256           (replace SERVER with your key name)
4) sudo openssl req -new -x509 -days 365 -key SERVER.key -out SERVER.crt (replace SERVER with your cert and key name)
