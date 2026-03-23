<p align="center">
  <img src="documents/Source%20Images%20%26%20Other%20DIagrams/logo1.png" width="180">
</p>

<h1 align="center">
LoRa Room Server — Documents Repository
</h1>

<p align="center">
Polytech Grenoble – INFO4 – 2025-2026
</p>

The project implements a persistent room-based messaging server running on a Raspberry Pi,
connected to a LoRa / Meshtastic network, allowing structured communication without internet.

---

## Contents

This repository includes:

- Final report
- Presentations (pre-defense and final defense)
- A1 Poster
- A4 Flyer (tri-fold brochure)
- Architecture diagrams
- Technical documents
- Weekly progress reports
- Source images and graphics used in the poster / flyer / report

Directory structure:
```
documents/
├── Diagrams/
├── Final Report/
├── Flyer/
├── Poster/
├── Presentations/
├── Initial Description/
├── Technical/
├── Weekly Progress Reports/
└── Source Images & Other Diagrams/
```

---

## Project Information

Developed by:  
Arhan UNAY  
Adam TAWFIK  

Supervised by:  
François LETELLIER  

Polytech Grenoble – INFO4  
2025-2026

---

## Source Code Repository

The source code of the project is available in the following repository:

https://github.com/arhis222/Meshtastic-LoRa-Room-Server-Code

This code repository contains:

- Python implementation of the Room Server
- Communication layer (LoRa / Meshtastic)
- SQLite storage module
- Command parser
- Technical architecture notes

---

## Description

The LoRa Room Server extends Meshtastic networks by adding:

- persistent chat rooms
- message history storage
- structured commands
- anti-spam protection
- message chunking for LoRa limits
- FIFO queue for safe transmission

The system runs fully offline on a Raspberry Pi connected to a LoRa module.

---

## License

This project is provided for academic purposes.
