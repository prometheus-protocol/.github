# Project Prometheus: The Decentralized Payment Protocol

### A community-owned payment rail for the modern web, designed to replace the 2.9% tax on the internet.

<img width="1536" height="1024" alt="banner-professional" src="https://github.com/user-attachments/assets/b1214338-c1e7-45d9-848b-d37f8983dfa2" />


**Objective:** To build a decentralized, open-source payment protocol that makes Web3 economics simple and accessible for all developers. We provide the tools to enable everything from global e-commerce checkouts to per-second micropayments, all with near-zero fees and unparalleled security.

---

### Phase 0: The Core - "Project Chimera" (The Payment Engine)

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

#### SDK 1: `prometheus-sdk` (The Core Payment Library)
This is the low-level, universal library for interacting with the Prometheus Protocol.

*   **`prometheus.mo` (for On-Chain Services):**
    *   [ ] Provide a simple `validate_jwt(token)` function that handles JWKS fetching, caching, and full token validation.
    *   [ ] Provide a helper function for on-chain resource servers to trigger per-use payments by calling our Auth Canister.

*   **`prometheus-js` (for Web2 Services & Clients):**
    *   [ ] Provide helpers for frontend applications (React, Svelte, etc.) to easily initiate the OAuth2 login flow.
    *   [ ] Implement the "Service Principal" logic, providing a simple function for a Node.js/Express server to trigger micropayments.

#### SDK 2: `mcp.mo` (The MCP Server Framework)
This is the high-level, "batteries-included" framework for the specific use case of building MCP servers on the IC.

*   **[ ] The Framework:**
    *   [ ] Design the high-level `McpServer` class API.
    *   [ ] Implement the internal HTTP router and JSON-RPC handling.
    *   [ ] Implement the abstracted SSE streaming logic.
*   **[ ] Pluggable Authentication:**
    *   [ ] Design a clean middleware interface for authentication.
    *   [ ] Build the `PrometheusMcpAuth` middleware, which will use our `prometheus.mo` library internally.
*   **[ ] The Developer Experience:**
    *   [ ] Implement the `server.add_tool()` framework for easy tool registration.
    *   [ ] Publish the initial `0.1.0` version of the package to the Mops package manager.

**Phase 1 Deliverable:** Two distinct, high-quality packages:
1.  **`prometheus-sdk`:** A core library in both Motoko and TypeScript for universal payment and auth integration.
2.  **`mcp.mo`:** A full-featured framework for building MCP servers, which uses the `prometheus.mo` library as its primary authentication mechanism.

---

### Phase 2: The Proof - "Project Tengu" (The Launch Demos)

**Goal:** Build live, working demos to prove the entire stack's versatility for both Web2 and Web3 use cases.

*   **The Demos.**
    *   [ ] **Demo 1 (The Web2 Revolution): The E-commerce Checkout.** Build a simple web store with a "Checkout with Prometheus" button to demonstrate the seamless, low-fee alternative to Stripe/PayPal. This will use the `prometheus-js` SDK.
    *   [ ] **Demo 2 (The Web3 Frontier): The MCP Micropayment Server.** Build a "Verifiable Randomness" MCP server to showcase the unique micropayment capabilities that enable the future agent economy. This will use the `mcp.mo` and `prometheus.mo` SDKs.

*   **The Client & Launch.**
    *   [ ] Build the frontend clients for both demos.
    *   [ ] Write a "Quickstart" tutorial and create a simple landing page for the protocol.
    *   [ ] **Launch Day:** Announce the project on Twitter, the DFINITY dev forums, and relevant Discord channels. Point everyone to the live demos and the GitHub repos.

**Phase 2 Deliverable:** Two live, interactive demos showcasing both e-commerce and micropayment use cases, plus the initial documentation to onboard developers from any background.

---

### Phase 3: The Future - "Project Orochi" (The Global Payment Rail)

**Goal:** Evolve from a project into a public good. Transition to community ownership and build the advanced features needed for global adoption.

*   [ ] **Governance:** Design and deploy a governance canister (DAO) to control the Protocol.
*   [ ] **Decentralize:** Execute the one-way transaction to make the DAO the sole controller.
*   [ ] **Advanced Payments:** Implement the "Toll Booth" per-use metering model and the full "Checkout with Prometheus" flow with a dedicated UI.
*   [ ] **Merchant Tooling:** Build dashboards and tools for merchants to track payments and manage their integration.
*   [ ] **Advanced Flows:** Implement on-chain escrow, automated royalty splits, and other programmable payment logic.
*   [ ] **Scale:** Design and implement the sharding and routing architecture as needed.
*   [ ] **Community:** Foster the community through grants, support, and continuous improvement based on feedback.
