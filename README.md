sudo -i

yum update -y

sudo amazon-linux-extras install java-openjdk11 -y

sudo amazon-linux-extras install epel -y

sudo yum install daemonize -y

sudo wget -O /etc/yum.repos.d/jenkins.repo \https://pkg.jenkins.io/redhat-stable/jenkins.repo

sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io.key

sudo yum upgrade

sudo yum install jenkins -y

sudo service jenkins start

sudo service jenkins status

sudo cat /var/lib/jenkins/secrets/initialAdminPassword
