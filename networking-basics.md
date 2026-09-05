# Basics of Computer Networks & Operating Systems

## LAN

collection of connected devices in a single geographic area

### Features

* limited coverage
* high transfer speeds
* resource sharing
* secure & controlled access


### Components

* **Devices** (Nodes) : Computers, printers etc
* **Switches** : act like traffic managers, ensuring right data goes to right device w/o delays
* **Routers** : connects LAN to internet
* Cables or Wireless connections
* Network Interface Cards (NICs) : installed in *each* device, allowing it to connect to LAN

### Topologies (Layouts)

* **Bus** : single cable (bus) connects all devices. Simple, cheap but fails if bus fails
* **Ring** : devices connected in circular path. Data travels around ring in **single direction**. Fails if any 1 device fails.
* **Star** : devices connected to central hub or switch. Common. 1 device failure => network remains same. Reliable

## WAN

[reference](https://www.tp-link.com/ph/blog/2065/what-is-wan-wide-area-network-a-simple-guide/)

large network connecting devices & smaller networks (eg: LANs) across bigger geographic areas (across continets). Eg: Internet.

### Types of WAN

* Leased line: dedicated point to point connection between 2 locations
* MPLs (Multi Protocol Label Switching) : Private, high-performance technique for WAN routing used by service providers
* Broadband Internet
* 4G/5G/LTE Wireless WAN : LTE = Long Term Evolution
* Satellite WAN 
* ISDN : Integrated Services Digital Network : Digital transmission over traditional telephone lines
* Frame Relay : Packet switching protocol for transmitting data over WAN
* SD-WAN (Software Defined WAN) : Modern WAN using software to manage multiple connection types (MPLS, broadband, LTE)

### WAN router

network device connects LAN to WAN

### WAN Optimization

set of techiniques to improve performance, speed & efficiency of data transmission across WAN

## Wireless Networks

* no cables
* radio waves (eg: cellular)
* Types: LAN, WAN, PAN (eg: Bluetooth), Zigbee

### Zigbee (LR WPAN)

* low power, low data rate & short range communication
* used for home automation
* Physical (1) & Medium Access Control (2) layer defined by IEEE 802.15.4 (LR WPAN)
* Higher protocols defined by Zigbee alliance
* 75-100 metres
* join quickly : < 30ms
* 3 frequency bands (each network uses only 1 channel at a time)
	* 868 MHz for Europe 1 channel
	* 915 MHz for USA  & Australia - 10 channels
	* 2.4 GHz worldwide - 16 channels 

* stochastic addressing : random
* network types
	* Star : 1 Coordinator + many End devices
	* Mesh : 1 Coordinator + many Router + many End devices. **Self healing**
	* Tree : 1 central Coordinator + many Router + many End devices. Routers extend coverage.
* Device types:
	* **Coordinator** : 
		* starts network & allows joining
		* assigns addresses
		* maintains security
		* Only 1 
	* **Router**
		* Forwards data packets between devices
		* extends range by acting as intermediary node
		* multiple
		* supports mesh network
		* never sleeps
		* multiple
	* **End device**
		* communicates only with parent (Coordinator or Router)
		* can sleep
		* low energy consumption
		* eg: switches, control units, sensors

## WLAN (Wireless Local Area Network)

* communicate wirelessly within limited area
* Coverage: building, tech park
* IEEE 802.11 + HiperLAN
* **Access Point** : connects WLAN to wired network => allows clients to communicate via wireless adapters
* to protect use WPA2 / WPA3 encryption 


### Components

* **Stations (STA)**  : laptops, smartphones, IOT devices
* **Access Points (AP)** : bridge between wireless & wired network
* **Base Service Set (BSS)** : smallest operational unit. Group of stations under 1 AP
* **Extended Service Set (ESS)** : multiple BSS connected via a Distribution System (DS)
* **Distribution System (DS)** : wired backbone linking multiple BSS in ESS

### Standards

* 802.11 (WiFi)
	* Foundational
	* specifies PHY & MAC layers
* 802.11a
	* 5 GHz
	* higher data rates
	* low interference (less crowded frequency)
	* high speed wireless in smaller areas
* 802.11b
	* 2.4 GHz
	* lower range but lower maximum data speed
	* compatible with older devices
	* homes/small offices
* 802.11g
	* 5 GHz
	* speed > 802.11b
	* backward device compatibility with 802.11b
	* small networks with moderate speeds
* 802.11n
	* 2.4 GHz & 5 GHz
	* Introduces MIMO : Multiple Input Output
	* improved converage
	* modern home & office WLAN
* 802.11ac
	* 5 GHz
	* very high data rates
	* advanced modulation techniques
	* video streaming & gaming
* 802.11ax (WiFi 6)
	* 2.4 , 5, 6 GHz
	* OFDMA & Mul MIMO
	* improved efficiency, capacity in dense networks

* B-NA-X : 2.4 GHz, rest 5 GHz
	
### WLAN:  Limitations

* Interference
* Secu vulnerabilities
* Limited Range
* Performance variability based on standard (802.11b/g/n/ac) & environmental conditions 


## LAN testing

* LAN cable (aka Ethernet cable) can be tested with or w/o LAN tester
* W/o
	* Network test from computer
	* try different cable
	* check Physical damage
	* use Multimeter
* With tester
	1. 1 cable end <-plug-> tester TX insertion port 
	2. 1 cable end <-plug-> tester RX receiver jack 
	3. switch on tester & check the lights
	4. if any lights other than Ground don't turn on, replace cable

## LAN Proxy Server

* intermediary sitting between device & internet
* masks user's IP
* cache data => improve browsing speed
* adds security layer
* filter content
* examine Packet headers & payloads
* encrypt web requests
* improve SEO monitoring : reduces location based & anti competitor results

### Proxy Types

#### Forward Proxy

Sits between users & internet, hiding the client's identity.

* Filters outgoing traffic
* Enhances user privacy
* Used by orgs to monitor employee traffic

#### Reverse Proxy

Sits in front of servers to hide/protect.

* Load balances traffic
* caches content to reduce traffic
* improves Security & Performance

#### Web Proxy

Handles only HTTP(s) traffic

* Often used in browsers
* Eg: Apache, HAPProxy

#### Anonymous Proxy

Partial anonymity : IP hidden but proxy identity is detectable

#### High Anonymity Proxy - Elite Proxy

Hides both IP & the fact you're using a proxy

#### Transparent Proxy

* Does not hide IP
* filtering only
* Users may not be aware of its usage

#### CGI Proxy

Access websites via web form usage

* no installation
* slow & outdated
* less private

#### Suffix proxy

Adds suffix to url to bypass filters

* easy to use
* low anonymity


#### Distorting proxy

Sends fake IP address

* more private
* false headers
* bypass region blocks

#### Tor Onion Proxy

Routes traffic via multiple encrypted layers

* hard to track
* multi level encryption
* open source & free

#### I2P Anonymous Proxy

Routes traffic via distributed encrypted network

* Very strong anonymity
* Resistant to censorship
* Fully decentralized

#### DNS Proxy

Handles DNS requests on behalf of clients

* speeds up DNS responses with caching
* block harmful domains
* content filtering usage

#### Rotating Proxy

New IP address for each request or user

* best for web scraping
* hard for websites to block
* used widely in automation

## OSI layers

6. Application Layer
5. Session & Presentation Layer
4. Transport Layer
3. Network Layer
2. Data Link Layer
1. Physical Layer






1. Physical layer