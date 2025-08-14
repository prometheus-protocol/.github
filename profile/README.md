# **Prometheus Protocol: The Trust Layer for Decentralized Commerce**

### Our mission is to enable a new generation of decentralized applications by providing the open-source, on-chain foundation for **verifiable trust, secure identity, and near-zero fee payments.**

<img width="1536" alt="Prometheus Protocol Banner" src="https://github.com/user-attachments/assets/0c7c5720-1d4a-4e50-b410-873a9ba9cc07" />

---

## **Overview**

Prometheus Protocol is a complete, on-chain economic engine for the Internet Computer. It provides a unified solution for the three pillars of a trustworthy digital economy:

1.  **Secure Identity & Authorization:** A full-featured, on-chain **OAuth 2.1 provider** serves as the robust foundation for any application requiring standards-based authentication.
2.  **Verifiable Trust & Discovery:** A high-assurance **Software Supply Chain Hub** that combines a versioned registry (ICRC-118), an audit bounty marketplace (ICRC-127), and an on-chain endorsement ledger (ICRC-126).
3.  **Direct & Efficient Payments:** An integrated **ICRC-2 allowance system** empowers users to grant services direct, metered access to tokens, enabling a new wave of monetizable applications.

By combining these layers, Prometheus provides the foundational infrastructure for a new generation of decentralized applications and the emerging AI agent economy.

## **Features & Compliance**

The protocol is composed of several key canisters and tools working in concert:

-   **`mcp_registry`:** The core of the app store. It implements `ICRC-118` for version management and `ICRC-126`/`ICRC-127` to manage the verification, auditing, and bounty lifecycle.
-   **`mcp_orchestrator`:** The deployment engine. It implements `ICRC-120` to securely deploy new canister instances using only DAO-verified WASM files.
-   **`auth_server`:** A full-featured, on-chain OAuth 2.1 provider that handles identity and authorization for the entire ecosystem.
-   **`@prometheus-protocol/cli` (CLI):** The developer-facing tool for interacting with the entire publishing lifecycle.

---

## **The Roadmap**

Our journey is structured in ambitious phases, building from a solid foundation towards a vibrant, trusted ecosystem.

### **Phase 0: The Foundation - "Project Hephaestus" (✅ COMPLETE)**

**Goal:** Forge the complete, end-to-end stack for secure identity and payments.

*   **The Core Auth Server:**
    *   [x] Implemented the core OAuth 2.1 flows, JWT signing, and modern security standards.
*   **The Developer SDKs:**
    *   [x] Released `motoko-mcp-sdk` and `@prometheus-protocol/typescript-sdk` for building and integrating monetizable services.
*   **The Proof of Concept:**
    *   [x] Deployed live demos showcasing the full identity and payment stack.

**Phase 0 Deliverable:** A complete, end-to-end, production-ready stack for building and monetizing services on the IC.

---

### **Phase 1: The Trust Layer - "Project Arsenal" (IN PROGRESS)**

**Goal:** Build the premier, high-trust software supply chain for provably safe services, establishing the gold standard for reliability in the agent economy.

*   **Completed in Phase 1:**
    *   [x] **The On-Chain Supply Chain Hub:** Deployed the `mcp_registry` (ICRC-118/126/127) and `mcp_orchestrator` (ICRC-120).
    *   [x] **The Developer & Operator Tooling:** Developed and tested the complete `@prometheus-protocol/cli`.
    *   [x] **The Governance & Audit Workflow:** Implemented the full on-chain workflow for Developers, Auditors, and the DAO.
*   **Next Steps for Phase 1:**
    *   [ ] **Web Portal & Discovery:** Deploy a user-friendly web interface for discovering services, viewing their certification status, and participating in the audit bounty marketplace.
    *   [ ] **DAO Formation & Onboarding:** Formally constitute the governing DAO and onboard the initial set of trusted auditors.
    *   [ ] **Security Hardening:** Submit the entire canister suite for a professional, third-party security audit.

**Phase 1 Deliverable:** A feature-complete, on-chain software supply chain, including a web portal for discovery and a full command-line interface for all core user journeys.

---

### **Phase 2: Ecosystem Growth - "Project Alliance"**

**Goal:** With a unified platform for trust, identity, and payments, the focus shifts to scaling the ecosystem through strategic onboarding and partnerships.

*   **Developer & Enterprise Onboarding:**
    *   [ ] Actively recruit the first wave of high-value developers to publish their services on the platform.
    *   [ ] Fund the initial audit bounties to bootstrap the marketplace.
*   **Client-Side Integration:**
    *   [ ] Partner with developers of AI agents and MCP clients to integrate the registry as a primary, high-trust service source.
*   **Community Growth:**
    *   [ ] Launch community initiatives such as hackathons, developer grants, and comprehensive tutorials to accelerate adoption.

---

### **Phase 3: The Autonomous Economy - "Project Agora"**

**Goal:** Evolve from a platform managed by the founding team into a self-sustaining, community-governed economic protocol.

*   **Decentralized Governance & Curation:**
    *   [ ] **The Handover:** Transition full control of the **Registry Hub** and its policies (e.g., managing the list of vetted auditors, fee structures) to the DAO, cementing its status as a decentralized public utility.
*   **Advanced Economic Primitives:**
    *   [ ] **Security Bonds:** Enable developers to stake tokens as a security bond, providing an economic guarantee of their service's integrity.
    *   [ ] **Atomic Revenue Sharing:** Enhance the SDK to allow services to programmatically split incoming revenue with other services, enabling more complex and collaborative applications.

---

## **Community & Contribution**

Prometheus is a fully open-source project. We welcome contributions, feedback, and collaboration from the community.

-   **Issues:** Report bugs or suggest features in this repository's [Issues tab](https://github.com/prometheus-protocol/mcp-hub/issues).
-   **Contribute:** Check out our `CONTRIBUTING.md` guidelines to get started.
