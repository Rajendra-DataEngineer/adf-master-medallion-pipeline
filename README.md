# Project 5: Master Medallion Pipeline - End-to-End Orchestration

## Project Overview
This project implements a **centralized Master Orchestrator Pipeline** in Azure Data Factory that coordinates the complete **Medallion Architecture** (Bronze → Silver → Gold). It sequentially executes child pipelines and integrates robust error handling.

## Key Features
- End-to-End orchestration of Medallion layers
- Sequential execution: Bronze → Silver → Gold
- Reusable Execute Pipeline pattern
- Centralized error handling with `pl_error_handler`
- Success and failure path management

## Architecture Flow
1. **Bronze Layer** → Raw data processing (`pl_customer_bronze_to_silver`)
2. **Silver Layer** → Cleansed data (`pl_silver_to_gold`)
3. **Gold Layer** → Aggregated business data
4. On Failure → Triggers centralized error logging

## Technologies Used
- Azure Data Factory (Execute Pipeline, If Condition)
- Mapping Data Flow
- Azure Data Lake Storage Gen2
- Error Handling Framework

## Screenshots
- [Master Medallion Orchestrator Pipeline]Master Pipeline (pl_master_medallion_pipeline) coordinating Bronze → Silver → Gold layers using Execute Pipeline activities(<img width="757" height="164" alt="image" src="https://github.com/user-attachments/assets/f916ed59-6c61-4ef8-8cab-e6b9291c4a46" />) 

- [Error handling path]Failure path triggering centralized error handler (pl_error_handler)(<img width="646" height="333" alt="image" src="https://github.com/user-attachments/assets/a343b317-b0c8-46ba-bbeb-e263c3577bbb" />)
- 
[Successful Pipeline Execution]-  Successful debug run of the complete Medallion Pipeline <img width="787" height="302" alt="image" src="https://github.com/user-attachments/assets/ee096301-d3a0-4a8b-9993-bc203874d10c" />


## How to Run
1. Update all Linked Services and Datasets
2. Execute the Master Pipeline (`pl_master_medallion_pipeline`)
3. Monitor child pipelines and error logs in ADLS

## Learnings
- Building end-to-end orchestrated data pipelines
- Implementing Medallion Architecture in ADF
- Centralized error handling and observability
- Reusable and maintainable pipeline design

---
**Made by Rajendra K**  
Aspiring Azure Data Engineer | Open to UK & Europe Opportunities
