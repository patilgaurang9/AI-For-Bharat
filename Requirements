# Requirements Specification: Krishi-Vani
**Project Goal:** To eliminate information asymmetry in the Indian agricultural supply chain through AI-driven diagnostics and marketplace access.

## 1. System Purpose
Krishi-Vani is an integrated AIoT platform designed for small-scale Indian farmers. It provides real-time crop disease diagnosis, a decentralized marketplace, and multilingual voice assistance to ensure data-driven farming and fair price discovery.

## 2. Functional Requirements (EARS Notation)

### 2.1 Ubiquitous Requirements
* **RQ-01:** The system shall provide a direct farmer-to-buyer marketplace interface.
* **RQ-02:** The system shall support multilingual voice interaction (Speech-to-Text/Text-to-Speech) in Kannada, Marathi, and Hindi.

### 2.2 Event-Driven Requirements
* **RQ-03:** When a user uploads a crop image, the system shall execute a Computer Vision inference model to detect pests and diseases.
* **RQ-04:** When field sensors (DHT-11, Soil Moisture) detect critical thresholds, the system shall trigger an automated alert to the farmer's mobile device via the ESP-8266 module.

### 2.3 State-Driven Requirements
* **RQ-05:** While in low-bandwidth or offline mode, the system shall provide cached diagnostic data and store pending marketplace transactions for later synchronization.

### 2.4 Unwanted Behavior Requirements
* **RQ-06:** If the image quality is insufficient for AI diagnosis, the system shall prompt the user to retake the photo with specific lighting instructions.

## 3. Non-Functional Requirements

### 3.1 Performance & Scalability
* **Latency:** AI inference for disease detection and voice translation must complete in under 2 seconds.
* **Scalability:** The Node.js and MongoDB backend must support 10,000+ concurrent users during peak harvest seasons.

### 3.2 Reliability & Environment
* **Connectivity:** The application must maintain core functionality in 2G/EDGE network environments.
* **Power:** The hardware sensor node must operate for 30+ days on a standard battery/solar charge.

## 4. Target Stakeholders
* **Small & Marginal Farmers:** End-users for diagnostics and price discovery.
* **Mandi Agents:** Procurement and logistics management.
* **Agri-Extension Officers:** Remote advisory and data monitoring.
