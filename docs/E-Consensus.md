# E. TrionChain Consensus

## E.1. Overview
TrionChain introduces **Trion-Consensus**, a hybrid Proof-of-Stake (PoS) mechanism combined with FEM-inspired boundary synchronization.  
The consensus model is designed to:

- Support high parallelism across Trion-Cells  
- Maintain deterministic global state assembly  
- Ensure security through PoS validator commitments  
- Synchronize inter-cell boundaries through the Frontier Engine  
- Produce globally consistent blocks without monolithic execution  

Trion-Consensus integrates *local cell finality* with *global network finality*.

---

## E.2. Key Principles of Trion-Consensus

### 1. **Local Execution, Global Agreement**
Each Trion-Cell processes transactions independently.  
Validators inside the cell reach **local finality** before global assembly.

### 2. **Boundary-Coordinated Synchronization**
Boundary Nodes provide cryptographic proofs for:
- Cross-cell interactions  
- Shared boundary variables  
- State deltas  

These proofs ensure deterministic behavior across the network.

### 3. **Hybrid PoS Validator Model**
Validators stake TON to participate in:
- Cell execution  
- Boundary verification  
- Global consensus  

Stake weight determines validator assignments and influence.

---

## E.3. Local Cell Finality

### Process:
1. Transactions enter a Trion-Cell.  
2. Compute Nodes execute them.  
3. Local validators propose a **cell block**.  
4. Validators sign the block (local attestation).  
5. The block becomes **cell-finalized**.

### Finality Guarantee
Once a cell reaches its local finality threshold,  
its state transitions become *immutable* from the perspective of the cell.

Local finality is **fast**, enabling high throughput.

---

## E.4. Boundary Finality (Frontier Engine)

The Frontier Engine processes all boundary-related events:

- Shared state variables  
- Cross-cell asset transfers  
- Contract calls across cells  
- RWA updates that span multiple regions  

### Boundary Finality occurs when:
1. Boundary Nodes exchange proofs  
2. Conflicts are resolved  
3. The engine guarantees determinism  
4. A boundary delta is published  

This ensures **global coherence** without requiring global execution.

---

## E.5. Global Consensus

After local and boundary finality, Consensus Nodes assemble:

1. All cell commitments  
2. Boundary deltas  
3. Global state updates  

### The Global Consensus Flow:
```
Local Cell States
      ↓
Boundary Proofs
      ↓
Frontier Engine Assembly
      ↓
Global Block Proposal
      ↓
Validator Attestations
      ↓
Global Finality
```

When ⅔ of global stake attests a block, it becomes **globally finalized**.

---

## E.6. Validator Roles in Consensus

TrionChain’s validator sets are dynamic and role-based:

| Node Type        | Role in Consensus |
|------------------|------------------|
| Compute Nodes    | Local block execution and proposal |
| Boundary Nodes   | Boundary delta generation and verification |
| Consensus Nodes  | Global block assembly and finality |
| Storage Nodes    | Long-term state storage and proof serving |
| Oracle Nodes     | Feed external data for RWA objects |

Stake is dynamically reallocated according to:
- Cell load  
- Boundary complexity  
- RWA demands  
- Network topology  

---

## E.7. Consensus Security Model

Trion-Consensus provides security through:

### **1. Economic Security**
Validators must stake TON; misbehavior results in slashing:
- Invalid cell blocks  
- Boundary manipulation  
- Fake proofs  
- Double-signing  
- Consensus attacks  

### **2. Deterministic Boundary Rules**
Boundary conditions impose strict constraints, reducing ambiguity.

### **3. Multi-Layer Finality**
Security exists at:
1. Local level  
2. Boundary level  
3. Global level  

This layered finality provides **resilience and precision**.

---

## E.8. Handling Cross-Cell Transfers

Cross-cell actions follow a strict workflow to maintain atomicity:

1. Origin cell locks the asset  
2. Boundary Nodes verify eligibility  
3. Frontier Engine applies rules  
4. Destination cell receives the transfer  
5. Global block assembles both operations  

This ensures:
- No double spending  
- No orphan states  
- Perfect determinism  

---

## E.9. Consensus Rewards

Validators earn rewards based on:

1. **Cell Execution Rewards**  
2. **Boundary Verification Rewards**  
3. **Global Consensus Rewards**  
4. **RWA Processing Rewards** (for institutional deployments)

Rewards are proportional to:
- Stake weight  
- Role performed  
- Accuracy of proofs  
- Uptime and reliability  

---

## E.10. Suggested Diagram (for `/diagrams/consensus-flow.png`)

```
 +---------------------------+
 |     Local Cell Finality   |
 | (Compute Validators)      |
 +-------------+-------------+
               |
               v
 +---------------------------+
 |   Boundary Synchronization|
 |   (Boundary Nodes + FE)   |
 +-------------+-------------+
               |
               v
 +---------------------------+
 |     Global Block Proposal |
 |    (Consensus Validators) |
 +-------------+-------------+
               |
               v
 +---------------------------+
 |      Global Finality      |
 +---------------------------+
```

---

## E.11. Summary

Trion-Consensus is a multi-layer, FEM-inspired consensus mechanism that provides:

- High throughput via localized execution  
- Global consistency through boundary synchronization  
- Strong PoS security  
- Deterministic behavior across computational regions  
- Robust support for institutional-grade RWA applications  

It enables TrionChain to scale without fragmentation,  
maintaining coherence and performance simultaneously.

