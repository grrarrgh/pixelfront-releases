# Pixel Front

A desert real-time strategy game for Windows. Play as the Terran Union or the Freehold
Federation: build a base, hold the energy wells and design your own units. Fight the computer
(Easy, Normal or Hard) or up to three friends on your network (1v1, 1v2 or 2v2).

This repository holds the game's downloads only. It's an early test build, so expect rough edges.

## Download and play

1. Open the **[latest release](https://github.com/grrarrgh/pixelfront-releases/releases/latest)**
   and download the `.zip` file under **Assets**.
2. Unzip it anywhere, for example to your Desktop.
3. Open the `Pixel Front` folder and run **`Pixelfront.exe`**.

Windows may say "Windows protected your PC" because the game isn't signed. Click
**More info**, then **Run anyway**.

You need 64-bit Windows 10 or 11. Nothing is installed: to remove the game, delete the folder.

## Playing together

- Everyone needs the **same version**. The game refuses to connect otherwise.
- One player hosts: on the title screen, **Multiplayer**, then **Host a match**. Leave
  **Host for** on **LAN** and click **Host**. The lobby shows the host's address, such as
  `192.168.1.20:7777`.
- The others pick **Multiplayer**, then **Join a match**, type that address under
  **Host's address** and click **Join**.
- The first time the host runs the game, Windows asks whether to allow it on networks. Allow it
  on **private networks**.
- The game connects directly between computers on the **same home network**. To play over the
  internet, the host needs to forward TCP port 7777 on their router, or everyone joins the same
  [Tailscale](https://tailscale.com) network and uses the host's Tailscale address.

If someone can't join, run this in a command prompt on their PC, with the host's address:

```
powershell Test-NetConnection 192.168.1.20 -Port 7777
```

`TcpTestSucceeded : True` means the network is fine. `False` means something between the two PCs
is blocking the connection: the host's firewall, a VPN, or a Wi-Fi extender or mesh satellite.

## Feedback

Found a bug or have an idea? Open an
[issue](https://github.com/grrarrgh/pixelfront-releases/issues) or tell the developer directly.
