#Hosting a Jenkins Server
- Hosting a jenkins server locally is easy to do
- Extensive documentation can be found at ```https://www.jenkins.io/doc/book/installing/linux/#debianubuntu```

## Installing
- As this is a server which will want longer support an LTS release will be installed
- First commands to be run install java which jenkins requires ```sudo apt install openjdk-11-jdk -y```
- Installation of java can be confirmed by running the command ```java --version```
- To install jenkins itself these commands need to be used:
    - ``` wget -q -O - https://pkg.jenkins.io/debian-stable/jenkins.io.key | sudo apt-key add -
        sudo sh -c 'echo deb https://pkg.jenkins.io/debian-stable binary/ > \
        /etc/apt/sources.list.d/jenkins.list'
        sudo apt-get update
        sudo apt-get install jenkins ```
- Status of jenkins can be confirmed with ```sudo systemctl status jenkins```

## Running
- After starting the server jenkins needs to be unlocked, this can be accessed by ```http://localhost:8080``` or in the case of this program ```http://192.168.10.150:8080/```
- After accessing this page a key will need to be used to access the server, this can be found by using the command ```sudo cat /var/lib/jenkins/secrets/initialAdminPassword```
- This will allow access to the jenkins server
- Admin users and plugins can then be installed
