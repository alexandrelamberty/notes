# Network

## Static IP

How to set a static ip to be used by the dhpc server of
your router.

### Get Network Interface

```sh
ip link show
```

ex: `enp2s0`

nmcli dev list iface eth0 | grep IP4

### Netmask

### Gateway

### #DNS Name servers

```
auto ens18
iface ens18 inet static
  address 192.168.0.2
  netmask 255.255.255.0
  gateway 192.168.0.1
  dns-nameservers 89.207.128.252 89.207.130.252
```

### Restart Neworking

```sh
ip link showPGi
```

## Network discory

In this section we will see how to scan our network to discover the
devices connected to it.

### Nmap

```sh
ip addr
```

```sh
sudo nmap -sn 192.168.1.0/24
```

## Wireless Newtwork in Linux

Computer sciences

## Table des matières

    Introduction
    Hardware identification
    Get hardware informations
    Network devices
    Usb devices
    Hardware support
    Package update and upgrade
    Update the package index
    Upgrade packages
    Wireless management
    Setup your connection
    Enable & disable your device
    List the available wireless access points
    Configure your wireless connection
    Get your IP address via dhcp
    Assign your IP manually
    Connecting to an OPEN / WEP WLAN (DHCP)
    Connecting to an OPEN / WEP WLAN (Manual IP Setup)
    iwconfig Commands:
    ifconfig Commands:
    iwpriv Commands:
    iwlist Commands:
    Madwifi-ng Commands:

## Références

https://wiki.archlinux.org/index.php/Wireless_Setup

Introduction
Connect a computer running linux to a wireless network.
Hardware identification
Get hardware informations
Network devices
lshw -C network
Usb devices
lsusb
Hardware support
Package update and upgrade
Update the package index
apt-get update
Upgrade packages
apt-get upgrade
Wireless management
Setup your connection
Enable & disable your device
ifconfig [interface] up
ifconfig [interface] down
List the available wireless access points
iwlist [interface] scan
Configure your wireless connection
iwconfig [interface] key “KEY” mode MODE essid “ESSID” channel INTEGER ap 00:00:00:00:00:00
Get your IP address via dhcp
dhclient [interface]
dhcpcd wlan0
Assign your IP manually
ip addr add 192.168.0.2/24 dev wlan0
ip route add default via 192.168.0.1
Connecting to an OPEN / WEP WLAN (DHCP)
Note: replace [interface] with your interface name as required (e.g. eth1, wlan0, ath0 etc.)

iwconfig [interface] mode managed key [WEP key] (128 bit WEP use 26 hex characters, 64 bit WEP uses 10)
iwconfig [Interface] essid "[ESSID]" (Specify ESSID for the WLAN)
dhclient [interface] (to receive an IP address, netmask, DNS server and default gateway from the Access Point)
ping www.bbc.co.uk (if you receive a reply you have access)
Connecting to an OPEN / WEP WLAN (Manual IP Setup)
Note: replace [interface] with your interface name as required (e.g. eth1, wlan0, ath0 etc.)

It may be necessary to run some packet capture software (e.g. Ethereal) to determine the IP addresses of both the Default Gateway and DNS servers.

iwconfig [interface] mode managed key [WEP key] (128 bit WEP use 26 hex characters, 64 bit WEP uses 10)
iwconfig [interface] essid "[ESSID]"
ifconfig [interface] [IP address] netmask [subnetmask]
route add default gw [IP of default gateway] (Configure your default gateway; usually the IP of the Access Point)
echo nameserver [IP address of DNS server] >> /etc/resolve.conf (Configure your DNS server)
ping www.bbc.co.uk (if you receive a reply you have access)
iwconfig Commands:
Note: replace [interface] with your interface name as required (e.g. eth1, wlan0, ath0 etc.)

iwconfig [interface] mode master (set the card to act as an access point mode)
iwconfig [interface] mode managed (set card to client mode on a network with an access point)
iwconfig [interface] mode ad-hoc (set card to peer to peer networking or no access point mode)
iwconfig [interface] mode monitor (set card to RFMON mode our favourite)
iwconfig [interface] essid any (with some cards you may disable the ESSID checking)
iwconfig [interface] essid “your ssid_here” (configure ESSID for network)
iwconfig [interface] key 1111-1111-1111-1111 (set 128 bit WEP key)
iwconfig [interface] key 11111111 (set 64 bit WEP key)
iwconfig [interface] key s:mykey (set key as an ASCII string)
iwconfig [interface] key off (disable WEP key)
iwconfig [interface] key open (sets open mode, no authentication is used and card may accept non-encrypted sessions)
iwconfig [interface] channel [channel no.] (set a channel 1-14)
iwconfig [interface] channel auto (automatic channel selection)
iwconfig [interface] freq 2.422G (channels can also be specified in GHz)
iwconfig [interface] ap 11:11:11:11:11:11 (Force card to register AP address)
iwconfig [interface] rate 11M (card will use the rate specified)
iwconfig [interface] rate auto (select automatic rate)
iwconfig [interface] rate auto 5.5M (card will use the rate specified and any rate below as required)
ifconfig Commands:
Note: replace [interface] with your interface name as required (e.g. eth1, wlan0, ath0 etc.)

ifconfig [interface] up (bring up specified interface)
ifconfig [interface] down (take down specified interface)
ifconfig [interface] [IP address] netmask [subnet-mask] (manually set IP and subnet-mask details)
ifconfig [interface] hw ether [MAC] (Change the wireless cards MAC address, specify in format 11:11:11:11:11:11)
iwpriv Commands:
Note: replace [interface] with your interface name as required (e.g. eth1, wlan0, ath0 etc.)

iwpriv [interface] hostapd 1 (used to set card mode to hostapd e.g. for void11)

When the monitor mode patch is installed as per the Wireless Build HOWTO the following commands may be used to set the card into monitor mode.

iwpriv [interface] monitor [A] [B]

[A]
0 = disable monitor mode
1 = enable monitor mode with Prism2 header
2 = enable monitor mode with no Prism2
[B]
Channel to monitor (1-14)
iwlist Commands:

Note: replace [interface] with your interface name as required (e.g. eth1, wlan0, ath0 etc.)

iwlist is used to display some large chunk of information from a wireless network interface that is not displayed by iwconfig.

iwlist [interface] scan (Give the list of Access Points and Ad-Hoc cells in range (ESSID, Quality, Frequency, Mode etc.) Note: In tests only worked with Atheros cards).
iwlist [interface] channel (Give the list of available frequencies in the device and the number of channels).
iwlist [interface] rate (List the bit-rates supported by the device).
iwlist [interface] key (List the encryption key sizes supported and display all the encryption keys available in the device).
iwlist [interface] power (List the various Power Management attributes and modes of the device).
iwlist [interface] txpower (List the various Transmit Power available on the device).
iwlist [interface] retry (List the transmit retry limits and retry lifetime on the device).
iwlist [interface] ap (Give the list of Access Points in range, and optionally the quality of link to them. Deprecated in favour of scan)
iwlist [interface] peers (Give the list of Peers associated/registered with this card).
iwlist [interface] event (List the wireless events supported by this card).
Madwifi-ng Commands:
MADWiFi supports virtual access points (VAPS), which means you can create more than one wireless device per wireless card (the host wireless card = wifi0).

By default, a sta mode VAP is created by, which is MadWifi talk for a 'managed mode wireless interface'.

Note: replace athx with your interface name as required (e.g. ath0, ath1)

wlanconfig athx destroy (Destroy VAP, athx)
wlanconfig athx create wlandev wifi0 wlanmode sta (Create a managed mode VAP, athx)
wlanconfig athx create wlandev wifi0 wlanmode ap (Create an Access Point VAP, athx)
wlanconfig athx create wlandev wifi0 wlanmode adhoc (Create an Ad-Hoc VAP, athx)
wlanconfig athx create wlandev wifi0 wlanmode monitor (Create a Monitor mode VAP, athx)

Changing modes:
ifconfig athx down (Take the VAP down)
wlanconfig athx destroy (Destroy the VAP, athx)
wlanconfig athx create wlandev wifi0 wlanmode [sta|adhoc|ap|monitor] (Create a new sta, adhoc, ap or monitor VAP)
Scan for Access Points (requires both steps):
modprobe wlan_scan_sta (To insert the scanning module)
wlanconfig athx list scan (To list the APs)

For more detailed information, see Madwifi Docs

Logicallysecure have produced an A4 leaflet of the above commands that can be downloaded here
