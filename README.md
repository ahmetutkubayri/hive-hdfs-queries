# Hive Database and Querying Tasks

This project demonstrates how to create and manage Hive databases, load data, and perform SQL operations.

## 🚀 Features
- Create Hive databases and tables
- Load CSV and TXT files into Hive tables
- Filter and insert data into new tables
- Drop databases including all underlying tables
- Query data with specific conditions

## 📁 Repository Structure
- `setup.md` → Step-by-step guide for setting up the Hive environment
- `solutions.md` → Solutions to the given tasks

## 🔧 Prerequisites
- Hadoop & Hive installed and configured
- HDFS running
- Basic knowledge of HiveQL

## 🏗️ Setting up the Hive Environment
1. Start Hadoop and Hive services:
   ```bash
   start-all.sh
   hive --service metastore &
   ```

2. Verify Hive is running:
   ```bash
   hive
   ```

## 📌 Tasks and Solutions
Refer to the [solutions.md](solutions.md) file for the detailed commands and explanations.
