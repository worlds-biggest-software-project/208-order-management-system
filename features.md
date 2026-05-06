# Order Management System — Feature & Functionality Survey

> Candidate #208 · Researched: 2026-05-03

## Solutions Analysed

| Tool | Type | Licence / Model | URL |
|------|------|-----------------|-----|
| Manhattan Active OMS | Enterprise SaaS | Commercial (custom quote) | https://www.manh.com/solutions/omnichannel-software-solutions/order-management-system |
| IBM Sterling Order Management | Enterprise SaaS/On-prem | Commercial (custom quote) | https://www.ibm.com/products/order-management |
| Fluent Commerce | Cloud-native SaaS | Commercial (custom quote) | https://fluentcommerce.com/ |
| Salesforce Order Management | SaaS | Commercial (custom quote) | https://www.salesforce.com/commerce/ |
| Kibo Commerce | Composable SaaS | Commercial (custom quote) | https://kibocommerce.com/ |
| Fabric OMS | Headless SaaS | Commercial (custom quote) | https://fabric.inc/products/order-management |
| Pipe17 | Mid-market SaaS | Commercial (subscription) | https://pipe17.com/ |
| Linnworks | SMB SaaS | Commercial (from $499/month) | https://www.linnworks.com/ |
| KBRW | AI-native SaaS | Commercial (custom quote) | https://kbrw.com/ |

---

## Feature Analysis by Solution

### Manhattan Active OMS

**Core features**
- Real-time global inventory visibility across all fulfilment nodes (DCs, stores, 3PLs)
- Intelligent Available to Commerce (ATC) — controls which inventory is exposed to which channels
- Dynamic fulfilment optimisation routing orders to best source based on cost, speed, and inventory
- Omnichannel fulfilment modes: ship-from-store, BOPIS, BOPAC, ship-to-store, curbside pickup
- Carrier and shipping method management with rate shopping
- Returns and reverse logistics orchestration across all channels
- Customer Service representative workbench with full order lifecycle visibility
- Post-purchase personalised notifications and communication

**Differentiating features**
- 2026 agentic AI agents: Store Associate Agent, Contact Center Agent, OMS Configuration Agent
- Fulfilment Optimisation engine with real-time cost/speed/carbon trade-off scoring
- Manhattan Active platform — microservices on Kubernetes with 250+ Java/Spring services
- Continuous upgrades without implementation downtime (cloud-native, evergreen SaaS)
- Recognised as Nucleus Research 2026 OMS Technology Value Matrix Leader

**UX patterns**
- Role-based workbenches (store associate, contact centre, warehouse manager)
- Configurable rule sets for routing logic via UI (no-code for business users)
- Dashboards for real-time order exception management
- Mobile-optimised store fulfilment apps

**Integration points**
- REST APIs with OAuth 2.0 authentication (developer.manh.com)
- Pre-built connectors to major e-commerce platforms, ERPs, and WMS solutions
- Manhattan Active Platform SDK for custom extensions
- Webhooks for order event streaming

**Known gaps**
- Enterprise-only pricing excludes mid-market and SMB
- High implementation complexity and time-to-value
- Customisation requires deep Manhattan expertise

**Licence / IP notes**
- Proprietary SaaS; no open-source components exposed
- No patent concerns identified for open-source alternatives

---

### IBM Sterling Order Management

**Core features**
- Cross-channel order capture and orchestration (B2B and B2C)
- Single real-time inventory view across all supply chain nodes
- Multi-channel fulfilment: BOPIS, ship-from-store, curbside pickup
- Returns management across channels with standardised processes
- Customisable and automated order workflows
- Task management for warehouse and in-store fulfilment operations
- Global inventory ATP with supply-demand matching

**Differentiating features**
- Deep B2B order management capabilities (EDI 850/855/856, cXML integration)
- Agentic AI for order management launched March 2026 (GA)
- Hybrid-cloud deployment options (cloud, on-prem, hybrid)
- Extreme customisability for complex enterprise-specific rules
- Java-based extensibility framework for custom logic

**UX patterns**
- Legacy UI supplemented by modern web-based dashboards
- Configurable workflows through Sterling Business Center administration console
- XML-based API model (XAPI) with REST wrapper layer
- Javadoc-based developer documentation for API customisation

**Integration points**
- REST XAPI framework (IBM docs: ibm.com/docs/en/order-management)
- SOAP/XML APIs for legacy B2B integrations
- EDI translation via IBM Sterling B2B Integrator
- GitHub open-source integration samples (github.com/IBM/oms-convey-integration)

**Known gaps**
- UI is dated; significantly behind cloud-native competitors on UX
- Implementation costs frequently exceed $500K; long time-to-value
- Declining market share to modern cloud-native alternatives
- Limited self-service configuration for business users

**Licence / IP notes**
- Proprietary IBM commercial software
- Some integration samples published under Apache 2.0 on GitHub

---

### Fluent Commerce

**Core features**
- Distributed Order Management with real-time inventory across all locations
- Rules-based order routing: DC, drop-ship vendor (DSV), store, 3PL
- Available to Promise (ATP) calculation: configurable by channel, loyalty status, product attributes
- Pre-built fulfilment templates: BOPIS, home delivery, Click & Collect
- In-store pick, pack, and dispatch management
- Customer service module with full order visibility and action capabilities
- Reporting and analytics on fulfilment performance

**Differentiating features**
- Processes up to 675 orders/second; handles 500,000 allocation decisions/minute
- Launched industry-first OMS MCP Server for AI agent integration (2026)
- GraphQL-first API with a configurable domain model
- Fluent Builder MCP Server for developer productivity within IDE/Claude Code
- Available on AWS Marketplace and Salesforce AppExchange
- commercetools Marketplace certified integration

**UX patterns**
- Low-code rule configuration for business teams
- Pre-built accelerators reduce deployment time for standard fulfilment scenarios
- GraphQL Playground for developer API exploration
- Visual workflow builder for fulfilment processes

**Integration points**
- REST and GraphQL APIs (docs.fluentcommerce.com)
- MCP Server: Fluent Order Management MCP Server for AI agents
- Fluent Builder MCP Server for developer tooling
- Salesforce Commerce Cloud native integration
- AWS and commercetools ecosystem

**Known gaps**
- Premium pricing targets $100M+ revenue brands only
- Steep learning curve for custom rule development
- Limited self-service analytics; relies on custom BI integrations

**Licence / IP notes**
- Proprietary SaaS; no open-source components identified
- MCP server specifications follow Anthropic's open MCP protocol standard

---

### Salesforce Order Management

**Core features**
- Full order lifecycle management from creation to fulfilment
- Omnichannel inventory visibility across up to 500 locations (Growth plan)
- Automated order routing, approvals, and status updates
- BOPIS, ship-from-store, return-to-any-location fulfilment support
- Customer service team order view and management across all channels
- Integration with Salesforce CRM, Marketing Cloud, and Commerce Cloud
- Cross-sell and upsell recommendations during service interactions

**Differentiating features**
- Native integration with the full Salesforce Customer 360 platform
- Omnichannel Inventory module for multi-location ATP
- Salesforce Flow for no-code order workflow automation
- AppExchange partner ecosystem with 3,000+ connectors
- Data Cloud integration for AI-driven personalisation

**UX patterns**
- Salesforce Lightning UX familiar to existing Salesforce users
- Drag-and-drop Flow builder for order automation
- Unified console view for agents handling orders and service cases
- Trailhead learning platform for guided onboarding

**Integration points**
- Salesforce REST and SOAP APIs (standard Salesforce platform)
- Salesforce AppExchange for pre-built integrations
- Mulesoft for enterprise API integration (separate licence)
- Native Salesforce webhooks and platform events

**Known gaps**
- Limited fulfilment complexity for large multi-node DC networks
- Expensive when adding multiple Salesforce cloud licences
- Dependent on the Salesforce ecosystem; limited portability
- Complex multi-organisation Salesforce configurations add cost

**Licence / IP notes**
- Proprietary Salesforce commercial SaaS
- Appexchange partner integrations governed by separate partner agreements

---

### Kibo Commerce

**Core features**
- MACH-certified (Microservices, API-first, Cloud-native, Headless) OMS
- Intelligent order routing by inventory, location, cost, or custom business rules
- Automated order-splitting across fulfilment locations
- Real-time inventory visibility including in-transit and future inventory
- BOPIS and BODFS (Buy Online Deliver From Store) fulfilment support
- Full customer profile, order history, and return management — no CRM required
- Modular deployment: OMS can be purchased independently of commerce front-end

**Differentiating features**
- Composable architecture: add modules incrementally without system overhaul
- Unified B2B and B2C order management on a single platform
- Built-in customer service workbench without requiring a separate CRM
- Real-time inventory ATP for sales and service teams
- 2026 Nucleus Research OMS Leader recognition

**UX patterns**
- Composable admin UI with module-based navigation
- Configurable routing rule builder for business users
- Developer-first headless API — front-end agnostic
- Progressive feature activation without re-implementation

**Integration points**
- REST APIs (MACH-compliant API-first architecture)
- Pre-built connectors to major e-commerce platforms
- Webhook event streaming for order lifecycle events
- ERP and WMS integration via standard REST endpoints

**Known gaps**
- Smaller partner ecosystem than Salesforce or IBM
- Less extensive global customer base — fewer enterprise reference customers outside North America
- Documentation and developer tooling less mature than larger vendors

**Licence / IP notes**
- Proprietary SaaS
- MACH Alliance certified (vendor-neutral architectural standard)

---

### Fabric OMS

**Core features**
- Distributed Order Management (DOM) with advanced order routing
- Network aggregation for inventory across all fulfilment locations
- Pre-order and backorder inventory management
- BOPIS, ship-to-store, and store-as-mini-DC fulfilment models
- Inventory availability storefront APIs for real-time ATP on product pages
- Recurring export scheduling for inventory synchronisation to external systems
- Over 50 incremental features shipped in recent updates for inventory accuracy

**Differentiating features**
- Headless, API-first v2 architecture built for microservices composability
- Configurable data model for the fulfilment orchestration process
- High-performance endpoints on highly scalable architecture
- Developer-friendly: full API reference at developer.fabric.inc
- Designed to be adopted as a standalone OMS within existing commerce stacks

**UX patterns**
- API-first; UI is secondary to programmatic access
- Admin portal for configuration and order visibility
- Comprehensive developer documentation with API reference
- Modular adoption — can replace just the OMS layer

**Integration points**
- REST APIs (developer.fabric.inc/v2/api-reference/orders-v2)
- Headless commerce APIs for product, inventory, and order management
- Webhooks for order lifecycle events
- Pre-built integrations with major commerce platforms

**Known gaps**
- Newer platform with limited enterprise track record
- Less mature partner ecosystem compared to Manhattan, IBM, or Salesforce
- No MCP server or AI agent integration announced as of research date

**Licence / IP notes**
- Proprietary SaaS
- Raised $140M Series B (2022); independent company

---

### Pipe17

**Core features**
- AI-native order operations hub connecting channels, 3PLs, WMSs, and ERPs
- Visual workflow builder and natural language AI rule configuration via Pippen AI assistant
- Order routing, order holds, inventory buffers, exception notifications
- Dynamic kits and bundled product management
- SKU maps and shipping method maps for channel-to-fulfilment translation
- LiveOps dashboard for real-time exception monitoring
- Multi-tenant 3PL architecture with client-specific routing and SLA management

**Differentiating features**
- Industry-first MCP Server for order management (2025): connects AI assistants (Claude, ChatGPT, Gemini) directly to order operations
- Pippen AI assistant: natural language configuration of integrations and automation rules — no technical intervention required
- 400+ pre-built managed connectors maintained and updated by Pipe17
- Agentic commerce support: processes orders from AI shopping agents (ChatGPT, Claude, Perplexity)
- OAuth2 and API Key authentication for Claude and Gemini MCP integrations
- 2025: 60+ enhancements shipped across 32 connectors including TikTok Shop, Amazon, NetSuite

**UX patterns**
- No-code visual workflow builder for order automation rules
- Natural language prompt interface via Pippen for rule creation
- LiveOps exception dashboard for operational monitoring
- Self-service connector management

**Integration points**
- REST API (apidoc.pipe17.com)
- MCP Server (pipe17.com/ai/mcp) — AI agent integration
- 400+ pre-built connectors: Shopify, Amazon, TikTok Shop, NetSuite, Logiwa, and more
- OAuth 2.0 and API Key authentication methods

**Known gaps**
- Mid-market positioning; limited for complex enterprise fulfilment routing
- Less sophisticated DOM (Distributed Order Management) logic than Manhattan or Fluent
- Primarily a connectivity/orchestration layer rather than full-stack OMS

**Licence / IP notes**
- Proprietary SaaS with subscription pricing
- MCP Server follows Anthropic's open MCP protocol specification

---

### Linnworks

**Core features**
- Multi-channel order aggregation into a single dashboard
- Real-time inventory synchronisation across all selling channels
- Automated order routing with rules engine
- Batch order processing for warehouse efficiency
- Shipping carrier integration with rate comparison
- Demand forecasting using sales data and trend algorithms
- Multi-channel listing management (Amazon, eBay, Shopify, Magento, and more)
- Warehouse pick, pack, and dispatch workflows

**Differentiating features**
- Widest range of out-of-the-box marketplace and channel integrations for SMB/mid-market
- Accessible pricing starting at $499/month — most affordable in this survey
- Demand forecasting with predictive stock management built into core platform
- Combined order management and inventory management in a single product
- Strong e-commerce SMB community and self-service onboarding

**UX patterns**
- Single-dashboard view of all channels and orders
- Rules-based automation wizard for order routing
- Self-service onboarding with guided setup
- Help centre and community forums for support

**Integration points**
- REST API for custom integrations
- Native integrations with Amazon, eBay, Shopify, Magento, WooCommerce, and 100+ others
- Shipping carrier integrations (Royal Mail, UPS, FedEx, DHL, and more)
- Open API for ERP and accounting system connections

**Known gaps**
- Limited omnichannel fulfilment logic for complex multi-DC routing
- No AI-native features or agentic commerce support
- Less suitable for enterprise-scale operations
- Limited B2B order management capabilities

**Licence / IP notes**
- Proprietary SaaS
- No open-source components; acquired by Linnworks group

---

### KBRW

**Core features**
- Rules-based real-time ATP calculation with stock allocation
- Safety stock configuration and quota management by channel
- Smart order routing and orchestration by time, cost, and constraint rules
- Rule-based competitive fulfilment and return-anywhere features
- Highly configurable business rules engine with simulation capability
- Real-time inventory synchronisation across all channels
- Full compliance with European data regulations (GDPR); data hosted in France

**Differentiating features**
- AI-native architecture recognised as Nucleus Research 2026 OMS Leader
- European sovereignty: designed and built in Europe for trust, independence, and regulatory compliance
- Embedded integration platform for advanced configuration and adaptation to any business process
- Gartner Representative Vendor in Distributed Order Management Systems Market Guide (June 2025)
- High configurability without code — business rules engine with simulation before deployment

**UX patterns**
- Business rules configuration interface with simulation/preview
- Composable high-performance core with embedded integration layer
- Designed for complex European retail and multi-country operations
- Partner ecosystem through commercetools Marketplace

**Integration points**
- API-first architecture (REST)
- commercetools Marketplace integration
- Embedded integration platform for ERP, WMS, and carrier connections
- European cloud infrastructure (hosted in France, GDPR compliant)

**Known gaps**
- Limited brand recognition outside Europe
- Smaller partner and implementation ecosystem vs. North American vendors
- English-language documentation and support less comprehensive than US competitors

**Licence / IP notes**
- Proprietary SaaS; privately funded (European growth capital)
- GDPR-compliant data handling by design

---

## Cross-Cutting Feature Themes

### Table-Stakes Features
- Real-time inventory visibility across all fulfilment locations
- Multi-channel order aggregation (e-commerce, marketplace, in-store, B2B)
- Configurable order routing rules (cost, speed, inventory position, location)
- Standard omnichannel fulfilment modes: BOPIS, ship-from-store, home delivery, Click & Collect
- Returns and reverse logistics management
- Order lifecycle tracking with customer-facing status updates
- Carrier integration with shipping label generation
- Customer service workbench for order visibility and intervention
- REST API with OAuth 2.0 authentication

### Differentiating Features
- AI-native agentic order management (Pipe17's Pippen, Manhattan's AI agents, IBM's Agentic AI)
- MCP Server for AI agent integration (Fluent Commerce, Pipe17 — both launched 2025/2026)
- Carbon impact scoring in fulfilment decisions (Manhattan)
- Natural language rule configuration (Pipe17/Pippen)
- European data sovereignty with GDPR-native architecture (KBRW)
- Extreme throughput: 675 orders/second, 500,000 allocation decisions/minute (Fluent)
- Composable MACH-certified architecture (Kibo, Fabric)
- Pre-order and backorder management with ATP (Fabric)

### Underserved Areas / Opportunities
- Real-time inventory synchronisation during flash sales and high-velocity events — oversells remain a leading complaint
- Transparent, customer-facing carbon impact data for sustainable fulfilment choices
- Returns prediction at point of purchase to pre-position reverse logistics
- AI-driven exception resolution that acts autonomously without human escalation
- Accessible, open-source OMS suitable for mid-market companies who cannot afford enterprise pricing
- Natural language interface for configuring routing logic without technical expertise
- Unified analytics combining order, inventory, and fulfilment performance data in one view
- Demand signal sensing feeding upstream replenishment from real-time order flow
- Agentic commerce order intake from AI shopping agents (emerging; only Pipe17 has addressed this)

### AI-Augmentation Candidates
- Order exception detection and autonomous resolution (stock-outs, payment failures, carrier delays)
- Intelligent routing scoring that learns from outcomes and continuously optimises
- Returns prediction model based on order characteristics, customer history, and product type
- Dynamic post-purchase communication generation personalised to each customer and event
- Natural language configuration of routing rules and automation workflows
- Anomaly detection on fulfilment performance metrics (OTIF, WISMO rate, carrier performance)
- Demand signal extraction from real-time order flow to inform replenishment

---

## Legal & IP Summary

All solutions analysed are proprietary commercial software. No open-source OMS solutions with significant market adoption were identified in this space; the closest alternatives are lightweight open-source tools with limited enterprise-grade capabilities. The MACH Alliance (Microservices, API-first, Cloud-native, Headless) provides a vendor-neutral architectural standard that is relevant to composable OMS design but carries no IP restrictions. MCP (Model Context Protocol) is an open standard from Anthropic with no licence restrictions for implementation. EDI standards (ANSI X12, GS1, cXML) are industry-maintained specifications open for implementation. No patented features were identified as blocking concerns for an open-source AI-native OMS implementation.

---

## Recommended Feature Scope

**Must-have (MVP)**:
- Multi-channel order ingestion via REST API (e-commerce platforms, marketplaces, manual/API entry)
- Real-time inventory visibility across configurable fulfilment locations
- Rules-based intelligent order routing (cost, speed, inventory, location)
- Standard fulfilment modes: ship-from-DC, BOPIS, ship-from-store
- Order lifecycle state machine with event streaming (webhooks / message bus)
- Returns and RMA management with configurable return-routing logic
- Customer-facing order status and tracking (WISMO self-service)

**Should-have (v1.1)**:
- AI exception management: autonomous detection and resolution of at-risk orders
- Natural language routing rule configuration (LLM-powered)
- MCP Server for AI agent integration (agentic commerce support)
- Carrier rate shopping and shipping label generation
- Analytics dashboard: OTIF, fill rate, exception rate, fulfilment cost per order

**Nice-to-have (backlog)**:
- Returns prediction model at point of purchase
- Carbon impact scoring in fulfilment routing decisions
- Demand signal extraction pipeline feeding upstream replenishment
- EDI 850/855/856 adapter for B2B order management
- Multi-tenant 3PL architecture with client-isolated routing and SLA management
