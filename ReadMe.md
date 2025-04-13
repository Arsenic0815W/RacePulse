# RacePulse 🏎️💨  
**Real-Time F1 Telemetry Analytics Pipeline**  

[![Python](https://img.shields.io/badge/Python-3.9%2B-blue)](https://www.python.org/)
[![Apache Airflow](https://img.shields.io/badge/Airflow-2.5%2B-orange)](https://airflow.apache.org/)
[![License](https://img.shields.io/badge/License-MIT-green)](LICENSE)

*A data engineering project to capture, process, and visualize live F1 race data.*  

---

## 🚦 **Development Roadmap**  
Here’s how I’m building RacePulse step-by-step:  

### Phase 1: Setup & Data Ingestion (✅ Completed)  
- **Goal**: Ingest live F1 telemetry data.  
- **Progress**:  
  - Set up Apache Airflow to schedule data fetches from the [FastF1 API](https://github.com/theOehrly/Fast-F1).  
  - Created Kafka producers to stream real-time car sensor data (speed, RPM, lap times).  

### Phase 2: Data Processing (⚡ In Progress)  
- **Goal**: Clean and analyze streaming data.  
- **Current Task**:  
  - Using PySpark to calculate **average lap speeds** and detect anomalies (e.g., sudden speed drops).  
  - Storing processed data in PostgreSQL for dashboards.  

### Phase 3: Visualization & Deployment (🛠️ Up Next)  
- **Goal**: Build real-time dashboards and deploy the pipeline.  
- **Planned Work**:  
  - Create Grafana dashboards to show driver rankings and telemetry trends.  
  - Deploy the entire stack on AWS EC2 with Docker.  

---

## 🛠️ **Tech Stack**  
- **Data Ingestion**: FastF1 API, Apache Kafka  
- **Orchestration**: Apache Airflow  
- **Processing**: PySpark, Pandas  
- **Storage**: PostgreSQL, Redis (caching)  
- **Visualization**: Grafana, Plotly  
- **Infrastructure**: Docker, AWS EC2  

---

## 🏁 **Getting Started**  
### Prerequisites  
- Python 3.9+  
- Docker & Docker Compose  

### Installation  
1. Clone the repo:  
   ```bash  
   git clone https://github.com/your-username/RacePulse.git  
   cd RacePulse  