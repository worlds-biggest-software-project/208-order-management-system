# Order Management System (OMS)

> Part of the [worlds-biggest-software-project](https://github.com/worlds-biggest-software-project) initiative.
>
> An AI-native, open-source order management system for multi-channel order routing, fulfilment orchestration, and returns.

The Order Management System (OMS) project aims to deliver an accessible alternative to enterprise OMS platforms for retailers, e-commerce operators, and 3PLs who need real-time inventory visibility, intelligent order routing, and omnichannel fulfilment without enterprise-tier pricing or implementation timelines. It targets the gap between SMB tools with limited fulfilment logic and enterprise suites costing $500K+ to deploy.

---

## Why an Open-Source OMS?

- IBM Sterling implementations frequently exceed $500K total cost and have long time-to-value, excluding mid-market adopters.
- Manhattan Active OMS and Fluent Commerce are positioned at enterprise and $100M+ revenue brands with custom-quoted, premium pricing.
- SMB-accessible tools like Linnworks (from $499/month) lack omnichannel fulfilment logic and have no AI-native or agentic commerce features.
- No open-source OMS with significant market adoption was identified during research; the closest alternatives are lightweight tools without enterprise-grade capabilities.
- AI-native capabilities (agentic order management, MCP servers, natural-language rule configuration) are emerging only in the most expensive proprietary platforms.

---

## Key Features

### Order Capture and Inventory

- Multi-channel order ingestion via REST API from e-commerce platforms, marketplaces, and manual/API entry
- Real-time inventory visibility across configurable fulfilment locations (DCs, stores, 3PLs)
- Available-to-Promise (ATP) calculation configurable by channel, location, and product attributes
- Pre-order and backorder inventory management

### Routing and Fulfilment

- Rules-based intelligent order routing by cost, speed, inventory position, and location
- Standard fulfilment modes: ship-from-DC, BOPIS, ship-from-store, Click & Collect
- Order lifecycle state machine with event streaming via webhooks or message bus
- Carrier rate shopping and shipping label generation

### Returns and Customer Service

- Returns and RMA management with configurable return-routing logic
- Customer-facing order status and tracking (WISMO self-service)
- Customer service workbench for order visibility and intervention
- Reverse logistics orchestration across channels

### AI and Agentic Operations

- Autonomous detection and resolution of at-risk orders (stock-outs, payment failures, carrier delays)
- Natural-language routing-rule configuration powered by LLMs
- MCP Server for AI agent integration, enabling agentic commerce intake from AI shopping agents
- Analytics dashboard covering OTIF, fill rate, exception rate, and fulfilment cost per order

---

## AI-Native Advantage

Incumbent OMS platforms are only beginning to expose agentic AI features (Manhattan AI agents, IBM Agentic AI GA in March 2026, Pipe17's Pippen, Fluent's MCP Server). This project is designed AI-native from the start: an intelligent routing engine that learns from outcomes and balances cost, speed, carbon impact, and inventory; autonomous exception management; returns prediction at point of purchase; and dynamic personalised post-purchase communication. Natural-language configuration removes the technical barrier that makes incumbent rule engines costly to operate.

---

## Tech Stack & Deployment

The project targets a composable, API-first architecture aligned with the MACH (Microservices, API-first, Cloud-native, Headless) approach used by Kibo and Fabric. Expected interfaces include REST APIs with OAuth 2.0, webhook event streaming for order lifecycle events, and an MCP Server following Anthropic's open MCP protocol for AI agent integration. Industry standards in scope include GS1 (GTIN, GLN, SSCC), ANSI X12 EDI (850 / 855 / 856) and cXML for B2B flows, plus PCI DSS, GDPR, and CCPA compliance considerations.

---

## Market Context

The global multichannel order management market was valued at USD 3.90 billion in 2025 and is projected to reach USD 13.01 billion by 2035 (Precedence Research). The broader OMS software segment grew from ~$1B in 2021 to ~$1.9B in 2026 at a 12.3% CAGR. Primary buyers include heads of e-commerce or digital operations at omnichannel retailers, supply chain directors, IT architects implementing composable commerce stacks, customer experience leaders, and 3PL operators.

---

## Project Status

> This project is in the **research and specification phase**.  
> Contributions, feedback, and domain expertise are welcome.

---

## Contributing

We welcome contributions from developers, domain experts, and potential users.
See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines.

**Important:** All contributions must be your own original work or clearly attributed
open-source material with a compatible licence. Copyright infringement and licence
violations will not be tolerated and will result in immediate removal of the offending
contribution. If you are unsure whether a piece of code, text, or other material is
safe to contribute, open an issue and ask before submitting.

---

## Licence

Licence to be determined. See [discussion](#) for context.
