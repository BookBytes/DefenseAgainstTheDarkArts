# Tuesday, September 5th: Course Introduction
* This is my favorite course
* Administrative changes:
	- Grace period on all lab due dates
	- No class on the week of Thanksgiving
* A little exercise:
	- When you hear the term "cyber security", list some topics, issues, or things that come to mind. Free-for-all
* What this course is NOT
* What this course IS and expectations
* The schtick is very different in this course, and this may be arguably the most "different" course you will take in the CS curriculum
* Terminology: Is it Computer Security?  Is it Information Security (infosec)?  Is it Cyber Security?
* The definition of security in the context of technology, information, computers
* Why study security?
	- So how far have we come? (or lack thereof)
	- The Tacoma Bridge Failure https://www.youtube.com/watch?v=XggxeuFDaDU
* One outcome of this course: question and debate everything
* What's my ultimate goal for you in this course?  We'll revisit this on the last day of class.
* Technology requirement for this class: virtual machine (we will use VirtualBox) and Kali Linux

# Thursday, September 7th: Networking 101
* The really hard problems in Security
	- Sexual harassment and gender
	- Attribution
	- Software security
* The "Trinity of Trouble" by Gary McGraw
	- Complexity
	- Extensibility
	- Connectivity
* Why study networking?
	- The "Connectivity" issue
	- Where the "cool stuff" happens
	- The cyber attribution problem => https://twitter.com/thegrugq/status/706545282645757952
* The telephone conversation analogy for basic networking stuff
* Take it a step further: the OSI model and the seven layers
* Analogy for the OSI model: the US Postal Service => http://bpastudio.csudh.edu/fac/lpress/471/hout/netech/postofficelayers.htm
* Get comfortable reading Request For Proposals (RFPs):
	- Internet Protocol (IP): RFC 791 => http://www.ietf.org/rfc/rfc791.txt
	- Transfer Control Protocol (TCP): RFC 793 => http://www.ietf.org/rfc/rfc793.txt
* A packet: contains implementations of all the protocol layers; encapsulation model
* A PCAP: a file of packet captures from a network

# Tuesday, September 12th: Sniffing
* The next lab
* So you may be curious: how did we capture all those packets?
* The Wall of Sheep
* tcpdump, Wireshark, ettercap
* Two types of networks:
  1. Unswitched - packets flow through all devices on network but you look at only the packets addressed to you......
    - Welp... http://superuser.com/questions/191191/where-can-i-find-an-unswitched-ethernet-hub
  2. Switched - packets flow through specific devices on network
* Promiscuous mode
* Preventing sniffing:
  1. Use encryption and encrypted network protocols
  2. VPN
  3. Use switched network......?
* LAN Tap: http://hakshop.myshopify.com/products/throwing-star-lan-tap-pro
* Address Resolution Protocol
  - IP address to MAC address on a network
  - Recall OSI model and packets
  - `arp -a`
  - ARP cache on machine for 20 minutes
  - No authentication
* ARP spoofing or ARP poisoning
* Bettercap

# Thursday, September 14th: Scanning
* Last class: sniffing unswitched and switched networks
* Is sniffing still relevant today?
* Preventing sniffing on switched network:
  - anti-arpspoof
  - ArpON
  - Antidote
  - Arpwatch
* About that problem on the PCAPs lab
  - A goal of this class: recognition and mindset
  - Base64: binary-to-text encoding scheme.  That is: binary data to ASCII
  - http://stackoverflow.com/questions/6916805/why-does-a-base64-encoded-string-have-an-sign-at-the-end
  - Why? Dangers in printing payload: https://unix.stackexchange.com/questions/73713/how-safe-is-it-to-cat-an-arbitrary-file
  - Why? Basic authentication on web. Example: https://github.com/LiamRandall/BsidesDC-Training/blob/master/http-auth/http-basic-auth-multiple-failures.pcap
* Scanning
  - Why? Network reconnaissance.  Warfare 101
  - What devices and computers are up?
  - What ports are open on a computer?
  - What services are running
  - Determine possible vulnerabilities
* Is scanning still relevant today?
* Basic method: ping sweep
* Problems with ping?
* Netcat
* Nmap