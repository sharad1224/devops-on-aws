# AWS CloudWatch

## Definition
Amazon CloudWatch is a monitoring and observability service that provides data and actionable insights to monitor applications, respond to system-wide performance changes, and optimize resource utilization.

## Key Features
- Collect and track metrics for AWS services and custom applications  
- Log collection and analysis (CloudWatch Logs)  
- Alarms for sending notifications or automatically making changes  
- Dashboards for visualization  
- Events and rules for automation and triggering actions  
- Integration with AWS services like EC2, Lambda, RDS, ECS, etc.

## Use Cases
- Monitoring infrastructure and application performance  
- Setting alarms for operational thresholds  
- Centralized log management and analysis  
- Triggering automated responses to events  
- Creating custom dashboards for real-time insights  

## Key Components / Concepts
- **Metrics**: Time-ordered set of data points (e.g., CPU utilization)  
- **Logs**: Application/system logs collected and stored  
- **Alarms**: Watches a single metric over a time period and performs actions  
- **Dashboards**: Customizable views of metrics and alarms  
- **Events**: React to changes in your environment (e.g., EC2 state changes)  
- **Insights**: Analyze logs with queries (e.g., CloudWatch Logs Insights)

## Architecture Diagram
![Insert CloudWatch Architecture Diagram Here](#)

## Best Practices
- Use high-resolution metrics for real-time monitoring  
- Aggregate logs from multiple sources using agents  
- Set up alarms for thresholds and automation  
- Enable detailed monitoring for EC2 instances  
- Use metric filters to extract specific log data

## Pricing Model
- Pay per metric, dashboard, log ingestion, and log storage  
- Charges for custom metrics and high-resolution data  
- Pricing varies based on region and usage tier  

## Exam Tips
- Know the difference between standard and detailed monitoring  
- Understand the components: metrics, logs, alarms, events, dashboards  
- Be familiar with CloudWatch integration with other AWS services  
- Use cases for custom metrics and CloudWatch Logs Insights  

## Quick Recap
- CloudWatch is a key AWS service for monitoring and observability  
- Use it to collect, visualize, and act on metrics and logs  
- Combine alarms and events to automate responses  
- Visualize performance with dashboards  



## Create Alarm using Instance dashboard

![36](https://github.com/user-attachments/assets/18cae54d-cdb6-4e3c-a88d-33063b0fe994)
![37](https://github.com/user-attachments/assets/6dca13fa-d855-497b-ae6b-336d0a84ddfa)
![38](https://github.com/user-attachments/assets/7a18d368-fd6d-41b5-a4b1-9b64c8cf54d0)
![39](https://github.com/user-attachments/assets/5fc21259-8eac-48ad-a88e-6bea1c60ed16)
![40](https://github.com/user-attachments/assets/065572b8-9d8f-4d89-a3b7-01c2efb0f22e)
![41](https://github.com/user-attachments/assets/6d51b1e3-47c3-481f-9825-8321348c09a4)
![42](https://github.com/user-attachments/assets/46b26dcd-f91f-458f-a35b-0c98a54cb6b0)
![43](https://github.com/user-attachments/assets/c4dc7487-5edf-471e-8129-f8a5fce86d11)
![44](https://github.com/user-attachments/assets/5febc549-ce56-4826-9789-91ef0a2b9350)
![44 1](https://github.com/user-attachments/assets/855ab911-961c-4e23-8f65-5e90c6ccc6ff)
![46](https://github.com/user-attachments/assets/498abaf6-d208-4a71-9d7f-bb5b06616819)
![47](https://github.com/user-attachments/assets/d6ad7a73-9f9c-406f-aefe-4a05b67836d3)


## Create Alarm using ClousWatch service dashboard


![49](https://github.com/user-attachments/assets/76b99929-0897-45bf-b7d2-c5019678780a)
![52](https://github.com/user-attachments/assets/41bb2fa9-510d-4aad-a12f-04e14c8b2078)
![54](https://github.com/user-attachments/assets/0dd20367-eb16-465d-9401-116e51f24d10)
![55](https://github.com/user-attachments/assets/591c8db7-69f4-44fa-bc83-909308f81de0)
![56](https://github.com/user-attachments/assets/636f0854-b2be-4fca-b9e9-e17b90740221)
![58](https://github.com/user-attachments/assets/0b9532bc-fb53-43cf-8898-9f200625482c)
![59](https://github.com/user-attachments/assets/863f31d1-e711-445c-8585-5d02aa0d4b2b)
![61](https://github.com/user-attachments/assets/966aba78-b8a2-4ee0-bca3-ff728a9d8dbc)
![63](https://github.com/user-attachments/assets/028c96d1-f7ca-4b66-9769-7e2180d49769)
![63 1](https://github.com/user-attachments/assets/68b67b71-3c73-4ea0-99a4-4e331975601e)
![64](https://github.com/user-attachments/assets/53d8b925-c904-4f15-8f23-3952613ef2c7)
![65](https://github.com/user-attachments/assets/763ff9d1-33ec-4f4b-a695-6c2c59208535)
![69](https://github.com/user-attachments/assets/a6b91601-4fd6-4161-85c9-850bb29652a4)
![70](https://github.com/user-attachments/assets/66281d6c-8ea4-4886-952a-d93118fb15ed)
![71](https://github.com/user-attachments/assets/0f529cf8-e857-4ab5-8d42-06b6f7913c46)
![72](https://github.com/user-attachments/assets/732b8e3b-2a9c-4e69-95b3-5deaf543578f)
![73](https://github.com/user-attachments/assets/7397475a-7f55-43bc-9d33-3eb2baba5ee1)
![75](https://github.com/user-attachments/assets/35c45bc1-b9b9-4840-8a2e-ed5fc99ba1ef)
![76](https://github.com/user-attachments/assets/48f930a9-0f24-43d4-ba0d-1dcac54147ff)
![77](https://github.com/user-attachments/assets/c83360ef-4ab0-47ab-8f87-80e49e74793f)
![78](https://github.com/user-attachments/assets/8b666298-b7b0-4c73-ba2d-83b629dc1c74)
![79](https://github.com/user-attachments/assets/9df9362c-ba0b-4065-b095-fbcc8bc0ad0e)
![81](https://github.com/user-attachments/assets/104c1e0c-fda5-447e-8d25-d1086fa037ca)



