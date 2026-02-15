# Design Specification: Krishi-Vani System Architecture

## 1. Overview
Krishi-Vani is a cloud-native AIoT platform. It leverages AWS for scalable AI inference and real-time data processing, connecting on-field ESP-8266 sensors to a robust Node.js/MongoDB backend.

## 2. System Components

### 2.1 Edge & IoT Layer (Hardware)
* **Microcontroller:** ESP-8266 (NodeMCU) for Wi-Fi connectivity.
* **Sensors:** DHT-11 (Temperature/Humidity), LDR (Light), and Soil Moisture sensors.
* **Protocol:** MQTT/HTTP for low-latency data transmission to the cloud.

### 2.2 Cloud Infrastructure (AWS Integration)
* **Compute:** AWS Lambda for serverless execution of marketplace logic and sensor alerts.
* **AI Services:** * **Amazon Bedrock:** Powering the multilingual LLM for voice assistance and farmer advisory.
    * **Amazon Rekognition (Custom Labels):** For computer vision-based crop disease and pest detection.
* **Storage:** * **Amazon S3:** For storing high-resolution crop images for AI analysis.
    * **MongoDB Atlas:** Distributed database for user profiles, mandi prices, and sensor history.
* **Communication:** Amazon SNS (Simple Notification Service) for sending SMS alerts to farmers.

## 3. Data Flow

### 3.1 AI Diagnostic Pipeline
1.  **User Upload:** Farmer captures a crop image via the mobile app.
2.  **Ingestion:** Image is uploaded to an **Amazon S3** bucket.
3.  **Inference:** An S3 Trigger activates an **AWS Lambda** function that calls the **Amazon Rekognition** model.
4.  **Result:** The diagnosis and treatment plan are sent back to the app and translated into the local language using **Amazon Bedrock**.

### 3.2 IoT Monitoring Pipeline
1.  **Sensing:** ESP-8266 reads soil moisture and DHT-11 data.
2.  **Transmission:** Data is sent to the **Node.js** backend via REST API.
3.  **Analysis:** If moisture falls below a threshold defined in **requirements.md**, a notification is pushed via **Amazon SNS**.

## 4. User Interface Design
* **Mobile App:** Built with React Native for cross-platform support.
* **Voice Module:** Integration with AWS Transcribe and Polly to facilitate the multilingual "Vani" (Voice) interface.

## 5. Security & Scalability
* **Authentication:** JWT-based secure login for farmers and traders.
* **Scalability:** Horizontal scaling of Node.js containers to handle harvest-season traffic spikes.
