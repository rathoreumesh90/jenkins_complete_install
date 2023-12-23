# jenkins_complete_install
Installing Jenkins 
Follow the lInk  to download and  install latest version of jenkins >  https://www.jenkins.io/doc/book/installing/linux/
Jenkins installers are available for several Linux distributions.
For Debian/Ubuntu >  Long Term Support release
A LTS (Long-Term Support) release is chosen every 12 weeks from the stream of regular releases as the stable release for that time period. It can be installed from the debian-stable apt repository.
Run These commands in your Terminal > 
> sudo wget -O /usr/share/keyrings/jenkins-keyring.asc \
  https://pkg.jenkins.io/debian-stable/jenkins.io-2023.key
>  echo deb [signed-by=/usr/share/keyrings/jenkins-keyring.asc] \
  https://pkg.jenkins.io/debian-stable binary/ | sudo tee \
  /etc/apt/sources.list.d/jenkins.list > /dev/null
> sudo apt-get update
> sudo apt-get install jenkins

For Fedor
You can install Jenkins through dnf. You need to add the Jenkins repository from the Jenkins website to the package manager first.

Long Term Support release
A LTS (Long-Term Support) release is chosen every 12 weeks from the stream of regular releases as the stable release for that time period. It can be installed from the redhat-stable yum repository.
Run Below Commands 
>  sudo wget -O /etc/yum.repos.d/jenkins.repo \
    https://pkg.jenkins.io/redhat-stable/jenkins.repo
> sudo rpm --import https://pkg.jenkins.io/redhat-stable/jenkins.io-2023.key
> sudo dnf upgrade
# Add required dependencies for the jenkins package
> sudo dnf install fontconfig java-17-openjdk
> sudo dnf install jenkins
> sudo systemctl daemon-reload
