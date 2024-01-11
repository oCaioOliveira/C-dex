# Network Guide: Understanding Subnets, Hosts, and Choosing the Right Mask

## Introduction

This guide provides a overview of key concepts and pratical tips for subnetting.

## IP Addressing Basics

### IPv4 Overview

IPv4 addresses are 32-bit numerical labels assigned to devices in a network. 

For example: `192.168.1.1`

### Subnetting

Subnetting is the process of dividing an IP network into smaller and manageable segments. 

This provide some benefits:
- Improved network performance;
- Enhanced security through segmentation;
- Efficient resources utilization.

### Calculation Subnets and Hosts

The subnet mask is represented by the representation /X, indicating the number of bits reserved for the network.

The number of hosts per subnet is calculated as 2^(32 - X), where X is the subnet mask.

For example: `10.1.240.0/21`

This example has capacity for 2040 IP addresses (2^(32 - 21)).

### Pratical Examples

Example | Network Size | Suggested Subnet |
------- | ------------ | ---------------- |
Small Office Network | 50 devices | /26 (64 IP addresses) |
Data Center | 1000 devices | /22 (1024 IP addresses) |
Delivery App in Stores | 350 devices | /23 (512 IP addresses)

## Version History

Name | Description | Version | Date |
---- | ----------- | ------- | ---- |
Caio | Create Network Guide | 1.0.0 | 10/01/2024 |
