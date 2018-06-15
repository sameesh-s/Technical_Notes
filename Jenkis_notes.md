Installing Jenkins on Ubuntu
----------------------------
1. wget -q -O -https://pkg.jenkins.io/debian/jenkins.io.key | sudo apt-key add -
2. sudo sh -c 'echo deb http://pkg.jenkins.io/debian-stable binary/ > /etc/apt/sources.list.d/jenkins.list'
3. sudo apt-get update
4. sudo apt-get install jenkis

help: https://jenkins.io/doc/book/installing/#debian-ubuntu
  https://www.digitalocean.com/community/tutorials/how-to-install-jenkins-on-ubuntu-16-04

5. Port changing
  sudo vim /etc/default/jenkins 
  and add HTTP_PORT=8081
  sudo service jenkins restart (Restart Jenkins)
  help: https://stackoverflow.com/questions/28340877/how-to-change-port-number-for-jenkins-installation-in-ubuntu-12-04
  Installing using Shell script: https://gist.github.com/seanbuscay/2732705
 
6. Visit http://localhost:8081/   => then paste the password from: /var/lib/jenkins/secrets/initialAdminPassword
  [ERROR] when offline instence error is showing then 
  * /var/lib/jenkins/hudson.model.UpdateCenter.xml and change url to user http instead of https
  * Restart jenkins
  help: https://stackoverflow.com/questions/42408703/why-does-jenkins-say-this-jenkins-instance-appears-to-be-offline
 
