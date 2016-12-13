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
