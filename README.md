# Stock Market Kafka Real-Time Data Engineering Project

![Python](https://img.shields.io/badge/Python-3.8+-blue?style=flat-square) 
![Kafka](https://img.shields.io/badge/Apache%20Kafka-streaming-orange?style=flat-square)
![AWS](https://img.shields.io/badge/AWS-cloud-yellow?style=flat-square) 
![License](https://img.shields.io/badge/License-MIT-green?style=flat-square) 
![Project Status](https://img.shields.io/badge/Project%20Status-Active-brightgreen?style=flat-square)

![Architecture Diagram](./Architecture.jpg)

---

## Table of Contents

- [Overview](#overview)  
- [Goal / Purpose](#goal--purpose)  
- [Technologies Used](#technologies-used)  
- [Architecture](#architecture)  
- [Dataset](#dataset)  
- [Setup Instructions](#setup-instructions)  
- [Usage](#usage)   
- [Contributing](#contributing)  
- [License](#license)  
- [Contact](#contact)  

---

## Overview

This project demonstrates an end-to-end data engineering pipeline for **real-time stock market data** using Apache Kafka and various AWS services. The pipeline ingests stock market data, processes it, and stores it in a structured format for analytics.

The main objective is to build a **robust, scalable, and real-time data pipeline** capable of handling high-frequency stock market data for analytics and business intelligence.

---

## Goal / Purpose

The goal of this project is to provide a practical example of a **real-time data engineering workflow** for financial data, enabling:

- Real-time ingestion and processing of stock market data  
- Seamless integration with AWS services (S3, Glue, Athena)  
- Analytics-ready storage for dashboards and reporting  
- Hands-on experience with Apache Kafka for streaming pipelines  

---

## Technologies Used

- **Programming Language**: Python  
- **Data Streaming**: Apache Kafka  
- **Cloud Services**:
  - AWS S3 (Simple Storage Service)  
  - AWS Glue Crawler & Catalog  
  - AWS Athena  
  - AWS EC2  
- **Data Format**: CSV  
- **Data Processing**: AWS Glue, Athena  

---

## Architecture

The pipeline architecture consists of:

1. **Data Ingestion**: Fetch stock market data using `yfinance` Python library  
2. **Data Streaming**: Stream data in real-time with Apache Kafka  
3. **Data Storage**: Store streamed data in AWS S3 buckets  
4. **Data Processing**:  
   - AWS Glue Crawler to infer schema and create Glue Catalog  
   - AWS Athena to query structured data stored in S3  
5. **Data Consumption**: Analytics, dashboards, or reporting  

![Architecture Diagram](./Architecture.jpg)

---

## Dataset

The dataset contains historical stock market data in CSV format:

- `indexProcessed.csv`: Historical stock prices and trading data for selected indices  

---

## Setup Instructions

### Prerequisites

- Python 3.8+  
- Apache Kafka installed and running  
- AWS Account with permissions  
- AWS CLI installed and configured  
- Python libraries from `requirements.txt`  

### Installation

1. **Clone the Repository**  

```bash
git clone https://github.com/KibutuJr/Stock-Market-Real-Time-Kafka-Streaming-Project.git
cd "C:\Stock Market Real-Time Kafka Streaming Project"
````

2. **Install Python Dependencies**

```
pip install -r requirements.txt
```

3. **Set Up Apache Kafka**

Follow [Kafka Quickstart](https://kafka.apache.org/quickstart) guide to set up locally.

4. **Configure AWS CLI**

```
aws configure
```

5. **Set Up AWS Services**

* **S3**: Create a bucket for streamed data
* **Glue**: Configure a Glue Crawler to infer schema
* **Athena**: Configure Athena to query S3 data

---

## Usage

### Start Kafka Producer

```
python KafkaProducer.py
```

### Start Kafka Consumer

```
python KafkaConsumer.py
```

### Query Data with Athena

```
SELECT * FROM stock_data WHERE symbol = 'AAPL';
```

---

## Contributing

Contributions are welcome!

1. Fork the repository
2. Create a new branch
3. Make your changes
4. Submit a pull request

Please follow coding standards and document your contributions.

---

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file.

---

## Contact

For any questions, collaboration, or feedback:

- **Email**: [kibutujr@gmail.com](mailto:kibutujr@gmail.com)  
- **LinkedIn**: [LinkedIn Profile](https://www.linkedin.com/in/fred-kibutu/)  
- **Portfolio**: [Portfolio](https://kibutujr.github.io/Portfolio-KibutuJr/)

```
