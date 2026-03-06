# Setup Guide

This guide explains how the SOC monitoring lab was built using Wazuh SIEM.

## 1. Create Virtual Machines

Three virtual machines were created using VirtualBox:

* Ubuntu Server (Wazuh SIEM)
* Windows Machine (Endpoint with Wazuh Agent)
* Kali Linux (Attack Simulation)

## 2. Install Wazuh Server

Wazuh was installed on the Ubuntu server using the official installation script.

The Wazuh server includes:

* Wazuh Manager
* Wazuh Indexer
* Wazuh Dashboard

## 3. Install Wazuh Agent on Windows

The Wazuh agent was installed on the Windows endpoint and connected to the Wazuh server.

After installation, the Windows system appeared as an active agent in the Wazuh dashboard.

## 4. Configure File Integrity Monitoring

A monitored directory was created:

C:\soc-monitor

Wazuh was configured to monitor this directory for file changes.

## 5. Verify Log Collection

Windows security logs were successfully collected and displayed in the Wazuh dashboard.
