# How-to-Build-a-Pumpkin-Pi-The-Rogue-AP-MITM-Framework-That-Fits-in-Your-Pocket

A man-in-the-middle attack places you between your target and the internet, pretending to be a Wi-Fi network while secretly inspecting every packet that flows through the connection. The WiFi-Pumpkin is a rogue AP framework to easily create these fake networks, all while forwarding legitimate traffic to and from the unsuspecting target.

Today, i'll show you how to set up this framework on a low-cost Raspberry Pi running Kali Linux. You may want to look into getting a Raspberry Pi 3 kit or Raspberry Pi 3 B+ kit for this guide. If you already have one, great, let's begin!

# Man-in-the-Middle Pumpkin Pie
On the Raspberry Pi 3 running Kali Rolling, some Kali Linux tools can be broken out into standalone, almost disposable devices. One perfect example is the WiFi-Pumpkin, an attack framework for creating rogue access points to stage man-in-the-middle (MitM) attacks. This allows an attacker to lure victims to their evil access point and begin monitoring internet traffic, effectively seizing control over the flow of data to any connected victims.
