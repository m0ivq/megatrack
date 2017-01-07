# MegaTrack
Standalone APRS Tracker with Digipeater &amp; iGate options

# What is it?
An APRS tracker that uses a fork of markqvist/LibAPRS modified to work with the Arduino Mega (ATMega2560). The RF stage uses a DRA818V transceiver module based on the RFIC RDA1846 and a Mitsubishi RA08H1317M RF Amplifier Module to give up to 10W RF Power (the RA08H1317M is actually rated at 8W but happily works at 10W reliably).

# Why?
The project was originally born out of the frustration of not being able to source a standalone, low cost APRS tracker for RAYNET use in the UK. The Byonics MicroTrak 8000 (superceded by the Micro-Trak RTG) would have done the job if I didn't have to pay the import duty from the US. The original design was based on the MicroTrak 8000 but with the DRA818V (cheaper), attenuator between the RF Module and RF Amplifier (the RA08H1317M can't handle the 300mW from the Radiometrix HX1 module used in the MicroTrak) and output filter to suppress the harmonics.

In 2015 the transceiver of my home station iGate died so this project evolved to incorporate digipeater/iGate functionality, negating the need for the Raspberry Pi/2m Transceiver combo and interface hardware. The Ethernet connection is provided by an ENC28J60 SPI Ethernet LAN Network Module (still working on this bit!).
