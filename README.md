# MC-Domain Setup

Private server hosted through VPN

---

## Table of Contents

1. [Forge Setup](#forge-setup)

   1. [Download](#1-download)

   2. [Install](#2-install)

   3. [Running](#3-running)

2. [VPN Setup](#vpn-setup)

3. [Connecting to the server](#connecting-to-the-server)

   1. [Server IP](#ip_address) or [Hostname](#hostname_address)

4. [Troubleshooting](#troubleshooting)

---

## Forge Setup
**What is this?** *Forge is essentially a mod manager. This set of instructions will have you set up through an app called CurseForge, but you can install forge directly if you prefer. We will be using Minecraft 1.20.1*

### 1. Download

Download the CurseForge app for your operating system [here](https://www.curseforge.com/download/app).\
Or download directly from the links below.

[Windows](https://download.overwolf.com/install/Download?ExtensionId=cfiahnpaolfnlgaihhmobmnjdafknjnjdpdabpcm&utm_term=eyJkb21haW4iOiJjZi13ZWIifQ%3D%3D) | [Linux](https://curseforge.overwolf.com/downloads/curseforge-latest-linux.deb) | [Mac](https://curseforge.overwolf.com/downloads/curseforge-latest.dmg)

Once downloaded run the installer and login or continue as guest

### 2. Install

Download the latest .zip release from this repository.

In CurseForge's home menu and select "Minecraft Java Edition". Then you will want to add a profile by clicking *IMPORT*. Select the zip file you downloaded.

### 3. Running

At this point you can run the game by clicking "play". CurseForge also allows you to create a shortcut to the profile.

You can also add any mods, resource packs, and shaders to the profile. *Only add CLIENT mods to the profile, adding SERVER mods will not allow you to connect to the server.*

---

## VPN Setup
**Why is this necessary?** *Hosting servers requires that your machine is able to connect to the other device through LAN or WAN. Normal servers pay for certificates and security that allow them to open ports and expose their IP address to the world wide web. While this is possible for our use-case, it is not practical. So this leaves us with LAN. The issue with a LAN is you must be on the SAME local network as the server. To get around this we use something called a **Virtual Private Network** **(VPN)**. VPNs tunnel encrypted traffic from one device to another. This allows us to create a virtual LAN that can be accessed from anywhere in the world without worrying about more complex security.*

*Our VPN of choice: **Tailscale (free)***

### Installing Tailscale

1. Go to the [Tailscale website](https://tailscale.com) and create an account (use personal emails)

2. Download the installer from the [Tailscale website](https://tailscale.com/download).

3. Follow the instructions given to you by Tailscale to add your device.

   1. *When you go to[ http://100.100.100.100](http://100.100.100.100) you should see your computer and it should say "connected"*

   2. *If this is not the case you have done something wrong.*

4. Click this share link =&gt; Link Expires: --/--/----

   1. What this does: *Adds my server to your "Tailnet", putting it on the virtual LAN.*

---

## Connecting to the server

To do this both ***Forge Setup*** and ***VPN Setup*** must be complete.

1. Launch Minecraft from the CurseForge profile

2. Go to Multiplayer and click "Direct Connect" or "Add Server"

3. Use this IP address: <x id="ip_address">*x.x.x.x*</x>

   1. Alternatively you can connect through the hostname: <br><x id="hostname_address">*mc-domain.cougar-pikes.ts.net*</x>

---

## Troubleshooting

If you experience difficulties here are some things you can try:

- **Server not found**
    1. Check your [admin console](https://tailscale.com/admin). If both your device and the server say ONLINE then its something else
        - If your device is offline you need to connect it to tailscale
        - If 'mc-server' is offline contact Luke
    2. Try using IP address instead of hostname (Make sure you're not specifying any ports)
    3. Try disabling any other VPN you might be using
- **Incompatible Mods**
    1. If you added any mods you may have added a server side mod. You can request it be added but no guarantees.
    2. Download and use the most recent .zip release from the repo listed in [Forge Setup](#forge-setup)
