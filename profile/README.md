# Project Prometheus: The Decentralized Payment Protocol

### A community-owned payment rail for the modern web, designed to replace the 2.9% tax on the internet.

<img width="1536" height="1024" alt="banner-professional" src="https://github.com/user-attachments/assets/0c7c5720-1d4a-4e50-b410-873a9ba9cc07" />

**Objective:** To build a decentralized, open-source payment protocol that makes Web3 economics simple and accessible for all developers. We provide the tools to enable everything from global e-commerce checkouts to per-second micropayments, all with near-zero fees and unparalleled security.

---

### [Phase 0: The Core - "Project Chimera" (The Payment Engine)](https://github.com/prometheus-protocol/chimera)

**Goal:** Build the foundational on-chain payment engine. It must be a production-grade, secure, and standards-compliant OAuth2 server capable of brokering payments and issuing authorization tokens.

*   **Scaffolding & Identity.**
    *   [x] Set up the Motoko project repository on GitHub with a permissive license (MIT).
    *   [x] Implement the core data structures in stable memory.
    *   [x] Implement the Internet Identity integration for the `/authorize` endpoint.

*   **The OAuth2 Engine.**
    *   [x] Implement the `/token` endpoint for the `authorization_code` grant type.
    *   [x] Integrate a JWT signing library and return standard, signed JWTs.
    *   [x] Implement the `/.well-known/jwks.json` endpoint for public key discovery.

*   **The Economic Layer (Subscription Model).**
    *   [x] Integrate with an ICRC-2 compliant token ledger.
    *   [x] Implement the subscription logic to gate token issuance.
    *   [x] Implement the `register_subscription` payment flow.

*   **Security & Public Readiness.**
    *   [x] **Implement PKCE (Proof Key for Code Exchange):** Secure the authorization flow for public clients (web & mobile apps) as per RFC 7636.
    *   [x] **Implement Dynamic Client Registration (DCR):** Create a public `/register` endpoint that allows clients to register programmatically, protected by an anti-spam fee.
    *   [x] **Implement OAuth Server Metadata:** Expose a `/.well-known/oauth-authorization-server` discovery document for automated client configuration.

*   **Finalization.**
    *   [ ] Write comprehensive unit and integration tests for all flows, including PKCE and DCR.
    *   [ ] **Action Item:** Submit the canister code for a professional security audit.

**Phase 0 Deliverable:** A production-ready, on-chain OAuth2 payment server that supports PKCE, DCR, and can issue authorization tokens based on a user's on-chain payment or subscription status.

---

### Phase 1: Developer Enablement - "Project Kitsune" (The SDKs)

**Goal:** Create a modular set of SDKs that make it dead simple for developers to integrate with the Prometheus Protocol, whether they are building on-chain services or traditional Web2 applications.

#### SDK 1 (Launch Priority): `prometheus-js` (for Web2 Services & Clients)
This is the low-level, universal library for integrating existing Web2 stacks with the Prometheus Protocol.

*   [ ] Provide helpers for frontend applications (React, Svelte, etc.) to easily initiate the OAuth2 login flow.
*   [ ] Implement the "Service Principal" logic, providing a simple function for a Node.js/Express server to trigger micropayments.

#### SDK 2 (Launch Priority): `prometheus.mo` (for On-Chain Services)
A small, focused library for any on-chain service needing to integrate Prometheus payments.

*   [ ] Provide a simple `validate_jwt(token)` function that handles JWKS fetching, caching, and full token validation.
*   [ ] Provide a helper function for on-chain resource servers to check a user's subscription status.

#### SDK 3 (Post-Launch): `mcp.mo` (The MCP Server Framework)
A high-level, "batteries-included" framework for the specific use case of building MCP servers on the IC.

*   [ ] Design and build the `McpServer` class, JSON-RPC handling, SSE streaming, and pluggable auth middleware using `prometheus.mo`.

**Phase 1 Deliverable:** Two core SDKs (`prometheus-js`, `prometheus.mo`) ready for launch, enabling both Web2 and Web3 integration.

---

### Phase 2: The Proof - "Project Tengu" (The Launch Demos)

**Goal:** Build live, working demos to prove the entire stack's versatility and its immediate value to developers.

*   **The Demos.**
    *   [ ] **Demo 1 (The Web2 Revolution): Micropayments for Existing APIs.** We will take an existing MCP server running on Google Cloud and use our new `prometheus-js` SDK to add micropayments for each API call. This demonstrates the power of Prometheus as a "drop-in" Web3 upgrade for any Web2 service.
    *   [ ] **Demo 2 (The Web3 Foundation): On-Chain Subscriptions.** We will build a simple "premium content" canister that uses the `prometheus.mo` SDK to grant access based on a user's on-chain subscription status. This demonstrates the ease of building new, sovereign, monetizable services on the IC.

*   **The Client & Launch.**
    *   [ ] Build the frontend clients for both demos.
    *   [ ] Write a "Quickstart" tutorial and create a simple landing page for the protocol.
    *   [ ] **Launch Day:** Announce the project on Twitter, the DFINITY dev forums, and relevant Discord channels. Point everyone to the live demos and the GitHub repos.

**Phase 2 Deliverable:** Two live, interactive demos showcasing both Web2 micropayment integration and Web3 subscription services, plus the initial documentation to onboard developers.

---

### Phase 3: The Future - "Project Orochi" (The Global Payment Rail)

**Goal:** Evolve from a project into a public good. Transition to community ownership and build the advanced features needed to challenge incumbent payment providers and enable the next generation of internet commerce.

*   **Governance & Decentralization:**
    *   [ ] **DAO Formation:** Design and deploy a governance canister (DAO) to give the community full control over the Protocol's treasury and future development.
    *   [ ] **The Handover:** Execute the one-way transaction to make the DAO the sole controller of the Prometheus Protocol, cementing its status as a decentralized public utility.

*   **The Universal Payment Suite (The Stripe Killers):**
    *   [ ] **Universal Checkout:** Launch a dedicated, secure checkout UI (`checkout.prometheus.icp.io`) that provides a seamless, one-click payment experience for e-commerce, rivaling Stripe Checkout and Apple Pay.
    *   [ ] **Streaming Subscriptions & Real-Time Metering:** Go beyond monthly billing. Enable services to charge users by the second, per API call, or per megabyte streamed, with funds flowing directly and continuously.
    *   [ ] **On-Chain Invoicing & Escrow:** Allow businesses and freelancers to issue invoices as on-chain objects (or NFTs). Funds can be held in a secure, programmatic escrow and released automatically when on-chain conditions are met.
    *   [ ] **Atomic Revenue Sharing:** Build a "Prometheus Connect" equivalent. Allow platforms and marketplaces to instantly and automatically split incoming revenue among multiple parties (creators, affiliates, treasuries) in a single, atomic transaction.
    *   [ ] **Cross-Chain Commerce:** Natively support payments via `ckBTC`, `ckETH`, and other chain-key stablecoins, turning Prometheus into a universal payment rail for the entire Web3 ecosystem.

*   **Ecosystem & Growth:**
    *   [ ] **Merchant Dashboard & Analytics:** Launch a comprehensive dashboard for merchants to track revenue, manage integrations, and view real-time analytics.
    *   [ ] **Architect for Hyper-Scale:** Design and implement the sharding and routing architecture to ensure the protocol can handle millions of transactions per second.
    *   [ ] **Community Grants & Incubation:** Use the DAO treasury to fund and support the most promising projects building on top of the Prometheus Protocol.
