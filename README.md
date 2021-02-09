# **NodeRed Enigma2 Subflow** ![picture](https://avatars3.githubusercontent.com/u/5375661?s=40&v=4)
## `V 1.0.1`
 - Subflow for Nodered to retrieve information from an enigma2 receiver and send commands.
 - (DE) Subflow für Nodered um Informationen von einem enigma2 Receiver abzufragen und Befehle zu senden


![Logo](https://homematic-forum.de/forum/styles/prosilver/theme/images/homematic-logo.png)

Forum: https://homematic-forum.de/forum/viewtopic.php?f=77&t=58690


https://github.com/Matten-Matten/node-red-enigma2-flow/blob/master/enigma2-SUB-Flow.json

---
## Beispiel:

https://github.com/Matten-Matten/node-red-enigma2-flow/blob/master/enigma2-BSP-Flow.json

![picture](https://raw.githubusercontent.com/Matten-Matten/node-red-enigma2-flow/master/picture/Node-RED_enigma2.png)
![picture](https://raw.githubusercontent.com/Matten-Matten/node-red-enigma2-flow/master/picture/Node-RED%20_%201enigma2%20flow%20config.png)

---

# **Input:**

`manuell Polling`

---
### _msg.message:_


- Message **Type**: **0**= Yes/No, **1**= Info, **2**=Message, **3**=Attention

**`Beispiel: `**
_`msg.message = {`_**`text`**_`:"Das ist eine Testnachricht!",`_**`Type`**_`:0,`_**`Timeout`**_`:30};`_

---
### _msg.command:_

`REMOTE-CONTROL-(Number! not String)`

 - 116 Key "Power"	
 - 2   Key "1"	 
 - 3   Key "2"	
 - 4   Key "3"	
 - 5   Key "4"	
 - 6   Key "5"	
 - 7   Key "6"	
 - 8   Key "7"	
 - 9   Key "8"	
 - 10  Key "1"	
 - 11  Key "0"	
 - 412 Key "previous"	
 - 407 Key "next	
 - 115 Key "volume up"	
 - 113 Key "mute"	
 - 402 Key "bouquet up"	
 - 114 Key "volume down"	
 - 174 Key "lame"	
 - 403 Key "bouquet down"	
 - 358 Key "info"	
 - 103 Key "up"	
 - 139 Key "menu"	
 - 105 Key "left"	
 - 352 Key "OK"	
 - 106 Key "right"	
 - 392 Key "audio"	
 - 108 Key "down"	
 - 393 Key "video"	
 - 398 Key "red"	
 - 399 Key "green"	
 - 400 Key "yellow"	
 - 401 Key "blue"	
 - 377 Key "tv"	
 - 385 Key "radio"	
 - 388 Key "text"	
 - 138 Key "help"	

---
### _msg.command:_

 - `MUTE_TOGGLE`
 
 - `RADIO`
 
 - `CHANNEL_DOWN`
 
 - `CHANNEL_UP`
 
 - `DOWN`
 
 - `EPG`
 
 - `EXIT`
 
 - `LEFT`
 
 - `MENU`
 
 - `OK`
 
 - `PLAY_PAUSE`
 
 - `REC`
 
 - `STANDBY_TOGGLE`
 
 - `STOP`
 
 - `TV`
 
 - `UP`
 
 - `VOL_UP`
 
 - `VOL_DOWN`
 
 - `MEDIA`

 - `REWIND`

 - `FORWARD`
 
 - `GREEN`

 - `BLUE`

 - `YELLOW`

 - `RED`

---
### _msg.zap:_

 - `"servicereference"`

---
### _msg.volume:_

 - `0-100`

---
### _msg.main__command:_

 - `WAKEUP_FROM_STANDBY`
 
 - `IN_STANDBY`
 
 - `DEEP_STANDBY`
 
 - `REBOOT`
 
 - `RESTART_GUI`


---

### **Output:**

 * `Einschaltstatus`
 
 * `Message Answer`
 
 * `Festplatte 1 Speicher Größe`
 
 * `Festplatte 1 Speicher Frei`
 
 * `Festplatte 2 Speicher Größe`
 
 * `Festplatte 2 Speicher Frei`
 
 * `Volume - e2volume`
 
 * `Mute - e2ismuted`
 
 * `Channel - e2servicename`
 
 * `Event Description - e2eventdescription`
 
 * `Event Description Extended - e2eventdescriptionextended`
 
 * `Event Name`
 
 * `Servicereference (Sender ID)`
 
 * `Picon Path (only OpenWebInterface)`
 
 * `Event Time Passed`
 
 * `Event Progress Percent (Sendezeit)`
 
 * `Eventduration`
 
 * `Event Start`
 
 * `Event End`
 
 * `Eventremaining`
 
 * `Is Record (Aufnahme aktiv)`

---

## Changelog

### 1.0.1 (2021-02-09)
* (Matten-Matten)       bugfix: `REMOTE-CONTROL`

### 1.0.0 (2021-02-09)
* (Matten-Matten)       add:  Password `uri encode`
* (Matten-Matten)       add: `Output values with every update`
* (Matten-Matten)       bugfix: `Message Text uri encode`

### 0.0.9 (2020-12-01)
* (Matten-Matten)       some litle fixes

### 0.0.8 (2020-07-06)
* (Matten-Matten)       add:  commands `GREEN`,`BLUE`,`YELLOW`,`RED`
* (Matten-Matten)       bugfix: `error in the form of a command`

### 0.0.7 (2020-07-05)
* (Matten-Matten)       add:  commands `VOL_UP`,`VOL_DOWN`,`MEDIA`,`REWIND`,`FORWARD`

### 0.0.4 (2020-05-15)
* (Matten-Matten)       bugfix: `fix bug in message reply`

### 0.0.3 (2020-05-12)
* (Matten-Matten)       bugfix: `decode special characters in the message text (äöüÄÖÜß)`

### 0.0.2 (2020-05-02)
* (Matten-Matten)       bugfix: `correction in error handling`

### 0.0.1 (2020-05-01)
* (Matten-Matten)       add: `first publication`

---
made by [Matten Matten](https://github.com/Matten-Matten)
