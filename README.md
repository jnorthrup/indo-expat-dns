# indo-expat-dns
indonesian DNS selective /etc/hosts repair scripts

## description:

there are sometimes well intentioned DNS restrictions that can affect certain regions  

## setup 

`sudo apt install curl jq sed` 

### identifying good intentions:

 1. go to site 
 1. open inspector, console
 1. read console connection interruptions ![image](https://user-images.githubusercontent.com/73514/107647288-f4fc7c00-6cb5-11eb-938d-5368c24ce788.png)

### resolve a DNS regional issue:
  run the sdns script(s) with permissions (sudo) to append /etc/hosts 

```bash
sudo bash ./sdns https://bin.bnbstatic.com/static/runtime/main-3486bb56e76ee78256b4.js wss://stream.binance.com/stream
52.84.229.71 bin.bnbstatic.com
54.65.83.59 stream.binance.com
```

## effects 

this script will use root access so you must excercise caution by reading the script and learning the potential risks

IP access to google dns is necessary 

the script will write entries to /etc/hosts and copy to console 

no error checking is performed.

