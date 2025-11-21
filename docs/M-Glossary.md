# M. Glossary

A comprehensive glossary of technical terms, concepts, and components used throughout the TrionChain whitepaper.

---

## A

### **Assembly (Global Assembly)**
The process where TrionChain combines all cell-level states and boundary deltas into a single globally consistent blockchain state.

---

## B

### **Boundary Conditions**
Rules governing interactions between adjacent Trion-Cells, inspired by the Finite Element Method (FEM).  
They ensure consistency, conservation, and deterministic cross-cell operations.

### **Boundary Delta**
A cryptographic summary of all cross-cell interactions and shared variables between two or more Trion-Cells.

### **Boundary Node**
Validators responsible for verifying and propagating boundary conditions and cross-cell state transitions.

---

## C

### **Cell (Trion-Cell)**
A discrete computational region within TrionChain, responsible for localized execution, state management, and regional autonomy.

### **Cell Finality**
The process of finalizing state transitions within a single Trion-Cell before global consensus.

### **Consensus Node**
Validators responsible for forming and finalizing global blocks by assembling cell commitments.

### **Compute Node**
Validators performing local transaction execution inside a specific Trion-Cell.

---

## D

### **Delta (State Delta)**
The change in state produced during a single local computation cycle within a Trion-Cell.

### **Deterministic Execution**
A property where the same inputs always yield the same outputs, essential for blockchain reproducibility.

---

## E

### **Event Object**
An object representing outputs generated during local execution (logs, triggers, boundary events).

### **Execution Layer**
The layer responsible for local transaction processing within Trion-Cells.

---

## F

### **FEM (Finite Element Method)**
A computational method used in physics and engineering.  
In TrionChain, FEM inspires the regionalized architecture and boundary interactions between Trion-Cells.

### **Frontier Engine**
The system module responsible for resolving boundary deltas, enforcing cross-cell constraints, and assembling global consistency.

---

## G

### **Global Finality**
The process where the entire network agrees on a new globally valid block after assembling all local and boundary data.

### **Governance**
The on-chain decision-making system including global, regional, and institutional voting mechanisms.

---

## I

### **Institutional Oracle**
A trusted data source providing verified real-world information (e.g., RWA data, infrastructure metrics).

### **Institutional Layer**
A subsystem that ensures regulatory compliance, authorization, and high-quality RWA integration.

---

## L

### **Local Execution**
All computation performed inside a single Trion-Cell before boundary or global processing.

---

## N

### **Node Roles**
Specialized validator types (Compute, Boundary, Consensus, Storage, Oracle) that secure and operate the network.

---

## O

### **Oracle Node**
A validator or trusted party providing external data for RWA, compliance, or system parameters.

### **Object (Trion Object)**
A standardized structured entity representing state, transactions, events, RWA metadata, or system-level data.

---

## R

### **Real-World Asset (RWA)**
Any physical or financial asset represented digitally on TrionChain with compliance and institutional rules.

### **RWA Object**
A data structure representing tokenized real-world assets with metadata, compliance validations, and cell assignments.

---

## S

### **Slashing**
Penalty applied to validators who behave maliciously or incorrectly.  
Penalties range from partial stake loss to permanent removal.

### **State Object**
A persistent piece of data stored inside a Trion-Cell.

### **Storage Node**
Validators responsible for storing global history, proofs, and snapshots.

---

## T

### **TON Token**
The native asset of TrionChain, used for gas, staking, governance, and incentives.

### **Trion-Consensus**
The hybrid PoS mechanism combining local finality, boundary synchronization, and global finality.

### **Trion-Nodes**
Validators participating in various roles: Compute, Boundary, Consensus, Storage, Oracle.

---

## W

### **Whitepaper**
The official technical document describing the protocol architecture, computation model, and system design.

