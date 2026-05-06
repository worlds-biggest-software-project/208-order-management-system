# Standards & API Reference

> Project: Order Management System · Generated: 2026-05-03

## Industry Standards & Specifications

### ISO Standards

- **ISO 28219: Labelling and Direct Part Marking of Products and Components**
  URL: https://www.iso.org/standard/62593.html
  Relevant for OMS implementations that manage physical goods — defines label and marking standards used to track products through fulfilment and returns workflows.

- **ISO 22000 / Supply Chain Management Standards**
  URL: https://www.iso.org/standard/65464.html
  Relevant to food and perishable order management contexts; provides a framework for supply chain traceability that may inform OMS data model design for regulated goods.

- **ISO/IEC 27001: Information Security Management**
  URL: https://www.iso.org/standard/27001
  Applicable to any OMS handling customer PII, payment data, or enterprise supply chain data; defines security controls and risk management practices.

- **ISO 9001: Quality Management Systems**
  URL: https://www.iso.org/standard/62085.html
  Relevant for enterprise OMS implementations where process consistency, traceability, and continual improvement in fulfilment operations are required.

### W3C & IETF Standards

- **RFC 7231: Hypertext Transfer Protocol (HTTP/1.1) — Semantics and Content**
  URL: https://www.rfc-editor.org/rfc/rfc7231
  Defines HTTP method semantics (GET, POST, PUT, DELETE, PATCH) foundational to any REST API implementation in an OMS. All OMS REST APIs rely on this specification.

- **RFC 7807: Problem Details for HTTP APIs**
  URL: https://www.rfc-editor.org/rfc/rfc7807
  Defines a standard JSON format for machine-readable error details in HTTP API responses. Recommended for consistent OMS API error handling.

- **RFC 8288: Web Linking**
  URL: https://www.rfc-editor.org/rfc/rfc8288
  Defines link relations for hypermedia APIs; relevant when implementing HATEOAS-style OMS APIs with navigable order resource relationships.

- **RFC 6749: OAuth 2.0 Authorization Framework**
  URL: https://www.rfc-editor.org/rfc/rfc6749
  The foundational authorisation standard for OMS API access. All major OMS platforms (Manhattan, Fluent, Pipe17, IBM Sterling) use OAuth 2.0 for API authentication.

- **RFC 7519: JSON Web Token (JWT)**
  URL: https://www.rfc-editor.org/rfc/rfc7519
  Standard token format used in OAuth 2.0 flows for OMS API authentication and authorisation; widely used in all cloud-native OMS platforms.

- **RFC 7386: JSON Merge Patch**
  URL: https://www.rfc-editor.org/rfc/rfc7386
  Defines a simple JSON format for partial updates to resources — relevant for OMS PATCH operations on orders (e.g., updating shipping address or order status).

### Data Model & API Specifications

- **OpenAPI Specification (OAS) 3.1**
  URL: https://spec.openapis.org/oas/v3.1.0
  The industry standard for describing REST APIs. An AI-native OMS should publish its API as an OpenAPI 3.1 document to enable auto-generated SDKs, documentation, and client tooling.

- **GraphQL Specification**
  URL: https://spec.graphql.org/
  Used by Fluent Commerce as its primary API paradigm. GraphQL enables clients to request only the fields they need, reducing over-fetching in complex order data queries. Relevant for OMS APIs serving diverse consumer applications.

- **JSON Schema (IETF Internet Draft)**
  URL: https://json-schema.org/
  Standard for defining and validating JSON data structures. Essential for OMS data model definitions (order, line item, inventory, fulfilment node schemas).

- **AsyncAPI Specification 2.x / 3.x**
  URL: https://www.asyncapi.com/
  Standard for documenting event-driven and message-based APIs. Highly relevant for an OMS with event streaming (order placed, order shipped, order cancelled events) via Kafka, RabbitMQ, or webhook delivery.

- **CloudEvents Specification (CNCF)**
  URL: https://cloudevents.io/
  A CNCF specification for a common format for event data across services. Relevant for standardising OMS order lifecycle events published to downstream consumers (WMS, ERP, customer notifications).

- **GS1 Standards (GTIN, GLN, SSCC, GS1-128)**
  URL: https://www.gs1.org/standards
  Global product and location identification standards. GTINs identify products in OMS line items; GLNs identify fulfilment locations; SSCCs identify shipment containers. Foundational for multi-party supply chain traceability.

### EDI Standards

- **ANSI X12 850 — Purchase Order**
  URL: https://www.seeburger.com/resources/good-to-know/ansi-x12-edi-850-purchase-order-message
  North American standard for electronic purchase orders in B2B order management. Widely used between retailers, suppliers, and 3PLs. An OMS B2B module should support inbound and outbound EDI 850.

- **ANSI X12 855 — Purchase Order Acknowledgement**
  Companion to EDI 850; the supplier's confirmation of receipt and acceptance of a purchase order. Relevant for supplier-facing OMS modules.

- **ANSI X12 856 — Ship Notice / Advance Ship Notice (ASN)**
  Notification from supplier or 3PL of a pending shipment. Enables OMS to pre-receive inventory and trigger downstream fulfilment events.

- **UN/EDIFACT ORDERS / ORDRSP / DESADV**
  URL: https://www.unece.org/trade/untdid/
  European equivalent of ANSI X12 850/855/856 — used widely in EU retail supply chains. Relevant for OMS deployments serving European markets alongside KBRW and other EU-focused vendors.

- **cXML (Commerce XML)**
  URL: https://cxml.org/
  XML-based standard for procurement transactions between buyers and suppliers; used in B2B procurement platforms (Ariba, Coupa) that feed orders into OMS systems.

### Security & Authentication Standards

- **OAuth 2.0 (RFC 6749)**
  URL: https://oauth.net/2/
  Universal standard for delegated API authorisation; used by all major OMS platforms for third-party and internal API access.

- **OpenID Connect 1.0 (OIDC)**
  URL: https://openid.net/connect/
  Identity layer on top of OAuth 2.0; enables single sign-on and user identity federation for OMS multi-tenant environments and enterprise identity providers.

- **PCI DSS v4.0 (Payment Card Industry Data Security Standard)**
  URL: https://www.pcisecuritystandards.org/standards/
  Mandatory for any OMS that captures, processes, stores, or transmits cardholder data. PCI DSS v4.0 explicitly includes custom code and APIs as in-scope; requires code review and API inventory maintenance.

- **OWASP API Security Top 10**
  URL: https://owasp.org/www-project-api-security/
  The reference checklist for API security covering broken object-level authorisation, authentication weaknesses, excessive data exposure, and injection. Essential for OMS API security hardening.

- **GDPR (General Data Protection Regulation)**
  URL: https://gdpr.eu/
  EU regulation governing handling of personal data including customer names, addresses, and order histories stored in OMS systems. Requires data minimisation, consent management, right to erasure, and data residency compliance.

- **CCPA (California Consumer Privacy Act)**
  URL: https://oag.ca.gov/privacy/ccpa
  US (California) consumer data privacy regulation analogous to GDPR; applicable to OMS systems handling data of California residents.

### MCP Server Specifications

- **Model Context Protocol (MCP) — Anthropic**
  URL: https://modelcontextprotocol.io/
  Open standard for connecting AI assistants to software applications via a standardised interface. Two major OMS vendors (Fluent Commerce and Pipe17) have already published production MCP Servers for their platforms. An AI-native OMS should implement an MCP Server as a first-class integration surface for AI agents.

- **Fluent Order Management MCP Server (Pilot)**
  URL: https://docs.fluentcommerce.com/landing/fluent-order-management-mcp-server
  Production implementation of MCP for OMS by Fluent Commerce; covers WISMO use cases, order status retrieval, order cancellation, and address change actions.

- **Pipe17 MCP Server**
  URL: https://pipe17.com/ai/mcp/
  Production MCP server for order operations; exposes Orders, Products, Inventory, Fulfillments, Shipments, Customers, Locations, and Exceptions to any MCP-enabled AI client.

---

## Similar Products — Developer Documentation & APIs

### Shopify Admin API (GraphQL)

- **Description:** Shopify's primary API for order management within the Shopify e-commerce platform. As of April 2025, all new public apps must use the GraphQL Admin API exclusively; the REST Admin API is legacy.
- **API Documentation:** https://shopify.dev/docs/api/admin-graphql/latest/objects/Order
- **SDKs/Libraries:** Shopify Admin API libraries for Node.js, Ruby, Python, PHP — https://shopify.dev/docs/api/usage/client-libraries
- **Developer Guide:** https://shopify.dev/docs/api/admin-graphql/latest
- **Standards:** GraphQL; versioned quarterly (current: 2026-04)
- **Authentication:** OAuth 2.0 (for public apps); Access Tokens (for custom apps)

### WooCommerce REST API

- **Description:** REST API for WordPress-based WooCommerce stores enabling order creation, retrieval, updates, and status management. Integrated with WordPress REST API infrastructure.
- **API Documentation:** https://woocommerce.github.io/woocommerce-rest-api-docs/
- **SDKs/Libraries:** WooCommerce API libraries for Node.js, Python, PHP, Ruby — https://woocommerce.com/document/woocommerce-rest-api/
- **Developer Guide:** https://woocommerce.com/document/woocommerce-rest-api/
- **Standards:** REST/JSON; OpenAPI definitions available
- **Authentication:** Consumer Key / Consumer Secret (OAuth 1.0a or Basic Auth over HTTPS)

### Adobe Commerce (Magento) Web API

- **Description:** Comprehensive REST and GraphQL API covering the full order lifecycle — quote, order creation, invoicing, shipment, and returns — for Adobe Commerce on-premises and cloud.
- **API Documentation:** https://developer.adobe.com/commerce/webapi/rest/reference/
- **SDKs/Libraries:** PHP SDK; community libraries for Node.js and Python
- **Developer Guide:** https://developer.adobe.com/commerce/webapi/rest/tutorials/orders/
- **Standards:** REST/JSON, GraphQL, SOAP (legacy)
- **Authentication:** OAuth 1.0a (for third-party integrations); Bearer Token (admin REST)

### Manhattan Active API

- **Description:** REST API for Manhattan Active OMS and supply chain suite built on 250+ microservices on Kubernetes. Supports order orchestration, inventory management, fulfilment, and returns.
- **API Documentation:** https://developer.manh.com/docs/how-to/rest-api/reference/
- **SDKs/Libraries:** No public SDKs; REST API with JSON; platform SDK for extension development via developer hub
- **Developer Guide:** https://developer.manh.com/docs/
- **Standards:** REST/JSON; predictable resource-oriented URLs with standard HTTP verbs
- **Authentication:** OAuth 2.0

### IBM Sterling Order Management REST API

- **Description:** REST XAPI framework exposing IBM Sterling OMS Java-based business services as HTTP REST endpoints. Supports order lifecycle management, inventory, and fulfilment orchestration for enterprise deployments.
- **API Documentation:** https://www.ibm.com/docs/en/order-management
- **SDKs/Libraries:** Java SDK (Sterling extensibility framework); REST XAPI for external integrations
- **Developer Guide:** https://www.ibm.com/docs/en/order-management?topic=database-sterling-order-management-system-apis-services
- **Standards:** REST/JSON (REST wrapper over XML/SOAP XAPI); legacy SOAP/XML also supported
- **Authentication:** IBM Cloud IAM (OAuth 2.0); session-based for on-prem deployments

### Fluent Commerce API

- **Description:** Cloud-native distributed OMS with GraphQL as primary API. REST is available for specific platform operations only. GraphQL provides the full configurable domain model for orders, inventory, fulfilment, and returns.
- **API Documentation:** https://docs.fluentcommerce.com/essential-knowledge/apis-overview
- **SDKs/Libraries:** Fluent CLI with embedded MCP Server for developer tooling
- **Developer Guide:** https://docs.fluentcommerce.com/
- **Standards:** GraphQL (primary); REST (limited platform operations); MCP Server (AI agent integration)
- **Authentication:** OAuth 2.0

### Pipe17 API

- **Description:** Order operations integration hub API for connecting channels, 3PLs, WMSs, and ERPs. Exposes order routing, inventory, fulfilment, exceptions, and shipment data via REST.
- **API Documentation:** https://apidoc.pipe17.com/
- **SDKs/Libraries:** No public SDKs identified; REST API with MCP Server for AI clients
- **Developer Guide:** https://support.pipe17.com/hc/en-us
- **Standards:** REST/JSON; MCP Server for AI agent integration
- **Authentication:** OAuth 2.0; API Key (for non-OAuth MCP clients)

### Kibo Commerce OMS API

- **Description:** MACH-certified composable OMS REST API supporting order lifecycle management, inventory, routing, and customer service for B2B and B2C retailers.
- **API Documentation:** https://apidocs.kibocommerce.com/
- **SDKs/Libraries:** JavaScript/TypeScript and .NET SDKs available via Kibo developer resources
- **Developer Guide:** https://apidocs.kibocommerce.com/
- **Standards:** REST/JSON; OpenAPI 3.0 specification available
- **Authentication:** OAuth 2.0

### Fabric OMS API v2

- **Description:** Headless, API-first distributed OMS with high-performance REST endpoints built on scalable microservices architecture. Configurable data model for order fulfilment orchestration.
- **API Documentation:** https://developer.fabric.inc/v2/api-reference/orders-v2/order-management-system
- **SDKs/Libraries:** REST API; no published SDKs
- **Developer Guide:** https://knowledgebase.fabric.inc/docs/developer-portal/oms-developer-guide/oms-overview/
- **Standards:** REST/JSON; OpenAPI reference available in developer portal
- **Authentication:** API Key / Bearer Token

### Linnworks API

- **Description:** REST API for multi-channel order and inventory management targeting SMB/mid-market e-commerce. Supports order retrieval, status updates, inventory synchronisation, and shipping management.
- **API Documentation:** https://developer.linnworks.com/
- **SDKs/Libraries:** .NET and JavaScript client libraries
- **Developer Guide:** https://developer.linnworks.com/
- **Standards:** REST/JSON
- **Authentication:** OAuth 2.0

---

## Notes

**Emerging Standard — MCP for Order Management**: The Model Context Protocol is rapidly becoming a de-facto standard for AI-to-OMS integration. Both Fluent Commerce and Pipe17 launched MCP Servers in 2025–2026. An AI-native OMS should treat MCP Server implementation as a first-class requirement, not an afterthought.

**GraphQL vs REST**: Enterprise OMS platforms are diverging on API paradigm. Fluent Commerce is GraphQL-first; most others are REST-first. For an AI-native OMS, REST with OpenAPI 3.1 is recommended for maximum ecosystem compatibility, with GraphQL as an optional secondary interface for complex querying use cases.

**Event-Driven Architecture**: There is no dominant standard for OMS event streaming. CloudEvents (CNCF) and AsyncAPI represent best-practice specifications but are not universally adopted. A new AI-native OMS has an opportunity to establish AsyncAPI-documented CloudEvents as its event standard, increasing interoperability.

**EDI Bridging**: Traditional B2B supply chains still rely heavily on ANSI X12 and UN/EDIFACT. An AI-native OMS that targets enterprise B2B use cases will need EDI translation capability, either natively or via integration with a B2B integration platform (IBM B2B Integrator, SPS Commerce, etc.).
