This is a binary explotation challenge. Its a server that listens on port 3490. Any input will cause the program to send a copy of its binary as a response and then close the connection. The binary is vulnerable to buffer overflow. Participants must overflow the 256 byte buffer and then write 12 more bytes out in little endian. These bytes are:

0x7f170f13
0x444f4e54
0x5e3d7d42

This will cause the program to open flag.txt and send it over the socket instead of the binary file.