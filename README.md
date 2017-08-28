# Trolley Simulator

## Getting Started

1. Build image using the following command:
```
./build.sh
```
This will compile an image which includes the TaniumClient and a simple boot script.

2. Start up 5 containsers:
```
./start.sh -s 192.168.1.2
```
The ip address here is the address of our Tanium Server where the client will start talking into.
> If you'd like to have more or less containers, add `-n #` where # is the number of containers to spin up.
Now go checkout your Tanium Console under System Status... you should see your new containers checking in.

3. (Optional) Connect to a bash prompt onto one of your containers:
```
docker exec -i -t d5f491f505ca /bin/bash
```
The `d5f491f505ca` is the container id as displayed by the `./start.sh` command or identified via `docker ps -a`.

4. Stop and delete all containers:
```
./stop.sh
```
This will stop all containers that are currently running and delete/cleanup all containers seen within `docker ps -a`.

5. Cleanup build images:
```
./clean.sh
```
If you'd like to cleanup your build environment and remove any docker images built from step 1, use the command above.
