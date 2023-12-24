
# Generate and Capture RADIUS Traffic

**Description:**

This project dives into the exploration of clear-text protocols, with a specific focus on the RADIUS protocol. The primary aim is to dissect the process of generating, capturing, and analyzing RADIUS traffic using Wireshark. By unveiling the vulnerabilities associated with unencrypted communication, the project underscores the critical need for secure data transmission in network protocols.




## Project Walkthrough:

**Overview of Clear-Text Protocols:**

Clear-text protocols are communication methods where data is transmitted in an unencrypted, readable format. While they offer simplicity and efficiency, they expose data to interception. In this project, we focus on RADIUS as a clear-text protocol, exploring its vulnerabilities and highlighting the need for securing sensitive information during network communication.

**Accessing RADIUS Server GUI:**

* Open the RADIUS server GUI.
* Briefly introduce RADIUS as a client/server protocol operating on Port 1812.

![App Screenshot](https://i.imgur.com/AnzC7Jt.jpg)

**Capturing RADIUS Traffic Using a Filter:**

* In Wireshark, set a filter for capturing traffic on Port 1812.
* Initiate the capture to focus only on RADIUS traffic.

![App Screenshot](https://i.imgur.com/NaxO7Pl.jpg)

**Authenticating Using NTRadPing:**

* Use NTRadPing, the RADIUS client, to send authentication requests.
* Configure the client with the server's IP, port, and shared secret.
* Send successful and unsuccessful authentication requests.

![App Screenshot](https://i.imgur.com/u55CiuD.jpg)

![App Screenshot](https://i.imgur.com/ybUekJS.jpg)

![App Screenshot](https://i.imgur.com/IChd4el.jpg)

**Analyzing Unencrypted RADIUS Traffic:**

* Stop Wireshark capture and observe unencrypted RADIUS traffic.
* There is lack of security as anyone can see requests visible to anyone in the middle.


![App Screenshot](https://i.imgur.com/hjVRkGa.jpg)


**Decrypting RADIUS Passwords in Wireshark:**

* RADIUS employs the MD5 hashing mechanism, using a pre-shared secret, to conceal passwords during transmission, ensuring that even if intercepted, only the hashed values are exposed, enhancing the security of the authentication process.
* Navigate through Wireshark to decrypt RADIUS passwords.
* Update Wireshark preferences with the shared secret.



![App Screenshot](https://i.imgur.com/PmkZmrG.jpg)

![App Screenshot](https://i.imgur.com/VLRNOq6.jpg)


![App Screenshot](https://i.imgur.com/AJGjvqd.jpg)







## Summary:

The Network Traffic Analysis - RADIUS Protocol project delved into the examination of RADIUS, an unencrypted protocol widely used for authentication and accounting in network services. The project highlighted the vulnerability of RADIUS to interception and demonstrated how Wireshark could decrypt RADIUS passwords. By capturing and analyzing RADIUS traffic, users gained insights into the clear-text nature of the protocol and the importance of implementing stronger security measures in network authentication.
