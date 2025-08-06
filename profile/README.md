# **Prometheus Protocol: The Trust Layer for Decentralized Commerce**

### Our mission is to enable a new generation of decentralized commerce by providing the open-source foundation for **verifiable trust, secure identity, and near-zero fee payments.**

<img width="1536" alt="Prometheus Protocol Banner" src="https://github.com/user-attachments/assets/0c7c5720-1d4a-4e50-b410-873a9ba9cc07" />

---

## **Overview**

Prometheus Protocol is a complete, on-chain economic engine for the Internet Computer. It provides a unified solution for the three pillars of a trustworthy digital economy:

1.  **Secure Identity & Authorization:** A full-featured, on-chain **OAuth 2.1 provider** serves as the robust foundation for any application requiring standards-based authentication.
2.  **Verifiable Trust & Discovery:** A high-assurance **App Store and Registry** allows users and AI agents to discover and connect to MCP servers whose code has been cryptographically verified and certified.
3.  **Direct & Efficient Payments:** An integrated **ICRC-2 allowance system** empowers users to grant services direct, metered access to tokens, enabling a new wave of monetizable applications.

By combining these layers, Prometheus provides the foundational infrastructure for a new generation of decentralized applications and the emerging AI agent economy.

## **Features & Compliance**

The core of Prometheus is a production-ready Authorization Server implementing the latest security best practices from the IETF and the specific requirements of the MCP specification.

- ✓ **OAuth 2.1 Core:** Implements the modern, secure baseline for OAuth, including mandatory PKCE (`RFC 7636`) and the Authorization Code Flow (`RFC 6749`).
- ✓ **Refresh Token Rotation:** Enhances security by issuing a new, single-use refresh token each time one is used, mitigating the risk of token theft.
- ✓ **Dynamic Client Registration (DCR):** A public `/register` endpoint (`RFC 7591`) allows applications to register programmatically without manual intervention.
- ✓ **Resource Indicators:** Supports token audience binding via the `resource` parameter (`RFC 8707`), ensuring tokens are used only at their intended destination.
- ✓ **Multi-Token Payment Authorization:** Enables resource servers to define a list of accepted ICRC-2 compliant tokens for payment-gated scopes.
- ✓ **Server Metadata:** Provides `/.well-known/oauth-authorization-server` (`RFC 8414`) and `/.well-known/jwks.json` endpoints for automated client configuration and key discovery.
- ✓ **MCP Authorization Spec Compliant:** Fully adheres to the requirements for an Authorization Server within the MCP ecosystem (rev. 2025-06-18).

---

## **The Roadmap**

Our journey is structured in ambitious phases, building from a solid foundation towards a vibrant, trusted ecosystem.

### **Phase 0: The Foundation - "Project Hephaestus" (✅ COMPLETE)**

**Goal:** Forge the complete, end-to-end stack for secure identity and payments: a production-grade auth server, developer-friendly SDKs, and live proof-of-concept demonstrations.

*   **The Core Auth Server:**
    *   [x] Implemented the core OAuth 2.1 flows (`/authorize`, `/token`) with Internet Identity.
    *   [x] Integrated JWT signing and public key discovery (`/.well-known/jwks.json`).
    *   [x] Implemented modern security standards: PKCE, DCR, Refresh Token Rotation, and Resource Indicators.
    *   [x] Enabled resource servers to define accepted ICRC-2 payment tokens and for users to set per-service allowances.
    *   [ ] **Action Item:** Submit the canister code for a professional security audit.
*   **The Developer SDKs:**
    *   [x] **`motoko-mcp-sdk`:** A complete server framework for building production-ready, monetizable MCP services in Motoko.
    *   [x] **`@prometheus-protocol/typescript-sdk`:** A client library for web apps and a server library for integrating off-chain services with on-chain payments.
*   **The Proof of Concept:**
    *   [x] Deployed live demos showcasing both on-chain native services (built with the Motoko SDK) and Web2 services bridged into the on-chain economy (using the TypeScript SDK).

**Phase 0 Deliverable:** A complete, end-to-end, production-ready stack for building and monetizing MCP servers on the IC, all available within this GitHub organization.

---

### **Phase 1: The Trust Layer - "Project Arsenal" (IN PROGRESS)**

**Goal:** Build the premier, high-trust marketplace for provably safe MCP services, establishing the gold standard for reliability in the agent economy by leveraging community standards.

*   **The Certified Registry (`The Arsenal`):**
    *   [ ] Implement and deploy our official **ICRC-118 compliant Registry**. This will serve as the on-chain, versioned catalog for all certified MCP services.
*   **The Provably Secure Framework:**
    *   [ ] Develop and publish the **`Immutable Orchestrator`**, our hardened, open-source **ICRC-120** implementation. This canister enforces that only certified code can be run.
    *   [ ] Require developers to **blackhole** their Orchestrator, making its security rules immutable and tamper-proof.
*   **The On-Chain Certification Process:**
    *   [ ] Deploy our **ICRC-126 `Validator` canister**, which will cryptographically sign and issue endorsements for audited Wasm hashes.
    *   [ ] Implement a multi-tiered certification system (**Bronze, Silver, Gold**) based on the level of scrutiny, from automated reproducible builds to full manual source code audits.
*   **The User & Agent Experience:**
    *   [ ] Deploy a web frontend for discovering, filtering, and connecting to services in `The Arsenal`.
    *   [ ] Integrate the **Security Certificate UI** into the discovery and consent flows, giving users transparent, real-time verification of a server's integrity.
*   **Key Objective:** Onboard and certify the first 5-10 flagship applications to seed the ecosystem with high-quality, trusted tools.

---

### **Phase 2: Ecosystem Growth - "Project Alliance"**

**Goal:** With a unified platform for trust, identity, and payments, the focus shifts to scaling the ecosystem through strategic business development and partnerships.

*   **Developer & Enterprise Onboarding:**
    *   [ ] Actively recruit high-value developers to publish their services on the platform.
    *   [ ] Develop B2B offerings, such as managed private registries and support for enterprise clients.
*   **Client-Side Integration:**
    *   [ ] Partner with developers of AI agents and MCP clients (e.g., VSCode, autonomous agent frameworks) to integrate our registry as a primary, high-trust service source.
*   **Community Growth:**
    *   [ ] Launch community initiatives such as hackathons, developer grants, and comprehensive tutorials to accelerate adoption.

---

### **Phase 3: The Autonomous Economy - "Project Agora"**

**Goal:** Evolve from a platform managed by the founding team into a self-sustaining, community-governed economic protocol.

*   **Decentralized Governance & Curation:**
    *   [ ] **DAO Formation:** Deploy a governance DAO to give the community control over the platform's treasury, fee structures, and policies.
    *   [ ] **The Handover:** Transition control of the **Registry (ICRC-118)** and **Validator (ICRC-126)** canisters to the DAO, cementing their status as a decentralized public utility.
    *   [ ] **Community Curation:** Allow the DAO to manage the list of vetted auditors and vote on community-driven standards.
*   **Advanced Economic Primitives:**
    *   [ ] **Security Bonds:** Enable developers to stake tokens as a security bond, providing an economic guarantee of their service's integrity that can be slashed to compensate users in case of malpractice.
    *   [ ] **Atomic Revenue Sharing:** Enhance the SDK to allow services to programmatically split incoming revenue with other services, enabling more complex and collaborative applications.

---

## **Community & Contribution**

Prometheus is a fully open-source project. We welcome contributions, feedback, and collaboration from the community.

-   **Issues:** Report bugs or suggest features in this repository's [Issues tab](https://github.com/prometheus-protocol/mcp-hub/issues).
-   **Contribute:** Check out our `CONTRIBUTING.md` guidelines to get started.
