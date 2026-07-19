# IETF AI Agent Standards Landscape

**Author**: Chris Hood, chris@chrishood.com, chris@nomotic.ai
**Version**: v.00 - 2026-07-15 (based on IETF Datatracker, mailing lists, BoF schedules for IETF 126 Vienna, and cross-referenced drafts)
**Purpose**: Living document to track venues, work items, competitors, and gaps for AI agent / agentic standards.

---

## How to read this document

Each category uses three standard subsections, with bullets listed alphabetically:

- **IETF venues** — WGs, BoFs, RGs, mailing lists, side meetings where the topic lives.
- **IETF work items** — Internet-Drafts, WG documents, and proposed contributions in or targeting the IETF/IRTF stream.
- **External protocols & industry** — non-IETF specs, consortia, and vendor efforts that shape (or compete with) the IETF conversation.

All Internet-Draft references link to the Datatracker document page and will resolve to the current version.

---

## 1. Agent Identity, Auth & Attestation

**IETF venues**
- AI Agent Security side meeting — IETF 125 (Shenzhen, March 2026), organized via Huawei (agenda/slides at github.com/liuchunchi/IETF125-AI-Agent-Security-Side-Meeting); venue where [draft-kiliram-agent-trust-auth-framework](https://datatracker.ietf.org/doc/draft-kiliram-agent-trust-auth-framework/) was presented.
- DISPATCH — [draft-klrc-aiagent-auth](https://datatracker.ietf.org/doc/draft-klrc-aiagent-auth/) was dispatched at IETF 125 with a hoped outcome of AD-sponsorship or adoption into OAuth/WIMSE.
- OAUTH WG (oauth@ietf.org) — venue for agent delegation extensions.
- RATS WG (rats@ietf.org) — venue hook for agent attestation (EAT profiles).
- Related: WEBBOTAUTH WG (bot/crawler auth — see Category 13).
- SCIM WG (scim@ietf.org) — agent identity provisioning/lifecycle extensions (see work items).
- SPICE WG (spice@ietf.org) — confirmed venue for the actor-chain / intent-chain drafts (draft-mw-spice-*); SPICE coordinates with RATS, OAuth, JOSE, COSE, and SCITT per its charter.
- WIMSE WG (wimse@ietf.org) — de facto home for agent-identity applicability discussions.

**IETF work items**
- [draft-aap-oauth-profile](https://datatracker.ietf.org/doc/draft-aap-oauth-profile/) (AAP; Agent Authorization Profile for OAuth 2.0) — OAuth profile scoped to agent authorization patterns.
- [draft-abbey-scim-agent-extension](https://datatracker.ietf.org/doc/draft-abbey-scim-agent-extension/) (Abbey & Cohen, Okta; Oct 2025) — SCIM "Agent" resource type and schemas for provisioning/deprovisioning agents and agentic applications across domains; earlier filed as draft-scim-agent-extension.
- [draft-aip-agent-identity-protocol](https://datatracker.ietf.org/doc/draft-aip-agent-identity-protocol/) — Agent Identity Protocol: agentic authentication and authorized policy enforcement.
- [draft-barney-caam](https://datatracker.ietf.org/doc/draft-barney-caam/) (Barney; CAAM) — Contextual Agent Authorization Mesh.
- [draft-beyer-agent-identity-architecture](https://datatracker.ietf.org/doc/draft-beyer-agent-identity-architecture/) — architectural model for human-anchored agent identity.
- [draft-beyer-agent-identity-problem-statement](https://datatracker.ietf.org/doc/draft-beyer-agent-identity-problem-statement/) — problem statement for human-anchored identity.
- [draft-bondar-wca](https://datatracker.ietf.org/doc/draft-bondar-wca/) (WCA; Warrant Certificate Authorities) — auditable data provenance for AI-agent tool-call chains; identity anchor for provenance claims.
- [draft-chen-agent-decoupled-authorization-model](https://datatracker.ietf.org/doc/draft-chen-agent-decoupled-authorization-model/) — decoupled authorization model for agent2agent interactions.
- [draft-chen-oauth-rar-agent-extensions](https://datatracker.ietf.org/doc/draft-chen-oauth-rar-agent-extensions/) — policy, lifecycle, and intent extensions for OAuth Rich Authorization Requests.
- [draft-chen-oauth-scope-agent-extensions](https://datatracker.ietf.org/doc/draft-chen-oauth-scope-agent-extensions/) — structured and constraint extensions for OAuth scopes for agents.
- [draft-diaconu-agents-authz-info-sharing](https://datatracker.ietf.org/doc/draft-diaconu-agents-authz-info-sharing/) — cross-domain authorization information sharing for agents.
- [draft-drake-agent-identity-registry](https://datatracker.ietf.org/doc/draft-drake-agent-identity-registry/) — federated registry with hardware-anchored identity.
- [draft-ferro-dnsop-apertoid](https://datatracker.ietf.org/doc/draft-ferro-dnsop-apertoid/) (Ferro; ApertoID) — DNS-based agent identity declaration protocol.
- [draft-ferro-httpbis-apertoid-sig](https://datatracker.ietf.org/doc/draft-ferro-httpbis-apertoid-sig/) (Ferro) — ApertoID-Signature: HTTP request signing for AI agent identity.
- [draft-gaikwad-south-authorization](https://datatracker.ietf.org/doc/draft-gaikwad-south-authorization/) (SOUTH) — stochastic authorization protocol; referenced by the Web of Agents discovery draft.
- [draft-goswami-agentic-jwt](https://datatracker.ietf.org/doc/draft-goswami-agentic-jwt/) (Goswami; Secure Intent Protocol) — JWT-compatible agentic identity and workflow management.
- [draft-gudlab-agentid-protocol](https://datatracker.ietf.org/doc/draft-gudlab-agentid-protocol/) (GudLab; AgentID) — identity protocol for autonomous AI agents.
- [draft-hartman-credential-broker-4-agents](https://datatracker.ietf.org/doc/draft-hartman-credential-broker-4-agents/) (Hartman; CB4A) — credential broker for agents.
- [draft-hood-independent-agtp](https://datatracker.ietf.org/doc/draft-hood-independent-agtp/), [draft-hood-agtp-agent-cert](https://datatracker.ietf.org/doc/draft-hood-agtp-agent-cert/), [draft-hood-agtp-identifiers](https://datatracker.ietf.org/doc/draft-hood-agtp-identifiers/), [draft-hood-agtp-trust](https://datatracker.ietf.org/doc/draft-hood-agtp-trust/) — AGTP substrate identity primitives: X.509 v3 Agent Certificates with canonical Agent-ID (SHA-256 of Agent Genesis) and Owner-ID, trust score model, wire-layer attribution; identity bound directly into the transport substrate rather than composed from workload-identity primitives.
- [draft-ietf-wimse-arch](https://datatracker.ietf.org/doc/draft-ietf-wimse-arch/), [draft-ietf-wimse-identifier](https://datatracker.ietf.org/doc/draft-ietf-wimse-identifier/), [draft-ietf-wimse-workload-creds](https://datatracker.ietf.org/doc/draft-ietf-wimse-workload-creds/), [draft-ietf-wimse-wpt](https://datatracker.ietf.org/doc/draft-ietf-wimse-wpt/), [draft-ietf-wimse-http-signature](https://datatracker.ietf.org/doc/draft-ietf-wimse-http-signature/) — foundational WIMSE deliverables that the agent-identity drafts compose.
- [draft-jia-oauth-scope-aggregation](https://datatracker.ietf.org/doc/draft-jia-oauth-scope-aggregation/) — OAuth 2.0 scope aggregation for multi-step AI agent workflows.
- [draft-kavian-agent-enrollment-protocol](https://datatracker.ietf.org/doc/draft-kavian-agent-enrollment-protocol/) — agent enrollment; part of a kavian draft family including AEP session-credential and did-web identity-method documents.
- [draft-kiliram-agent-trust-auth-framework](https://datatracker.ietf.org/doc/draft-kiliram-agent-trust-auth-framework/) (King et al.; March 2026) — protocol-agnostic architectural framework for a cross-domain trust substrate covering verifiable agent identity, credentialing, cross-domain authorization, delegation, revocation, and auditability; presented at the IETF 125 AI Agent Security side meeting.
- [draft-klrc-aiagent-auth](https://datatracker.ietf.org/doc/draft-klrc-aiagent-auth/) (Kasselman et al.; -03 July 2026) — AIMS (Agent Identity Management System); proposes a model that composes WIMSE, SPIFFE, OAuth 2.0, and OpenID SSF/CAEP rather than defining new protocols; delegation with user/system context preserved in tokens and audit trails.
- [draft-liu-oauth-a2a-profile](https://datatracker.ietf.org/doc/draft-liu-oauth-a2a-profile/) — OAuth profile for agent-to-agent interactions (Liu, Huawei).
- [draft-messous-eat-ai](https://datatracker.ietf.org/doc/draft-messous-eat-ai/) — Entity Attestation Token profile for autonomous AI agents; claims for agent integrity, training provenance, runtime authorization (RATS-adjacent; referenced by the WIMSE applicability draft).
- [draft-mishra-oauth-agent-grants](https://datatracker.ietf.org/doc/draft-mishra-oauth-agent-grants/) (Mishra; DAAP) — Delegated Agent Authorization Protocol.
- [draft-morrison-identity-accord](https://datatracker.ietf.org/doc/draft-morrison-identity-accord/) (Morrison, Alter Meridian) — identity accord specification for agents.
- [draft-morrison-identity-attributed-commits](https://datatracker.ietf.org/doc/draft-morrison-identity-attributed-commits/) (Morrison) — identity-attributed commits for source version control.
- [draft-morrison-identity-pronouns](https://datatracker.ietf.org/doc/draft-morrison-identity-pronouns/) (Morrison) — reference-axis pronoun grammar for handle identity.
- [draft-mw-oauth-actor-chain](https://datatracker.ietf.org/doc/draft-mw-oauth-actor-chain/) and [draft-mcguinness-oauth-actor-profile](https://datatracker.ietf.org/doc/draft-mcguinness-oauth-actor-profile/) — OAuth delegation-chain claims (nested act per RFC 8693; acti/actc candidates) and an actor-profile vocabulary distinguishing AI Agent, Sub-Agent, Tool, Service, and Human; cited as building blocks by the audit architecture draft (Category 8).
- [draft-mw-spice-actor-chain](https://datatracker.ietf.org/doc/draft-mw-spice-actor-chain/), [draft-mw-spice-intent-chain](https://datatracker.ietf.org/doc/draft-mw-spice-intent-chain/), and [draft-mw-spice-inference-chain](https://datatracker.ietf.org/doc/draft-mw-spice-inference-chain/) (Krishnan et al.; March 2026) — actor chain = delegation provenance; intent chain = content provenance; inference chain = computational provenance. Merkle-rooted in the OAuth token, addressing STRIDE spoofing/tampering/repudiation/privilege-escalation threats.
- [draft-nandakumar-agent-sd-jwt](https://datatracker.ietf.org/doc/draft-nandakumar-agent-sd-jwt/) (Nandakumar; SD Agent) — selective disclosure for agent discovery and identity management.
- [draft-nennemann-wimse-ect](https://datatracker.ietf.org/doc/draft-nennemann-wimse-ect/) (Nennemann; ECT) — execution context tokens for distributed agentic workflows.
- [draft-ni-wimse-ai-agent-identity](https://datatracker.ietf.org/doc/draft-ni-wimse-ai-agent-identity/) (Huawei) — WIMSE applicability to agentic AI; independent agent identities/credentials distinct from users and devices; dual-identity model; includes explicit comparison to CHEQ.
- [draft-niyikiza-oauth-attenuating-agent-tokens](https://datatracker.ietf.org/doc/draft-niyikiza-oauth-attenuating-agent-tokens/) (Niyikiza) — attenuating authorization tokens for agentic delegation chains.
- [draft-oauth-ai-agents-on-behalf-of-user](https://datatracker.ietf.org/doc/draft-oauth-ai-agents-on-behalf-of-user/) — OAuth 2.0 on-behalf-of extension; authorization-endpoint agent identification plus a new grant type; resulting token records user, agent, and client identity for audit.
- [draft-pidlisnyi-aps](https://datatracker.ietf.org/doc/draft-pidlisnyi-aps/) (Pidlisnyi; APS) — Agent Passport System: cryptographic identity, faceted authority attenuation, and governance for AI agent systems.
- [draft-prakash-aip](https://datatracker.ietf.org/doc/draft-prakash-aip/) (Prakash; AIP) — Agent Identity Protocol: verifiable delegation for AI agent systems.
- [draft-ravikiran-clawdentity-protocol](https://datatracker.ietf.org/doc/draft-ravikiran-clawdentity-protocol/) (Ravikiran; Clawdentity) — cryptographic identity and trust protocol for AI agent communication.
- [draft-rosenberg-oauth-aauth](https://datatracker.ietf.org/doc/draft-rosenberg-oauth-aauth/) (AAuth) — OAuth 2.1 extension for agents obtaining tokens on behalf of users reached over PSTN/texting channels; anti-hallucination impersonation controls.
- [draft-shang-campus-agent-scope-down](https://datatracker.ietf.org/doc/draft-shang-campus-agent-scope-down/) — campus agent identification and scope-down access control.
- [draft-sharif-agent-identity-framework](https://datatracker.ietf.org/doc/draft-sharif-agent-identity-framework/) — five-layer model (identity, authorization, attestation, evidence, trust) separating concerns current standards conflate.
- [draft-sharif-openid-agent-identity](https://datatracker.ietf.org/doc/draft-sharif-openid-agent-identity/) — OpenID Connect agent identity claims for autonomous AI agents.
- [draft-singla-agent-identity-protocol](https://datatracker.ietf.org/doc/draft-singla-agent-identity-protocol/) (Singla, Independent) — did:aip DIDs with delegation chains.
- [draft-somoza-dmsc-atn-agent-trust-negotiation](https://datatracker.ietf.org/doc/draft-somoza-dmsc-atn-agent-trust-negotiation/) — Agent Trust Negotiation: Capability, Delegation, and Provenance Binding for AI Agents.
- [draft-song-oauth-ai-agent-collaborate-authz](https://datatracker.ietf.org/doc/draft-song-oauth-ai-agent-collaborate-authz/) — OAuth 2.0 extension for multi-AI agent collaboration.
- [draft-vandemeent-jis-identity](https://datatracker.ietf.org/doc/draft-vandemeent-jis-identity/) (van de Meent; JIS) — JTel Identity Standard: identity and trust establishment for autonomous agents.
- [draft-wahl-scim-agent-schema](https://datatracker.ietf.org/doc/draft-wahl-scim-agent-schema/) and [draft-wzdk-scim-agent-resource](https://datatracker.ietf.org/doc/draft-wzdk-scim-agent-resource/) (Wahl/Zollner/Dingle/Kazzouzi — Microsoft, Okta, Nextident; June 2026) — platform-neutral SCIM "AgenticIdentity" schema for representing and lifecycle-managing AI agent identities; the second active SCIM agent cluster alongside draft-abbey.
- [draft-williams-intent-token](https://datatracker.ietf.org/doc/draft-williams-intent-token/) (Williams) — Intent Token: cryptographic authorization primitive for autonomous agents.
- [draft-yakung-oauth-agent-attestation](https://datatracker.ietf.org/doc/draft-yakung-oauth-agent-attestation/) (Yakung; ACAP) — Agent Credential Attestation Protocol.

**External protocols & industry**
- NIST — NCCoE concept paper on AI agent identity/authorization and the AI Agent Standards Initiative, both centered on WIMSE/SPIFFE + OAuth.
- OpenID Foundation — "Identity Management for Agentic AI" whitepaper; SSF/CAEP for monitoring.
- SPIFFE/SVID (CNCF) — workload identity primitives adopted wholesale by the klrc approach.
- W3C DIDs — identity layer used by ANP (see Categories 2 and 9).

---

## 2. Agent Discovery, Naming & Directories

**IETF venues**
- agentproto / agent2agent discussions (discovery threads).
- DAWN BoF (WG-forming; 21 July 2026, IETF 126) + dawn@ietf.org (created April 2026; proponents include Farrel, King, Boucadair). Scope: discovery of "entities" generally — tasks, workloads (cf. WIMSE), endpoints (cf. CoRE), services, AI agents.
- DNSOP (dnsop@ietf.org) — venue for DNS-AID and DNS-based discovery mechanisms.

**IETF work items**
- [draft-aiendpoint-ai-discovery](https://datatracker.ietf.org/doc/draft-aiendpoint-ai-discovery/) — well-known, unauthenticated HTTP "AI Discovery Document" for service discovery and capability exposure.
- [draft-cui-ai-agent-discovery-invocation](https://datatracker.ietf.org/doc/draft-cui-ai-agent-discovery-invocation/) (AIDIP; Tsinghua University / Zhongguancun Lab) — unified agent metadata schema, two-mode discovery, semantic resolution, unified invocation API, security framework.
- [draft-cui-dns-native-agent-naming-resolution](https://datatracker.ietf.org/doc/draft-cui-dns-native-agent-naming-resolution/) (Cui) — DNS-Native AI Agent Naming and Resolution.
- [draft-gaikwad-woa](https://datatracker.ietf.org/doc/draft-gaikwad-woa/) (Web of Agents) — host-level agent manifest primitive designed to be consumed by higher-level discovery systems.
- [draft-hood-agtp-discovery](https://datatracker.ietf.org/doc/draft-hood-agtp-discovery/) and [draft-hood-agtp-presence](https://datatracker.ietf.org/doc/draft-hood-agtp-presence/) — AGTP substrate discovery (Agent Name Service, Agent Registry/Discovery components) and ambient substrate visibility; covers tool, resource, and API discovery in addition to agent discovery; positioned as complementary to DNS-AID for global substrate visibility rather than local-link rendezvous.
- [draft-jakab-dawn-agent-discovery-mdns](https://datatracker.ietf.org/doc/draft-jakab-dawn-agent-discovery-mdns/) (Jakab, Brockners, Cisco; June 2026) — local-link agent discovery using mDNS/DNS-SD zero-configuration machinery; complementary to global discovery mechanisms.
- [draft-kay-dawn-use-cases](https://datatracker.ietf.org/doc/draft-kay-dawn-use-cases/) — DAWN use cases for agents/workloads/named entities.
- [draft-king-dawn-requirements](https://datatracker.ietf.org/doc/draft-king-dawn-requirements/) — companion DAWN requirements draft.
- [draft-liu-agent-metadata-sync-protocol](https://datatracker.ietf.org/doc/draft-liu-agent-metadata-sync-protocol/) (Liu) — agent metadata synchronization protocol.
- [draft-morrison-mcp-dns-discovery](https://datatracker.ietf.org/doc/draft-morrison-mcp-dns-discovery/) (Morrison, Alter Meridian) — domain-scoped unicast DNS TXT records for MCP server discovery.
- [draft-mozley-aidiscovery](https://datatracker.ietf.org/doc/draft-mozley-aidiscovery/) — the AID problem statement (requirements: context-aware discovery, capability schemas, versioning/lifecycle, trust in the discovery process, organizational control over advertising agents). Distinct document from the dnsop mechanism draft.
- [draft-mozleywilliams-dnsop-dnsaid](https://datatracker.ietf.org/doc/draft-mozleywilliams-dnsop-dnsaid/) (Infoblox, Deutsche Telekom, Amazon) — DNS SVCB/HTTPS records for federated capability discovery; reference implementation exists.
- [draft-mp-agntcy-ads](https://datatracker.ietf.org/doc/draft-mp-agntcy-ads/) — Agntcy Agent Directory Service (Muscariello/Polic): Cisco / Linux Foundation Agntcy work entering the IETF stream; strategically significant as an industry directory architecture landing at IETF.
- [draft-narajala-courtney-ansv2](https://datatracker.ietf.org/doc/draft-narajala-courtney-ansv2/) — active successor to the expired original ANS draft; DNS-anchored identity providing stable cross-domain identifiers referenced by delegation chains (cited in AUDIT BoF charter discussion).
- [draft-narvaneni-agent-uri](https://datatracker.ietf.org/doc/draft-narvaneni-agent-uri/) (Narvaneni) — the agent:// Protocol: URI-based framework for interoperable agents.
- [draft-nemethi-aid-agent-identity-discovery](https://datatracker.ietf.org/doc/draft-nemethi-aid-agent-identity-discovery/) — DNS TXT records under _agent.<domain> for agent identity discovery.
- [draft-ni-agent-entity-discovery](https://datatracker.ietf.org/doc/draft-ni-agent-entity-discovery/) — DNS/DANE-style entity-level discovery with credential bindings; direct competitor to DNS-AID.
- [draft-pioli-agent-discovery](https://datatracker.ietf.org/doc/draft-pioli-agent-discovery/) (Pioli; ARDP) — Agent Registration and Discovery Protocol.
- [draft-rehfeld-apix-core](https://datatracker.ietf.org/doc/draft-rehfeld-apix-core/) (APIX; Rehfeld; -00 April 2026 through -04 May 2026) — HATEOAS-based, commercially sustainable machine-native service index for autonomous agents; governance model, three-dimensional trust model, APIX Manifest (APM), Index API; profile documents [draft-rehfeld-apix-services](https://datatracker.ietf.org/doc/draft-rehfeld-apix-services/) (web APIs/bots) and [draft-rehfeld-apix-iot](https://datatracker.ietf.org/doc/draft-rehfeld-apix-iot/) (IoT devices).
- [draft-seethiraju-dawn-dan-00](https://datatracker.ietf.org/doc/draft-seethiraju-dawn-dan/) — DNS-Based Agent Naming (DAN): AIDISCA and AIINDEX Resource Records for AI Agent Discovery
- [draft-song-anp-ans](https://datatracker.ietf.org/doc/draft-song-anp-ans/) (Agent Name System) and [draft-song-anp-adp](https://datatracker.ietf.org/doc/draft-song-anp-adp/) (Agent Description Protocol) — naming and description/discovery members of the ANP suite; agent:// URIs mapped to cryptographic peer identities with DHT/GossipSub dissemination.
- [draft-vandemeent-ains-discovery](https://datatracker.ietf.org/doc/draft-vandemeent-ains-discovery/) (van de Meent; AINS) — AInternet Name Service: agent discovery and trust resolution protocol.
- [draft-ye-problems-and-requirements-of-dns-for-ioa](https://datatracker.ietf.org/doc/draft-ye-problems-and-requirements-of-dns-for-ioa/) (Ye) — problem statement and requirements analysis of DNS for Internet of Agents.

**External protocols & industry**
- A2A Agent Cards, MCP server discovery conventions — de facto discovery metadata formats the IETF drafts must interoperate with or replace.
- Agntcy (Linux Foundation) directory service — the upstream of draft-mp-agntcy-ads.

---

## 3. Agent-to-Agent Communication (Core Protocols)

**IETF venues**
- agentproto BoF (WG-forming; 23 July 2026, IETF 126) + agent2agent@ietf.org (created April 2025; the primary hub list).
- CATALIST coordination (BoF held at IETF 125 — see Category 15).
- IETF 124 side meeting (Rosenberg/Jennings; ~125 in room, similar online) that produced the strawman charter.

**IETF work items**
- [draft-chang-agent-context-interaction](https://datatracker.ietf.org/doc/draft-chang-agent-context-interaction/) (Chang) — agent context interaction optimizations.
- [draft-cowles-aee](https://datatracker.ietf.org/doc/draft-cowles-aee/) (Cowles; AEE) — Agent Envelope Exchange: minimal JSON envelope format for inter-agent communication.
- [draft-cowles-aocl](https://datatracker.ietf.org/doc/draft-cowles-aocl/) (Cowles; AOCL) — Agent Orchestration Control Layers protocol.
- [draft-eckert-catalist-acip-framework](https://datatracker.ietf.org/doc/draft-eckert-catalist-acip-framework/) (ACIP) — Agent Communications Internet Protocol; framework for agent-aware networks.
- [draft-fu-nmop-agent-communication-framework](https://datatracker.ietf.org/doc/draft-fu-nmop-agent-communication-framework/) (Fu) — agent communication framework for Network AIOps.
- [draft-han-agent-comm-enterprise](https://datatracker.ietf.org/doc/draft-han-agent-comm-enterprise/) (Han) — considerations for AI agent communication and networking in enterprise.
- [draft-han-rtgwg-agent-gateway-intercomm-framework](https://datatracker.ietf.org/doc/draft-han-rtgwg-agent-gateway-intercomm-framework/) (Han) — agent gateway intercommunication framework.
- [draft-hood-independent-agtp](https://datatracker.ietf.org/doc/draft-hood-independent-agtp/), [draft-hood-agtp-api](https://datatracker.ietf.org/doc/draft-hood-agtp-api/), [draft-hood-agtp-session](https://datatracker.ietf.org/doc/draft-hood-agtp-session/), [draft-hood-agtp-communication](https://datatracker.ietf.org/doc/draft-hood-agtp-communication/) — AGTP core protocol suite: agent-to-agent transport substrate with RCNS (Runtime Contract Negotiation Substrate) for dynamic request-time agent↔server contract negotiation; agent-native intent methods (QUERY, DISCOVER, DELEGATE, EXECUTE, COLLABORATE, PURCHASE); session protocol with continuity across network interruptions; bilateral multi-modal communication (audio, video, structured data) on the substrate.
- [draft-hw-protocol-agent](https://datatracker.ietf.org/doc/draft-hw-protocol-agent/) — AI agent protocols for multi-modality.
- [draft-jeskey-anml](https://datatracker.ietf.org/doc/draft-jeskey-anml/) (Jeskey; ANML) — Agent Native Messaging Language; semantic vocabulary and message envelope for agent-to-agent messaging that composes with a substrate rather than defining its own transport.
- [draft-jesske-ai-enablement-interface](https://datatracker.ietf.org/doc/draft-jesske-ai-enablement-interface/) (Jesske, Kreipl; Deutsche Telekom) — AI enablement interface between telco communication platforms and AI service providers for live translation, call summarization, contextual assistance, fraud detection, and media enhancement during multimedia communication sessions.
- [draft-jurkovikj-httpapi-agentic-state](https://datatracker.ietf.org/doc/draft-jurkovikj-httpapi-agentic-state/) (Jurkovikj) — HTTP profile for synchronized resource state (agentic state transfer).
- [draft-mallick-muacp](https://datatracker.ietf.org/doc/draft-mallick-muacp/) (Mallick; uACP) — Micro Agent Communication Protocol.
- [draft-nederveld-adl](https://datatracker.ietf.org/doc/draft-nederveld-adl/) (Nederveld; ADL) — Agent Definition Language.
- [draft-rosenberg-aiproto-framework](https://datatracker.ietf.org/doc/draft-rosenberg-aiproto-framework/) (formerly draft-rosenberg-ai-protocols) — framework, use cases, and requirements for AI agent protocols; surveys MCP, A2A, Agntcy; the anchor document for agentproto.
- [draft-teodor-pilot-protocol](https://datatracker.ietf.org/doc/draft-teodor-pilot-protocol/) (Teodor) — Pilot Protocol: overlay network for autonomous agent communication.
- [draft-zyyhl-agent-networks-framework](https://datatracker.ietf.org/doc/draft-zyyhl-agent-networks-framework/) — framework for AI agent networks based on ANP, focused on operator-managed trust domains.

**External protocols & industry**
- A2A (Agent2Agent — Google, now Linux Foundation).
- AConP (Agent Connect Protocol — Cisco/Agntcy), AITP (NEAR), and other survey-documented entrants.
- ACP (Agent Communication Protocol).
- ANP (Agent Network Protocol — open-source community, Gaowei Chang et al.).
- MCP (Model Context Protocol — Anthropic / now under AAIF stewardship).

---

## 4. Agent-to-Tool / API Invocation

Agent↔tool is a distinct interaction plane from agent↔agent — the agentproto framing treats them separately — and has its own draft cluster.

**IETF venues**
- agentproto BoF / agent2agent list (tool-invocation building blocks are explicitly in scope of the charter discussion).

**IETF work items**
- [draft-cui-ai-agent-discovery-invocation](https://datatracker.ietf.org/doc/draft-cui-ai-agent-discovery-invocation/) (AIDIP) — unified invocation API also reaches into this category (see Category 2).
- [draft-hood-agtp-discovery](https://datatracker.ietf.org/doc/draft-hood-agtp-discovery/) and [draft-hood-agtp-api](https://datatracker.ietf.org/doc/draft-hood-agtp-api/) — AGTP substrate handles tool/resource/API discovery and invocation within the same substrate as agent-to-agent communication, using the agent-native intent methods (QUERY, EXECUTE, DELEGATE) rather than as a separate protocol.
- [draft-pelov-bounded-agent-capabilities](https://datatracker.ietf.org/doc/draft-pelov-bounded-agent-capabilities/) (Pelov; problem statement, posted July 2026) — bounded agent capabilities: problem statement for how agents can be granted narrow, verifiable capabilities for tool interaction rather than open-ended invocation.
- [draft-pelov-rich-architecture](https://datatracker.ietf.org/doc/draft-pelov-rich-architecture/) (Pelov; companion architecture, posted July 2026) — one possible implementation path for bounded agent capabilities.
- [draft-rosenberg-aiproto-a2t](https://datatracker.ietf.org/doc/draft-rosenberg-aiproto-a2t/) (A2T — Agent-to-Tool Protocol) — OpenAPI-style enumeration + invocation of third-party tools by enterprise agents; positioned against MCP's dedicated-server model (A2T APIs are "just APIs," consumable by non-LLM software too).
- [draft-rosenberg-aiproto-nact](https://datatracker.ietf.org/doc/draft-rosenberg-aiproto-nact/) (N-ACT — Normalized API for AI Agents Calling Tools) — companion normalized enumeration/invocation API.

**External protocols & industry**
- MCP — the incumbent tool-invocation protocol the IETF drafts define themselves against.
- OpenAPI/JSON-RPC ecosystems as substrate.

---

## 5. Semantic Intent, Verb Taxonomies & Action Description Layers

**IETF venues**
- No dedicated venue. Embedded in Communication (agentproto) and Collaboration (DMSC) discussions; potential dedicated semantic/interop threads on agent2agent.

**IETF work items**
- Agent description schemas (ADP in the ANP suite, AIDIP metadata, A2A-style capability cards mirrored in discovery drafts) — carry partial semantics but no cross-agent action taxonomy.
- [draft-hood-agtp-api](https://datatracker.ietf.org/doc/draft-hood-agtp-api/) — AGTP intent-based verb taxonomy with categories such as ACQUIRE, COMPUTE, TRANSACT, ORCHESTRATE, NOTIFY, QUERY; machine-readable intent expression and semantic interoperability at the wire; agent-native methods (QUERY, DISCOVER, DELEGATE, EXECUTE, COLLABORATE, PURCHASE) rather than repurposed HTTP verbs. Currently the only comprehensive cross-agent action taxonomy in or targeting the IETF stream.
- [draft-jeskey-anml](https://datatracker.ietf.org/doc/draft-jeskey-anml/) (Jeskey) — Agent Native Messaging Language semantic vocabulary; also fits Category 3.
- [draft-sz-iaip](https://datatracker.ietf.org/doc/draft-sz-iaip/) (Sz) — Intent-Aware Interconnection Protocol; intent-based routing semantics at the gateway boundary.
- [draft-verma-dmsc-nlip-notes](https://datatracker.ietf.org/doc/draft-verma-dmsc-nlip-notes/) — using natural language for universal coordination in multi-agent systems (NLIP notes; DMSC-tagged).
- [draft-yang-gateway-semantic-layer](https://datatracker.ietf.org/doc/draft-yang-gateway-semantic-layer/) (Yang) — semantic translation layer at the gateway boundary.
- [draft-zhang-dmsc-ioa-semantic-interaction](https://datatracker.ietf.org/doc/draft-zhang-dmsc-ioa-semantic-interaction/) — semantic interaction for the Internet of Agents (DMSC-tagged; presented in CATALIST context at IETF 125).

**External protocols & industry**
- Academic literature on semantic views of agent communication protocols is beginning to frame this gap.
- MCP, A2A, et al. — structured actions/tools but no formalized cross-agent verb taxonomy.

---

## 6. Multi-Agent Collaboration & Gateways

**IETF venues**
- agent2agent; CATALIST (DMSC presented in the CATALIST BoF at IETF 125).
- DMSC BoF (non-WG-forming; 22 July 2026, IETF 126) — AI Agent Gateway-mediated collaboration: capability exposure, request forwarding, coordination, synchronization, policy control, observability, secure communication. Proponents span Alibaba, Huawei, China Telecom, and others; a GitHub org (ietf-dmsc) tracks meeting materials.
- Mailing lists — dmsc@ietf.org exists (archive at mailarchive.ietf.org/arch/browse/dmsc/), and the IETF 126 BoF announcement additionally directs discussion to the DAWN list (dawn@ietf.org). Cite both.

**IETF work items**
- 6G agent use-case drafts (China Mobile et al.): [draft-sarischo-6gip-aiagent-requirements](https://datatracker.ietf.org/doc/draft-sarischo-6gip-aiagent-requirements/), [draft-stephan-ai-agent-6g](https://datatracker.ietf.org/doc/draft-stephan-ai-agent-6g/), and the "AI Network for Training, Inference, and Agentic Interactions" draft circulated on agent2agent.
- [draft-agent-gw](https://datatracker.ietf.org/doc/draft-agent-gw/) (Tsinghua) — agent communication gateway for semantic routing and working memory.
- [draft-cui-ai-agent-task](https://datatracker.ietf.org/doc/draft-cui-ai-agent-task/) (Cui) — task-oriented coordination requirements for AI agent protocols.
- [draft-cui-dmsc-agent-cdi](https://datatracker.ietf.org/doc/draft-cui-dmsc-agent-cdi/) — cross-domain interoperability framework for AI agent collaboration.
- [draft-dunbar-aap](https://datatracker.ietf.org/doc/draft-dunbar-aap/) (Dunbar; AAP) — Agent Access Protocol; agent access mechanisms.
- [draft-dunbar-agent-attachment](https://datatracker.ietf.org/doc/draft-dunbar-agent-attachment/) (Dunbar) — Agent Attachment Protocol.
- [draft-dunbar-dmsc-gw-scenarios-gap-analysis](https://datatracker.ietf.org/doc/draft-dunbar-dmsc-gw-scenarios-gap-analysis/) (Dunbar, Futurewei) — seven gateway properties and gap analysis; the anchoring analytical framework for the DMSC gateway proposal.
- [draft-hood-agtp-session](https://datatracker.ietf.org/doc/draft-hood-agtp-session/) — AGTP session substrate for multi-agent orchestration via sessions, transfer, intent routing; gateway-friendly design where the substrate carries the primitives (identity, authority, delegation, attribution) that gateways enforce.
- [draft-li-dmsc-inf-architecture](https://datatracker.ietf.org/doc/draft-li-dmsc-inf-architecture/) (China Telecom et al.) — DMSC infrastructure architecture.
- [draft-li-dmsc-macp](https://datatracker.ietf.org/doc/draft-li-dmsc-macp/) (Li/Liu/Du/Zhang — China Telecom, BUPT, Zhongguancun Lab, AsiaInfo; -02 Feb 2026) — Multi-agent Collaboration Protocol Suite; Agent Gateways handle registration, authentication, capability management while preserving peer-to-peer semantic interactions.
- [draft-li-macp](https://datatracker.ietf.org/doc/draft-li-macp/) (Li) — Multi-Agent Coordination Protocol.
- [draft-liu-dmsc-acps-arc](https://datatracker.ietf.org/doc/draft-liu-dmsc-acps-arc/) (BUPT) — agent collaboration protocols architecture for the Internet of Agents.
- [draft-liu-dmsc-gw-requirements](https://datatracker.ietf.org/doc/draft-liu-dmsc-gw-requirements/) (Huawei) — agent gateway requirements.
- [draft-mapmw-task-discovery](https://datatracker.ietf.org/doc/draft-mapmw-task-discovery/) — task discovery in agentic networks.
- [draft-morrison-agent-channel-fan-out](https://datatracker.ietf.org/doc/draft-morrison-agent-channel-fan-out/) (Morrison, Alter Meridian) — application-layer delivery frame for intra-principal and intra-organisation fan-out over a per-handle stream, addressed by identity scope rather than by domain host.
- [draft-song-dmsc-problem-statement](https://datatracker.ietf.org/doc/draft-song-dmsc-problem-statement/) (Song/Song/Zhang/Li/Zhao — Alibaba Cloud; March 2026) — problem statement and requirements for DMSC; gateway layer offloading secured communication, cross-domain connectivity, multi-tenant policy enforcement, and collaboration assistance.
- [draft-sun-zhang-iaip](https://datatracker.ietf.org/doc/draft-sun-zhang-iaip/) and [draft-sz-dmsc-iaip](https://datatracker.ietf.org/doc/draft-sz-dmsc-iaip/) — Intent-based Agent Interconnection Protocol at Agent Gateway.
- [draft-yang-dmsc-ioa-task-protocol](https://datatracker.ietf.org/doc/draft-yang-dmsc-ioa-task-protocol/) (Yang) — Internet of Agents Task Protocol for heterogeneous agent collaboration.
- [draft-zhang-directory-sync](https://datatracker.ietf.org/doc/draft-zhang-directory-sync/) (Zhang) — directory synchronization across gateways.
- Note: the DMSC proponents list 10+ related drafts in total (including draft-wang-hjs-judgment-event and others); the above are the core set.

**External protocols & industry**
- Enterprise "agent gateway" products (API-gateway vendors extending to agent mediation) — the deployment reality DMSC is profiling.
- ETSI ENI GR 056 — multi-agent frameworks for next-generation core networks (telecom-side counterpart).

---

## 7. Trust, Human-in-the-Loop, Oversight & Confirmation

**IETF venues**
- No dedicated venue yet; discussed within agentproto framing (confirming high-impact actions), OAuth (CIBA-based flows), WIMSE applicability comparisons, and the proposed AUDIT charter (step-up approvals/refusals as auditable records — see Category 8).

**IETF work items**

- [draft-cui-nmrg-llm-nm](https://datatracker.ietf.org/doc/draft-cui-nmrg-llm-nm/) (Cui) — framework for LLM Agent-assisted network management with human-in-the-loop.
- [draft-hood-independent-agtp](https://datatracker.ietf.org/doc/draft-hood-independent-agtp/) and [draft-hood-agtp-trust](https://datatracker.ietf.org/doc/draft-hood-agtp-trust/) — AGTP intervention and governance layers; confirmation and oversight supported natively at the substrate rather than as an overlay protocol.
- [draft-klrc-aiagent-auth](https://datatracker.ietf.org/doc/draft-klrc-aiagent-auth/) — CIBA-based human-in-the-loop mechanism inside the AIMS model; identity-bound audit trails cited as supporting EU AI Act Art. 14 human-oversight obligations.
- [draft-kuehlewind-audit-architecture](https://datatracker.ietf.org/doc/draft-kuehlewind-audit-architecture/) — models human-in-the-loop escalations (step-up approvals, refusals, missed escalations) as identifiable records bindable to a run's Interaction Record.
- [draft-morrison-binding-moment-envelope](https://datatracker.ietf.org/doc/draft-morrison-binding-moment-envelope/) (Morrison, Alter Meridian) — how consequential decisions are presented to a human principal at binding moments; dual-veto envelope with typed outcomes (commit, decline, amend, reject).
- [draft-morrison-org-alter-policy-provision](https://datatracker.ietf.org/doc/draft-morrison-org-alter-policy-provision/) (Morrison) — organizational policy provision for agents.
- [draft-ni-wimse-ai-agent-identity](https://datatracker.ietf.org/doc/draft-ni-wimse-ai-agent-identity/) — contains an explicit comparison with CHEQ (out-of-band verification vs. user double-confirmation of token requests).
- [draft-rosenberg-aiproto-cheq](https://datatracker.ietf.org/doc/draft-rosenberg-aiproto-cheq/) (CHEQ; earlier draft-rosenberg-cheq) — human confirmation of agent-proposed decisions before execution, plus privacy-preserving human entry of information needed for tool invocation without disclosure to the agent.
- [draft-somoza-dmsc-atn-agent-trust-negotiation](https://datatracker.ietf.org/doc/draft-somoza-dmsc-atn-agent-trust-negotiation/) — Agent Trust Negotiation: Capability, Delegation, and Provenance Binding for AI Agents.

**External protocols & industry**
- EU AI Act Articles 14/26 (human oversight, log retention) as regulatory drivers; OpenID CIBA as the underlying flow.

---

## 8. Audit & Accountability

**IETF venues**
- CATALIST.
- Proposed AUDIT BoF (Kühlewind/Birkholz) — draft + strawman charter circulated 19 May 2026 on agent2agent and cross-posted to the OAuth and WIMSE lists (charter at github.com/mirjak/draft-audit-architecture); proposed deliverables include an architecture, audit data models/semantics, token formats for audit information, and a deployment BCP. AUDIT was excluded from the five approved IETF 126 BoFs, so watch for IETF 127.
- SCITT WG (supply-chain transparency machinery reusable for agent action transparency; the verifiable-conversations format is designed for SCITT Transparency Services).

**IETF work items**
- [draft-birkholz-verifiable-agent-conversations](https://datatracker.ietf.org/doc/draft-birkholz-verifiable-agent-conversations/) (Birkholz et al.; Feb 2026) — CDDL data format (JSON and CBOR) for verifiable agent conversation records: session metadata, message exchanges, tool invocations, reasoning traces, system events; COSE-signed for native SCITT Transparency Service interoperability and RFC 9334 Evidence integration.
- [draft-bondar-wca](https://datatracker.ietf.org/doc/draft-bondar-wca/) (Bondar; WCA) — Warrant Certificate Authorities: auditable data provenance for AI-agent tool-call chains.
- [draft-cui-cdi](https://datatracker.ietf.org/doc/draft-cui-cdi/) (Cui) — Cross-Domain Interaction with delegation constraints.
- [draft-helixar-hdp-agentic-delegation](https://datatracker.ietf.org/doc/draft-helixar-hdp-agentic-delegation/) (Helixar; HDP) — Human Delegation Provenance Protocol: cryptographic chain-of-custody for agentic AI systems.
- [draft-hood-agtp-log](https://datatracker.ietf.org/doc/draft-hood-agtp-log/) and [draft-hood-agtp-identifiers](https://datatracker.ietf.org/doc/draft-hood-agtp-identifiers/) — AGTP logging: five identity-lifecycle events (genesis issued, revoked, suspended, reinstated, deprecated) as a governance-signed SCITT-aligned transparency log, plus per-action Attribution-Records that are agent-signed, hash-chained via previous_audit_id, and self-contained third-party-verifiable via AGTP-CERT; cryptographic accountability chain and participation history for evidentiary continuity across systems.
- [draft-kuehlewind-audit-architecture](https://datatracker.ietf.org/doc/draft-kuehlewind-audit-architecture/) (Kühlewind & Birkholz; -00 May 2026) — architecture for auditing AI agent delegation and interactions; Interaction/Action/Delegation Records; work items include a delegation-chain wire profile building on RFC 8693 nested act claims, draft-mw-oauth-actor-chain, and draft-mcguinness-oauth-actor-profile.
- [draft-liu-agent-operation-authorization](https://datatracker.ietf.org/doc/draft-liu-agent-operation-authorization/) (-02 March 2026) — two-phase framework for verifiable delegation of actions from human principals to autonomous agents with fine-grained operation authorization.
- [draft-mih-agent-bilateral-attestation](https://datatracker.ietf.org/doc/draft-mih-agent-bilateral-attestation/) (Mih, Action State) — bilateral attestation for cross-organization actions.
- [draft-mih-sato-agent-accountability-composition](https://datatracker.ietf.org/doc/draft-mih-sato-agent-accountability-composition/) (Mih, Sato) — CAN/WHO/WHAT/AUDIT accountability composition.
- [draft-mih-scitt-agent-action-capsule](https://datatracker.ietf.org/doc/draft-mih-scitt-agent-action-capsule/) (Mih) — SCITT-anchored action records.
- [draft-morrison-substrate-provenance-grammar](https://datatracker.ietf.org/doc/draft-morrison-substrate-provenance-grammar/) (Morrison, Alter Meridian) — annotation grammar for agent output provenance.
- [draft-mw-spice-actor-chain](https://datatracker.ietf.org/doc/draft-mw-spice-actor-chain/), [draft-mw-spice-intent-chain](https://datatracker.ietf.org/doc/draft-mw-spice-intent-chain/), and [draft-mw-spice-inference-chain](https://datatracker.ietf.org/doc/draft-mw-spice-inference-chain/) — delegation, content, and computational provenance chains.
- [draft-nelson-agent-delegation-receipts](https://datatracker.ietf.org/doc/draft-nelson-agent-delegation-receipts/) (Nelson, Authproof) — cryptographic delegation receipt protocol with model state attestation.
- [draft-rampalli-pedigree](https://datatracker.ietf.org/doc/draft-rampalli-pedigree/) (Rampalli; PEDIGREE) — delegation chain semantics with pre-authorization model.
- [draft-sato-soos-aep](https://datatracker.ietf.org/doc/draft-sato-soos-aep/) (Sato, MyAuberge; SOOS Agent Execution Protocol) — SENSE/PLAN/ACT/OBSERVE flow with governance enforcement component boundary.
- [draft-sato-soos-cap](https://datatracker.ietf.org/doc/draft-sato-soos-cap/) (Sato; SOOS Constitutional AI Protocol) — enforcement architecture using Cedar policy evaluation with three-tier prohibitions.
- [draft-sato-soos-cap-rrs](https://datatracker.ietf.org/doc/draft-sato-soos-cap-rrs/) (Sato; SOOS Regulation Record Specification) — machine-compilable representations of legal compliance obligations.
- [draft-sato-soos-dam](https://datatracker.ietf.org/doc/draft-sato-soos-dam/) (Sato; SOOS Data Artifact Management).
- [draft-sato-soos-faip](https://datatracker.ietf.org/doc/draft-sato-soos-faip/) (Sato; SOOS Federated Agent Intelligence Protocol).
- [draft-sato-soos-gar](https://datatracker.ietf.org/doc/draft-sato-soos-gar/) (Sato; SOOS Governance Audit Record).
- [draft-sato-soos-hem](https://datatracker.ietf.org/doc/draft-sato-soos-hem/) (Sato; SOOS Human Escalation Mechanism).
- [draft-sato-soos-idp](https://datatracker.ietf.org/doc/draft-sato-soos-idp/) (Sato; SOOS Intent Declaration Primitive).
- [draft-sato-soos-mjwt](https://datatracker.ietf.org/doc/draft-sato-soos-mjwt/) (Sato; SOOS Mandate JWT).
- [draft-sato-soos-pt](https://datatracker.ietf.org/doc/draft-sato-soos-pt/) (Sato; SOOS Progressive Trust).
- [draft-sato-soos-sov](https://datatracker.ietf.org/doc/draft-sato-soos-sov/) (Sato; SOOS Sovereign Object).
- [draft-sharif-agent-audit-trail](https://datatracker.ietf.org/doc/draft-sharif-agent-audit-trail/) (Sharif) — Agent Audit Trail: standard logging format for autonomous AI systems.
- [draft-sharif-attp-agent-trust-transport](https://datatracker.ietf.org/doc/draft-sharif-attp-agent-trust-transport/) (Sharif; ATTP) — protocol-agnostic framework for trust scoring, cryptographic identity, action-limit enforcement, compliance gating, and tamper-evident audit for autonomous AI agents.
- [draft-sharif-audit-trail](https://datatracker.ietf.org/doc/draft-sharif-audit-trail/) (Sharif) — audit trail patterns.
- [draft-stone-atep](https://datatracker.ietf.org/doc/draft-stone-atep/) (Stone; ATEP) — Agent Trust and Execution Passport.
- [draft-wang-hjs-accountability](https://datatracker.ietf.org/doc/draft-wang-hjs-accountability/) (Wang; HJS) — Accountability Receipts for AI Agents: minimal JEP profile for exportable AI receipts.
- [draft-wang-jac](https://datatracker.ietf.org/doc/draft-wang-jac/) (Wang; JAC) — Declared Dependency Chains for Agent Receipts.
- Identity-bound audit-trail requirements also appear inside draft-klrc-aiagent-auth and draft-oauth-ai-agents-on-behalf-of-user (token records naming user + agent + client).

**External protocols & industry**
- ACTA (Agent Communication Trust Architecture) receipts and AgentROA audit patterns.
- EMILIA Protocol (Schrock) — verifiable receipts and boundary-derived claims.
- OpenID SSF/CAEP for continuous monitoring signals.
- Regulatory drivers: EU AI Act logging obligations; Colorado AI Act "reasonable care" standard.

---

## 9. Agent Transport & Connectivity

This category is defined by architectural role: transport substrate specifications intended to carry agent traffic, distinct from application-layer protocols that ride on existing transports (HTTP, QUIC). Any future substrate proposal would land here regardless of author.

**IETF venues**
- CATALIST coordination; enterprise@ietf.org (IoA@Enterprise); aidc@ietf.org (Data Center Networking for AI Clusters); mcast4ai@ietf.org (Multicast for AI); DNSOP (DNS-AID as connectivity bootstrap).
- PTTH BoF (IETF 123 and returning at IETF 126 with a proposed charter) — HTTP client/server role reversal; relevant because reverse connectivity to agents behind restrictive network positions is a recurring agent deployment problem.

**IETF work items**
- [draft-hood-independent-agtp](https://datatracker.ietf.org/doc/draft-hood-independent-agtp/) — AGTP core protocol: dedicated application-layer transport substrate for agents on IANA-registered port 4480; identity, sessions, semantic methods, authority scope, delegation chains, and attribution built into the substrate rather than reconstructed at each application layer. Bindings and composition profiles that carry agent protocols on this substrate or on existing transports are catalogued in Category 17.

**External protocols & industry**
- QUIC/HTTP3, WebTransport, WebSockets, and SLIM (see Category 14) as the substrates that agent application protocols currently ride; MCP/A2A transport bindings. These are transport work at IETF that agent traffic uses, without themselves being agent-specific substrate.

---

## 10. Security & Threat Modeling for Agent Protocols

No IETF group currently owns cross-cutting agent-protocol security: prompt injection across agent boundaries, confused-deputy problems in delegation chains, tool-poisoning, and inter-agent trust escalation. Flagging the vacancy is itself useful analysis for BoF chartering discussions.

**IETF venues**
- AI Agent Security side meeting — IETF 125 (see Category 1); the most focused security venue to date.
- IETF 123 Hackathon: "Agent Protocol Security" project — the main running-code security effort so far.
- No single owner; fragments live in WEBBOTAUTH (impersonation), WIMSE/OAuth drafts (delegation security), and SAAG hallway discussion.

**IETF work items**
- [draft-baysal-asimov-safety-architecture](https://datatracker.ietf.org/doc/draft-baysal-asimov-safety-architecture/) (Baysal) — Asimov Safety Architecture for autonomous AI agents.
- [draft-berlinai-vera](https://datatracker.ietf.org/doc/draft-berlinai-vera/) (BerlinAI; VERA) — Verifiable Enforcement for Runtime Agents.
- [draft-feng-nmrg-ain-architecture](https://datatracker.ietf.org/doc/draft-feng-nmrg-ain-architecture/) — names the coordination-plane threat surface (capability-claim spoofing, routing-state poisoning, semantic namespace abuse/IC-OID hijacking, intent privacy leakage) with detailed threat modeling deferred as a research problem.
- [draft-hood-agtp-trust](https://datatracker.ietf.org/doc/draft-hood-agtp-trust/) — AGTP trust scores, package integrity verification, and governance binding as security-relevant primitives; three Tier 1 verification paths (DNS-anchored, log-anchored, hybrid) declared interchangeable for protocol purposes; a dedicated cross-cutting threat-model document remains a gap in the space.
- [draft-messous-eat-ai](https://datatracker.ietf.org/doc/draft-messous-eat-ai/) — attestation as a security primitive; overlaps from Category 1.
- [draft-mw-spice-intent-chain](https://datatracker.ietf.org/doc/draft-mw-spice-intent-chain/) — explicitly maps its chains to the STRIDE threat model (spoofing, tampering, repudiation, elevation of privilege) for agent workflows.
- [draft-ni-a2a-ai-agent-security-requirements](https://datatracker.ietf.org/doc/draft-ni-a2a-ai-agent-security-requirements/) — security requirements for A2A-style agent interactions (Huawei).
- [draft-stone-aivs](https://datatracker.ietf.org/doc/draft-stone-aivs/) (Stone; AIVS) — Agentic Integrity Verification Standard.
- [draft-stone-swarmscore-v1](https://datatracker.ietf.org/doc/draft-stone-swarmscore-v1/) (Stone) — SwarmScore V1: volume-scaled agent reputation protocol.
- [draft-stone-swarmscore-v2-canary](https://datatracker.ietf.org/doc/draft-stone-swarmscore-v2-canary/) (Stone) — SwarmScore V2 Canary: safety-aware agent reputation protocol.
- [draft-westerbeck-reason-protocol](https://datatracker.ietf.org/doc/draft-westerbeck-reason-protocol/) (Westerbeck) — reason:// URI scheme and registry protocol for validated agent reasoning artifacts.
- Security Considerations sections of the drafts throughout this document (uneven; at least one prominent identity draft shipped with a placeholder Security Considerations section in -00).

**External protocols & industry**
- OWASP Top 10 for Agentic Applications (2026).
- Vendor threat-modeling work around MCP tool poisoning and injection.

---

## 11. Agentic Commerce (Transactions, Merchant Identity, Payments)

**IETF venues**
- No dedicated venue or BoF. Emerging discussion threads in agent2agent / CATALIST; potential overlap with existing payments-adjacent work.

**IETF work items**
- Commerce-adjacent primitives inside [draft-rehfeld-apix-core](https://datatracker.ietf.org/doc/draft-rehfeld-apix-core/): commercial onboarding, sanctions compliance, and a supply-side funding model for agent-consumable services.
- [draft-hood-agtp-commerce](https://datatracker.ietf.org/doc/draft-hood-agtp-commerce/), [draft-hood-agtp-merchant-identity](https://datatracker.ietf.org/doc/draft-hood-agtp-merchant-identity/), [draft-hood-agtp-lei](https://datatracker.ietf.org/doc/draft-hood-agtp-lei/) — AGTP commerce substrate: merchant identity primitives, Legal Entity Identifier binding, transaction support via the PURCHASE method and TRANSACT verb category; economic agent flows on the substrate rather than reconstructed at application layer.
- [draft-sharif-agent-payment-trust](https://datatracker.ietf.org/doc/draft-sharif-agent-payment-trust/) (Sharif) — trust scoring and identity verification for autonomous AI agent payment transactions.
- [draft-stone-vcap](https://datatracker.ietf.org/doc/draft-stone-vcap/) (Stone; VCAP) — Verified Commerce for Agent Protocols.
- [draft-stone-vcap-ap2-binding](https://datatracker.ietf.org/doc/draft-stone-vcap-ap2-binding/) (Stone) — VCAP-AP2 Binding: verified commerce settlement for the Agent Payments Protocol.
- WEBBOTAUTH is the closest chartered dependency (agent verification as the front door to commerce flows).

**External protocols & industry**
- AAIF — the Linux Foundation Agentic AI Infrastructure Foundation (founding members include AWS, Anthropic, Block, Bloomberg, Cloudflare, Google, Microsoft, OpenAI).
- ANP community roadmap includes an AP2 agent payment protocol at its application layer; AP2 is also referenced in draft-klrc-aiagent-auth.
- Visa TAP and Mastercard Agent Pay — both adopting Web Bot Auth as their agent-verification foundation. The center of gravity for agentic commerce currently sits outside the IETF; that external pull is the defining dynamic of this category.

---

## 12. AI Content Preferences (Opt-outs, Training Data Control)

**IETF venues**
- AIPREF WG (chartered January 2025; first met at IETF 122 Bangkok).
- Mailing list correction: the active WG list is aipref@ietf.org; ai-control@ietf.org was the pre-WG / workshop-era list and should be treated as historical.
- Origin: IAB AI-CONTROL workshop (September 2024) — the provenance of AIPREF and useful history for why the WG exists and moved on a compressed timeline.

**IETF work items**
- [draft-ietf-aipref-attach](https://datatracker.ietf.org/doc/draft-ietf-aipref-attach/) — attachment via robots.txt extensions, HTTP headers, Well-Known URIs.
- [draft-ietf-aipref-vocab](https://datatracker.ietf.org/doc/draft-ietf-aipref-vocab/) — vocabulary for AI-usage preferences.

**External protocols & industry**
- Liaisons/adjacent: IPTC, PLUS Coalition, WHATWG/W3C, Common Crawl, publisher coalitions.

---

## 13. Bot/Crawler Authentication

**IETF venues**
- WEBBOTAUTH WG (chartered early 2026 following the IETF 123 BoF; chairs Schinazi/Shekh-Yusef) + web-bot-auth@ietf.org. Charter liaises with AIPREF, HTTPBIS, OAUTH, TLS, WIMSE. Scope: authenticates the agent/bot to sites intended for humans; end-user auth and agent-to-agent/API auth are explicitly out of scope (those live in Categories 1 and 3).

**IETF work items**
- [draft-meunier-web-bot-auth-architecture](https://datatracker.ietf.org/doc/draft-meunier-web-bot-auth-architecture/) — core architecture (HTTP Message Signatures / RFC 9421, Signature-Agent header, key directory).
- [draft-meunier-webbotauth-registry](https://datatracker.ietf.org/doc/draft-meunier-webbotauth-registry/) — registry and signature agent card.
- WG milestones: standards-track auth + bot-information specs to IESG April 2026; key-management/deployment BCP August 2026.

**External protocols & industry**
- Adopted as the verification foundation for Visa TAP / Mastercard Agent Pay (see Category 11).
- Cloudflare (originator), Google (testing on its AI-browsing agent), Amazon, Akamai, OpenAI, Vercel, Shopify, Stytch implementations.

---

## 14. AI for Network Management, Operations & Agent Networking

**IETF venues**
- IRTF NMRG + ainetops@ietf.org; OPS-area discussions.
- IRTF T2TRG — agentic operation of IoT/constrained environments; the main running-code agentic work in the IRTF.

**IETF work items**
- AINetOps draft ("AI for Network Operations") circulated on agent2agent.
- ANP network requirements (Kehan Yao / China Mobile); IPv6-for-IoA capability-requirements discussions.
- [draft-akhavain-moussa-ai-network](https://datatracker.ietf.org/doc/draft-akhavain-moussa-ai-network/) — AI Network for Training, Inference, and Agentic Interactions.
- [draft-an-nmrg-i2icf-cits](https://datatracker.ietf.org/doc/draft-an-nmrg-i2icf-cits/) — agentic interface to in-network computing functions for software-defined vehicles in cooperative intelligent transportation systems.
- [draft-bernardos-nmrg-agentic-network-optimization](https://datatracker.ietf.org/doc/draft-bernardos-nmrg-agentic-network-optimization/) — solutions for enabling agentic sensing with network optimization.
- [draft-chen-nmrg-multi-provider-inference-api](https://datatracker.ietf.org/doc/draft-chen-nmrg-multi-provider-inference-api/) — multi-provider extensions for agentic AI inference APIs.
- [draft-chuyi-nmrg-agentic-network-inference](https://datatracker.ietf.org/doc/draft-chuyi-nmrg-agentic-network-inference/) and [draft-chuyi-nmrg-ai-agent-network](https://datatracker.ietf.org/doc/draft-chuyi-nmrg-ai-agent-network/) (Guo, China Mobile; March 2026) — agentic network architecture/protocol for agent interconnection and multi-level inference (households, industrial pipelines, drone groups, vehicle networking).
- [draft-cui-nmrg-llm-benchmark](https://datatracker.ietf.org/doc/draft-cui-nmrg-llm-benchmark/) (Cui) — framework to evaluate LLM agents for network configuration.
- [draft-du-catalist-routing-considerations](https://datatracker.ietf.org/doc/draft-du-catalist-routing-considerations/) — routing considerations in agentic networks.
- [draft-feng-nmrg-ain-architecture](https://datatracker.ietf.org/doc/draft-feng-nmrg-ain-architecture/) (Chong Feng, Ruijie Networks; -00 April 2026, active) — Agentic Intent Network (AIN), a routing-based architecture for AI agent coordination at scale. Applies IP structural logic to inter-agent coordination: Intent Datagrams (~IP datagrams), Intent Routers, Capability Routing Tables (~forwarding tables), IC-OID semantic identifiers as routing keys, Agent Domains (~ASes); explicitly positions MCP/A2A/AutoGen/LangGraph as lacking discovery/routing substrates, and frames "networked infrastructure for AI-agent coordination" as a third NMRG research dimension alongside draft-irtf-nmrg-ai-challenges and draft-irtf-nmrg-ai-deploy. Cross-cuts Categories 2 (capability discovery), 5 (Semantic Substrate / IC-OID taxonomy governance), and 10 (capability-claim spoofing, routing-state poisoning, intent privacy).
- [draft-hong-nmrg-agenticai-ps](https://datatracker.ietf.org/doc/draft-hong-nmrg-agenticai-ps/) — problem statement for agentic AI in network management (NMRG session at IETF 124 flagged the lack of standardized A2A protocols as the integration bottleneck).
- [draft-irtf-nmrg-ai-challenges](https://datatracker.ietf.org/doc/draft-irtf-nmrg-ai-challenges/) and [draft-irtf-nmrg-ai-deploy](https://datatracker.ietf.org/doc/draft-irtf-nmrg-ai-deploy/) — the adopted NMRG baseline documents that agentic drafts position themselves against.
- [draft-jadoon-nmrg-agentic-ai-autonomous-networks](https://datatracker.ietf.org/doc/draft-jadoon-nmrg-agentic-ai-autonomous-networks/) (Jadoon, Robitzsch, Bernardos) — architectural principles for "agentic augmentation" of the IP suite; deterministic protocol layering intact while AI agents become first-class entities at each layer, coordinated by agent controllers.
- [draft-jimenez-t2trg-iot-agent](https://datatracker.ietf.org/doc/draft-jimenez-t2trg-iot-agent/) — agentic AI operation of constrained RESTful (CoAP) environments; demonstrated at IETF 123 T2TRG session and the IETF 124 hackathon.
- [draft-mpsb-agntcy-messaging](https://datatracker.ietf.org/doc/draft-mpsb-agntcy-messaging/) — overview of messaging systems and their applicability to Agentic AI.
- [draft-song-anp-aip](https://datatracker.ietf.org/doc/draft-song-anp-aip/) (Agent Internet Protocol) and [draft-song-anp-aitp](https://datatracker.ietf.org/doc/draft-song-anp-aitp/) (Agent Internet Transport Protocol).
- [draft-wmz-nmrg-agent-ndt-arch](https://datatracker.ietf.org/doc/draft-wmz-nmrg-agent-ndt-arch/) — network digital twin and agentic AI based architecture for AI-driven network operations.
- [draft-yc-ipv6-for-ioa](https://datatracker.ietf.org/doc/draft-yc-ipv6-for-ioa/) — capabilities and future requirements of IPv6 for the Internet of Agents.
- [draft-zhang-cats-token-aware-ts](https://datatracker.ietf.org/doc/draft-zhang-cats-token-aware-ts/) — token-aware traffic steering solution for agent service.
- [draft-zhang-rtgwg-agent-policy-aware-network](https://datatracker.ietf.org/doc/draft-zhang-rtgwg-agent-policy-aware-network/) — use cases and requirements for AI agent policy-aware network.
- [draft-zhao-ccamp-actn-optical-network-agent](https://datatracker.ietf.org/doc/draft-zhao-ccamp-actn-optical-network-agent/) — integration of Network Management Agent into ACTN-based optical network.
- [draft-zhao-nmop-network-management-agent](https://datatracker.ietf.org/doc/draft-zhao-nmop-network-management-agent/) — AI-based Network Management Agent (NMA): concepts and architecture.
- [draft-zhao-nmrg-ai-agent-for-ndt](https://datatracker.ietf.org/doc/draft-zhao-nmrg-ai-agent-for-ndt/) — AI agent architecture for Network Digital Twin.

**External protocols & industry**
- ETSI ENI multi-agent studies; vendor AIOps platforms.

---

## 15. Coordination, Problem Framing & Architectural Principles

Documents in this category inform how the community thinks about agent standards without themselves being protocol specifications. Includes cross-effort coordination, problem-space analyses, dimensional frameworks, and architectural principles that shape (or should shape) other work in the landscape.

**IETF venues**
- agentproto / DAWN / DMSC BoF preparation threads; IETF-OPS-AD / AINETOPS GitHub tracking.
- CATALIST — where DMSC and related agent efforts presented; associated with agent2agent.

**IETF work items**
- [draft-agentic-ai-usecases-requirements](https://datatracker.ietf.org/doc/draft-agentic-ai-usecases-requirements/) (Reddy, Sarker, Yao; Nokia/China Mobile) — use cases and protocol requirements for AGENTPROTO.
- [draft-farrel-catalist-ai4all](https://datatracker.ietf.org/doc/draft-farrel-catalist-ai4all/) — emerging applications of AI in IETF specifications.
- [draft-foroughi-agent-protocol-dimensions](https://datatracker.ietf.org/doc/draft-foroughi-agent-protocol-dimensions/) (Foroughi, Nokia; July 2026) — dimensional model for characterizing agent protocols and their substrates; analytical instrument routing each concern to its proper layer (a dimensional choice at the agent protocol layer, a substrate-inherited property, or broader-scope work). Reference framework for community discussions.
- [draft-morrison-substrate-observation](https://datatracker.ietf.org/doc/draft-morrison-substrate-observation/) (Morrison, Alter Meridian) — architectural principle that concurrent heterogeneous sessions should observe a shared substrate rather than negotiate an envelope wire format; informs how substrate-layer and application-layer work should compose without itself being a transport specification.
- [draft-rosenberg-aiproto-framework](https://datatracker.ietf.org/doc/draft-rosenberg-aiproto-framework/) + strawman charter (feeding agentproto) — see Category 3.
- [draft-scrm-aiproto-usecases](https://datatracker.ietf.org/doc/draft-scrm-aiproto-usecases/) — agentic AI use cases (SCRM contributors).
- [draft-teodor-pilot-problem-statement](https://datatracker.ietf.org/doc/draft-teodor-pilot-problem-statement/) (Teodor) — problem statement: network-layer infrastructure for autonomous agent communication.
- [draft-yao-catalist-problem-space-analysis](https://datatracker.ietf.org/doc/draft-yao-catalist-problem-space-analysis/) (Kehan Yao / Zaheduzzaman Sarker) — analysis of the IETF-relevant problem space, candidate WG areas, and open-source coordination; frequently referenced.

**External protocols & industry**
- AAIF (Linux Foundation) as the open-source coordination counterpart; W3C AI-adjacent community groups.

---

## 16. Agent Packaging, Manifests, Integrity Verification & Unified Lifecycle Management

**IETF venues**
- No dedicated venue. Discussions surface in agent2agent / CATALIST / discovery contexts; potential overlap with SUIT (software update manifests) and SCITT (artifact transparency) machinery, or a future agentproto work item. SCIM agent lifecycle drafts (Category 1) cover the provisioning slice.

**IETF work items**
- [draft-hood-independent-agtp](https://datatracker.ietf.org/doc/draft-hood-independent-agtp/) family (packaging/lifecycle profiles under development) — AGTP open agent package format (.agent / .nomo): Merkle-tree integrity, manifest verification, unified lifecycle platform with cryptographic accountability chain, trust scores bound to packages, marketplace orchestration/discovery support. The only agent-native packaging/lifecycle work targeting the IETF stream (most other drafts are protocol-focused).
- Closest reusable primitives: SUIT manifests, SCITT receipts, EAT attestation (Category 1); none agent-specific.
- Discovery-side manifest fragments: [draft-gaikwad-woa](https://datatracker.ietf.org/doc/draft-gaikwad-woa/) host manifests; [draft-narvaneni-agent-uri](https://datatracker.ietf.org/doc/draft-narvaneni-agent-uri/) URI-based framework; ADP agent descriptions (ANP suite); Agntcy directory records; APIX Manifests (APM).

**External protocols & industry**
- OCI images / npm-style registries as the de facto packaging substrate for agent frameworks; no integrity-verified agent-native package standard exists externally either.

---

## 17. Agent Bindings & Composition

This category captures work that binds agent protocols to specific underlying transports, or that specifies composition profiles for combining agent-layer semantics with substrate-layer or transport-layer implementations. These drafts pick a lane (a particular transport, an existing protocol to compose beneath, or a specific integration pattern) rather than defining new substrate primitives.

**IETF venues**
- agentproto / DMSC BoF preparation threads; MoQ (Media over QUIC) coordination.

**IETF work items**
- [draft-hood-agtp-bindings](https://datatracker.ietf.org/doc/draft-hood-agtp-bindings/) — AGTP substrate profiling for composition with existing transports (HTTP, QUIC) and existing protocols.
- [draft-hood-agtp-composition](https://datatracker.ietf.org/doc/draft-hood-agtp-composition/) — AGTP composition profiles: agent group messaging protocols, external identity providers, and HTTP gateways.
- [draft-jennings-ai-mcp-over-moq](https://datatracker.ietf.org/doc/draft-jennings-ai-mcp-over-moq/) (Jennings) — Model Context Protocol and Agent Skills over Media over QUIC Transport.
- [draft-liu-agent-protocol-over-moq](https://datatracker.ietf.org/doc/draft-liu-agent-protocol-over-moq/) (Liu) — Agent Protocol over MoQ.
- [draft-nandakumar-ai-agent-moq-transport](https://datatracker.ietf.org/doc/draft-nandakumar-ai-agent-moq-transport/) (Nandakumar) — MOQ transport for agent protocols.
- [draft-wang-lisp-ai-agent](https://datatracker.ietf.org/doc/draft-wang-lisp-ai-agent/) (Wang) — using LISP as a network substrate for AI agent communication.

**External protocols & industry**
- MoQ (Media over QUIC) as the emerging transport being bound to; MCP transport bindings from Anthropic; A2A transport bindings from AGNTCY.

---

## Additional Cross-Cutting or Minor Items

- **Containerless Wasm / Virtual Actor Runtimes for Instant Scale** — runtime/execution rather than standards (zero cold starts, 10M+ agent targets), but informs Transport (Category 9) and Packaging (Category 16) discussions.
- **IRTF / Research Aspects** — beyond NMRG and T2TRG, general research interest in agentic systems; less standards-track.
- **Privacy-Preserving Interactions & Data Minimization for Agents** — cross-cutting (Identity, Communication, Commerce, Governance). Limited dedicated IETF focus; CHEQ's disclosure-avoiding credential entry is the closest concrete mechanism; draft-birkholz-verifiable-agent-conversations documents privacy risks of reasoning traces and metadata in audit records. Could tie into existing privacy work or a future agent-specific effort.
- **RCNS (Runtime Contract Negotiation Substrate)** — dynamic request-time agent↔server contract negotiation (part of the AGTP work items in Category 3); ANP's meta-protocol negotiation layer (ANP-06, still draft in that community) is the nearest external analogue.
- **OT/ICS Agent Authority** — physical-world/industrial control agent authority. [draft-morrison-ot-command-authority](https://datatracker.ietf.org/doc/draft-morrison-ot-command-authority/) (Morrison, Alter Meridian) addresses this space; the only dedicated draft for OT/ICS agent command authority.
- **Additional Morrison drafts (Alter Meridian)** covering adjacent architectural principles: [draft-morrison-live-reference-resolution](https://datatracker.ietf.org/doc/draft-morrison-live-reference-resolution/), [draft-morrison-compute-location-gate](https://datatracker.ietf.org/doc/draft-morrison-compute-location-gate/), [draft-morrison-consent-settlement](https://datatracker.ietf.org/doc/draft-morrison-consent-settlement/).
- **Running code inventory** — IETF 123 hackathon (Agent Protocol Security), IETF 124 hackathon (T2TRG IoT agent), DNS-AID reference implementation, Web Bot Auth production deployments (Cloudflare/Google/Stytch), AGTP MCP-over-AGTP running implementation (github.com/nomoticai/agtp, mcp.nomotic.ai:4480). Worth maintaining as its own list: BoF chartering arguments increasingly turn on demonstrated interop.

