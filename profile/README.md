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
- ✓ **Server Metadata:** Provides `/.well-known/oauth-authorization-server` (`RFC 8414`) and `/.well-known/jwks.json` endpoints for automated client configuration and key discovery.
- ✓ **MCP Authorization Spec Compliant:** Fully adheres to the requirements for an Authorization Server within the MCP ecosystem (rev. 2025-06-18).

---

## The Roadmap

Our development is organized into distinct, thematic phases.

### Phase 0: The Core Engine - "Project Chimera" (✅ COMPLETE)

**Goal:** Build the foundational on-chain engine: a production-grade, standards-compliant OAuth 2.1 server capable of brokering microtransactions.

*   **The OAuth 2.1 Server:**
    *   [x] Implemented the core flows (`/authorize`, `/token`) with Internet Identity.
    *   [x] Integrated JWT signing and public key discovery (`/.well-known/jwks.json`).
    *   [x] Implemented modern security standards: PKCE, DCR, Refresh Token Rotation, and Resource Indicators.
*   **The Microtransaction Engine:**
    *   [x] Integrated with ICRC-2 compliant token ledgers.
    *   [x] Implemented the core `charge_user` primitive for pay-per-use transactions.
    *   [x] Implemented a user-facing global allowance model for security and control.
*   **Finalization:**
    *   [x] Wrote comprehensive unit, integration, and end-to-end tests for all flows.
    *   [ ] **Action Item:** Submit the canister code for a professional security audit.

**Phase 0 Deliverable:** A production-ready, on-chain OAuth 2.1 server that can broker microtransactions.
- **Repo:** [`prometheus-protocol/auth-canister`](https://github.com/prometheus-protocol/auth-canister)

---

### Phase 1: Developer Enablement - "Project Kitsune" (The SDKs)

**Goal:** Create a modular set of SDKs that make it dead simple for any service to integrate Prometheus authentication and payments.

*   **SDK for Web2 & Off-Chain Services (`@prometheus-protocol/typescript-sdk`):**
    *   [x] **Frontend Client:** A single `createPrometheusClient` function that encapsulates the entire user authentication and authorization flow.
    *   [x] **Backend Client:** A simple `PrometheusServerClient` with a `charge()` method, allowing any server to trigger microtransactions.
*   **SDK for On-Chain Services (`prometheus.mo`):**
    *   [ ] Provide a simple `validate_jwt(token)` function that handles JWKS fetching, caching, and full token validation.
    *   [ ] Provide a helper function for on-chain services to initiate a `charge` call against the Prometheus payment engine.

**Phase 1 Deliverable:** Core SDKs enabling any Web2 or Web3 developer to integrate in minutes.
- **NPM Package:** [`@prometheus-protocol/typescript-sdk`](https://www.npmjs.com/package/@prometheus-protocol/typescript-sdk)

---

### Phase 2: The Proof - "Project Tengu" (The Launch Demos)

**Goal:** Build live, working demos to prove the power and simplicity of the protocol for both human and machine economies.

*   **Demo 1 (The Agent Economy): Monetizing AI Tools.**
    *   [x] We have taken a standard Model Context Protocol (MCP) server and used our SDK to add per-call microtransactions. This demonstrates our flagship use case: creating a true pay-per-use model where AI agents can autonomously pay for the tools they need.
*   **Demo 2 (The Sovereign SaaS): Building New Business Models.**
    *   [ ] We will build a simple "premium content" canister that uses the `charge()` primitive to bill users, demonstrating how developers retain full control over their business model while using Prometheus as a simple payment utility.

---

### Phase 3: The Future - "Project Orochi" (The Programmable Money Layer)

**Goal:** Evolve from a protocol into a global, community-owned programmable money layer for the internet.

*   **Decentralization & Governance:**
    *   [ ] **DAO Formation:** Deploy a governance DAO to give the community full control over the Protocol's treasury and future development.
    *   [ ] **The Handover:** Make the DAO the sole controller of the Prometheus Protocol, cementing its status as a decentralized public utility.
*   **The Programmable Money Suite:**
    *   [ ] **On-Chain Service Catalogs:** Allow AI agents to autonomously discover, understand, and pay for the tools they need to complete a task.
    *   [ ] **Streaming Payments:** Enable services to charge users by the second, per API call, or per megabyte streamed.
    *   [ ] **Atomic Revenue Sharing:** Allow platforms and marketplaces to instantly and automatically split incoming revenue among multiple parties.

---

## Community & Contribution

Prometheus is an open-source project. We welcome contributions, feedback, and collaboration from the community.

-   **Issues:** Report bugs or suggest features in the relevant repository's [Issues tab](https://github.com/prometheus-protocol/auth-canister/issues).
-   **Contribute:** Check out our `CONTRIBUTING.md` guidelines in each repository to get started.
