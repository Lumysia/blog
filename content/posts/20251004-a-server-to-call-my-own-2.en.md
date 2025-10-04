---
# --- Core Content ---
title: 'A Server to Call My Own: Opening the Door to the World'
subtitle: ""
date: '2025-10-04T14:33:18-04:00'
draft: false
description: "Yay! We're at the second stop of our A Server to Call My Own adventure!"

# --- Author ---
author: "Lumysia"
authorLink: ""
license: ""

# --- Images ---
images: []
#featuredImage: ""
#featuredImagePreview: ""

# --- Taxonomies ---
categories:
  - Digital Homestead
tags:
  # Topic
  - Homelab
  - Networking
  - Cloudflare Tunnel
  - Python
  # Type/Style
  - Getting Started
  - Tutorial

# --- Page Behavior ---
hiddenFromHomePage: false
hiddenFromSearch: false

# --- Page Features ---
twemoji: false
lightgallery: true
ruby: true
fraction: true
fontawesome: true
linkToMarkdown: true
rssFullText: false

toc:
  enable: true
  auto: true

# --- Advanced Configuration ---
code:
  copy: true
  maxShownLines: 50
math:
  enable: false
mapbox:
share:
  enable: true
comment:
  enable: true
library:
  css:
    # someCSS = "some.css"
    # located in "assets/"
    # Or
    # someCSS = "https://cdn.example.com/some.css"
  js:
    # someJS = "some.js"
    # located in "assets/"
    # Or
    # someJS = "https://cdn.example.com/some.js"
seo:
  images: []
  # ...
---

## The Foundation of Your Digital Castle

So, we've gathered all our shiny hardware parts! Now, where should our little digital home actually live? On a traditional, cozy Windows cottage? A super-geeky and customizable Linux treehouse? Or a fancy, money-consuming macOS villa?

Honestly, any of these are perfectly fine for a beginner, and you can totally use them for your homelab adventure. It's your world, so you make the rules!

But! The main character I want to introduce you to today is the amazing [Proxmox Virtual Environment](https://pve.proxmox.com/wiki/Main_Page). Ooooh, that sounds super technical, right? Don't worry! Think of it like a magical piece of land. On this land, you can build a Windows house, a Linux house, and even a macOS house, and they can all live together as happy little neighbors! It's the perfect, reliable foundation for all the other fun things we want to build.

You can follow the [official guide](https://pve.proxmox.com/wiki/Installation) to get your own little plot of Proxmox land ready. Or, if you prefer, just stick with your favorite Windows, Linux, or macOS for now. You are the boss of this adventure!

The system is just the ground our digital nest is built on, so we won't spend too much time here. If you're not sure how to install an operating system, YouTube has tons of super helpful videos. I really, really recommend checking them out!

## Let's Open the Doors to Your Digital Home

Okay, so you have your internet connection, and your ISP has handled all the boring stuff. How about we do something super exciting? Do you wanna host a tiny, simple website and show it to the world in, like, 5 minutes? Let's gooooo!

First things first... you know what system your computer is running, right? Hehe, just kidding!

### For my Windows 10/11 Pals

1. Summoning a Little Magic with Python
   1. First, press the `Win` key and the `R` key together on your keyboard. In the little box that pops up, type `powershell` and press `Enter`. This opens our magical command window!
   2. Now, let's chant our first spell. Copy and paste this into the PowerShell window: `winget install Python.Python.3.13` and press `Enter`. This tells your computer to install Python for us! (Just a little note: this version is super new as of Oct 2025, so some old scripts might be a bit grumpy with it, but I always prefer the newest shiny things!)
   3. **Super Important!** Close the PowerShell window, and then open a brand new one. This lets our computer know about the new magic we just installed.
   4. Type `python -m http.server` and press `Enter`. You should see a message that says something like `Serving HTTP on :: port 8000`. If you see that... Tada!
2. Visiting Your Creation
   1. See that `8000` in the message? That's the secret door number to your new server! Let's go visit it. Open any web browser and go to this address: `http://127.0.0.1:8000`.
   2. What do you see? Aha! That's your home folder, right? It's because that's where you cast your Python spell from.
3. The Secret Passageway: Cloudflare Tunnel
   1. Let's install our secret ingredient! Open a new PowerShell window and type this spell: `winget install Cloudflare.cloudflared`, then press `Enter`.
   2. Once that's done, it's time for the final enchantment! Open a new PowerShell window, type: `cloudflared tunnel --url http://127.0.0.1:8000`
   3. Give it about 10 seconds to work its magic... have you seen a bunch of text pop up with a special `trycloudflare.com` link?

    ```log
    2025-10-04T19:05:45Z INF Thank you for trying Cloudflare Tunnel. Doing so, without a Cloudflare account, is a quick way to experiment and try it out. However, be aware that these account-less Tunnels have no uptime guarantee, are subject to the Cloudflare Online Services Terms of Use (https://www.cloudflare.com/website-terms/), and Cloudflare reserves the right to investigate your use of Tunnels for violations of such terms. If you intend to use Tunnels in production you should use a pre-created named tunnel by following: https://developers.cloudflare.com/cloudflare-one/connections/connect-apps
    2025-10-04T19:05:45Z INF Requesting new quick Tunnel on trycloudflare.com...
    2025-10-04T19:05:48Z INF +--------------------------------------------------------------------------------------------+
    2025-10-04T19:05:48Z INF |  Your quick Tunnel has been created! Visit it at (it may take some time to be reachable):  |
    2025-10-04T19:05:48Z INF |  https://gem-saw-passed-equilibrium.trycloudflare.com                                      |
    2025-10-04T19:05:48Z INF +--------------------------------------------------------------------------------------------+
    2025-10-04T19:05:48Z INF Cannot determine default configuration path. No file [config.yml config.yaml] in [~/.cloudflared ~/.cloudflare-warp ~/cloudflare-warp]
    2025-10-04T19:05:48Z INF Version 2025.8.1 (Checksum b5d598b00cc3a28cabc5812d9f762819334614bae452db4e7f23eefe7b081556)
    2025-10-04T19:05:48Z INF GOOS: windows, GOVersion: go1.24.2, GoArch: amd64
    2025-10-04T19:05:48Z INF Settings: map[ha-connections:1 protocol:quic url:http://127.0.0.1:8000]
    2025-10-04T19:05:48Z INF cloudflared will not automatically update on Windows systems.
    2025-10-04T19:05:48Z INF Generated Connector ID: 3f5d9474-b25a-44f0-987a-2140fbf9a9c1
    2025-10-04T19:05:48Z INF Initial protocol quic
    2025-10-04T19:05:48Z INF ICMP proxy will use 192.168.1.233 as source for IPv4
    2025-10-04T19:05:48Z INF ICMP proxy will use fdaa:2937:24e1::80e in zone Wi-Fi as source for IPv6
    2025-10-04T19:05:48Z ERR Cannot determine default origin certificate path. No file cert.pem in [~/.cloudflared ~/.cloudflare-warp ~/cloudflare-warp]. You need to specify the origin certificate path by specifying the origincert option in the configuration file, or set TUNNEL_ORIGIN_CERT environment variable originCertPath=
    2025-10-04T19:05:48Z INF cloudflared does not support loading the system root certificate pool on Windows. Please use --origin-ca-pool <PATH> to specify the path to the certificate pool
    2025-10-04T19:05:48Z INF ICMP proxy will use 192.168.1.233 as source for IPv4
    2025-10-04T19:05:48Z INF Tunnel connection curve preferences: [X25519MLKEM768 CurveP256] connIndex=0 event=0 ip=198.41.200.73
    2025-10-04T19:05:48Z INF ICMP proxy will use fdaa:2937:24e1::80e in zone Wi-Fi as source for IPv6
    2025-10-04T19:05:48Z INF Starting metrics server on 127.0.0.1:20241/metrics
    2025-10-04T19:05:48Z INF Registered tunnel connection connIndex=0 connection=ea01956f-739a-4251-aeb4-ea9b96f24037 event=0 ip=198.41.200.73 location=yyz06 protocol=quic
    ```

4. Say Hello to the World! Go on, copy that link and open it in your browser! What's on the screen? Yes! It's your little Python web server! You haven't closed it, right? lol. It's now visible to anyone in the world who has that secret link. You did it!

### For my macOS Friends

1. Summon Python
   1. Open your `Terminal`. (Press `Cmd + Space`, type `Terminal`, and hit `Enter`).
   2. Chant this spell: `python3 -m http.server`
   3. Tada! That's it! Your little server should be running. You can now visit `http://127.0.0.1:8000` in your browser to see it.
2. Getting Your Magic Cauldron: Homebrew
   1. Your Mac has a super cool magic cauldron called Homebrew that can get you almost any tool you need! First, let's open `Terminal`. Press `Cmd + Space` to open Spotlight, type `Terminal`, and press `Enter`.
   2. Check if you already have Homebrew by typing `brew --version`. If you see a version number, you can skip to the next step! If not, just copy this whole spell and paste it into your Terminal to install it: `/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"`
   3. It might ask for your password. Don't worry, it's safe!
3. Opening the Tunnel!
   1. Type `brew install cloudflared` and press `Enter`.
   2. And for the final magic trick, type: `cloudflared tunnel --url http://127.0.0.1:8000`
   3. After a few seconds, you'll get your very own special `trycloudflare.com` link. Share it with a friend and show them your magic!

### For my Linux Adventurers

For all the Linux wizards out there, I have a feeling you might already know this little trick! The steps are super similar to the Windows ones, and I totally believe in you! You got this!

### But... What Was That Magic All About?

So why did we go through all that trouble? Why did I design this little magic trick for you? Here's the secret.

Think of your home's router as a very strict but well-meaning castle guard. Its job is to protect all the devices in your home (your computer, your phone) from scary things on the internet. It gives all your devices a secret, internal IP address that only people inside the castle can see.

The problem is, this guard is SO good at its job that when a friendly visitor from the outside world tries to visit your new Python website using your public IP address, the guard just says "NOPE!" and slams the door. It's a very common problem for everyone!

So, how did Cloudflare Tunnel work? What was its magic?

Well, the Cloudflare Tunnel is like a secret royal messenger! Instead of trying to break down the castle gate from the outside, the messenger starts from inside your castle (your computer) and creates a secure, secret tunnel that leads out to the world. Anyone with the secret address (that trycloudflare.com link) can give a message to the messenger, who then safely brings it back to your server inside.

The grumpy castle guard never even has to open the main gate! Isn't that clever? (´-ω-)`

## Magical Conclusion

Look at you! You just summoned a little web server from thin air with a Python spell, and then you opened a magical portal for the entire world to see using Cloudflare Tunnel! You should be super proud of yourself!

Now, this "quick tunnel" was a super fun party trick, right? It was like shouting "hello!" to the entire world from our digital doorstep, and it was the perfect way to get our first taste of success! But what if you want to create a private, cozy space just for your devices to talk to each other, without letting the whole world peek in?

That's exactly what's next on our adventure! We're going to learn a whole new kind of magic called Tailscale. Instead of opening a big door to the public, Tailscale helps us build a secret, magical network just for our own devices. It's like creating a private little clubhouse where your laptop, phone, and new server can all whisper secrets to each other, no matter where they are in the world! And with its own special spell, `tailscale serve`, we'll see how easy it is to share services inside our exclusive club.

Thank you for being such a wonderful magic apprentice today! See you next time! (´-ω-)`
