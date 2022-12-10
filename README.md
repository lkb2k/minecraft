# Minecraft Server

## Setting up mods on the server
* Find the URL to the jar file from curseforge.  
  * So far the easiest way has been to go through the dumb download process, then just copy the final CDN download URL from the browser downloads history.
* Put the url into mods.txt
* make sure the VERSION on the docker-compose configuration matches the required version for the mod
* `docker compose up`

The forge install in the docker container will download the mod jar files and put them into the mounted 'mods' folder.  Share the mods folder on the LAN to make it easier to set up additional clients.


## Setting up the client
* download the correct version from https://files.minecraftforge.net
* run the forge installer
* copy the jar files from the 'mods' share into 
  * `~/Library/Application Support/minecraft/mods`
* run the launcher and select the installation you just created

### Troubleshooting
Make sure the docker image you're using on the server is :java8-multiarch if you are running on an M1 Mac




