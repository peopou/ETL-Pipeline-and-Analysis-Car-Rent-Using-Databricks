# 🚗 ETL-Pipeline-and-Analysis-Car-Rent-Using-Databricks

## 📋 Overview

An ETL pipeline built to process vehicle rental transactions for a car rental company operating in Jakarta, covering the period from january to december 2024. This pipeline is designed to transform raw data into clean, structured dataset ready for :

- **Operational Database** (organized data storage)
- **Business Analytics** (rental patterns, customer behavior)
- **Forecasting** (revenue prediction)

## ⚙️ Tech Stack

- Platform      : Databricks
- Engine        : Apache Spark 3.5
- Storage       : Delta Lake
- Language      : Python, SQL

## 📁 Dataset

### 👤 Customer Domain

| column          | Type    | Description               |
| --------------- | ------- | ------------------------- |
| customer_name   | String  | Custumer Name             |
| customer_phone  | String  | Phone Number of Custumer |
| customer_email  | String  | Email Address of Customer  |
| customer_city   | String  | Origin City of Customer   |
| customer_age    | Integer | Customer Age              |
| customer_gender | String  | ACustomer Gender          |

### 🚗 Vehicle Domain

| column        | Type    | Description             |
| ------------- | ------- | ----------------------- |
| vehicle_id    | String  | Unique ID of Vehicle    |
| vehicle_plate | String  | Plate Number of Vehicle |
| vehicle_brand | String  | Brand of Vehicle        |
| vehicle_model | String  | Model of Vehicle        |
| vehicle_year  | Integer | Year of Vehicle         |
| vehicle_type  | Scolumn | Type (MPV/criptionl)    |
| vehicle_fuel  | String  | Fuel Type of Vehicle    |

### 📍 Location Domain

| column                    | Type   | Description                 |
| ------------------------- | ------ | --------------------------- |
| pickup_location           | String | Pick-Up Location            |
| destination_location      | String | Destination Location        |
| pickup_location_city      | String | Pick-Up Location (city)     |
| destination_location_city | String | Destination Location (city) |

### 💰 Rental Domain

| column               | Type    | Description            |
| -------------------- | ------- | ---------------------- |
| rental_date          | Date    | Rental Date            |
| rental_duration_days | Integer | Rental Duration (days) |
| daily_rate           | Integer | Daily Rate of Rental   |
| discount_percent     | Integer | Discount (%)           |
| total_amount         | Integer | Amount                 |

### 💳 Payment Domain

| column         | Type   | Description                  |
| -------------- | ------ | ---------------------------- |
| payment_method | String | Payment Method               |
| payment_status | String | Status (Paid/Pending/Failed) |

### 🧑‍✈️ Driver Domain

| column         | Type    | Description   |
| -------------- | ------- | ------------- |
| include_driver | Boolean | Using Driver? |
| driver_name    | String  | Driver Name   |

### 📅 Return Domain

| column               | Type    | Description                     |
| -------------------- | ------- | ------------------------------- |
| expected_return_date | Date    | Date of Planning for Car Return |
| actual_return_date   | Date    | Date of Car Return              |
| is_late_return       | Boolean | Late?                           |
| penalty_fee          | Integer | Penalty Fee                     |

## 🏗️ Architecture

This pipeline using Medallion Architecture

- Bronze Layer : Raw Data
- Silver Layer : Clean Data
- Gold Layer : Modeled
