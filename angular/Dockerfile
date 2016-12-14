from node:6

user root
run apt-get update -y
run apt-get install -y vim sudo
run echo "node    ALL=(ALL:ALL) NOPASSWD: ALL" >> /etc/sudoers
run npm install -g angular-cli
run apt-get install -y tmux
env TERM=xterm-256color
run su -c 'ng new angular-template' - node
run su -c 'cd angular-template && ng build' - node
run apt-get install -y openssh-server rsyslog man
run yes | xargs -i echo password | passwd node
run apt-get install -y apache2
workdir /etc/apache2/mods-enabled
run ln -s ../mods-available/userdir.* .
run su -c 'ng completion >> .bashrc' - node
run npm install -g cordova ionic
run su -c 'ionic start ionic-template' - node
run su -c 'cd ionic-template && ionic build browser' - node
run su -c 'git clone https://github.com/niwenhao/myhome.git' - node
run su -c 'ls -d myhome/_* | while read f; do ln -s $f .${f#*_}; done' - node
cmd bash -c 'service rsyslog start; service ssh start; service cron start; service apache2 start; tail -f /var/log/auth.log'
