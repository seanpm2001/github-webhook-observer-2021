# github-webhook-observer-2021

This server monitors Github webhooks and rebuilds projects when new commits are made to their repos. 

It's designed around docker-compose projects and utilizes some of docker-compose's configuration to rebuild only the docker comtainers that need to.

The webhook should be set to send PUSH notifications only.

## Installation
```
npm i
```
I prefer to install npm through [nvm](https://tecadmin.net/how-to-install-nvm-on-ubuntu-20-04/)

## Usage
```
node git-observer.js [path/to/project/folder] [github-webhook-secret] [port] [rebuild.sh]

arguments:

[path/to/project/folder] - Required. This is from the point of the .js file, 
        so if the observer and target folders are in the same directory then it would
        look like. "../targert-project-folder".

[github-webhook-secret] - Required. This is the secret set in the github webhook settings.

[port] - Optional. The default is 8000.

[rebuild.sh] - Optional. name of Bash script to rebuild project. Expected in project root directory. 
               The default is 'rebuild.sh'
```

##Run as service
```soon```


