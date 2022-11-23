# MQTT configuration on network

Recapitulation of Topology Network:
        Topology used

        |- h1
        |- h2
nat0 ---|
        |- h3
        |- h4


After finished (network setup)[../network/setup] and you have mininet CLI, let's continue configuration
Here you'll have to manage a lot of terminals, so please be careful on the instructions.

1. Start central broker(everything is already configured in VM) that is the middleware from utput 

In mininet console, open nat0 console
```console
mininet> xterm nat0
```
Start central broker
```console
wifi@wifi-virtualbox:/home/wifi/mininet-wifi/mininet/examples/# sudo mosquitto -c /etc/mosquitto/mosquitto_central.conf -v
```

2. Start local broker on a internal node h1 (similar to a drone)

In mininet console, open h1 console
```console
mininet> xterm h1
```
Start local broker
```console
wifi@wifi-virtualbox:/home/wifi/mininet-wifi/mininet/examples/# sudo mosquitto -c /etc/mosquitto/mosquitto_local.conf -v
```

3. Connect h1 to external internet

In mininet console, open another h1 console
```console
mininet> xterm h1
```
Start a tunnel to internet using ngrok
```console
wifi@wifi-virtualbox:/home/wifi/mininet-wifi/mininet/examples/# sudo ngrok tcp 1883
```

From the console extract the path and port ngrok serve to connect to the node and use in the android app, since this is a simulation this is not a problem. In real world, both android app and host need to be in the same local network, but in this case since we just created some virtualization nodes, it'll be tricky to connect the android app directly to the internal network of the NAT.