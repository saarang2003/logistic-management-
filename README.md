📦 DashBird - Logistics Management Data Analysis
This repository contains a Power BI dashboard and supporting analysis for logistics management using trip data. The project focuses on understanding trip efficiency, identifying delays, and improving route performance.

📊 Project Overview
Goal: Analyze trip data to track logistics performance, identify delays, and improve delivery efficiency.

Tools Used: Power BI, PowerPoint (reporting), SQL/DAX

🧾 Dataset Summary
Key columns in the dataset include:

trip_creation_time: Timestamp when the trip was created

route_type: Type of route (e.g., Carting, FTL)

trip_uuid: Unique trip identifier

source_name & destination_name: Location details

od_start_time & od_end_time: Trip duration timestamps

is_cutoff: Indicates if a trip was cut off

actual_time, osrm_time: Actual vs expected duration

segment_*: Segment-level performance details

📈 Key Metrics Visualized
Delayed Shipments (%)

sql
Copy
Edit
= DIVIDE(COUNTROWS(FILTER(delhivery, delhivery[is_cutoff] = FALSE)), [Total Shipments], 0) * 100
On-Time Deliveries (%)

sql
Copy
Edit
= DIVIDE(COUNTROWS(FILTER(delhivery, delhivery[is_cutoff] = TRUE)), [Total Shipments], 0) * 100
📝 Deliverables
📊 Interactive Power BI Dashboard

📄 PowerPoint Summary Report with insights and recommendations

📂 Folder Structure
bash
Copy
Edit
📁 DashBird/
├── 📊 DashBird_Report.pbix     # Power BI file
├── 📄 Summary_Report.pptx      # Final presentation
├── 📁 data/                    # Raw and cleaned data
└── README.md
