# Secure share

A client-side secure P2P file sharing using WebRTC.

## Features

- Send multiple files in parallel.
- Generate SDP connection for WebRTC data channel.
- No server side (only use public STUN servers for ICE candidates).
- PGP Encryption.
- Responsive UI.
- Open-source license.
- QR Scan for SDP trade.
- Paste from the clipboard.

## Usage

1. The offer goes to <https://share-17ddf.web.app//>.
2. The offer generates an offer link and then sends it to the answer.
3. The answer opens the offer link and then sends it to the offer.
4. The offer paste the answer code then click `Accept Answer`.
5. The offer/answer can now select and send files.


## How does it work?

Secure share client will get ICE Candidate from STUN/TURN server and make a connections between peers.

Thanks to the Interactive Connectivity Establishment (ICE) protocol, Two peers will have the shortest path to travel between them without caring the Network address translation (NAT).

WebRTC protocol will secure by DTLS (Datagram Transport Layer Security) But DTLS can be vulnerable to man-in-the-middle (MITM), So we provide a second layer encryption using PGP (RSA-OAEP-1024, AES-128).



