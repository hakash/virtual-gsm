# virtual-gsm
A simple node.js app for emulating the modem sending and receiving the text messages. 

This app will be a replacement for the hardware based GSM Modems used for sending SMS or text messages. A lot of old legacy systems does not support using web-based APIs, SMPP or other protocols for sending and receiving text messages, and relies upon directly connected hardware modems. 

In a rapidly chaning world with virtualization and cloud as the new norm, there are many cases where the directly connected hardware is no longer an option. Virtualizing the serial-ports of systems to allow the usage of serial-to-IP converters and virtual COM-ports has long been an option for housing the physical hardware in another location, but there are no good alternatives for converting the old AT-commands from the legacy systems to a more modern protocol.

SMS Server Tools 3 will mainly be used as the SMS client part during development. At some later point adjustments will probably have to be made when real world experience and testing is done.

##The initial road map is as follows:
1. Accept connections from SMS software with basic dummy emulation of the AT-commands used by the software
2. Interpret the data to extract the to, from, timestamp and body and save to file as json for later parsing by other software.
3. Add support for emulating incoming messages read from a file
4. Add support for storing outgoing and incoming messages in a database
5. Add support for sending through simple URL API's, i.e. http://myapi.example.com/send.php?to=12345678&from=87654321&message=...
6. Add support for receving through an API
