# 🚀 AdaptivePuzzleMind  
### Real-Time Data Engineering Pipeline (Kafka + Spark + Python)

AdaptivePuzzleMind is a real-time data pipeline designed to simulate, ingest, process, and analyze high-volume event streams using **Apache Kafka**, **PySpark**, and **Python**.  
This project demonstrates core **Data Engineering**, **ETL processing**, and **Distributed System** skills using industry-standard tools.

---

## 🧠 Project Purpose
This project was created to showcase hands-on experience with real-time data pipelines, message streaming, distributed batch processing, and analytics workflows — all essential skills for Data Engineering and Backend roles.

---

## 🔥 Key Features
- ⚡ **Real-time event generation** using Kafka Producers  
- 🔄 **Stream ingestion** with Kafka Consumers  
- 🗃 **Raw data storage** in JSON format  
- 🔍 **Batch processing & aggregation** using PySpark  
- 🧮 Analytics on event volume, clicks, cost  
- 🐳 **Docker Compose** setup for Kafka + Zookeeper  
- 📁 Clean ETL folder structure  
- 🧪 Sample dataset included to test Spark without Kafka  

---

## 🏗 Architecture Overview

┌────────────────────┐
│ Event Generator │
│ (Kafka Producer) │
└──────────┬─────────┘
│ JSON Events
▼
┌────────────────┐
│ Kafka Topic │
│ "events" │
└────────┬───────┘
│
▼
┌────────────────────┐
│ Kafka Consumer │
│ Writes to /data/ │
└──────────┬─────────┘
│
▼
┌────────────────┐
│ Raw JSON Files │
│ /data/raw │
└────────┬───────┘
│
▼
┌────────────────────┐
│ PySpark Batch Job │
│ Aggregates + ETL │
└──────────┬─────────┘
│
▼
┌────────────────┐
│ Processed Data │
│ /data/processed│
└────────────────┘


---

## 📂 Folder Structure



AdaptivePuzzleMind/
│
├── producer.py
├── consumer.py
├── spark_job.py
├── requirements.txt
├── docker-compose.yml
├── README.md
│
├── sample_data/
│ └── events.json
│
└── data/
├── raw/
└── processed/


---

## 🛠 Tech Stack
- **Python 3**
- **Apache Kafka**
- **Kafka Python Client**
- **Apache Spark (PySpark)**
- **Docker & Docker Compose**
- **JSON Serialization**
- **Distributed Systems Concepts**

---

## ⚙️ Installation & Setup

### **1️⃣ Install Dependencies**
```bash
pip install -r requirements.txt

2️⃣ Start Kafka & Zookeeper
docker-compose up -d

3️⃣ Start Producer
python3 producer.py --topic events --brokers localhost:9092 --rate 20

4️⃣ Start Consumer
python3 consumer.py --topic events --brokers localhost:9092 --out_dir data/raw

5️⃣ Run Spark Batch Job
spark-submit spark_job.py data/raw data/processed

📊 Output Example

Processed JSON output:

{
  "ad_id": "ad_12",
  "events": 147,
  "clicks": 41,
  "total_cost": 82.37
}

🧪 Testing Without Kafka

You can test Spark using sample data:

cp sample_data/events.json data/raw/
spark-submit spark_job.py data/raw data/processed

🧩 Skills Demonstrated

Real-time streaming pipeline design

Kafka producers/consumers

PySpark ETL and batch processing

Data transformation & aggregation

Distributed system handling

Serialization, retries, partitions

GitHub version control & project documentation

👨‍💻 Author

Pankaj Kumar
Data Engineering & Backend Enthusiast

📧 Email: pankajchhonker28@gmail.com

🔗 LinkedIn: https://www.linkedin.com/in/pankaj-kumar-19b240231

⭐ If you like this project, please star the repository!

---

