# Network Traffic Analysis

[All CTF techniques](../ctf-techniques.md)

## My approach

I used Wireshark to narrow packet captures by protocol, endpoint, and conversation. Rather than treating each packet in isolation, I followed exchanges and considered request direction, response direction, and the layer where a field belonged.

My practice included interpreting name resolution, time synchronization, host identity, and wireless management traffic. I documented methods for reconstructing application streams and working with authorized decryption material when available. These exercises reinforced the difference between what a packet directly shows and what a vendor lookup or service convention merely suggests.

## What I learned

Accurate attribution needs context. A network interface vendor does not necessarily identify the complete device, and a familiar port does not establish the actual application. Capture location, packet order, and protocol fields all affect the interpretation.
