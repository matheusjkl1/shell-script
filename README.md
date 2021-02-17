# shell-script

## Removendo travas eventuais do apt ##
sudo rm /var/lib/dpkg/lock-frontend
sudo rm /var/cache/apt/archives/lock

## Atualizando o repositório ##

sudo apt update -y

## Download Aplicativos externos ##

mkdir /home/$USER/Downloads/essentials-programs

cd /home/$USER/Downloads/essentials-programs

wget -c https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb

wget -c https://cdn.zoom.us/prod/5.5.7011.0206/zoom_amd64.deb

wget -c https://dl.discordapp.net/apps/linux/0.0.13/discord-0.0.13.deb

wget -c https://az764295.vo.msecnd.net/stable/622cb03f7e070a9670c94bae1a45d78d7181fbd4/code_1.53.2-1613044664_amd64.deb

sudo dpgk -i *.deb -y

sudo apt update

## Install Brave Browser ##

sudo apt install apt-transport-https curl gnupg -y

curl -s https://brave-browser-apt-release.s3.brave.com/brave-core.asc | sudo apt-key --keyring /etc/apt/trusted.gpg.d/brave-browser-release.gpg add -

echo "deb [arch=amd64] https://brave-browser-apt-release.s3.brave.com/ stable main" | sudo tee /etc/apt/sources.list.d/brave-browser-release.list

sudo apt update -y

sudo apt install brave-browser -y

sudo apt-get install git-all -y

## Install snapd ##

sudo apt install snapd -y

snap install spotify -y

snap apt install slack --classic

sudo apt update -y

sudo apt-get install npm

sudo apt-get install nodejs

sudo apt update && sudo apt dist-upgrade -y
