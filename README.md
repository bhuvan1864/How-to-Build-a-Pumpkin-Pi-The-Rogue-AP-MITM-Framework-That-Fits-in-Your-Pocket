# How to Build a Pumpkin-Pi:The-Rogue AP-MITM-Framework that fits in your pocket

A man-in-the-middle attack places you between your target and the internet, pretending to be a Wi-Fi network while secretly inspecting every packet that flows through the connection. The WiFi-Pumpkin is a rogue AP framework to easily create these fake networks, all while forwarding legitimate traffic to and from the unsuspecting target.

Today, i'll show you how to set up this framework on a low-cost Raspberry Pi running Kali Linux. You may want to look into getting a Raspberry Pi 3 kit or Raspberry Pi 3 B+ kit for this guide. If you already have one, great, let's begin!

# Man-in-the-Middle Pumpkin Pie
On the Raspberry Pi 3 running Kali Rolling, some Kali Linux tools can be broken out into standalone, almost disposable devices. One perfect example is the WiFi-Pumpkin, an attack framework for creating rogue access points to stage man-in-the-middle (MitM) attacks. This allows an attacker to lure victims to their evil access point and begin monitoring internet traffic, effectively seizing control over the flow of data to any connected victims.


# When to Use the WiFi Pumpkin
The WiFi-Pumpkin is a great tool to use when you can bridge an existing Ethernet or Wi-Fi connection, serving internet access to anyone willing to connect to an open network without asking too many questions. It comes stuffed with features, including rogue Wi-Fi access points, deauth attacks on client APs, a probe request and credentials monitor, transparent proxy, Windows update attack, phishing manager, ARP Poisoning, DNS Spoofing, Pumpkin-Proxy, and image capture on the fly. wireless probe frames can reveal networks a phone or laptop is probing for. One way we can use the WiFi-Pumpkin is to monitor probe frames and create a network in response. We can use the WiFi-Pumpkin to conduct a "Karma" attack and create a network with the same SSID that the target device is expecting, or has connected to before.

The name of your network will have a significant effect on how people interact with it. If you are in a crowd, creating a network with names like "Starbucks" can cause a startling number of devices to connect to you in under a minute. Be creative in how you trick users into connecting to your evil AP. When you want precision control over the various elements of a man-in-the-middle attack, the WiFi-Pumpkin's easy GUI is straightforward enough for most beginners to grasp.

# What You'll Need to Get Started
The setup to create a WiFi-Pumpkin is minimal and requires only a few components. To put this together, you'll need the following.

* Kali compatible wireless network adapter

* Ethernet cable

* Raspberry Pi 3 or 3 B+

* microSD card

* Power source

* USB keyboard/mouse interface

* SD card adapter

* Laptop to load files on the SD card

![prerequisites](https://user-images.githubusercontent.com/67831210/96422281-7155e580-1215-11eb-9bb7-3b9984a6c581.jpg)

I personally use a Raspberry Pi 3 B+ as it's got a large Developer Community

![Raspberry pi 3 B+](https://user-images.githubusercontent.com/67831210/96428456-68691200-121d-11eb-852d-45f7087ec5c1.jpg)

Now fire up your Kali machine terminal and follow the provided steps below

![Screenshot from 2020-10-19 05-36-48](https://user-images.githubusercontent.com/67831210/96428326-440d3580-121d-11eb-89db-131faa09ca07.png)



# Installing & Running WiFi-Pumpkin (Kali Linux)
As before any new install, ensure that your system is fully updated. WiFi-Pumpkin will require that you have an up-to-date Python installed on your machine.

    sudo apt-get update

WiFi-Pumpkin has a number of dependencies you will need to have installed before it can run smoothly. Install the following if you don't already have them on your Kali-Pi.

# Step 1: Install Dependencies
Python's package manager, Pip, will help us manage the rest of the installation. To install it on Kali Linux, run the following commands.

    sudo apt-get install -y python-pip

The next three dependencies will allow WiFi-Pumpkin to verify certificates, add HTTP layer support, and intercept and inspect traffic flows. Install each as shown below.

    pip install service_identity

    pip install scapy_http

    sudo apt-get install mitmproxy
  
# Step 2: Install WiFi-Pumpkin
Download WiFi-Pumpkin by cloning the GitHub repository:

    git clone https://github.com/P0cL4bs/WiFi-Pumpkin.git
  
Now change directory to the downloaded folder

    cd WiFi-Pumpkin
  
And change the permission of the installer file:

    chmod +x installer.sh
  
And then run the installer by entering the following.

    ./installer.sh --install
  
This may take a little time, during which you can go grab some tea..../

# Step 3: Run WiFi-Pumpkin
When it's complete, run WiFi-Pumpkin by simply entering the following.

    sudo wifi-pumpkin

You're ready to get started creating fake APs!

# Some Considerations with the WiFi-Pumpkin
Keep in mind, in order for WiFi-Pumpkin to work, you will need to have access to at least one Kali Linux compatible wireless adapter with AP/Monitor mode support. You will need your Pi to be connected to the internet while also capable of monitoring wireless traffic around you.

You can achieve this by using one wireless network adapter and your Pi's internal Wi-Fi card in tandem or a wired Ethernet connection and one wireless network adapter. In the case your particular Pi isn't Wi-Fi capable, you'll need two wireless network adapters. If you are unsure if the wireless adapter you have supports AP/Monitor mode, you can check in terminal with iw list. If there is an "AP" in the list of "Supported interface modes," then your device supports it.

If you are not familiar with WiFi-pumpkin or you got stuck in between...worry not amigo I'll add in a link for you, you can refer this video where the entire process is demonstrated in detail.

https://www.youtube.com/watch?v=tIM-kdmKhnE&feature=emb_logo


Until next time...

-B

  
  







