# Understanding-and-maintenance-of-Networks-5
# Q1.Connect your laptop and a friend's phone to the same Wi-Fi network, then use the ping command to check if both devices can communicate with each other.<br><br><em><strong>Hint:</strong> On Windows, use 'ping [IP address]' in Command Prompt; on Android, try a ping app or use Termux.</em>
Ans.>
## Practical: Testing Communication Between a Laptop and a Phone Using Ping

### Objective
To check whether a laptop and a friend's phone can communicate with each other on the same Wi-Fi network.

### Requirements
- Laptop with Windows
- Friend's Android phone
- Same Wi-Fi network for both devices
- Command Prompt on Windows and a ping app or Termux on Android

### Procedure

**Step 1: Connect to Wi-Fi**  
Connect both the laptop and the phone to the same Wi-Fi network.

**Step 2: Find the Laptop's IP Address**  
Open Command Prompt on the laptop and type:

```cmd
ipconfig
```

Note the laptop's IPv4 address.

**Step 3: Find the Phone's IP Address**  
Open the phone's Wi-Fi settings, select the connected network, and find its IP address.

**Step 4: Ping the Phone from the Laptop**  
In Command Prompt, type the following command, replacing the example address with the phone's actual IP address:

```cmd
ping 192.168.1.5
```

**Step 5: Check the Result**  
If replies are received, the phone is responding to the laptop's ping requests. If the request times out, check the Wi-Fi connection and whether the router or phone is blocking ping requests.

### Observation
- Laptop IP address: `[Enter laptop IP address]`
- Phone IP address: `[Enter phone IP address]`
- Ping result: `[Replies received / Request timed out]`

### Result
The ping command was used to test communication between the laptop and the phone on the same Wi-Fi network. The test result indicates whether the phone responded to the laptop's ping requests.

### Precaution
# Q2.Run the traceroute (tracert on Windows or traceroute on Mac/Linux) command to www.youtube.com from your device and note down the number of hops it takes to reach the destination.
Ans.>
## Practical: Tracing the Network Route to YouTube

### Objective
To use the `tracert` or `traceroute` command to find the network hops between my device and `www.youtube.com`.

### Procedure

**Step 1: Open the Command Line**
- On Windows, open Command Prompt.
- On macOS or Linux, open Terminal.

**Step 2: Run the Command**

On Windows, type:

```cmd
tracert www.youtube.com
```

On macOS or Linux, type:

```bash
traceroute www.youtube.com
```

**Step 3: Observe the Output**

Wait for the command to display the route. Each numbered line represents a hop (a router or network point along the route). Some hops may time out or may not respond.

### Observation
- **Destination:** `www.youtube.com`
- **Command used:** `tracert` / `traceroute`
- **Number of hops:** `[Enter the number shown in your output]`
- **Result:** The command displayed the route taken by network packets toward the destination.

### Result
The traceroute command was used to examine the network path to YouTube and identify the hops along the route. The total number of hops observed was **[enter your result]**.

### Note
The number of hops can vary depending on the internet connection and routing conditions. If the destination is not reached or some hops time out, record that accurately rather than assuming those hops do not exist.
# Q3.Disconnect one device from the Wi-Fi, then try pinging it again from your laptop and describe the error message you receive.
Ans.
## Practical: Ping a Device After Disconnecting It from Wi-Fi

### Objective
To observe the error message received when pinging a device that has been disconnected from Wi-Fi.

### Procedure
1. Connect the laptop and phone to the same Wi-Fi network.
2. Find the phone's IP address in its Wi-Fi settings.
3. Open Command Prompt on the laptop and run:

   ```cmd
   ping [Phone IP Address]
   ```

4. Disconnect the phone from Wi-Fi.
5. Run the same ping command again and observe the output.

### Observation
The laptop may display the following message:

```text
Request timed out.
```

This means the laptop did not receive a reply to its ping request within the allowed time.

### Result
After the phone was disconnected from Wi-Fi, the laptop stopped receiving ping replies from it. This shows that ping can be used to test whether a device responds over a network.

### Note
The exact error message may vary. A timeout can also occur because of firewall settings or other network restrictions.
# Q4.Create a simple table listing the IP addresses of all devices connected to your home Wi-Fi (use 'arp -a' on Windows), and identify which device belongs to which person or gadget.
Ans.>
## Practical: Listing Devices Connected to Home Wi-Fi

### Objective
To identify devices listed in the local network's ARP table and record their IP addresses and corresponding devices.

### Procedure

1. Connect your laptop to your home Wi-Fi.
2. Open **Command Prompt** on Windows.
3. Type the following command:

   ```cmd
   arp -a
   ```

4. Press Enter to display the IP addresses and physical (MAC) addresses currently listed in the ARP cache.
5. Identify devices by checking their network settings or router's connected-device list.

### Observation Table

| S. No. | IP Address | Device / Person | MAC Address |
|---|---|---|---|
| 1 | [Enter IP address] | My laptop | [Enter MAC address] |
| 2 | [Enter IP address] | My phone | [Enter MAC address] |
| 3 | [Enter IP address] | Family member's phone | [Enter MAC address] |
| 4 | [Enter IP address] | Smart TV / Other device | [Enter MAC address] |

### Result
The `arp -a` command displayed IP-to-MAC address entries stored in the laptop's ARP cache. The available entries were recorded in a table, and devices were identified using their network settings or router information.

### Note
The ARP table may not show every device connected to Wi-Fi. It lists devices whose addresses are currently cached, usually on the local network. To identify all connected devices, check the router's connected-device list as well.
# Q5.Write a one-page report explaining step-by-step how you set up the network, tested connectivity using ping and traceroute, and what results or issues you observed.<br><br><em><strong>Hint:</strong> Include screenshots or command outputs if possible.</em>
Ans.>
# Network Setup and Connectivity Testing Report

## 1. Introduction
The purpose of this practical was to set up a small network and test connectivity between devices using the `ping`, `tracert`, and `arp -a` commands.

## 2. Network Setup
First, I connected my laptop and a friend's phone to the same Wi-Fi network. I checked the IP addresses of both devices through their network settings. This allowed me to prepare for connectivity testing between the devices.

## 3. Connectivity Testing Using Ping
I opened Command Prompt on my Windows laptop and used the following command to test communication with the phone:

```cmd
ping [Phone IP Address]
```

When the phone was connected to Wi-Fi, I checked whether the laptop received replies. I then disconnected the phone from Wi-Fi and ran the command again. The laptop could no longer receive replies, and the output could show **"Request timed out."** This can happen when the device is unavailable or does not respond to ping requests.

## 4. Traceroute Testing
Next, I used the following command to examine the network route to YouTube:

```cmd
tracert www.youtube.com
```

The command displayed the network hops between my device and the destination. Some hops may not respond because routers can block or limit traceroute responses. The number of hops depends on the network route and connection.

## 5. Identifying Network Devices
I used the following command to view IP and MAC address entries stored in the laptop's ARP cache:

```cmd
arp -a
```

I recorded the available addresses and used device network settings or the router's connected-device list to help identify devices on the network.

## 6. Results and Issues Observed
- Ping was used to test whether the phone responded over the local network.
- Disconnecting the phone could result in a timeout or another ping error.
- Traceroute displayed the network path and its responding hops toward YouTube.
- The ARP table showed cached IP-to-MAC address entries, but it might not include every connected device.
- Firewall settings, Wi-Fi client isolation, and unresponsive routers can affect test results.

## 7. Conclusion
This practical helped me understand how devices communicate over Wi-Fi and how command-line tools can be used to troubleshoot network connectivity. Ping tested device responsiveness, traceroute examined the network path, and ARP displayed cached local network address information.

## 8. Evidence / Screenshots
Add screenshots of the actual command outputs below.

- **Ping test:** Attach a screenshot showing the ping results.
- **Traceroute test:** Attach a screenshot showing the `tracert` output.
- **ARP table:** Attach a screenshot showing the `arp -a` output.

A failed ping does not always mean the devices cannot communicate; firewall settings or Wi-Fi client isolation may block ping requests.
