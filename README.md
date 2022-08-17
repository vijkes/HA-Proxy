# HA-Proxy Histroy


 1  yum install haproxy

    5  vim my.key
  
    8  chmod 400 my.key

   10  ssh -i my.key ec2-user@172.31.42.49
   
   11  rpm -q haproxy
   
   
   12  vim /etc/haproxy/haproxy.cfg
   
   13  npm install express

   15  node -e "console.log('Running Node.js ' + process.version)"
   
   16  curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.34.0/install.sh | bash
   
   17  . ~/.nvm/nvm.sh
   
   18  nvm install --lts
   
   19  node -e "console.log('Running Node.js ' + process.version)"
   
   20  mkdir /app
   
   21  cd /app/
   
   22  npm install express
   
   23  vim server.js

   26  vim mylb.cfg
   
   27  haproxy -f mylb.cfg -c
   
   28  ip addr
   
   
  
   32  ip a

   34  vim mylb.cfg
   
   35  haproxy -f mylb.cfg -c
   
   36  node server.js &

   43  haproxy -f mylb.cfg
