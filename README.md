# clojure-nginx-setup-ssh
Quick Clojure-Nginx server setup with ssh file 

I created a quick ssh for Clojure-Nginx server setup for Ubuntu 14.04 Trusty. Around 40 steps in 1. ;)
Update: I added lein2, MongoDB, plus Redis for session handling. 

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
