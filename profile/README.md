# **Prometheus Protocol: The Trust Layer for Decentralized Commerce**

### Our mission is to enable a new generation of decentralized commerce by providing the open-source foundation for **verifiable trust, secure identity, and near-zero fee payments.**

<img width="1536" alt="Prometheus Protocol Banner" src="https://github.com/user-attachments/assets/0c7c5720-1d4a-4e50-b410-873a9ba9cc07" />

---

## **Overview**

Prometheus Protocol is a complete, on-chain economic engine for the Internet Computer. It provides a unified solution for the three pillars of a trustworthy digital economy:

1.  **Secure Identity & Authorization:** A full-featured, on-chain **OAuth 2.1 provider** serves as the robust foundation for any application requiring standards-based authentication.
2.  **Verifiable Trust & Discovery:** A high-assurance **App Store and Software Supply Chain** allows users and AI agents to discover and safely upgrade to services whose code has been cryptographically verified and certified.
3.  **Direct & Efficient Payments:** An integrated **ICRC-2 allowance system** empowers users to grant services direct, metered access to tokens, enabling a new wave of monetizable applications.

By combining these layers, Prometheus provides the foundational infrastructure for a new generation of decentralized applications and the emerging AI agent economy.

## **Core Components & Compliance**

### Identity & Authorization (OAuth 2.1)

The core of Prometheus is a production-ready Authorization Server implementing the latest security best practices from the IETF and the specific requirements of the MCP specification.

- ✓ **OAuth 2.1 Core:** Implements the modern, secure baseline for OAuth, including mandatory PKCE (`RFC 7636`) and the Authorization Code Flow (`RFC 6749`).
- ✓ **Refresh Token Rotation:** Enhances security by issuing a new, single-use refresh token each time one is used.
- ✓ **Dynamic Client Registration (DCR):** A public `/register` endpoint (`RFC 7591`) allows applications to register programmatically.
- ✓ **Resource Indicators:** Supports token audience binding via the `resource` parameter (`RFC 8707`).
- ✓ **Server Metadata:** Provides `/.well-known/oauth-authorization-server` (`RFC 8414`) and `/.well-known/jwks.json` endpoints for automated client configuration.

### The Software Supply Chain (ICRC-118, 120, 126)

Prometheus implements a complete, on-chain software supply chain, enabling developers to publish verifiably safe software and operators to upgrade with confidence.

- ✓ **Certified Registry (ICRC-118):** An on-chain, versioned catalog for certified software.
- ✓ **Immutable Upgrades (ICRC-120):** A hardened orchestrator canister that enforces that only certified code from the registry can be deployed.
- ✓ **Developer CLI:** A comprehensive command-line tool (`prometheus-cli`) that empowers developers and operators to interact with the entire lifecycle: `publish`, `add-controller`, `register`, `upgrade`, and more.

---

## **The Roadmap**

Our journey is structured in ambitious phases, building from a solid foundation towards a vibrant, trusted ecosystem.

### **Phase 0: The Foundation - "Project Hephaestus" (✅ COMPLETE)**

**Goal:** Forge the complete, end-to-end stack for secure identity and payments: a production-grade auth server, developer-friendly SDKs, and live proof-of-concept demonstrations.

*   **The Core Auth Server:**
    *   [x] Implemented the core OAuth 2.1 flows, JWT signing, and modern security standards (PKCE, DCR, Refresh Token Rotation, Resource Indicators).
    *   [x] Enabled resource servers to define accepted ICRC-2 payment tokens.
*   **The Developer SDKs:**
    *   [x] **`motoko-mcp-sdk`:** A complete server framework for building production-ready, monetizable MCP services in Motoko.
    *   [x] **`@prometheus-protocol/typescript-sdk`:** A client library for web apps and a server library for integrating off-chain services.
*   **The Proof of Concept:**
    *   [x] Deployed live demos showcasing both on-chain native services and bridged Web2 services.

**Phase 0 Deliverable:** A complete, end-to-end, production-ready stack for building and monetizing MCP servers on the IC.

---

### **Phase 1: The Trust Layer - "Project Arsenal" (IN PROGRESS)**

**Goal:** Build the premier, high-trust marketplace for provably safe services, establishing the gold standard for reliability in the agent economy.

*   **Completed in Phase 1:**
    *   [x] **ICRC-118 Registry Canister:** Deployed the on-chain, versioned catalog for all certified services.
    *   [x] **ICRC-120 Orchestrator Canister:** Deployed the hardened, open-source canister that enforces immutable upgrade rules.
    *   [x] **`prometheus-cli` Tool:** Developed and tested the complete command-line interface for the entire software lifecycle. Developers can `publish` new versions, and operators can securely `upgrade` their canisters.
*   **Next Steps for Phase 1:**
    *   [ ] **ICRC-126 Validator Canister:** Deploy our on-chain `Validator`, which will cryptographically sign and issue endorsements for audited Wasm hashes.
    *   [ ] **Web Frontend:** Deploy a user-friendly web interface for discovering, filtering, and connecting to services in `The Arsenal`.
    *   [ ] **Security Audit:** Submit the entire canister suite (Auth, Registry, Orchestrator) for a professional, third-party security audit.
    *   [ ] **Onboard Flagship Apps:** Onboard and certify the first 5-10 applications to seed the ecosystem with high-quality, trusted tools.

---

### **Phase 2: Ecosystem Growth - "Project Alliance"**

**Goal:** With a unified platform for trust, identity, and payments, the focus shifts to scaling the ecosystem through strategic business development and partnerships.

*   **Developer & Enterprise Onboarding:**
    *   [ ] Actively recruit high-value developers to publish their services on the platform.
    *   [ ] Develop B2B offerings, such as managed private registries and support for enterprise clients.
*   **Client-Side Integration:**
    *   [ ] Partner with developers of AI agents and MCP clients to integrate our registry as a primary, high-trust service source.
*   **Community Growth:**
    *   [ ] Launch community initiatives such as hackathons, developer grants, and comprehensive tutorials to accelerate adoption.

---

### **Phase 3: The Autonomous Economy - "Project Agora"**

**Goal:** Evolve from a platform managed by the founding team into a self-sustaining, community-governed economic protocol.

*   **Decentralized Governance & Curation:**
    *   [ ] **DAO Formation:** Deploy a governance DAO to give the community control over the platform's treasury, fee structures, and policies.
    *   [ ] **The Handover:** Transition control of the **Registry (ICRC-118)** and **Validator (ICRC-126)** canisters to the DAO.
*   **Advanced Economic Primitives:**
    *   [ ] **Security Bonds:** Enable developers to stake tokens as a security bond, providing an economic guarantee of their service's integrity.
    *   [ ] **Atomic Revenue Sharing:** Enhance the SDK to allow services to programmatically split incoming revenue with other services.

---

## **Community & Contribution**

Prometheus is a fully open-source project. We welcome contributions, feedback, and collaboration from the community.

-   **Issues:** Report bugs or suggest features in this repository's [Issues tab](https://github.com/prometheus-protocol/mcp-hub/issues).
-   **Contribute:** Check out our `CONTRIBUTING.md` guidelines to get started.
