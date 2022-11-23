# Network setup

1. Import and start the virtual machine configured disponible [here(TODO: Finish)](google.com)

The machine name is wifi, and password is wifi as well

2. Start the topology network used:
        Topology used
```
        |- h1
        |- h2
nat0 ---|
        |- h3
        |- h4
```

```console
wifi@wifi-virtualbox:~$ cd mininet-wifi/mininet/examples/
wifi@wifi-virtualbox:~$ sudo python mynat.py
```

After you have finished this part of configurations, continue on [MQTT setup](../mqtt/setup.md)