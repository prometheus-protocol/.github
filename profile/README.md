# Prometheus Protocol: An Open Standard for Authorization & Payments

### Our mission is to replace the 2.9% tax on internet commerce with a decentralized, open-source, and near-zero fee payment protocol.

<img width="1536" alt="Prometheus Protocol Banner" src="https://github.com/user-attachments/assets/0c7c5720-1d4a-4e50-b410-873a9ba9cc07" />

---

## Overview

Prometheus Protocol is a full-featured, on-chain **OAuth 2.1 provider** built for the Internet Computer. It provides a robust, general-purpose solution for any application requiring standards-based authentication and authorization.

While designed for broad use, it is also a fully compliant **Authorization Server** for the **Model Context Protocol (MCP)** ecosystem. This dual focus ensures that Prometheus is both a flexible tool for the wider IC community and a hardened, specification-compliant engine for enterprise-grade protocols.

Ultimately, it serves as the foundational security and payment layer for a new generation of decentralized applications and AI agent economies.

## Features & Compliance

The core of Prometheus is a production-ready Authorization Server implementing the latest security best practices from the IETF and the specific requirements of the MCP specification.

- ✓ **OAuth 2.1 Core:** Implements the modern, secure baseline for OAuth, including mandatory PKCE (`RFC 7636`) and the Authorization Code Flow (`RFC 6749`).
- ✓ **Refresh Token Rotation:** Enhances security by issuing a new, single-use refresh token each time one is used, mitigating the risk of token theft.
- ✓ **Dynamic Client Registration (DCR):** A public `/register` endpoint (`RFC 7591`) allows applications to register programmatically without manual intervention.
- ✓ **Resource Indicators:** Supports token audience binding via the `resource` parameter (`RFC 8707`), ensuring tokens are used only at their intended destination.
- ✓ **Multi-Token Payment Authorization:** Enables resource servers to define a list of accepted ICRC-2 compliant tokens for payment-gated scopes.
- ✓ **Server Metadata:** Provides `/.well-known/oauth-authorization-server` (`RFC 8414`) and `/.well-known/jwks.json` endpoints for automated client configuration and key discovery.
- ✓ **MCP Authorization Spec Compliant:** Fully adheres to the requirements for an Authorization Server within the MCP ecosystem (rev. 2025-06-18).

---

## The Roadmap

Our journey is structured in ambitious phases, building from a solid foundation towards a vibrant, trusted ecosystem.

### Phase 0: The Foundation - "Project Hephaestus" (✅ COMPLETE)

**Goal:** Forge the complete, end-to-end stack: a production-grade auth server, developer-friendly SDKs, and live proof-of-concept demonstrations.

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

**Phase 0 Deliverable:** A complete, end-to-end, production-ready stack for building and monetizing MCP servers on the IC.
- **Auth Canister:** [`prometheus-protocol/auth-canister`](https://github.com/prometheus-protocol/auth-canister)
- **Motoko SDK:** [`mops.one/mcp-motoko-sdk`](https://mops.one/mcp-motoko-sdk) | [`GitHub Repo`](https://github.com/prometheus-protocol/motoko-sdk)
- **TypeScript SDK:** [`npmjs.com/package/@prometheus-protocol/typescript-sdk`](https://www.npmjs.com/package/@prometheus-protocol/typescript-sdk)

---

### Phase 1: The High-Trust Registry - "Project Arsenal"

**Goal:** Build the premier, high-trust marketplace for audited, monetizable MCP services, establishing the gold standard for safety and reliability in the agent economy.

*   **The Registry Canister (`The Arsenal`):**
    *   [ ] Develop a versioned, on-chain catalog for MCP services, storing immutable Wasm hashes and service manifests.
    *   [ ] Build a developer CLI (`mcp-cli`) for seamless publishing and version management.
*   **The On-Chain Audit Process:**
    *   [ ] Establish a framework for vetted, third-party auditors to submit on-chain audit reports for specific Wasm hashes.
    *   [ ] Integrate audit results directly into the service manifest, enabling "Verified & Audited" badges in the UI.
*   **The User & Agent Experience:**
    *   [ ] Deploy a web frontend for discovering, filtering, and interacting with services in `The Arsenal`.
    *   [ ] Expose a rich, machine-readable API for agents to programmatically discover services based on keywords, signatures, and audit status.
*   **Business Model Implementation:**
    *   [ ] Implement a one-time registration fee for new services to cover the cost of an initial safety and compliance audit.
    *   [ ] Implement a small, transparent transaction fee on payments brokered through the platform to ensure long-term sustainability.
*   **Key Objective:** Onboard and facilitate the audit of the first 5-10 flagship applications to seed the ecosystem with high-quality, trusted tools.

---

### Phase 2: Ecosystem Growth - "Project Alliance"

**Goal:** With a functional marketplace and a core set of trusted apps, the focus shifts to scaling the ecosystem through strategic business development and partnerships.

*   **Developer & Enterprise Onboarding:**
    *   [ ] Actively recruit high-value developers to publish their services on the platform.
    *   [ ] Develop B2B offerings, such as managed private registries and support for enterprise clients.
*   **Client-Side Integration:**
    *   [ ] Partner with developers of AI agents and MCP clients (e.g., VSCode, autonomous agent frameworks) to integrate our registry as a primary, high-trust service source.
*   **Community Growth:**
    *   [ ] Launch community initiatives such as hackathons, developer grants, and comprehensive tutorials to accelerate adoption.

---

### Phase 3: The Autonomous Economy - "Project Agora"

**Goal:** Evolve from a centrally-managed platform into a self-sustaining, community-governed economic protocol.

*   **Decentralized Governance & Curation:**
    *   [ ] **DAO Formation:** Deploy a governance DAO to give the community control over the platform's treasury, fee structures, and policies.
    *   [ ] **The Handover:** Transition control of `The Arsenal` and its policies to the DAO, cementing its status as a decentralized public utility.
    *   [ ] **Community Curation:** Allow the DAO to manage the list of vetted auditors and vote on community-driven standards.
*   **Advanced Economic Primitives:**
    *   [ ] **Security Bonds:** Enable developers to stake tokens as a security bond, providing an economic guarantee of their service's integrity that can be slashed to compensate users in case of malpractice.
    *   [ ] **Atomic Revenue Sharing:** Enhance the SDK to allow services to programmatically split incoming revenue with other services, enabling more complex and collaborative applications.

---

## Community & Contribution

Prometheus is an open-source project. We welcome contributions, feedback, and collaboration from the community.

-   **Issues:** Report bugs or suggest features in the relevant repository's [Issues tab](https://github.com/prometheus-protocol/auth-canister/issues).
-   **Contribute:** Check out our `CONTRIBUTING.md` guidelines in each repository to get started.
