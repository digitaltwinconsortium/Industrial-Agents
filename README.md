<h1 align="center">The Industrial AI Agent Manifesto</h1>
<h3 align="center">Governance Requirements for Trustworthy Autonomous Operations</h3>

<p align="center">
  <a href="LICENSE"><img src="https://img.shields.io/badge/License-CC_BY--SA_4.0-blue.svg" alt="License: CC BY-SA 4.0"></a>
  <img src="https://img.shields.io/badge/Version-1.0-green.svg" alt="Version 1.0">
  <img src="https://img.shields.io/badge/February-2026-orange.svg" alt="February 2026">
  <a href="https://www.digitaltwinconsortium.org"><img src="https://img.shields.io/badge/Digital_Twin_Consortium-Framework-purple.svg" alt="DTC"></a>
</p>

<p align="center"><em>A product of the Digital Twin Consortium Composability Framework Working Group</em></p>

<p align="center">
  <strong>Lead Author:</strong> Pieter van Schalkwyk, XMPro &nbsp;|&nbsp;
  <strong>Contributor:</strong> Sean Whiteley, Axomem<br>
  <strong>Technical Editors:</strong> Dan Isaacs, CTO and Will Thompson, Digital Twin Consortium
</p>

---

> [!NOTE]
> **10 engineering laws for governing AI agents in safety-critical industrial environments** — healthcare, manufacturing, aerospace, energy, mining, and infrastructure. Built on decades of safety-critical systems development. Backed by the Digital Twin Consortium's 200+ member organizations.
>
> **Read the full technical brief:** [Industrial AI Agent Manifesto (PDF)](DTC_TechBrief_IndustrialAgentManifesto.pdf)

---

## Table of Contents

- [The Challenge](#the-challenge)
- [The Deployment Pattern We Keep Seeing](#the-deployment-pattern-we-keep-seeing)
- [What Trustworthy Agents Actually Need](#what-trustworthy-agents-actually-need)
- [Why Digital Twins Provide the Answer](#why-digital-twins-provide-the-answer)
- [The Ten Laws of Trustworthy AI Agent Governance](#the-ten-laws-of-trustworthy-ai-agent-governance)
- [Implementation Across Domains](#implementation-varies-across-domains-requirements-do-not)
- [What This Means for Key Stakeholders](#what-this-means-for-key-stakeholders)
- [From Manifesto to Standardization](#from-manifesto-to-standardization)
- [The Real Question](#the-real-question)
- [About the Digital Twin Consortium](#about-the-digital-twin-consortium)

---

## The Challenge

We are entering the most consequential transition in safety-critical operations since the digital control revolution. Autonomous AI agents are moving into healthcare, manufacturing, aerospace, energy, and infrastructure — not because the technology has suddenly become trustworthy, but because economic pressure, workforce scarcity, and geopolitical competition are forcing deployment faster than governance can mature. The opportunity is enormous. So is the risk of systems whose decisions cannot be explained, constrained, or audited once they are in the loop.

In regulated environments, proof matters more than promise. When an agent influences patient care, process control, structural integrity, or grid stability, operators and regulators require evidence of three things: what the system decided, why it decided it, and whether unsafe outcomes were structurally prevented. Today, most organizations cannot demonstrate any of the three. Without that proof, autonomy does not scale — it stalls in pilots, triggers compliance backlash, and introduces silent operational risk into the systems we rely on most.

Industrial AI is also arriving at a moment of profound workforce transition. Across sectors, experienced operators are retiring faster than replacements can be trained, and the systems they ran depend as much on judgment and intuition as on software. Properly governed AI agents are not substitutes for that expertise but one of the few tools capable of preserving it — capturing institutional knowledge, supporting thin workforces, and enabling more resilient domestic production in an era of supply-chain volatility.

This manifesto sets out ten laws for deploying trustworthy AI agents. They are not brakes on progress, but the conditions that make progress durable. Autonomy does not eliminate human judgment — it encodes it, preserves it, and ensures that automation strengthens resilience rather than undermining it.

## The Deployment Pattern We Keep Seeing

Organizations build one agent. It works. They build ten more. Each carries its own constraints, its own safety logic, its own logging format.

Ask: "Show me all agent decisions last quarter where constraint X was active." The answer requires manually querying ten systems, assuming the logs even captured that information.

Then a regulation changes. Updating a safety constraint means manual reconfiguration across all agents. Version drift, compliance gaps, and compounding risk follow. Scale to 50 or 100 agents and it breaks completely.

> [!WARNING]
> Gartner predicts **40% of agentic AI deployments will fail by 2028**. Not because the AI is incapable. Because the governance infrastructure does not exist.

## What Trustworthy Agents Actually Need

High-stakes environments share five non-negotiable requirements. Clinical treatment. Building life safety. Grid stability. Process safety. Mission-critical aerospace operations. All require the same governance capabilities.

### 1. Reproducible Context

Restore the complete operational state that existed when the agent made a decision. Equipment status, active constraints, relevant history, environmental conditions. Without this, you cannot verify correctness.

### 2. Domain Constraints as Hard Boundaries

Prove the agent cannot violate critical domain rules. Architecturally, not through monitoring. No code path should allow a medication dosage to exceed protocols, a building control to disable fire safety, or a grid decision to breach stability limits.

### 3. Validation Before Execution

Architectural separation between agent recommendation and action execution. The agent proposes. Something validates against constraints. Only validated actions execute. Direct execution authority is a single point of failure.

### 4. Complete Audit Trails

Answer instantly: "Show me every decision where constraint X was active, what alternatives the agent considered, and why it chose this action."

If the answer requires manually reviewing logs from 50 agents, you do not have auditability.

### 5. Fleet-Scale Policy Management

Update a constraint once and have it propagate reliably to all agents. Without manual reconfiguration. Without the risk of missing a constraint.

## Why Digital Twins Provide the Answer

Digital twins were built to maintain synchronized models of operational systems. They already encode domain knowledge: clinical protocols, building codes, equipment limits and grid requirements. They already integrate with operational systems and provide state management and audit infrastructure.

When an agent queries a digital twin, the twin checks current state, active constraints, and domain rules. It validates. It logs the decision with complete context. It serves as the single source of truth for policy updates.

When a constraint changes, it updates once. All agents query the same model.

This is already working in production. Digital twins are deployed today across DTC member organizations in hospitals, buildings, factories, power plants, mines, and aerospace operations.

## The Ten Laws of Trustworthy AI Agent Governance

These laws are engineering requirements derived from decades of safety-critical systems development, now formalized based on real-world experience with autonomous AI agents in industrial environments.

This "Industrial AI Agent Manifesto" defines what industrial agents must do to operate safely and securely in production environments. Each law specifies a required capability and shows why digital twins are uniquely positioned to provide that capability.

| # | Law | Requirement | Why It Matters |
|:-:|-----|-------------|----------------|
| 1 | **Deterministic Validation and Execution** | Industrial agents must produce deterministic validated actions given identical operational states, ensuring predictable and reproducible behavior in safety-critical decisions. | Regulators require reproducible decisions for compliance verification and incident investigation. |
| 2 | **Physics-Aware and Process-Aware Intelligence** | Agents must respect physical constraints and encode process models, not just statistical patterns. | General-purpose AI cannot understand domain-specific safety boundaries without structured domain knowledge. |
| 3 | **Symbolic Primacy with Sub-Symbolic Intelligence** | Symbolic reasoning must have architectural primacy over sub-symbolic AI, creating inherent trustworthiness and auditability. | Continuous learning systems can gradually erode safety margins unless constraints are architecturally protected. |
| 4 | **Separation of Control with Standardized Interoperability** | Agent cognition must be architecturally separated from action execution, with standardized protocols enabling secure coordination. | Safety-critical systems require validation layers between decision-making and actuation to prevent single points of failure. |
| 5 | **Emergency Stop, Human Override, and Graceful Degradation** | Immediate human override, safe shutdown, and graceful degradation to simpler control modes must be non-negotiable capabilities. | Abrupt agent halts can leave physical systems in undefined or unsafe states without proper degradation logic. |
| 6 | **Interoperability with Operational Systems** | Agent interaction with domain-specific systems must be mediated through semantic models, not a direct protocol interface. The agent reasons over domain models; the digital twin translates into system-specific protocols. | Industrial environments use diverse protocols (OPC UA, HL7, BACnet) that agents should not interface with directly. |
| 7 | **Auditability and Transparency** | All agent actions must be transparent, traceable, and explainable to regulators, operators, and stakeholders. | Regulated industries require complete decision provenance. Partial logs are insufficient for regulatory compliance. |
| 8 | **Progressive Autonomy with Safety Boundaries** | Autonomy levels must map to human roles, approvals, and safety criticality. Higher autonomy requires more structured safety, not less. | Direct deployment to full autonomy without validation stages creates unacceptable operational risk. |
| 9 | **Multi-Agent Safety Orchestration** | Complex industrial operations require coordination of specialized capabilities with clear safety hierarchies. Whether implemented as distinct agents or functional modules, the required behaviors remain constant. | Point-to-point agent communication cannot prevent conflicting objectives from creating unsafe system states. |
| 10 | **Safe and Secure Continuous Learning** | Industrial agents continuously collect operational data and evaluate performance, with learned improvements deployed only through controlled processes that maintain inviolable safety and security guarantees. | Production learning without validation can introduce unsafe and insecure behaviors that appear successful in training data. |

## Implementation Varies Across Domains. Requirements Do Not.

This Industrial Agent Manifesto defines governance requirements that apply universally. Implementation details vary by domain:

| Domain | Implementation |
|--------|---------------|
| **Healthcare** | Clinical decision support agent queries patient twin for medication interactions and protocol compliance before surfacing recommendations to physicians. |
| **Building Operations** | Building optimization agent queries building twin for comfort ranges and code compliance before adjusting HVAC setpoints. |
| **Process Manufacturing** | Process optimization agent queries process twin for thermodynamic limits and safety system status before recommending reactor adjustments. |
| **Utilities** | Grid dispatch agent queries grid twin for stability requirements and generation capacity before executing dispatch decisions. |
| **Mining** | Equipment dispatch agent queries mine twin for ground stability and equipment limits before routing haul trucks. |
| **Aerospace** | Mission planning agent queries vehicle twin for propellant budgets and mission rules before commanding orbital maneuvers. |

*Same governance framework. Different domain implementations.*

## What This Means for Key Stakeholders

<details>
<summary><b>For Digital Twin Platform Builders</b></summary>
<br>

The ten laws define governance capabilities your platforms should provide: state capture and replay, domain knowledge integration, validation architecture, audit infrastructure, and fleet-scale policy management.

If your digital twin cannot provide reproducible state snapshots, cannot enforce symbolic constraints, cannot mediate between agent recommendations and physical actuation, and cannot maintain audit trails, then your platform is not ready for industrial AI agent deployment.

</details>

<details>
<summary><b>For Organizations Deploying AI Agents</b></summary>
<br>

Use the ten laws as your deployment evaluation framework. Before granting any AI agent authority to act autonomously, ask yourself:

**Evaluation Checklist:**

- [ ] Can you reproduce any agent decision by restoring operational state?
- [ ] Are domain constraints architecturally enforced?
- [ ] Is there validation separating agent recommendation and action execution?
- [ ] Do you have complete audit trails linking decisions to context?
- [ ] Can you update policy once and propagate to all agent instances?

If you cannot answer yes to all five questions, you need governance infrastructure before autonomous deployment.

</details>

<details>
<summary><b>For AI Agent Developers</b></summary>
<br>

The ten laws define what your agents need from deployment environments: integration with validation layers, participation in fleet governance, audit capabilities, and shadow mode support.

Your agents will be evaluated on these criteria. Consider partnerships with digital twin vendors to provide complete solutions.

</details>

<details>
<summary><b>For Standards Bodies and Regulators</b></summary>
<br>

The Industrial Agent Manifesto provides technology-agnostic governance requirements that can inform domain-specific standards. Whether for clinical decision support, automated building controls, or grid dispatch systems, the framework is universal while implementation is domain-specific.

The DTC is actively working with ISO/IEC JTC 1/SC 41, OMG SDO and industry-specific regulatory bodies to align these principles with emerging regulatory frameworks for autonomous industrial systems.

</details>

## From Manifesto to Standardization

The Industrial AI Agent Manifesto builds on the Digital Twin Consortium's existing body of work:

- [Digital Twin Capabilities Periodic Table](https://github.com/digitaltwinconsortium/capabilities-toolkit/tree/main/digital-twin-cpt): Maps what digital twins can do
- [AI Agent Capabilities Periodic Table](https://github.com/digitaltwinconsortium/capabilities-toolkit/tree/main/ai-agent-cpt): Maps what AI agents can do
- [Industrial AI Agent Manifesto](https://github.com/digitaltwinconsortium/Industrial-Agents): Defines how they must work together safely
- [The Industrial Internet of Things Trustworthiness Framework Foundations](https://www.iiconsortium.org/pdf/Trustworthiness_Framework_Foundations.pdf)

This document introduces the concepts of the more detailed companion document: [Industrial AI Agent Manifesto (PDF)](DTC_TechBrief_IndustrialAgentManifesto.pdf), which represents the first phase of a holistic governance framework for AI Agent Deployment, with future documents to be released.

DTC members, including, NIST, MITRE, TUV SUD, Academia and Research Institutions, and others are already working in collaboration to further develop this framework.

**Collaboration:** Organizations that want to explore collaboration opportunities can reach us at [agent_governance@engage.digitaltwinconsortium.org](mailto:agent_governance@engage.digitaltwinconsortium.org)

**Next Phases:**

| Phase | Description |
|-------|-------------|
| **Domain-Specific Implementation Guidance** | Working with DTC vertical working groups (Healthcare, AECO, Aerospace, Manufacturing, Energy, and others) to develop domain-specific implementation guides. |
| **Standards Development** | Partnering with ISO/IEC, IEC TC65, and IEEE to formalize governance requirements into industry standards. |
| **Verification Frameworks** | Collaborating with independent verification organizations to develop compliance testing procedures for manifesto-aligned implementations. |
| **Reference Architectures** | Publishing reference implementations showing how digital twin platforms can implement the Ten Laws in practice. |

## The Real Question

Autonomous AI agents are no longer optional. Healthcare needs them for treatment optimization. Buildings need them for energy efficiency. Grids need them for stability management. Manufacturing needs them for quality and throughput. Aerospace needs them for mission complexity.

The question is not whether to deploy them. The question is whether you will deploy them with governance infrastructure that can prove they are safe.

That requires reproducible context, domain constraints as architectural boundaries, validation before execution, complete audit trails, and fleet-scale policy management. These are not nice-to-haves. They are the difference between autonomous operations and accidents waiting to happen.

Digital twins provide proven architectures for these governance capabilities across domains. They aren't the only possible solution. But they are already deployed, already maintaining operational models and already enforcing domain constraints. The governance capability exists. It needs to be recognized and formalized.

Organizations deploying agents without this governance infrastructure, regardless of how they implement it, are accepting risks that no responsible operator should accept.

## About the Digital Twin Consortium

The Digital Twin Consortium, a community of the Enterprise Data Management Association (EDMA) enables organizations move from digital twin concepts to real-world practice. With over 200 members across industry, academia, government, and technology providers, the DTC develops standard requirements, reference architectures, and implementation guidance across more industry working groups.

**Primary Contributors:** This manifesto was developed by the Digital Twin Consortium Composability Framework Working Group with lead authorship by Pieter van Schalkwyk (XMPro) and contributions from Sean Whiteley (Axomem) and editorial revisions by Dan Isaacs (DTC CTO) and Will Thompson (DTC).

*Opinions expressed in this content are solely those of the authors and do not necessarily represent those of the Digital Twin Consortium, EDMA or any other related parties.*

---

<p align="center">Version 1.0 | February 2026 | <a href="LICENSE">CC BY-SA 4.0</a></p>
