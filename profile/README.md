# Project Prometheus: The Open Payment Rail for the Internet

### Our mission is to replace the 2.9% tax on internet commerce with a decentralized, open-source, and near-zero fee payment protocol.

<img width="1536" height="1024" alt="banner-professional" src="https://github.com/user-attachments/assets/0c7c5720-1d4a-4e50-b410-873a9ba9cc07" />

---

**The Vision:**

Every economic interaction on the web—from e-commerce checkouts to API calls—is a transaction. Today, these transactions are gated by private companies that extract fees and control access. Prometheus changes this. We are building a public utility for money on the internet: a simple, powerful protocol that allows any developer to integrate secure, global, near-instant payments for any amount, no matter how small.

---

### [Phase 0: The Core - "Project Chimera" (The Payment Engine)](https://github.com/prometheus-protocol/auth-canister)

**Goal:** Build the foundational on-chain engine. It must be a production-grade, standards-compliant OAuth2 server capable of brokering microtransactions and issuing authorization tokens.

*   **The OAuth2 Engine.**
    *   [x] Implement the core OAuth2 flows (`/authorize`, `/token`) with Internet Identity.
    *   [x] Integrate JWT signing and public key discovery (`/.well-known/jwks.json`).
    *   [x] Implement modern security standards: PKCE (RFC 7636), Dynamic Client Registration (DCR), and Resource Indicators (RFC 8707).

*   **The Microtransaction Engine.**
    *   [x] Integrate with an ICRC-2 compliant token ledger.
    *   [x] Implement the `charge_user` function, allowing trusted resource servers to execute pay-per-use microtransactions.
    *   [x] Implement a user-facing allowance model for security and control.

*   **Finalization.**
    *   [ ] Write comprehensive unit and integration tests for all flows.
    *   [ ] **Action Item:** Submit the canister code for a professional security audit.

**Phase 0 Deliverable:** [A production-ready, on-chain OAuth2 server that can broker microtransactions and issue authorization tokens based on a user's on-chain allowance.](https://github.com/prometheus-protocol/auth-canister)

---

### Phase 1: Developer Enablement - "Project Kitsune" (The SDKs)

**Goal:** Create a modular set of SDKs that make it dead simple for developers to integrate the Prometheus microtransaction rail.

#### SDK 1 (Launch Priority): `prometheus-js` (for Web2 Services & Clients)
The universal library for integrating existing Web2 stacks with the Prometheus Protocol.

*   [x] **Frontend Client:** A single `createPrometheusClient` function that encapsulates the entire user authentication and authorization flow.
*   [x] **Backend Client:** A simple `PrometheusServerClient` with a `charge()` method, allowing any server to trigger microtransactions.

#### SDK 2 (Launch Priority): `prometheus.mo` (for On-Chain Services)
A focused library for any on-chain service needing to integrate Prometheus payments.

*   [ ] Provide a simple `validate_jwt(token)` function that handles JWKS fetching, caching, and full token validation.
*   [ ] Provide a helper function for on-chain services to initiate a `charge` call against the Prometheus payment engine.

**Phase 1 Deliverable:** Two core SDKs (`prometheus-js`, `prometheus.mo`) enabling any Web2 or Web3 developer to integrate microtransactions in minutes.

---

### Phase 2: The Proof - "Project Tengu" (The Launch Demos)

**Goal:** Build live, working demos to prove the power and simplicity of the microtransaction rail.

*   **The Demos.**
    *   [x] **Demo 1 (The Web2 Revolution): The Drop-in Payment Upgrade.** We have built a proof-of-concept Express API that uses the `prometheus-js` SDK to add per-call microtransactions. This demonstrates how any existing Web2 service can be upgraded to accept Web3 payments without a rewrite.
    *   [ ] **Demo 2 (The Sovereign SaaS): Building New Business Models.** We will build a simple "premium content" canister that manages its own subscription logic internally. It will use the `charge()` primitive from `prometheus.mo` to bill users. This demonstrates how developers retain full control over their business model while using Prometheus as a simple, powerful payment utility.

*   **The Launch.**
    *   [ ] Write a "Quickstart" tutorial and create a simple landing page for the protocol.
    *   [ ] **Launch Day:** Announce the project on Twitter, the DFINITY dev forums, and relevant Discord channels. Point everyone to the live demos and the GitHub repos.

**Phase 2 Deliverable:** Two live demos showcasing the immediate value of microtransactions for both existing and new applications, plus the documentation to onboard developers.

---

### Phase 3: The Future - "Project Orochi" (The Programmable Money Layer)

**Goal:** Evolve from a protocol into a global, community-owned programmable money layer for the internet.

*   **Decentralization & Governance:**
    *   [ ] **DAO Formation:** Deploy a governance DAO to give the community full control over the Protocol's treasury and future development.
    *   [ ] **The Handover:** Make the DAO the sole controller of the Prometheus Protocol, cementing its status as a decentralized public utility.

*   **The Programmable Money Suite:**
    *   [ ] **On-Chain Service Catalogs:** Allow trusted resource servers to publish and manage a dynamic, on-chain catalog of their services and prices. When a user authorizes an application, they will see a clear, human-readable list of potential charges (e.g., 'Purchase Digital Art: 5 ICP', 'Generate Hi-Fi Audio: 0.1 ICP'). This transforms the protocol into a full-fledged e-commerce engine with unparalleled user transparency.
    *   [ ] **Streaming Payments:** Enable services to charge users by the second, per API call, or per megabyte streamed, using the `charge` primitive as the foundation for real-time billing.
    *   [ ] **Atomic Revenue Sharing:** Allow platforms and marketplaces to instantly and automatically split incoming revenue among multiple parties (creators, affiliates, treasuries) in a single, atomic transaction.

*   **Ecosystem & Growth:**
    *   [ ] **Fiat On-Ramps:** Integrate third-party on-ramps directly into the user-facing "allowance management" UI, allowing users to seamlessly purchase tokens like USDC.
    *   [ ] **Merchant Dashboard & Analytics:** Launch a comprehensive dashboard for merchants to track revenue, manage their service catalogs, and view real-time analytics.
    *   [ ] **Community Grants & Incubation:** Use the DAO treasury to fund and support the most promising projects building on top of the Prometheus Protocol.
