# 🛡️ ThreatSense – AI-Powered Cyber Attack Visualization Dashboard

Welcome to **ThreatSense**, a Power BI-based interactive dashboard engineered to visualize, analyze, and understand network-based cyberattacks using the **UNSW-NB15 dataset**.

This project combines **Python-powered data cleaning**, **IP-based geolocation**, and **Power BI storytelling** to create a modern, dark-themed Security Operations Center (SOC)-style visualization system.

> 🎯 Goal: Turn raw, complex intrusion data into actionable cyber intelligence using AI and data analytics.

---

## 📂 Dataset Used

**Dataset**: [UNSW-NB15](https://research.unsw.edu.au/projects/unsw-nb15-dataset)  
**Provider**: Australian Centre for Cyber Security  
**Description**: A comprehensive network intrusion dataset featuring both normal and malicious traffic, with 10 unique attack categories (e.g., Fuzzers, Exploits, Reconnaissance, Shellcode, etc.).

**Files Used**:
- `UNSW-NB15_1.csv`
- `UNSW-NB15_2.csv`
- `UNSW-NB15_3.csv`
- `UNSW-NB15_4.csv`

---

## 📜 Data Preprocessing

> Because clean data = sharp insight. Here's what went under the hood.

- 🐍 **Python preprocessing**:
  - Cleaned missing, malformed, or redundant values
  - Parsed Unix timestamps into human-readable datetime
  - Combined the four datasets (`_1`, `_2`, `_3`, `_4`) into a single, unified master table
  - Standardized column names and fixed label inconsistencies

- 🌍 **IP Geolocation**:
  - Used the `ip-api.com` service to convert source/destination IPs into:
    - Latitude & Longitude
    - Country & City (optional)
  - Imported these into Power BI to **map the origin and target of attacks**

- 💾 Exported final clean dataset as `.csv` and loaded it into Power BI for visual modeling

---

## 📊 Dashboard Features

### 🧠 Key Insights Delivered:
- **Attack Volume Over Time** *(Time Series Line Chart)*
- **Protocol Usage Breakdown** *(Donut Chart)*
- **Attack Category Distribution** *(Pie Chart)*
- **Attack Category vs Protocol** *(Stacked Bar Chart)*
- **Total Bytes Sent/Received** *(KPI Cards)*
- **Map of Attack Origins** *(using IP geolocation)*

### 🧩 Visual Components:
| Visual Name                          | Description                                      |
|-------------------------------------|--------------------------------------------------|
| 📈 Attacks Over Time                | Daily trend of attacks across all categories     |
| 🍩 Protocol Usage (Donut)           | Shares of TCP, UDP, SCTP in the dataset          |
| 🥧 Attack Category (Pie)            | Distribution of major attack categories          |
| 📊 Attack Cat × Protocol (Bar)      | Cross-analysis of attack methods and protocols   |
| 📌 KPI Cards                        | Total Sent Bytes, Received Bytes, Total Events   |
| 🗺️ Attack Map (Optional)            | Geolocated attacks based on IP lookups           |
| 🎛️ Slicers                         | Filters by Protocol, Service, Label, Attack Type |

---

## 🎨 Design Highlights

| Feature           | Details                                                                 |
|------------------|-------------------------------------------------------------------------|
| **Theme**         | Jet black dark mode                                                     |
| **Visual Aesthetics** | Color-coded insights (🟢 safe, 🟡 suspicious, 🔴 malicious)       |
| **Layout**        | Optimized for 1000px width canvas; responsive layout                   |
| **Typography**    | Modern clean fonts with scalable font sizes                            |
| **Trend KPIs**    | Dynamic color indicators for rising or falling attack trends           |

---

## 🧰 Tools & Technologies

| Stack           | Description                                                  |
|----------------|--------------------------------------------------------------|
| **Power BI**   | Data visualization and dashboard design                      |
| **Python**     | Data cleaning, joining files, timestamp parsing, API queries |
| **IP-API**     | Geolocation lookup of IP addresses                           |
| **Pandas/NumPy** | Python libraries used for preprocessing                    |
| **GitHub**     | Version control and project publishing                       |

---

## 🧠 Project Summary

> *ThreatSense* is a modern cyber attack analysis dashboard built using real-world intrusion data from the UNSW-NB15 dataset.  
It uses Python scripts for data cleanup and geolocation, and visualizes threats through a fully interactive Power BI dashboard, simulating a SOC environment.

This project demonstrates:
- End-to-end data pipeline skills (from raw data to insight)
- Use of APIs (for IP location)
- Strong understanding of cybersecurity data features
- Clean UI/UX in analytics tools like Power BI

---

## 🧑‍💻 Developed By

**Samarth**  
Engineer | Data Analyst | Future Stark  
> *“Built to detect threats. Designed to impress. Powered by curiosity.”*

---

## 📝 Usage Instructions

1. Clone or download the repository
2. Open `ThreatSense.pbix` in **Power BI Desktop**
3. Explore the dashboard interactively using slicers and charts
4. Want to show your work? Export as **PDF** or **publish to Power BI Service**

---

## 📥 Future Work

- Add anomaly detection using ML (Scikit-learn or PyCaret)
- Enable real-time data pipeline with streaming inputs
- Integrate all 4 datasets with unified deduplication
- Embed dashboard in a live portfolio site

---

## 🔗 Resources

- [UNSW-NB15 Dataset Download](https://research.unsw.edu.au/projects/unsw-nb15-dataset)
- [Power BI Desktop](https://powerbi.microsoft.com/)
- [IP-API Documentation](http://ip-api.com/docs/)
- [Project Showcase (Coming Soon)](https://github.com/samarth/ThreatSense-Dashboard)

---

## 📎 License

This project is for educational and personal portfolio use.  
Dataset usage complies with UNSW’s academic research license.
