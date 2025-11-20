# SmartColdChain – AI-Powered Temperature Risk Detection  
## ##Summary
Smart Cold Chain Monitor (SCCM) uses AI to predict temperature risks in food and pharmaceutical logistics. It analyzes real-time sensor data, detects anomalies, and alerts operators before spoilage occurs. A simple tool designed for SMEs to reduce waste and protect product quality.

----
 Building AI course project

---

### ![image of an onlineRefrigerated trucks by Yaamboo is liscensed under Creative Commons Attribution-Share Alike 3.0 Unported](https://upload.wikimedia.org/wikipedia/commons/8/80/2008_Rally_Finland_preparations_08.JPG)


---
## Background  
Cold-chain failures are a serious issue in logistics. Even a small temperature deviation can spoil vaccines, pharmaceuticals, or perishable food. In Finland, this challenge is amplified by:

- Extreme seasonal temperature variation  
- Long distribution distances  
- Low population density  
- Strict safety and quality regulations  

Today, many companies already collect sensor data inside refrigerated vehicles and warehouses, but this data is often only reviewed after the fact, when damage has already happened. The goal of SmartColdChain is to shift from reactive monitoring to proactive risk prediction.

This project aims to address:

- Unnoticed temperature spikes during transport  
- Delayed reaction to cooling system failures  
- Manual monitoring errors and workload  
- Waste of products and embedded emissions from spoilage  
- Loss of quality, safety, and customer trust  

The motivation comes from cold-chain and sustainable logistics topics studied in Purchasing and Logistics Engineering. The idea is to create a simple, explainable AI helper that logistics operators could realistically adopt.

---
## Data sources and AI methods

### Data sources
SmartColdChain relies on data commonly available in cold-chain operations, such as:

- IoT temperature sensors inside vehicles or cold rooms  
- Humidity and door-open sensors  
- GPS location and vehicle speed tracking  
- Optional metadata: product category, route information, delivery time windows  

These datasets can come from commercial telematics systems, open IoT platforms, or simulated sample data for prototyping.

### AI methods
The prototype applies simple and explainable machine-learning techniques:

- **Logistic regression** to estimate probability of entering an unsafe temperature zone  
- **Moving averages and trend extraction** to detect upward or downward temperature drift  
- **Anomaly detection** (z-score or IQR based) to flag sudden abnormal values  
- **Optional:** time-series forecasting models (Holt-Winters or exponential smoothing) to predict future risk

These choices keep the system lightweight, transparent, and suitable for SMEs with limited data.

## How it is used  

SmartColdChain integrates into a typical cold-chain operation:

### **Data collection**  
   IoT sensors continuously measure:
   - Temperature  
   - Humidity  
   - GPS position  
   - Vehicle speed  

### **Data preprocessing**  
   The system:
   - Removes obvious sensor errors  
   - Smooths data with moving averages  
   - Extracts features such as trends and rates of change  

### **Risk prediction**  
   The AI model:
   - Estimates the probability that temperature is moving towards an unsafe range  
   - Flags abnormal patterns that indicate risk  

### **Alerts and actions**  
   If risk is detected:
   - Drivers receive a notification (for example, through a mobile app or in-cab display)  
   - Control room staff see warnings on a dashboard  
   They can then act early by:
   - Adjusting cooling  
   - Rerouting or prioritising delivery  
   - Moving goods to another unit  

## Typical users  

- Logistics companies operating refrigerated vehicles  
- Food distributors and retailers  
- Pharmaceutical wholesalers and hospitals  
- Cold storage warehouse operators  
- Quality and compliance teams
  
---
## Challenges

SmartColdChain does not solve all cold-chain problems. Important limitations include:

- Sensor failures, calibration errors, or network outages can mislead the model

- Sudden mechanical failures (e.g., compressor breakdown) may be hard to predict in advance

- Different products have different acceptable temperature ranges

- Data privacy and security must be handled carefully, especially if GPS tracks vehicles

- Overfitting is a risk if the model is trained on too little or unrepresentative data

The system is intended as a decision-support tool, not as an automatic replacement for human judgement or regulatory audits.

---
## What next?


Possible future directions:

- Building a real-time dashboard for dispatchers and quality managers

- Developing a simple driver app that visualises risk levels in an understandable way

- Integrating CO₂ footprint estimation for spoiled vs saved shipments

- Extending the model to support multiple product categories with different thresholds

- Applying the same concept to warehouse cold rooms and retail display units

- With more data and collaboration from industry, SmartColdChain could evolve from a prototype into a production-level monitoring service.

  ---
 ## Acknowledgments

- Developed as part of the Building AI course by the University of Helsinki and Reaktor

- Inspired by studies in Purchasing and Logistics Engineering and topics in cold-chain logistics

- Built using common open-source tools such as Python, NumPy, pandas, and scikit-learn

- Any external images, code samples, or datasets (if later added) will be used only under appropriate open-source or Creative Commons licences, and properly credited.




