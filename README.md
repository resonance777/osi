# osi
# OSI Model Data Flow Simulation (Python)

## About
This project is a simple Python simulation that demonstrates how data flows through the OSI model.

The program shows how a message is:
- Encapsulated (forward direction)
- Transmitted
- Decapsulated (backward direction)

It is designed for learning and visualization purposes.

---

##  How It Works
The user enters a message, and the program simulates how this message is processed at each OSI layer.

### Forward (Encapsulation)
- Application Layer → User input + HTTP simulation
- Presentation Layer → Base64 encoding + UTF-8 encoding
- Session Layer → Session ID added
- Transport Layer → Message split into segments + checksum + port number
- Network Layer → IP addresses added
- Data Link Layer → MAC addresses added
- Physical Layer → Data converted to binary

### Backward (Decapsulation)
- Binary converted back to data
- MAC and IP headers removed
- Segments reassembled
- Session removed
- Data decoded and decrypted
- Original message delivered back to application layer
