from node:6

user root
run apt-get update -y
run apt-get install -y vim sudo
run echo "node    ALL=(ALL:ALL) NOPASSWD: ALL" >> /etc/sudoers
run npm install -g angular-cli
run apt-get install -y tmux
env TERM=xterm-256color
run su -c 'ng new template' - node
run su -c 'cd template && ng build' - node
run apt-get install -y openssh-server rsyslog man
run yes | xargs -i echo password | passwd node
run apt-get install -y apache2
workdir /etc/apache2/mods-enabled
run ln -s ../mods-available/userdir.* .
cmd bash -c 'service rsyslog start; service ssh start; service apache2 start; tail -f /var/log/auth.log'
