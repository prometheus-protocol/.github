<img width="940" height="200" alt="prometheus-banner" src="https://github.com/user-attachments/assets/0e0cc899-def2-42dc-a365-a34512f280ba" />

# **The Trust Layer for the AI Economy**

### Our mission is to enable a new generation of decentralized applications by providing the open-source, on-chain foundation for **verifiable trust, secure identity, and near-zero fee payments.**

---

## **Overview**

Prometheus Protocol is a complete, on-chain economic engine for the Internet Computer. It provides a unified solution for the three pillars of a trustworthy digital economy:

1.  **Secure Identity & Authorization:** A full-featured, on-chain **OAuth 2.1 provider** serves as the robust foundation for any application requiring standards-based authentication.
2.  **Verifiable Trust & Discovery:** A high-assurance **App Store and Software Supply Chain Hub** that combines a versioned registry (ICRC-118), an audit bounty marketplace (ICRC-127), and an on-chain endorsement ledger (ICRC-126).
3.  **Direct & Efficient Payments:** An integrated **ICRC-2 allowance system** empowers users to grant services direct, metered access to tokens (like USDC), enabling a new wave of monetizable applications.

By combining these layers, Prometheus provides the foundational infrastructure for a new generation of decentralized applications and the emerging AI agent economy.

## **Features & Compliance**

The protocol is composed of several key canisters and tools working in concert:

-   **The App Store & Trust Hub (`mcp_registry`):** The core of the app store. It implements `ICRC-118` for version management and `ICRC-126`/`ICRC-127` to manage the verification, auditing, and bounty lifecycle.
-   **The Secure Deployer (`mcp_orchestrator`):** The deployment engine. It implements `ICRC-120` to securely deploy new canister instances using only DAO-verified WASM files.
-   **The Identity Provider (`auth_server`):** A full-featured, on-chain OAuth 2.1 provider that handles identity and authorization for the entire ecosystem.
-   **The Developer CLI (`@prometheus-protocol/app-store-cli`):** The developer-facing tool for interacting with the entire publishing and auditing lifecycle.

---

## **The Roadmap**

Our journey is structured in ambitious phases, building from a solid foundation towards a vibrant, trusted ecosystem.

### **Phase 0: The Foundation - "Project Hephaestus" (✅ COMPLETE)**

**Goal:** Forge the complete, end-to-end stack for secure identity and payments.

-   **Deliverables:** A production-ready OAuth 2.1 provider, comprehensive Motoko & TypeScript SDKs for building and monetizing services, and live demos showcasing the full stack.

---

### **Phase 1: The Trust Layer - "Project Arsenal" (✅ COMPLETE)**

**Goal:** Build the premier, high-trust software supply chain for provably safe services.

-   **Deliverables:** A feature-complete, on-chain software supply chain, including the `mcp_registry` (ICRC-118/126/127), the `mcp_orchestrator` (ICRC-120), a web portal for discovery, and a full command-line interface for all core user journeys.

---

### **Phase 2: Ecosystem Growth - "Project Alliance" (⏳ IN PROGRESS)**

**Goal:** Bootstrap a self-sustaining economy by launching the **Alpha Flywheel Initiative**. This is the current, active phase, focused on building the economic and community incentives to drive supply, trust, and demand using direct USDC rewards.

-   **The Supply Engine (Developer Incentives):**
    -   [ ] **MCP Server Bounty System:** A public bounty board where developers can claim **USDC rewards** for building and certifying specific, high-value MCP servers.
    -   [ ] **Ecosystem Grant Program:** A formal process for funding larger, more complex projects proposed by the community with USDC grants.

-   **The Trust Engine (Auditor Incentives):**
    -   [ ] **Auditor Hub & Reputation System:** A transparent marketplace for security audits where vetted auditors can build their on-chain reputation, claim audit bounties, and earn **USDC rewards**.
    -   [ ] **Real-Time Notifications:** Discord integration to instantly alert the community when new services are submitted for audit.

-   **The Demand Engine (End-User Incentives):**
    -   [ ] **Usage Mining System:** A client-agnostic "Authenticated Beacon" model. Developers integrate a lightweight Beacon library (Motoko/Rust) into their servers, which securely reports usage data on behalf of end-users, making them eligible for daily **USDC rewards**.
    -   [ ] **Showcase Agent:** A public Discord AI agent that uses certified servers from the App Store, demonstrating the power of the ecosystem and participating in the usage mining program.

-   **The Foundation (Documentation & Comms):**
    -   [ ] **Developer Documentation Hub:** Launch a comprehensive documentation site with quickstarts, tutorials, and core concepts.
    -   [ ] **Incentive Program Launch:** Announce the details of the Alpha Flywheel Initiative and its USDC reward structure to the public.

---

### **Phase 3: The Autonomous Economy - "Project Agora" (🚀 UP NEXT)**

**Goal:** Evolve from a platform managed by the founding team into a self-sustaining, community-governed economic protocol.

-   **Full Decentralization & Curation:**
    -   [ ] **The Handover:** Transition full control of the Registry Hub and its policies (e.g., managing the list of vetted auditors, fee structures) to a DAO, cementing its status as a decentralized public utility.
-   **Advanced Economic Primitives:**
    -   [ ] **Security Bonds:** Enable developers to stake **USDC** as a security bond, providing an economic guarantee of their service's integrity.
    -   [ ] **Atomic Revenue Sharing:** Enhance the SDK to allow services to programmatically split incoming revenue with other services, enabling more complex and collaborative applications.

---

## **Community & Contribution**

Prometheus is a fully open-source project. We welcome contributions, feedback, and collaboration from the community.

-   **Issues:** Report bugs or suggest features in this repository's [Issues tab](https://github.com/prometheus-protocol/mcp-hub/issues).
-   **Contribute:** Check out our `CONTRIBUTING.md` guidelines to get started.
