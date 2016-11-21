# clojure-nginx-setup-ssh
Quick Clojure-Nginx server setup with ssh file 

#!/bin/bash
#!/bin/bash
#

sudo apt-get install software-properties-common python-software-properties
sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java7-installer

cd $HOME

apt-get install git build-essential libreadline-dev  zlib1g-dev libpcre3 libpcre3-dev libncurses5-dev libpcre3-dev libssl-dev zlib1g-dev libpcrecpp0 perl make -y
sudo apt-get install zip unzip 

wget https://github.com/nginx-clojure/nginx-clojure/archive/v0.4.4.tar.gz
tar -zxvf v0.4.4.tar.gz
mv nginx-linux-x64 nginx 

sudo apt-get install libjpeg62 git-core
sudo apt-get install libfontconfig

cd /root/nginx-clojure-0.4.4/jars/
wget http://repo1.maven.org/maven2/org/clojure/clojure/1.8.0/clojure-1.8.0.zip
unzip clojure-1.8.0.zip

cd $HOME

wget http://nginx.org/download/nginx-1.10.1.tar.gz
tar -zxvf nginx-1.10.1.tar.gz
cd nginx-1.10.1
./configure --sbin-path=/etc/nginx/ --conf-path=/etc/nginx/nginx.conf --error-log-path=/var/log/nginx/error.log --http-log-path=/var/log/nginx/access.log --with-debug --with-pcre --with-http_ssl_module
make
sudo make install

cd $HOME
cd nginx-clojure-0.4.4
./nginx
