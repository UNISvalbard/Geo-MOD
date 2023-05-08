# Svalbox student server

```{note}
Usernames and passwords are the ones provided by UNIS.
```

Server address: [\\svalbox\AG222](\\svalbox\AG222)

#### Connecting Windows
When accessing these pages through the Windows File Explorer, one can copy the link to the server address to open the server directories in the file explorer.

```{figure} assets/1_server_path.png
:name: 1_server_path

```


You will then be prompted with the following login prompt, where you will have to supply the username and password provided to you in class.

This should connect you to the server shares through a temporary connection - in case you'd prefer having a semi-permanent connection, you may proceed with the steps below to map the server as a network drive.

#### Mapping server as a network drive:
In file explorer, proceed to Computer, and click Map network Drive:

```{figure} assets/3_map_network.png
:name: 3_map_network

```

You are then prompted by the following, where you can select the desired letter to map the drive at; a field where you passed the server address into; and two options that allow for the mounting of the network drive. Fill out as highlighted below, then proceed by clicking Finish.


The same username/password prompt as above will be shown, and after successfully logging in with the username and password provided in class, you should have access to the drive:


```{admonition} Support
:class: warning
In certain cases, another directory on the same server has already been mounted, and a warning will pop up. In those cases, make sure to disconnect the other mapped network drive before mapping a new one!
```