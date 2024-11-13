## OSI Model
Layers are organized into levels of increasing complexities. This means that lower-level layers are specific to the medium, and higher-level layers are specific to the application.
	- ### Application
	- ### Presentation
	- ### Session
	- ### Transport
	  Allows end-to-end communication via multiplexing.
	  
	  This effectively adds the "room number", which means you can multiplex a connection into individual ports.
	- ### Network
	  Creates, maintains, and uses global networking links.
	  
	  Provides services such as routing and forwarding from potentially non-adjacent hosts.
	  
	  Also uses the ARP to convert addresses from the data link layer to compatible addresses.
	  
	  This introduces the idea of a global address. This primarily is where IP addresses are implemented.
	- ### Data link
	  Checks that you are getting consistent and reliable connections via the link. This also arbitrates various conversations.
	  
	  Re-frames transmitted bits for data an control.
	  
	  Hardware address for the system. Typically interfaced via Ethernet, and the address is better known as the MAC address.
		- #### Frame Schema
		  * Preamble
		  * Destination Mac Address (6 bytes)
		  * Source Mac Address (6 bytes)
		  * Type or Length (2 bytes)
		  * User Data (46 to 1500 bytes)
		  * Frame Check Sequence (4 bytes)
	- ### Physical
	  Controls the distribution of raw bit streams over the medium in question.
	  
	  Primarily handled by modems (shorthand for modulator/de-modulator).