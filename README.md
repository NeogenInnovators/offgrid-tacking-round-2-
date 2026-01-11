## Round 1 repo : https://github.com/NeogenInnovators/Off-grid-Tracker

## Round 2 Demo Video 📁: https://drive.google.com/file/d/1f1_tJELBBs-CuIoNS1I9qu9m3IDeIrPI/view?usp=drivesdk
# 1. GPS Location Tracking Module 

---

The **GPS Location Tracking Module** is the core intelligence layer of the **Off-Grid Tracking System**. In **Round 2**, this module has been significantly upgraded to provide:

* Higher **location accuracy**
* Better **signal reliability**
* Smarter **data processing**
* Lower **power consumption**
* Fully **offline operation**

Unlike traditional tracking systems that depend on **cellular networks or internet connectivity**, this system operates **entirely independent of any network infrastructure** by using **GPS + LoRa communication**.

This makes the solution **ideal for forests, mountains, disaster zones, border areas, and remote villages** where communication networks are unavailable or unreliable.

---

## Objective of This Module
<img width="1919" height="1079" alt="image" src="https://github.com/user-attachments/assets/eade98be-561f-4d91-bdc9-1a94d35868f3" />


The GPS tracking enhancement in Round 2 is designed to:

* Continuously track the **real-time position** of a person or asset
* Maintain **reliable communication** in zero-network zones
* Reduce **false location jumps** and GPS noise
* Optimize **battery usage**
* Provide **actionable tracking intelligence** to authorities
* Create a **distributed location checkpoint network** using LoRa poles

---

## Hardware Components Involved

###  GPS Module (GY-NEO6MV2)

* High-sensitivity multi-channel GPS receiver
* Capable of receiving signals from multiple satellites simultaneously
* Provides:

  * Latitude
  * Longitude
  * Altitude (optional)
  * Speed
  * Time (UTC)

### Microcontroller Unit (Arduino Nano)

* Acts as the **brain of the wearable**
* Responsible for:

  * Reading raw GPS data
  * Parsing NMEA sentences
  * Filtering noise
  * Running movement detection logic
  * Controlling LoRa transmission
  * Power management

### LoRa Transceiver

* Enables **long-range (5km) communication**
* Works without:

  * SIM card
  * Internet
  * Mobile tower
* Used to transmit compressed GPS packets to nearby poles

---<img width="364" height="1195" alt="GPS Watch Data Workflow_ Pole_Checkpoint Interaction - visual selection (3)" src="https://github.com/user-attachments/assets/cc31a2ab-419c-44c9-9d38-f6b983a771c5" />

 # 2.Multi-Pole Expansion for Enhanced Coverage Radius
 ![IMG_20260105_154703787_HDR](https://github.com/user-attachments/assets/46d2c71f-36a9-48c2-8d11-6b3408cc3a3b)

In Round 2, the Off-Grid Tracking System introduces network expansion to significantly increase the geographical coverage area and improve tracking reliability.

Instead of relying on a two LoRa pole, the system now supports adding one more  LoRa tracking pole in a distributed manner. Each new pole acts as a smart relay checkpoint, effectively:

Expanding the total covered radius

Eliminating blind zones

Improving signal availability

Increasing system scalability

Making the system suitable for large forests, border areas, and disaster zones

## Multi-Pole Network Concept

In the enhanced system:

Three LoRa poles are deployed across the region

Each pole:

Acts as an independent receiving station

Covers its own local radius

Together, all poles form a distributed coverage mesh

 Result:
The total coverage area becomes the union of all pole coverage zones, allowing tracking across very large regions.
 ## A (radius covered 5 Km) + B (radius covered 5 Km) = Total (radius covered 10 Km)     {In round one}
 ## A (radius covered 5 Km) + B (radius covered 5 Km) +  C (radius covered 5 Km) = Total (radius covered 13 Km)      {UPDATION IN ROUND 2}

Excellent — this is another **very strong Round-2 feature**. I’ll write it in **deep, professional, README-ready format** just like your GPS and pole sections, with **technical depth + judge-friendly explanation**.

You can directly paste this into your documentation.

---

#  **3. NFC-Based User Identification**

---
The Off-Grid Tracking System introduces **NFC (Near Field Communication) based user identification** to provide **secure, fast, and contactless identity verification** inside the **completely offline tracking network**.

This enhancement ensures that:

* Each tracked person is **uniquely identifiable**
* Checkpoints can **verify physical presence**
* The system can distinguish between:

  * Multiple users
  * Multiple devices
  * Multiple movement paths
* All this works **without internet, passwords, biometrics, or mobile phones**

---

## **Problem Without NFC**

In a pure GPS-based system:

* You know **where a device is**
* But you cannot always guarantee:

  * **Who is carrying it**
  * Whether devices were **exchanged**
  * Whether the person actually **passed through a checkpoint**

NFC solves this by adding a **human identity layer** on top of GPS tracking.

---

##  Hardware Components Involved

###  **NFC Tag / Card**

* Each user is assigned a **unique NFC tag or smart card**
* Contains:

  * Unique ID (UID)
  * Optional encrypted data
* Can be:

  * Card
  * Keychain tag
  * Wristband

### **NFC Reader at Pole / Checkpoint**

* Installed at:
  * LoRa tracking poles
* Reads NFC tag when brought within **2–5 cm**

### **Microcontroller at Pole**

* Controls:

  * NFC reader
  * LoRa module
  * Data logging
* Packages and transmits NFC events

---

## **End-to-End Working Flow**

---

### **Step 1: User Identity Assignment**

* Each user is registered in the system
* Their:

  * NFC UID
  * Wearable Device ID
    Are **linked together** in the database

---

### **Step 2: User Reaches Checkpoint / Pole**

* User brings NFC card near reader
* No contact, no buttons, no delay

---

### **Step 3: Instant NFC Detection**

* NFC reader:

  * Reads the UID in **< 1 second**
  * Sends it to pole MCU

---

### **Step 4: Local Validation & Logging**

The pole:

* Records:

  * User ID
  * Time stamp
  * Pole ID (location)
* Creates a **verified presence event**

---

### 📡 **Step 5: LoRa Transmission**

* The pole sends this record via **LoRa**
* Data packet includes:

  * User ID
  * Device ID
  * Pole ID
  * Time
  * Event type = “NFC_CHECKPOINT_PASS”
  
<img width="468" height="818" alt="NFC-Based User Checkpoint Workflow - visual selection (1)" src="https://github.com/user-attachments/assets/06374b55-bd95-49ac-adb0-71024afb5ebc" />

---
"VIDEO DEMO : https://drive.google.com/file/d/1f1_tJELBBs-CuIoNS1I9qu9m3IDeIrPI/view?usp=drivesdk"
