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
> THIS DOES NOT WORK -> ERROR in FROM scratch









