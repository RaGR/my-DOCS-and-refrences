so system-md is the firts procces that luches into unix base OSs and the last one to terminate when shuting down.

i was wondering how to make multiple scripts happen at once in a single terminal without opening a new terminal. and here is your advanced profational answer:


# WHAT IS A SERVICE IN UNIX BASED SYSTEMS:

A Linux service is a background process that runs continuously to perform specific tasks. Services can start automatically at boot time and run without user intervention. Examples include web servers, database servers, and network services.

yes, so basicaly its a magic wood if you manage to create them and manage them and configure currectly

this is where the magic happens:
```bash
/etc/systemd/system/
```
unix GODs got your back and when you navigate into this directory you can see all other services too - you can nano them to see how real peopple wrote well services

i recomend:

```bash
ls -la | grep .service
```

here we can list and view all files containig .service in this magic dir, looks something like this:
![image](https://github.com/user-attachments/assets/ee9000c9-427b-4922-9fab-c225d99b4ba2)
