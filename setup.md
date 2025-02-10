# Hive Database Setup Guide

This document provides a step-by-step guide to setting up a Hive environment for the given tasks.

## Step 1: Install and Start Hadoop & Hive
Ensure Hadoop and Hive are installed and configured.

- Start Hadoop services:
  ```bash
  start-all.sh
  ```

- Start Hive metastore service:
  ```bash
  hive --service metastore &
  ```

- Open Hive CLI:
  ```bash
  hive
  ```

## Step 2: Load Data into HDFS
Download and move the dataset into HDFS:

```bash
hdfs dfs -mkdir -p /user/hive/warehouse/hive_odev
hdfs dfs -mkdir -p /user/hive/warehouse/company

hdfs dfs -copyFromLocal Wine.csv /user/hive/warehouse/hive_odev/
hdfs dfs -copyFromLocal employee.txt /user/hive/warehouse/company/
```
