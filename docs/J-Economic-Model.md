# J. Economic Model (TON Token Economy)

## J.1. Overview

The TON token is the native asset of the TrionChain protocol.  
It secures the network, powers computation, enables governance, and coordinates economic activity across Trion-Cells.

The economic model is designed to:

- Ensure long-term sustainability  
- Incentivize honest validator behavior  
- Support RWA and institutional operations  
- Provide predictable costs for users and enterprises  
- Fund ecosystem development  
- Align incentives across local cells and global layers  

---

## J.2. Core Functions of the TON Token

The TON token serves five essential functions:

1. **Staking & Security**  
   TON is staked by validators to secure:
   - Local cell execution  
   - Boundary synchronization  
   - Global consensus  

2. **Gas & Computation Fees**  
   All transactions and smart contract operations require TON.

3. **Slashing Collateral**  
   Misbehaving validators lose a portion of their staked TON.

4. **Governance Power**  
   TON holders vote on network upgrades, cell creation, and parameter changes.

5. **Economic Coordination**  
   TON is used for regional incentives, RWA operations, oracle compensation, and institutional workflows.

---

## J.3. Staking Model

Validators stake TON to participate in:

- **Compute Node Execution**  
- **Boundary Node Verification**  
- **Consensus Node Finality**  
- **Storage Node Persistence**  
- **Oracle Node Data Validation**

Staking is dynamic and allocated across cells based on:

- Activity level  
- RWA volume  
- Regional importance  
- Validator performance metrics  

### Minimum Stake
The network sets a dynamic minimum stake to enter validator rotation.  
This prevents low-quality or malicious operators from entering.

---

## J.4. Gas Model

TrionChain uses a **regional gas system**, where gas pricing depends on the cell being used.

### Gas Characteristics:

- **Local gas markets** inside each cell  
- **Lower global congestion** due to local execution  
- **Predictable fees** for institutional and RWA operations  
- **Cross-cell operations** require boundary fees  

Gas is paid exclusively in **TON**.

### Fee Flow:
1. Users pay gas in TON  
2. Fees are distributed to:
   - Compute validators  
   - Boundary validators  
   - Consensus validators  
   - Treasury pool  

This ensures incentives across all security layers.

---

## J.5. Validator Rewards

Rewards are distributed based on validator role.  
Four reward streams exist:

### 1. **Cell Execution Rewards**  
Paid to Compute Nodes for local block production.

### 2. **Boundary Verification Rewards**  
Paid to Boundary Nodes for generating boundary proofs and deltas.

### 3. **Global Consensus Rewards**  
Paid to validators participating in finality.

### 4. **Oracle Rewards**  
Paid for verified institutional data updates.

Rewards are calculated using:

```
Reward = (Stake Weight × Role Coefficient × Performance Score)
```

---

## J.6. Slashing (Economic Penalties)

Slashing is essential for enforcing honest behavior.

### Validators are slashed for:

- Incorrect execution  
- Conflicting signatures  
- Invalid boundary proofs  
- Consensus manipulation  
- Oracle falsification  

### Slashing Effects:

1. Loss of staked TON  
2. Removal from validator rotation  
3. Potential permanent ban  

Slashing is **proportional to damage risk**.

---

## J.7. Incentives for RWA Operations

TrionChain enables tokenized real-world asset (RWA) markets.  
The economic model includes incentives for:

### 1. **Authorized Issuers**  
Rewards for compliant, high-quality RWA creation.

### 2. **Institutional Oracles**  
Rewards for data integrity and high uptime.

### 3. **Cell Activity Rewards**  
Cells with high RWA or institutional load receive additional TON.

### 4. **Compliance Execution**  
Special incentives for providing verified regulatory data.

---

## J.8. TON Supply & Distribution

### Categories of Distribution:

1. **Validator Rewards** – Long-term emission schedule  
2. **Ecosystem Treasury** – Infrastructure and grants  
3. **RWA Incentive Pool** – Institutional adoption  
4. **Public Allocation** – Exchanges and liquidity  
5. **Core Contributors** – Developers and founding team  
6. **Strategic Partners** – Institutional investors  

### Emission Model

TrionChain uses a **controlled inflation model**:

- Predictable emission  
- Decreasing inflation over time  
- Sustainable reward cycle for validators  

A portion of gas fees is **burned**, making TON partially deflationary during high demand.

---

## J.9. Cross-Cell Economic Coordination

Each Trion-Cell has an independent economic profile:  
- Local gas  
- Local validator sets  
- Local rewards  
- Local RWA activity  

But global TON supply is unified.

The Frontier Engine ensures:

- Cross-cell economic synchronization  
- Fair distribution of boundary rewards  
- Transparent economic metrics  
- No fragmentation of liquidity  

---

## J.10. Treasury Model

The Treasury receives:

- A percentage of gas fees  
- Slashed TON from misbehaving validators  
- Institutional onboarding payments  
- DAO-controlled allocations  

The Treasury funds:

- Ecosystem grants  
- RWA expansion projects  
- Regional incentives  
- Infrastructure development  
- Research and protocol upgrades  

Governance determines Treasury disbursement.

---

## J.11. Example Economic Flow

A typical transaction producing value for all roles:

1. User sends a cross-cell transaction  
2. Pays gas in TON  
3. Compute Nodes validate it locally  
4. Boundary Nodes process cross-cell delta  
5. Consensus Nodes include it in the global block  
6. Validators receive rewards  
7. A portion of fees is burned  
8. A portion is sent to the Treasury  

This creates a balanced incentive structure.

---

## J.12. Suggested Diagram (for `/diagrams/economic-model.png`)

```
+------------------------------+
|          Users              |
+--------------+---------------+
               |
               v
       +---------------+
       |   Gas Fees    |
       +---------------+
         /      |      \
        /       |       \
       v        v        v
+-----------+ +-----------+ +-----------+
| Compute   | | Boundary  | | Consensus |
|  Rewards  | |  Rewards  | |  Rewards  |
+-----------+ +-----------+ +-----------+
         \        |        /
          \       |       /
           v      v      v
        +-------------------+
        |      Treasury     |
        +-------------------+
               |
               v
        +-------------+
        | Burned TON  |
        +-------------+
```

---

## J.13. Summary

The TON economic model provides:

- Strong PoS-based security  
- Balanced incentives across all validator roles  
- Predictable gas cost for institutions  
- Support for high-performance RWA workloads  
- Treasury-driven long-term growth  
- A sustainable token emission schedule  
- Localized economy per Trion-Cell with global cohesion  

TON is the economic engine powering TrionChain’s regional, FEM-based architecture.

