# Master_Thesis_AD_2026_HSC
Master Thesis work for Autonomous Driving, Hochschule Coburg 2026

Created by Ritwik Ranjit


# 🛰️ Satellite-Vehicle Communication Simulation Setup & Run Guide

**Project**: Real-time Satellite-to-Vehicle Communication with Multicast Routing  
**Version**: v0.3 (Space-Veins Framework)  
**Last Updated**: February 2026

---

## Overview

This simulation models real-time vehicle-satellite-to-vaehicle (V2S2V) network using LEO, MEO & Geo satellites. The tools and frameworks used are:

- **OMNeT++**: Network simulation engine
- **SUMO**: Urban mobility simulator for vehicles
- **Space-Veins 0.3**: Integration framework for satellite + vehicular networks
- **Veins**: Vehicle-to-infrastructure networking
- **INET**: Internet protocols and models

The architecture implements a **dual radio medium** approach:
- 🔼 **UPLINK**: Vehicles → Satellites (V2S)
- 🔽 **DOWNLINK**: Satellites → Vehicles (S2V)

## System Requirements

### Minimum System Specifications
- **OS**: Linux (Ubuntu 20.04 LTS or later recommended)
- **Disk Space**: 20 GB (for frameworks + compilation)
- **RAM**: 8 GB minimum (16 GB recommended)
- **CPU**: Multi-core processor (4+ cores recommended)

### Required Tools
```bash
# Essential packages
sudo apt-get update
sudo apt-get install -y \
    build-essential \
    gcc g++ gdb \
    git \
    automake \
    autoconf \
    libtool \
    pkg-config \
    bison \
    flex \
    perl \
    python3 \
    openjdk-11-jdk \
    libzmq3-dev \
    libxerces-c-dev
```

---

## Framework Links

> **⚠️ IMPORTANT**: Replace the placeholder links below with the actual GitHub repository URLs for your frameworks.

### OMNeT++ and SUMO Downloads

| Framework | Version | Official Link | 
|-----------|---------|---------------|-----------|
| **OMNeT++** | 5.7.1 | [OMNeT++ Website](https://omnetpp.org/download) | 
| **SUMO** | 1.18.0 | [SUMO Repository](https://github.com/eclipse/sumo) |

### Git Repository Links

| Repository | Purpose | Clone Command | Status |
|---|---|---|---|
| **Space-Veins** | Integration framework | `git clone [URL]` | [[Paste repo URL here]](https://github.com/veins/space_veins.git) |
| **Project (ntn_v2x_sims)** | This simulation project | `git clone [URL]` | (https://github.com/ritwikr18/Master_Thesis_AD_2026_HSC.git) |

**Reference Directory Structure After Setup**:
```
workspace/
├── omnetpp-6.0.x/
├── sumo-1.12.x/
├── space-veins-0.3/
│   ├── veins/               (Veins framework)
│   ├── inet/                (INET protocol library)
│   ├── space_veins/         (Integration layer)
│   └── [...other components]
└── [your-projects]/
    ├── ntn_v2x_sims/          (This project)
    └── [...]
```

---

## Step 1: Download & Install OMNeT++ 5.7.1

## Step 2: Download & Install SUMO 1.18.0

## Step 3: Clone & Setup Space-Veins Framework

## Step 4: Import & Build All Frameworks

## Step 5: Import & Build Project ntn_v2x_sims
### Step 5.1 After importing the project, reference the project to the framworks.
### Step 5.2 Build the project 

## Step 6: Run the Sumo TRaci server on the port 9999 using `./veins_launchd -vv `

## Step 7: Run the Simulation

### 7.1 Prepare Simulation Files (eg: omnetpp_360.ini)

```
# Verify required files exist
ls -la omnetpp_360.ini      # Configuration file ✓
ls -la SatelliteAlertGrid.ned  # Network topology ✓
ls -la kronach_coburg.launchd.xml  # Vehicle routes ✓
ls -la kronach_2.net.xml    # SUMO network ✓
ls -la TLEs_13_01/          # Satellite TLE data ✓
```

### 7.2 Run Multiple Simulations (Parameter Sweep)
Run the simualtions accroding to the parameters required for studying the behaviour.

### 6.6 Record the Results
The results are recorded under the files 'results'.


## ⚠️ Important Notes

1. **OMNeT++ and SUMO versions must be compatible** with Space-Veins 0.3
2. **Build frameworks in order**: Space-Veins → ntn_v2x_sims
3. **Library paths matter**: Ensure LD_LIBRARY_PATH is correctly set
4. **SUMO TraCI server** must be running before starting simulation
5. **TLE files must exist** in the correct directory
6. **Results directory** must have write permissions

---



