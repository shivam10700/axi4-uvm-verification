#  AXI4-FULL UVM Verification Environment (Industry-Grade)

##  Overview

This project implements a **complete AXI4-FULL verification environment using UVM (Universal Verification Methodology)**. It is designed to replicate **real-world SoC verification scenarios**, including out-of-order transactions, protocol compliance, and performance analysis.

---

##  Key Features

###  AXI4-FULL Protocol Support

* Read & Write Channels (AW, W, B, AR, R)
* Transaction IDs (AWID, ARID, BID, RID)
* Burst Transactions
* VALID–READY Handshake

###  Advanced Verification Components

* UVM Testbench Architecture
* Driver, Monitor, Agent, Environment
* Scoreboard with ID-based matching

###  Out-of-Order Transactions

* Multiple outstanding transactions
* Randomized response ordering
* ID-based tracking in scoreboard

###  Slave DUT Model

* Custom AXI4 slave implementation
* Handles requests and generates responses
* Simulates realistic hardware behavior

###  UVM RAL (Register Abstraction Layer)

* Register modeling
* Frontdoor access
* Scalable for large designs

###  AXI Protocol Checker (SVA)

* VALID–READY compliance
* Signal integrity checks
* Assertion-based verification

###  Performance Metrics

* Latency measurement per transaction ID
* Framework for throughput analysis

###  Functional Coverage

* Burst length coverage
* Read/Write coverage
* ID-based coverage
* Cross coverage

###  Coverage Closure

* Coverage reporting infrastructure
* Ensures verification completeness

---

##  Project Structure

```
axi4-uvm-verification/
│── rtl/
│   └── axi_slave.sv
│── tb/
│   ├── axi_if.sv
│   ├── axi_seq_item.sv
│   ├── axi_sequence.sv
│   ├── axi_driver.sv
│   ├── axi_monitor.sv
│   ├── axi_agent.sv
│   ├── axi_env.sv
│   ├── axi_scoreboard.sv
│   ├── axi_coverage.sv
│   ├── axi_perf.sv
│   ├── axi_ral.sv
│   ├── axi_assertions.sv
│   ├── axi_test.sv
│── top.sv
│── README.md
```

---

##  Simulation

### Requirements

* SystemVerilog Simulator (VCS / Questa / Xcelium)
* UVM Library

### Compile & Run

```bash
vlog *.sv
vsim top
run -all
```

---

##  Example Output

* Transaction logs
* Latency measurements
* Assertion checks
* Coverage reports

---

##  Concepts Demonstrated

* AXI4 Protocol Architecture
* UVM Methodology
* Constrained Random Verification
* Assertion-Based Verification (SVA)
* Coverage-Driven Verification
* Register Abstraction Layer (RAL)
* Out-of-Order Transaction Handling

---


##  Future Enhancements

* AXI Interconnect Modeling
* Advanced Error Injection
* Power-Aware Verification
* Formal Verification Integration

---

## ⭐ If you find this useful

Give it a star ⭐ and share with others!
