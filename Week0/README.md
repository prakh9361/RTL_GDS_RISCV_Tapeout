# VLSI Design and Open-Source EDA Tool-Flow

This repository documents the setup and installation process for a complete open-source Electronic Design Automation (EDA) toolchain. The instructions cover the system requirements and step-by-step installation of all necessary tools for VLSI design, from synthesis to layout.

[cite_start]This document fulfills **Task 1** [cite: 1] [cite_start]and **Task 2**  by providing a detailed guide for the tool installation.

---

## 💻 System Requirements

Before you begin, ensure your machine (or virtual machine) meets the following specifications:

* [cite_start]**RAM**: 6 GB [cite: 8]
* [cite_start]**HDD**: 50 GB of free space [cite: 8]
* [cite_start]**CPU**: 4 virtual CPUs (vCPUs) [cite: 10]
* [cite_start]**Operating System**: Ubuntu 20.04 or newer [cite: 9]

---

## 🛠️ Tool Installation

Follow the steps below to install the required EDA tools. It's recommended to run the commands in the order they appear.

### Yosys

Yosys is an open-synthesis suite used for Verilog synthesis.

```bash
# First, update your package list
sudo apt-get update [cite: 13]

# Clone the Yosys repository from GitHub
git clone [https://github.com/YosysHQ/yosys.git](https://github.com/YosysHQ/yosys.git) [cite: 14]
cd yosys [cite: 15]

# Install all required dependencies for building Yosys
sudo apt install make [cite: 16]
sudo apt-get install build-essential clang bison flex \
libreadline-dev gawk tcl-dev libffi-dev git \
graphviz xdot pkg-config python3 libboost-system-dev \
libboost-python-dev libboost-filesystem-dev zlib1g-dev [cite: 17, 18]

# Configure, build, and install Yosys
make config-gcc [cite: 19]
make [cite: 20]
sudo make install [cite: 21]
