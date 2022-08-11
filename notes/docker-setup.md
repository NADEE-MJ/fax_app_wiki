---
title: Create Docker Environment
desc: ''
---

## Install WSL and Docker

### Install WSL

   1. In powershell or cmd run "wsl --install"
   2. Check wsl is version 2 by running "wsl --set-default-version 2"
       1. May need to install wsl2 online

### Install Docker

   1. Install the windows version of Docker Desktop from <https://www.docker.com/get-started/>
   2. Select WSL 2 instead of Hypervisor during setup

### Pull/Clone the repo

Clone the repo from this link:
><https://github.com/fax-app/docker_env.git>

1. Open the repo in VS Code
2. Install the following extensions in VS Code:
   1. Remote - Containers by Microsoft
   2. Docker by Microsoft
3. Open the terminal in VS Code
4. Run the command "./scripts/compose.ps1"

## running the containers

1. Make sure Docker Desktop is open on your pc
2. Make sure you cd into the docker_env repo
3. Run ".\scripts\compose.ps1"
4. Wait for it to build, it will take a while
5. Once it completes the build, enter the command pallette (CTRL+SHIFT+P), then type "Remote-Containers:attach to running container...", and select fax_env
6. In your VS Code file explorer open the folder "/home/dev" or if you want to work on a specific repo then open to "/home/dev/repos/{repo you want to work on}"
7. You are up!

## environment variables

1. Make a copy of .env.example in the fax_server folder called .env
2. Set all of the variables inside
   1. For the secret key generate with: `openssl rand -base64 32`

## GIT SETUP

```zsh
gcg "{your github username}" "{your github email}"
```

### Recommended VS Code Extensions

run install-code-exts to install recommended extensions:

   1. Code Spell Checker
   2. Formatting Toggle
   3. Github Pull Requests and issues
   4. Gitlens
   5. Indent Rainbow
   6. Tabnine
   7. Wakatime
   8. Dart
      1. When using dart extension to avoid generating 500k+ errors in VS Code, either search for "dart.onlyAnalyzeProjectsWithOpenFiles" in VS Code settings and make sure it's enabled or you can remote directly into the repos folder or a specific repo folder to avoid the problem altogether.
   9. Flutter

