# Clojure-nginx quick start/ setup
Quick Clojure-Nginx server setup with ssh file 

I created a quick and easy start for Clojure-Nginx server on Ubuntu 14.04 Trusty. Around 50 steps in 1. If you don't want to create manually that is a great start. I added lein2, MongoDB, Redis for session handling, plus Nginx-Clojure package if you want to compile custom Nginx setup. 

If you installed `lein` before this, please use this code:
```
lein -v
whereis lein
sudo mv [[whatyougetURL]] [[whatyougeturl]]1
```
Start the setup process run these lines:
``` ruby
sudo apt-get install git
git clone https://github.com/damesek/clojure-nginx-setup-ssh.git
cd clojure-nginx-setup-ssh
sudo sh nginx-clojure-server-setup.ssh
```
When the script will finish (few Y, agree etc), check your IP address/ or your domain: 
- YOURIP:8080/clojure or YOURIP:8080
- domain:8080

Your Clojure-Nginx server is running now! 

Put your project in the main folder. Do you need to drop uberjar compiled jars in the jars folder and you can reload the server with `./nginx -s reload`.  

Have a nice day!
