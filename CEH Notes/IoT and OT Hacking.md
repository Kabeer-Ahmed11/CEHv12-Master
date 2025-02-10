# IoT and OT Hacking

## **Gather Information using Online Footprinting Tools**

**https://www.whois.com/whois/**

we can use google dorking for this
example

got from [https://www.exploit-db.com/google-hacking-database](https://www.exploit-db.com/google-hacking-database)

**"login" intitle:"scada login"**

 **intitle:"index of" scada**

**Shodan**

type **port:1883** in the address bar and press **Enter**.
Port 1883 is the default MQTT port; 1883 is defined by IANA as MQTT over TCP.
The result appears, displaying the list of IP addresses having port 1883 enabled

you can gather additional information on a target device using the following Shodan filters:

- **Search for Modbus-enabled ICS/SCADA systems:**
    
    port:502
    
- **Search for SCADA systems using PLC name:**
    
    “Schneider Electric”
    
- **Search for SCADA systems using geolocation:**
    
    SCADA Country:"US"
    

## **Capture and Analyze IoT Traffic using Wireshark**

In Wireshark

Type **mqtt** under the **filter** field and press **Enter**. To display only the MQTT protocol packets.

After establishing a successful connection with the MQTT broker, the MQTT client can publish messages. The headers in the Publish Message packet are given below:

- Header Flags: Contains information regarding the MQTT control packet type.
- DUP flag: If the DUP flag is 0, it indicates the first attempt at sending this PUBLISH packet; if the flag is 1, it indicates a possible re-attempt at sending the message.
- QoS: Determines the assurance level of a message.
- Retain Flag: If the retain flag is set to 1, the server must store the message and its QoS, so it can cater to future subscriptions matching the topic.
- Topic Name: Contains a UTF-8 string that can also include forward slashes when it needs to be hierarchically structured.
- Message: Contains the actual data to be transmitted.
- Payload: Contains the message that is being published.

The Publish Complete (PUBCOMP) packet is the response to a Publish Release (PUBREL) packet.