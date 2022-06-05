A step-by-step guide on installing **Minecraft Bedrock** server on Ubuntu 18.04 (LTS) for complete beginner.

## Basic Installation
1. Create a new directory for the server    
```mkdir /minecraft && cd /minecraft```  
2. Download the specific version of the server (other versions refer [here](https://minecraft.fandom.com/wiki/Bedrock_Dedicated_Server#Download))    
```wget https://minecraft.azureedge.net/bin-linux/bedrock-server-1.18.33.02.zip```  
3. ```unzip bedrock-server-1.18.31.zip```  
5. Allow ports **19132** and **25565** on server firewall  
```ufw allow 19132```  
```ufw allow 25565```

## Edit Server Properties
There are some important properties that you need to set before you run the server such as **world seed**, **server ports**, and **world name**. Other properties can be set later.  
| Properties              | Descriptions                  |
| ----------------------- |:------------------------------|
| ```level-seed```        | Set world seed |
| ```level-name```        | World name and save folder name |
| ```server-port```       | Custom IPv4 port |
| ```server-portv6```     | Custom IPv6 port |

1. Locate installed server directory with ```cd /minecraft```
2. ```nano server.properties```
3. Look for  **properties** and set to any value (example: ```level-seed=-1671764014```)
4. Save

\* If you change your **server ports**, make sure to ```ufw allow [ports]```. 

## Keep the Server Running  
1. ```screen```
2. Locate installed server directory with ```cd /minecraft```
3. Start the server file by ```./bedrock_server```  

