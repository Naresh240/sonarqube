# nodejs-module-sonarqube

# Pre-Requisites:
    - Install Docker
    - Install Docker-compose
    - Install npm
# Install Docker
    yum install docker -y
    service docker start
# Install docker compose
    sudo curl -L "https://github.com/docker/compose/releases/download/1.27.4/docker-compose-$(uname -s)-$(uname -m)" -o /usr/bin/docker-compose
    sudo chmod +x /usr/bin/docker-compose
    docker-compose --version
# Install npm
    sudo yum install -y gcc-c++ make
    curl -sL https://rpm.nodesource.com/setup_13.x | sudo -E bash -
    sudo yum install -y nodejs
# Run Sonar with docker-compose file
    docker-compose up -d
# Check sonar from UI
    http://<ip-address>:9000
# Install required modules for our application
    npm install
    It might install below modules, other wise need to install all manually
    [express, jest-sonar-reporter, sonarqube-scanner, supertest, sonar]
# Test application using below command
    npm run test
![image](https://user-images.githubusercontent.com/58024415/94837008-528fda80-0431-11eb-8437-5580495036fd.png)

After all tests are successfully executed, a folder named “coverage” will be generated
Coverage folder files are being referenced in sonar-project.js
# finally, the command must be executed
    npm run sonar
![image](https://user-images.githubusercontent.com/58024415/94836947-3855fc80-0431-11eb-877f-eb4c8688e35a.png)
