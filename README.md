# What is rocketchat-swarm
It is a docker swarm that runs rocketchat with the rocketchat hubot

# Requirements
Make sure you have this setup and installed **https://github.com/czadikem/core**

# rocketchat-swarm Install
1.  ```git clone https://github.com/czadikem/rocketchat-swarm.git```
2.  ```cd rocketchat-swarm```
3.  # I had to put these in this github repository so github would not remove these folders
    * ```rm data/db/blank.txt```
    * ```rm scripts/blank.txt```
    * ```rm uploads/blank.txt```
5.  ```cp .env.template .env```
6.  ```nano .env```  Put your hostname for rocketchat in this file along with your mail_url if you have one otherwise leave it as the default.  Also "You can get three free hostnames from noip"

# rocketchat-swarm Deployment
1.  ```docker stack deploy -c <(docker-compose config) rocketchat``` **You must be in the rocketchat-swarm folder for this to work**

# rocketchat-swarm Stop
1.  ```docker stack down rocketchat```

# Acknowledgments
Thanks to the wonderful people that made and maintain Rocketchat https://github.com/RocketChat/Rocket.Chat/ along with there docker-compose.yml https://github.com/RocketChat/Rocket.Chat/blob/develop/docker-compose.yml and thanks too Oscar at https://silkky.cloud/ for helping me learn, setup and understand docker swarm

