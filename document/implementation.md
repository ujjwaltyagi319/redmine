# IMPLEMENTATION JOURNAL - Redmine Installation with Podman and PHP Scripts Integration

**Submitted By:** Ujjwal Tyagi  
**Submitted To:** Vipin Tripathi  
**Test Case Version:** 1.1  
**Reviewer Name:** Vipin Tripathi  

## Goal
The goal of this project is to install and run Redmine using Podman, ensuring it is accessible on port 8080. Additionally, PHP scripts running on port 3000 will enable modifications to Redmine's data. Any changes made via the PHP scripts should be reflected immediately in the Redmine installation.

---

## Table of Contents
1. [PREREQUISITES](#prerequisites)
    1.1 [Hardware Requirements](#hardware-requirements)  
    1.2 [Software Requirements](#software-requirements)  
    1.3 [Network Requirements](#network-requirements)
2. [STEPS](#steps)
    2.1 [Install Redmine with Podman](#install-redmine-with-podman)  
    2.2 [Verify Redmine Installation](#verify-redmine-installation)  
    2.3 [Set Up PHP Scripts Environment](#set-up-php-scripts-environment)  
    2.4 [Establish PHP and Redmine Communication](#establish-php-and-redmine-communication)  
    2.5 [Test Changes Reflecting in Redmine](#test-changes-reflecting-in-redmine)

---

## 1. PREREQUISITES

### 1.1 Hardware Requirements
- **CPU:** Minimum 2 Cores  
- **RAM:** Minimum 4 GB  
- **Storage:** Minimum 10 GB Free Space  

### 1.2 Software Requirements
- **OS:** Ubuntu 20.04 or later  
- **Podman:** Version 4.4 or later  
- **PHP:** Version 8.1 or later  
- **Redmine:** Latest stable version  
- **MySQL:** Version 8.0  
- **VS Code:** For editing scripts  

### 1.3 Network Requirements
- **Open Ports:**
    - Port 8080 for Redmine  
    - Port 3000 for PHP Scripts  
- **Internal Network Communication:** Between PHP scripts and Redmine  
- **External Internet Access:** For downloading dependencies  

---

## 2. STEPS

### 2.1 Install Redmine with Podman
**Command Executed:**
```bash
podman run -d --name redmine -p 8080:3000 redmine:latest
