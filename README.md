### The Campaign: "Project Prometheus" - Bringing Fire to the Agents

**Objective:** To create a decentralized, open-source, and economically viable ecosystem for AI agents on the Internet Computer.

---

### Phase 0: The Core - "Project Chimera" (The Auth Canister MVP)

**Goal:** Build the foundational, monolithic Auth Canister. It must be secure, functional, and auditable.

*   **Scaffolding & Identity.**
    *   [x] Set up the Motoko project repository on GitHub with a permissive license (MIT).
    *   [x] Implement the core data structures in stable memory: `StableTrieMap` for clients, subscriptions, etc.
    *   [x] Implement the Internet Identity integration for the `/authorize` endpoint. The output is a simple redirect flow that produces an `authorization_code`.

*   **The OAuth2 Engine.**
    *   [x] Implement the `/token` endpoint. It must handle the `authorization_code` grant type.
    *   [x] Integrate a JWT signing library for Motoko. The `/token` endpoint must return a standard, signed JWT.
    *   [x] Implement the `/.well-known/jwks.json` endpoint to expose the canister's public key for external validation.

*   **The Economic Layer (Subscription Model).**
    *   [ ] Integrate with an ICRC-2 compliant token (we'll use a test ledger first).
    *   [ ] Implement the subscription logic: A user's `Principal` is checked for an active subscription before a token is issued.
    *   [ ] Implement the payment flow: A `register_subscription(duration)` function that triggers an `icrc2_transfer_from` call to pull funds from a user's pre-approved allowance.

*   **Security & Static Registration.**
    *   [ ] Implement a simple, controller-only `register_client()` function. For the MVP, we will manually register the first few resource servers. Dynamic registration is too complex for Phase 0.
    *   [ ] Write comprehensive unit and integration tests for all flows.
    *   [ ] **Action Item:** Submit the canister code for a preliminary security audit.

*   **Phase 0 Deliverable:** A functional, auditable on-chain OAuth2 server that can issue JWTs based on a user's on-chain subscription status.

---

### Phase 1: Developer Enablement - "Project Kitsune" (The Motoko MCP SDK)

**Goal:** Make it dead simple for a developer to build an MCP server using our system.

*   **The Framework.**
    *   [ ] Design the high-level `McpServer` class API. Focus on the developer experience.
    *   [ ] Implement the internal HTTP router that dispatches `GET` and `POST` requests.
    *   [ ] Build the robust JSON-RPC parser and serializer.

*   **The Magic.**
    *   [ ] Build the JWT authentication middleware. It must be a one-liner to enable, configured with the Auth Canister's ID.
    *   [ ] Implement the `server.add_tool()` framework. This is the core abstraction for developers.

*   **Streaming & Polish.**
    *   [ ] Implement the abstracted SSE streaming logic. A developer should be able to return a "Stream" object without knowing how it works.
    *   [ ] Publish the initial `0.1.0` version of the package to the Mops package manager.
    *   [ ] Write the initial SDK documentation with clear examples.

*   **Phase 1 Deliverable:** A Motoko package (`mcp.mo`) that allows a developer to create a secure, monetizable, and compliant MCP server in under 50 lines of code.

---

### Phase 2: The Proof - "Project Tengu" (The First Light Demo)

**Goal:** Build a live, working demo to prove the entire stack works end-to-end and to attract the first users/developers.

*   **The Reference Server.**
    *   [ ] **Eat our own dog food:** Build a simple but useful MCP server canister *using our new SDK*.
    *   **Use Case:** A "Verifiable Randomness" server. It exposes a tool `get_random_bytes()` that costs a tiny micropayment. This is a perfect demo of a paid, verifiable on-chain tool.
    *   [ ] Register this server as a client with our deployed Auth Canister.

*   **The Client & Launch.**
    *   [ ] Build a minimal web-based MCP client (React/Svelte) that demonstrates the entire flow: Login -> Pay for Subscription -> Call the Paid Tool -> Display Result.
    *   [ ] Write a "Quickstart" tutorial and create a simple landing page.
    *   [ ] **Launch Day:** Announce the project on Twitter, the DFINITY dev forums, and relevant Discord channels. Point everyone to the live demo and the GitHub repos.

*   **Phase 2 Deliverable:** A live, interactive demo and the initial documentation needed to onboard the first wave of developers.

---

### Phase 3: The Future - "Project Orochi" (Decentralization & Advanced Features)

**Goal:** Transition the project from our control to a true community-owned protocol and implement the advanced features needed for mass adoption.

*   [ ] **Governance:** Design and deploy a governance canister (DAO) to control the Auth Canister.
*   [ ] **Decentralize:** Execute the one-way transaction to make the DAO the sole controller of the Auth Canister.
*   [ ] **Advanced Payments:** Implement the "Toll Booth" per-use metering model.
*   [ ] **Advanced Registration:** Implement Dynamic Client Registration with the anti-spam fee.
*   [ ] **Scale:** Design and implement the sharding and routing architecture as needed.
*   [ ] **Community:** Foster the community through grants, support, and continuous improvement based on feedback.
