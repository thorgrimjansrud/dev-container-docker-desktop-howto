# dev-container-docker-desktop-howto
Branch for template

<br/>

## Steps

### Add devcontainer.json file

Press 'F1' and select 'Dev Containers: Add Dev Container Configuration Files ...'. <br/>
Select the prefered template, in this case 'ubuntu:bionic'. <br/>
Select prefered package to install. We select 'apt'. <br/>

### Run container
After created, vs-code prompt opening the dev container. Either select 'yes' or do it manually afterwards. <br/>
I manually, press 'F1' and select 'Reopen in container'. VS-Code will create, run and log into the conteiner. We can see this in teh docker extension. Here we can also remote log in to it.

### Multisatge build
Make a Dockerfile and edit the configuration to launch the Dockerfile. 

<br/>

THIS DOES NOT WORK -> ERROR in FROM scratch. Press message (log) while opening to see error in terminal.
Dette må være feil kommando:
[139668 ms] Start: Run: docker pull scratch

### What works

Det virker å kjøre dockerfile manuelt: <br/>

docker build -t thorgrim/dev-multistage-scratch:latest . <br/>

docker images:
REPOSITORY                                    TAG       IMAGE ID       CREATED        SIZE
thorgrim/dev-multistage-scratch               latest    4e833ce57f6a   19 hours ago   273MB

Det virker å endre 'scratch' til ett annet image og "reopen in container': <br/>

docker images:
REPOSITORY                                                                TAG       IMAGE ID       CREATED              SIZE
vsc-dev-container-docker-desktop-howto-ab4d0a4ab8575aed06ce733617a0f25f   latest    2317c5d01643   About a minute ago   550MB


Settings.json:
 "docker.commands.build": "${config:docker.dockerPath} build --rm -t ${tag} \"${context}\"",

No 'pull' here ..





