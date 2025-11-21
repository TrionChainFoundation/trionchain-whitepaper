# C. TrionChain Node Roles

## C.1. Overview
TrionChain introduces a specialized node architecture designed to support its FEM-inspired, region-based blockchain structure.  
Each node type contributes to a specific layer of the system, ensuring high performance, localized computation, global consistency, and institutional-grade reliability.

Node specialization enables:
- Predictable scaling  
- Efficient workload distribution  
- Secure inter-cell coordination  
- Reduced global computation overhead  

---

## C.2. Summary of Node Roles

TrionChain defines five primary node roles:

1. **Compute Nodes** – Execute transactions within individual Trion-Cells  
2. **Boundary Nodes** – Manage inter-cell boundaries and cross-cell synchronization  
3. **Consensus Nodes** – Maintain global consensus and validate network-wide blocks  
4. **Storage Nodes** – Preserve global blockchain history and serve state proofs  
5. **Oracle Nodes** – Provide external, real-world, or institutional data inputs  

These roles form a cooperative ecosystem, aligned with the FEM model of computation.

---

## C.3. Compute Nodes

### Purpose
Compute Nodes are responsible for executing all transactions **inside a specific Trion-Cell**, managing localized state transitions.

### Core Responsibilities
- Execute transactions and smart contracts  
- Maintain local state  
- Validate cell-level blocks  
- Participate in local cell finality  
- Produce local execution proofs  

### Importance
They represent the computational backbone of each cell, ensuring decentralized and parallel execution.

---

## C.4. Boundary Nodes

### Purpose
Boundary Nodes enforce the FEM-inspired boundary conditions between Trion-Cells.

### Core Responsibilities
- Validate cross-cell transactions  
- Exchange state deltas between adjacent cells  
- Monitor boundary variables and shared states  
- Prevent inconsistencies across the global ledger  
- Communicate with the Frontier Engine  

### Importance
Boundary Nodes guarantee that TrionChain remains **globally coherent** while still processing transactions locally.

---

## C.5. Consensus Nodes

### Purpose
Consensus Nodes maintain the global state and coordinate validator activity across the entire network.

### Core Responsibilities
- Propose and finalize global blocks  
- Validate cell commitments  
- Process boundary synchronization outputs  
- Form and publish global checkpoints  
- Ensure network-wide security under PoS  

### Importance
They are the final authority on block finality and global state assembly.

---

## C.6. Storage Nodes

### Purpose
Storage Nodes preserve the history and global state of the blockchain.

### Core Responsibilities
- Store blocks, snapshots, and historical records  
- Provide data to light clients and explorers  
- Offer state proofs and zero-knowledge compatible evidence (future module)  
- Maintain redundancy and data availability  

### Importance
These nodes ensure long-term durability and data integrity across the ecosystem.

---

## C.7. Oracle Nodes

### Purpose
Oracle Nodes introduce off-chain data into TrionChain, especially for institutional RWA use cases.

### Core Responsibilities
- Feed external data (infrastructure, agriculture, mining, pricing, energy grids)  
- Verify data authenticity  
- Interact with authorization layers for regulated use cases  
- Publish RWA object updates  

### Importance
They bridge real-world systems with TrionChain’s computational regions.

---

## C.8. Validator Assignment Model

Validators are dynamically allocated based on:

- **Cell importance** (economic activity, RWA load, traffic)  
- **Network topology** (neighboring cells and boundary complexity)  
- **Stake distribution**  
- **Resource metrics**  

Validators may rotate between:
- Compute roles  
- Boundary roles  
- Consensus roles  

This model optimizes both performance and security.

---

## C.9. Cooperation Between Node Types

The following workflow illustrates how node types collaborate:

1. **Compute Nodes** process transactions locally.  
2. **Boundary Nodes** synchronize shared states with neighboring cells.  
3. **Consensus Nodes** assemble all cell commitments into a global block.  
4. **Storage Nodes** save and serve the resulting global state.  
5. **Oracle Nodes** update real-world dependent objects when necessary.

This cooperation mirrors the FEM pipeline:
```
Local Computation → Boundary Conditions → Global Assembly → Persistence → External Inputs
```

---

## C.10. Suggested Diagram (for `/diagrams/node-roles.png`)

```
                       +-------------------------+
                       |     Consensus Nodes     |
                       |   Global Checkpoints    |
                       +-----------+-------------+
                                   |
             +---------------------+----------------------+
             |                                            |
   +---------+---------+                     +------------+-----------+
   |   Compute Nodes   |                     |   Boundary Nodes       |
   | (Local Execution) |<------------------->| (Cross-Cell Sync)      |
   +---------+---------+                     +------------+-----------+
             |                                            |
             +---------------------+----------------------+
                                   |
                      +------------+------------+
                      |     Storage Nodes       |
                      | (History + Availability)|
                      +------------+------------+
                                   |
                      +------------+------------+
                      |      Oracle Nodes       |
                      | (Real-World Inputs)     |
                      +-------------------------+
```

---

## C.11. Summary

TrionChain’s multi-role node architecture ensures:
- Efficient execution  
- Coherent boundary synchronization  
- Strong global consensus  
- Trustworthy data persistence  
- Real-world integration  

This specialization creates a blockchain infrastructure optimized for **scalability, determinism, and institutional-grade RWA deployment**.

