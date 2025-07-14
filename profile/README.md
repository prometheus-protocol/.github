### The Campaign: "Project Prometheus" - Bringing Fire to the Agents
<img width="1536" height="900" alt="banner" src="https://github.com/user-attachments/assets/f9189ebb-7dbd-4087-b8be-205c8e7ddc69" />

**Objective:** To create a decentralized, open-source, and economically viable ecosystem for AI agents on the Internet Computer.

---

### Phase 0: The Core - "Project Chimera" (MCP-Compliant Auth Server)

**Goal:** Build a foundational, secure, and MCP-compliant Auth Canister. It must be self-service for developers and ready for integration with public clients.

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

*   **Security & MCP Compliance.**
    *   [x] **Implement PKCE (Proof Key for Code Exchange):** Secure the authorization flow by requiring `code_challenge` and `code_verifier` parameters, as per RFC 7636. This is non-negotiable for public clients.
    *   [x] **Implement Dynamic Client Registration (DCR):** Create a public `/register` endpoint that allows clients to register programmatically. This endpoint must be protected by an anti-spam/collateral fee, using our existing economic layer.
    *   [x] **Implement OAuth Server Metadata:** Expose a `/.well-known/oauth-authorization-server` discovery document detailing all endpoints, supported grant types, PKCE methods, and other server capabilities.

*   **Finalization.**
    *   [ ] Write comprehensive unit and integration tests for all flows, including PKCE and DCR.
    *   [ ] **Action Item:** Submit the canister code for a preliminary security audit.

*   **Phase 0 Deliverable:** A functional, auditable, and MCP-compliant on-chain OAuth2 server that supports PKCE, Dynamic Client Registration, and issues JWTs based on a user's on-chain subscription status.

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
*   [ ] **Scale:** Design and implement the sharding and routing architecture as needed.
*   [ ] **Community:** Foster the community through grants, support, and continuous improvement based on feedback.
