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

### pull/clone the repo

git clone <https://github.com/fax-app/docker_env.git> {working path}

or any other clone method
open the repo in vs code
vs code install the following extensions:
Remote - Containers by microsoft
docker by microsoft
open terminal in vs code
run the command "docker build -t "fax_env" .

## running the containers

1. make sure docker is open on your pc
2. make sure you cd into the docker_env repo
3. run ".\scripts\compose.ps1"
4. wait for it to build, it will take a while
5. once it completes the build, CTRL+SHIFT+P, then type "Remote-Containers:attach to running container...", then select fax_env
6. in your vs code file explorer open the folder "/home/dev" or if you want to work on a specific repo then open to "/home/dev/repos/{repo you want to work on}"
7. you are up!

## environment variables
1. make a copy of .env.example called .env
2. set all of the variables inside
   1. generate a security with `openssl rand -base64 32`

## PGAdmin SETUP

## GIT SETUP

> github email and username then pull and enter yes
git config --global user.name "{your github username}"
git config --global user.email "{your github email}"
git config --list
git pull

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
   10. Dart
      a. Search "dart.onlyAnalyzeProjectsWithOpenFiles" in VS Code settings and make sure it's enabled.
   11. Flutter

