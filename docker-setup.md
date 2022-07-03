---
title: Create Docker Environment
desc: ''
---

## Install WSL and Docker

### Install WSL

   1. in powershell or cmd run "wsl --install"
   2. check wsl is version 2 run "wsl --set-default-version 2"
       1. may need to install wsl 2 online

### Install Docker

   1. Install the appropriate version of Docker Desktop from <https://www.docker.com/get-started/>
   2. Select WSL 2 instead of Hypervisor during setup

### pull the repo

git clone <https://github.com/fax-app/docker_env.git> {working path}

or any other clone method
open the repo in vs code
vs code install the following extensions:
Remote - Containers by microsoft
docker by microsoft
open terminal in vs code
run the command "docker build -t "fax_env" .

## PGAdmin SETUP

## GIT SETUP

> github email and username then pull and enter yes
git config --global user.name "NADEE-MJ"
git config --global user.email "nadeem.maida@gmail.com"
git config --list
git pull

## ADD TO .ENV file

python .env file setup: pip install python-dotenv

## ZSH setup and other vs code setup, maybe write a script for this?

~~~bash

sudo apt install zsh fzf tig chroma -y

echo "zsh" >> /home/deploy/.bashrc

sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

rm ~/.zshrc
echo "$(curl -fsSL https://gist.githubusercontent.com/NADEE-MJ/ebd8905c2b95e86b5d413e49d2d9cc0c/raw/.zshrc)" >> /home/deploy/.zshrc

rm ~/.p10k.zsh
echo "$(curl -fsSL https://gist.githubusercontent.com/NADEE-MJ/d1a275c1d780a7f17011cff25d573def/raw/.p10k.zsh)" >> /home/deploy/.p10k.zsh

git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone https://github.com/zsh-users/zsh-history-substring-search ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-history-substring-search
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting

source ~/.zshrc

~~~

### VS Code extensions to activate

   1. Code Spell Checker
   2. Formatting Toggle
   3. Github Pull Requests and issues
   4. Gitlens
   5. Indent Rainbow
   6. PHP Intelephense
   7. PHP Namespace Resolver
   8. tabnine
   9. wakatime
