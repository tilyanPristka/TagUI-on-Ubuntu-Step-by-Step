# TagUI on Ubuntu Step by Step

### Install PHP5.6
`sudo apt install software-properties-common`

`sudo add-apt-repository ppa:ondrej/php`

`sudo apt update`

`sudo apt install -y php5.6`

`sudo apt install php libapache2-mod-php php5.6-mysql php5.6-mcrypt php5.6-common php5.6-mysql php5.6-xml php5.6-xmlrpc php5.6-curl php5.6-gd php5.6-imagick php5.6-cli php5.6-dev php5.6-gmp php5.6-bz2 php5.6-imap php5.6-mbstring php5.6-opcache php5.6-soap php5.6-zip php5.6-intl php5.6-json php5.6-ldap php5.6-bcmath -y`

`sudo update-alternatives --config php`


### Download Requirement for TagUI
`wget https://github.com/kelaberetiv/TagUI/releases/download/v6.46.0/TagUI_Linux.zip`

`wget https://corretto.aws/downloads/latest/amazon-corretto-8-x64-linux-jdk.tar.gz`

`wget https://launchpad.net/sikuli/sikulix/2.0.5/+download/sikulixide-2.0.5-lux.jar`

`wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb`

`unzip TagUI_Linux.zip`

`sudo ln -sf /home/downloads/tagui/src/tagui /usr/local/bin/tagui`


### Install Google Chrome
`sudo apt install ./google-chrome-stable_current_amd64.deb`
check chrome already installed in Activities, open it for first time


### Install OpenJDK
`mkdir /opt/jdk`

`tar -zxf amazon-corretto-8-x64-linux-jdk.tar.gz -C /opt/jdk`

`update-alternatives --install /usr/bin/java java /opt/jdk/amazon-corretto-8.312.07.1-linux-x64/bin/java 100`

`update-alternatives --install /usr/bin/javac javac /opt/jdk/amazon-corretto-8.312.07.1-linux-x64/bin/javac 100`


### Install Others Requirement
`java -version`

`sudo apt install default-jre`

`sudo apt install python-is-python3`

`sudo apt install curl`

`wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2`

`sudo tar xvjf phantomjs-2.1.1-linux-x86_64.tar.bz2 -C /usr/local/share/`

`sudo ln -s /usr/local/share/phantomjs-2.1.1-linux-x86_64/bin/phantomjs /usr/local/bin/`

`phantomjs --version`

`sudo nano /etc/environment`

> TAGUI_DIR=/home/downloads/tagui/src

> tagui=/home/downloads/tagui/src/tagui

`sudo apt-get install jython`

`sudo apt-get install jruby`


### Install Adobe PDF Reader
`sudo dpkg --add-architecture i386`

`sudo apt install libxml2:i386 libcanberra-gtk-module:i386 gtk2-engines-murrine:i386 libatk-adaptor:i386`

`wget -O /home/downloads/adobe.deb ftp://ftp.adobe.com/pub/adobe/reader/unix/9.x/9.5.5/enu/AdbeRdr9.5.5-1_i386linux_enu.deb`

`sudo dpkg -i /home/downloads/adobe.deb`


