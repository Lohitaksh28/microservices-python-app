# Video Converter – DevOps Project

## Overview

This project demonstrates the deployment of a **Python-based microservices application** on **AWS EKS**. The application converts MP4 videos to MP3 using an asynchronous, containerized architecture. The focus of this project is on **DevOps practices**, Kubernetes deployment, and AWS infrastructure setup.

## Architecture Summary

The application consists of multiple microservices deployed on Kubernetes:

* **Auth Service** – Handles user authentication using JWT
* **Gateway Service** – Acts as the entry point for client requests
* **Converter Service** – Processes video-to-audio conversion asynchronously
* **Notification Service** – Sends email notifications after processing
* **Databases** – PostgreSQL and MongoDB for data storage
* **RabbitMQ** – Message queue for decoupled communication

## Tools & Technologies

* AWS EKS
* Docker & Kubernetes
* Helm Charts
* RabbitMQ
* PostgreSQL & MongoDB
* IAM Roles & Security Groups
* EBS CSI for Persistent Volumes

## High-Level Deployment Flow

1. Create an EKS cluster and node group on AWS
2. Configure IAM roles, security groups, and EBS CSI addon
3. Deploy MongoDB, PostgreSQL, and RabbitMQ using Helm
4. Deploy microservices using Kubernetes manifests
5. Validate application using kubectl and REST APIs

## Application Workflow

1. User logs in and receives a JWT token
2. User uploads an MP4 file
3. Converter service processes the file using RabbitMQ queues
4. User receives email notification with file ID
5. User downloads the converted MP3 file

## Learning Outcome

* Hands-on experience with **AWS EKS cluster setup**
* Understanding of **microservices deployment on Kubernetes**
* Working with **Helm, IAM, Security Groups, and Persistent Volumes**
* Basic exposure to **message queues and service-to-service communication**

## Cleanup

After testing, the infrastructure can be removed by deleting the EKS node group and cluster.

