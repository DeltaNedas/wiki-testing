# Servers

Servers are a large part of Mindustry in that they offer the ability to play the game with other people. There are two main types of servers; dedicated servers and local LAN servers. 

## Dedicated Servers

Dedicated servers are standalone, headless versions of the game that are focused only on providing a means for people to play Multiplayer. They are usually run on a computer as a separate program rather than in-game, and are operated from the terminal. These are usually stronger than a local LAN server as they have more resources available to them to support more than two or three players, and can be run 24/7. They are also more versatile and powerful in that they have many commands to provide the administrator with more control over it, and they can easily be modded to fit the administrator's needs. 

You can connect to one using the "Join Game" button under the "Play" menu. Unlike local LAN servers, you will have to enter the host's IP address and port. Also unlike local LAN servers, once you add a server, it will automatically show up on your server list when you open it, and the game will automatically check the server's status.

To establish a dedicated server, a dedicated Linux or Windows machine is **highly** recommended.

1. If you haven't already, install at least JRE and JDK 8.
2. Download the desired server release from [itch.io](https://anuke.itch.io/mindustry), or compile one yourself. 
3. Open a terminal or TTY session then change `cd` to the directory the JAR is placed in.
4. Run `java -jar server.jar` using Command Prompt (on Windows) or your favorite terminal (on Linux and Mac). The commands are explained in the `help` command.
5. Start hosting a map with `host <mapname> [mode]` after you configured your server.
6. If you are using Windows to run your server, use your favorite search engine to look up how to add rules to your Windows Firewall, as it blocks that port most of the time. Make sure to allow **port 6567 TCP and UDP**.

If you want your server to be publicly available around the world, then read the following. If not, then you are done! 
It is recommended and that you use a domain name or DNS service to mask your IP for public servers for ease of use, or even better, use a cloud service e.g. Amazon AWS or a dedicated server/VM from a hosting provider such as Linode or DigitalOcean, which is much safer. **Do your research**, and determine which option best fits your needs.

### What is an IP and how do I find out what mine is?

In simplified terms, an IP address is a number that identifies your computer on the internet. You can connect to someone's Mindustry server if you know their IP address. There are two types; a **public** and a **local** address.

- For a **local IP**, when for example you would like to play with a friend on the same network as yours, each device has its own way of showing it. You can Google how to do it for your device, e.g. "find local ip on Mac".
- For a **public IP**, you can simply Google "what is my ip".

### About Running A Dedicated Server At Home

Most of the time, this is what you should remember; **never share your public IP with the public if you're hosting from your home, unless you acknowledge the implications of doing so!** Your public IP is tied to your household, and if it falls into the wrong hands, and when put into the wrong hands, can open up your network to vulnerabilities and dangers. **Exercise caution, do your research, and use a VPN or webhost if possible.**

1. Find the make/model of your router. This is usually on a sticker on the bottom or back of the router.
2. Use your favorite search engine to search "port forward ASUS RT-ACRH17" and use the guide to foward **port 6567 TCP and UDP**. These instructions are different for every router, so be sure to read your guide thoroughly!
3. You can use a service such as [You Get Signal](https://www.yougetsignal.com/tools/open-ports/) to check if you have done your portforwarding correctly. 

## Local LAN & Steam Servers

A local LAN or Steam server is a server that is built into the game, and can be started using the "Host Multiplayer Game" button in the in-game menu. It is meant to be simple and straightforward, for sessions between a few players under a LAN network (aka in your household's WiFi network). It is not really meant for several players, as it takes more and more resources from your device to be able to use it that way; for that you will need a dedicated server mentioned above. It can only run when the game is open, and is immediately terminated when it is closed.

You can connect to one using the "Join Game" button under the "Play" menu. Unlike dedicated servers, your device will automatically find the host device and it will ususally appear in the server list without you having to enter the host's IP address in.
