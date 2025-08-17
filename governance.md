# SALI Governance Model (Lightweight, Layered, Transparent)

Purpose
- Provide a minimal, nested, and transparent governance structure for the SALI community and the Legal Matter Standard Specification (LMSS).
- Balance agility (working groups, lazy consensus) with quality and accountability (Editorial Council, Steering Committee, Board).

At‑a‑glance structure (nested)
- Board of Directors
  - Standards Steering Committee (SSC)
    - Editorial Council (EC)
      - Maintainers (per repository)
      - Working Groups (WGs)
        - Topic/Domain subgroups (optional, time‑boxed)
  - Secretariat (Index.io) supports all layers operationally

Decision flow (summary)
- Minor, within a WG’s charter → Lazy consensus in WG → Maintainer merge after CI passes → Logged.
- Structural/taxonomy‑wide or cross‑WG → EC review/approval → Maintainer merge.
- Breaking changes or major policy/licensing → SSC approval (supermajority) → Board ratification.
- Appeals path: WG → EC → SSC → Board.

Transparency defaults
- Open issues/PRs, public agendas/minutes (posted within 3 business days), decision log, labeled approvals in GitHub.
- Monthly operations dashboard from Secretariat.

---

## 1) Board of Directors

Purpose
- Strategy, fiduciary oversight, brand/IP stewardship, and ultimate accountability for SALI.

Scope and decision rights
- Approves: annual plan/budget, licensing/IPR policy, Code of Conduct, breaking‑changes policy, MAJOR version releases (ratification).
- Appoints: SSC members/chair, EC liaison or confirms EC slate, Secretariat Lead (Index.io).
- Final appeal body for disputes and CoC escalations.

Composition and terms
- 5–9 directors; balanced representation across firms, clients, vendors, academia/public interest.
- Terms: 2 years, staggered; renewable by vote.
- Conflict of interest: declare annually; recuse when directly interested.

Cadence and artifacts
- Meets at least quarterly; may convene ad hoc for ratifications.
- Receives monthly ops dashboard and quarterly roadmap from SSC.
- Publishes: Board resolutions (public summaries), ratifications, annual report.

Interfaces
- Receives proposals for policy and breaking changes from SSC.
- Provides oversight to Secretariat; conducts annual review of SSC/EC effectiveness.

---

## 2) Standards Steering Committee (SSC)

Purpose
- Owns the LMSS product direction: roadmap, prioritization, release planning, and cross‑WG coordination.

Scope and decision rights
- Sets/updates: roadmap, release calendar, prioritization across WGs.
- Approves: major policy updates related to taxonomy governance; MAJOR version proposals (supermajority, then Board ratification).
- Resolves: cross‑WG conflicts, resourcing priorities.
- Charters: creates/renews/closes WGs; appoints WG chairs.

Composition and terms
- 7–11 members; multi‑stakeholder mix; includes one EC liaison.
- 1‑year terms, renewable; mix of appointed and elected seats as defined in GOVERNANCE.md.

Cadence and artifacts
- Meets monthly (decision meeting) and quarterly for roadmap review.
- Publishes: roadmap, release plan, WG roster, policy updates, decisions to decision log.

Interfaces
- Receives: EC recommendations for structural/breaking changes; WG status and risks.
- Provides: guidance and priorities to WGs and Maintainers; escalations to Board when required.

---

## 3) Editorial Council (EC)

Purpose
- Editorial authority for taxonomy content quality, identifiers, style, deprecations, and errata.

Scope and decision rights
- Approves: release candidates for MINOR/PATCH versions; deprecations/removals per policy.
- Owns: Editorial Style Guide, identifier conventions, acceptance criteria for content.
- Manages: errata and non‑breaking corrections between releases.
- Recommends: MAJOR/structural changes to SSC with impact analysis.

Composition and terms
- 5–9 subject‑matter editors; appointed with SSC concurrence; one member acts as ombudsperson for dispute mediation.
- 1‑year terms; renewable; domain expertise and demonstrated contributions.

Cadence and artifacts
- Meets monthly (decision meeting); async reviews via GitHub.
- Publishes: release approvals, errata list, style guide updates, deprecation/migration notes.

Interfaces
- Works closely with Maintainers (merge gates) and WG chairs (shepherding proposals).
- Elevates structural proposals to SSC; mediates content disputes before escalation.

---

## 4) Working Groups (WGs)

Purpose
- Deliver focused, time‑boxed domain work (e.g., Courts, Matter Types, Crosswalks, Tooling/Validation).

Scope and decision rights
- Within charter: propose and approve minor changes via lazy consensus; submit RFCs for larger changes.
- Out of scope: licensing/policy decisions; breaking taxonomy changes without EC/SSC approval.

Composition and terms
- Open membership; chair (and optional co‑chair) appointed by SSC.
- Charters run 6–12 months with defined deliverables and sunset/review dates.

Cadence and artifacts
- Meets biweekly or monthly; posts agendas and minutes within 3 business days.
- Produces: RFCs, issues/PRs, draft term sets/crosswalks, user guidance.

Process (lazy consensus defaults)
- Minor issues: 7‑day window; RFCs/cross‑WG topics: 14‑day window.
- Substantive -1 objections trigger revise‑and‑reset or mediation by chair → EC if unresolved.

---

## 5) Maintainers (per repository)

Purpose
- Day‑to‑day stewardship of repos: hygiene, CI, reviews, merges, releases.

Scope and decision rights
- Enforces: contribution and editorial standards; CI “green” requirement.
- Merges: minor changes with WG consensus; EC‑approved content; tags releases per policy.
- Gates: blocks merges lacking required approvals (EC/SSC labels for structural/MAJOR).

Composition and terms
- Appointed by EC/SSC; least‑privilege access; quarterly access reviews.
- May be distinct for data vs tooling repos.

Cadence and artifacts
- Triage SLA: respond to new issues within 2 business days.
- Publishes: release tags/notes, CHANGELOG updates, CI status summaries.

Interfaces
- Coordinates with WG authors on PR readiness; requests EC review when needed.
- Reports repo health and blockers to EC/SSC and Secretariat.

---

## 6) Secretariat (Index.io)

Purpose
- Provides operations, program management, tooling/CI, comms, metrics, volunteer support; executes policy without setting it.

Scope and responsibilities
- Meeting ops (scheduling, agendas, minutes), issue/PR triage, CI stewardship, release engineering support.
- Website/docs updates, community comms, analytics, surveys/interviews, volunteer onboarding/recognition.
- Maintains decision log, governance repo, and monthly dashboard.

Authority
- May pause merges that violate process/CI; cannot approve policy or content beyond documented gates.

Cadence and artifacts
- Biweekly SALI–Secretariat sync; monthly ops dashboard; quarterly community report.

Interfaces
- Supports all bodies; maintains alignment and transparency across layers.

---

## Cross‑layer policies (applies to all)

Decision recording
- Every decision gets an ID and entry in DECISIONS/decision-log.md with link, status, and date.

Quorum and thresholds
- EC simple majority (quorum = 50%+1) for approvals.
- SSC supermajority (≥ 2/3) for breaking changes/MAJOR and major policy updates; simple majority for routine matters.
- Board majority for ratifications; can require supermajority for licensing/CoC.

Escalation and timelines
- WG → EC → SSC → Board; each step acknowledges within 3 business days and aims to decide within 10 business days (unless an announced public comment window is open).

Conduct and moderation
- Code of Conduct applies in all spaces; graduated sanctions; ombudsperson named by EC for confidential mediation.

Access and security
- Org‑wide 2FA; least privilege; quarterly access reviews; CODEOWNERS for protected paths; branch protections and required checks.

Transparency SLAs
- Minutes posted within 3 business days.
- Issue triage within 2 business days.
- Monthly dashboard by the 5th business day.

Licensing and IPR
- Taxonomy/content under CC BY 4.0 or CC0; code under Apache‑2.0 or MIT; contributions via DCO sign‑off.
- Crosswalks: verify target scheme licensing; include required attribution/version pinning.

Metrics and monitoring
- Community: active contributors, PRs opened/merged, time‑to‑first‑response, new contributors.
- Quality: CI pass rate, data‑quality checks, deprecation coverage.
- Adoption: downloads, site traffic to spec pages, implementer directory growth.

Amendments to this model
- Proposed via RFC with a 14‑day public comment window.
- Requires SSC approval; Board ratification; changes documented in decision log and GOVERNANCE.md.

---

## Relationship Map (who informs/approves whom)

- Board
  - Ratifies: MAJOR releases, licensing/CoC/policy changes.
  - Appoints: SSC, EC liaison, Secretariat Lead.
  - Receives: monthly dashboard; quarterly roadmap.

- SSC
  - Approves: WG charters; breaking changes; major governance updates.
  - Directs: roadmap/priorities to WGs and Maintainers.
  - Receives: EC recommendations; WG statuses; Secretariat reports.

- EC
  - Approves: release candidates (MINOR/PATCH); editorial standards.
  - Directs: Maintainers on editorial gates; advises WGs.
  - Receives: WG proposals; Maintainer signals on content quality.

- WGs
  - Produce: RFCs, proposals, PRs; validate with users.
  - Use: lazy consensus for minor changes; escalate structural to EC.

- Maintainers
  - Enforce: CI and policy gates; merge/tag releases.
  - Coordinate: with WGs/EC; report health to SSC/Secretariat.

- Secretariat
  - Orchestrates: meetings, records, CI/tooling, comms, metrics.
  - Gates: process compliance; enables transparency for all.

---

## Change Type Examples and Required Path

- Typo fix, synonym addition, non‑controversial definition tweak (within WG scope)
  - WG lazy consensus → CI green → Maintainer merge → Log decision.

- New term set within an existing domain (non‑breaking)
  - WG RFC (14 days) → EC approval → CI green → Maintainer merge → Release (MINOR).

- Restructuring a hierarchy, renaming identifiers, or changing identifier policy (breaking)
  - WG RFC → EC analysis and recommendation → SSC supermajority approval → Board ratification → Migration plan → Release (MAJOR).

- New crosswalk to an external scheme
  - Crosswalks WG draft + licensing check → EC review for mapping quality → CI validation → Maintainer merge → Release (MINOR or PATCH).

- Governance/policy update (e.g., decision windows, contribution rules)
  - RFC → 14‑day comment period → SSC approval → Board ratification (if major) → Publish.

---

## Lifecycle of a Working Group (WG)

1. Proposal
- Sponsor submits WG charter using WG_CHARTER_TEMPLATE.md.
- SSC reviews/approves; appoints chair; sets sunset/review date.

2. Launch
- Repo labels, meeting cadence, issue templates created.
- Kickoff meeting; backlog seeded; success metrics confirmed.

3. Execution
- Biweekly/monthly meetings; lazy consensus on minor changes; RFCs for larger items.
- Regular demos/check‑ins with EC; Secretariat posts minutes.

4. Review and Sunset
- Midpoint review with SSC; adjust scope if needed.
- At sunset, deliver final outputs; recommend continuation or closure.
- Archive or graduate outputs into core repos; document lessons learned.

---

## Roles at a Glance (summary)

- Board: strategy, fiduciary, final appeal, ratifications.
- SSC: roadmap, prioritization, cross‑WG coordination, MAJOR approvals.
- EC: editorial quality, identifiers, deprecations, release candidate approval.
- WGs: domain development, RFCs, user feedback, minor approvals via lazy consensus.
- Maintainers: repo hygiene, CI gates, merges, releases.
- Secretariat: operations, CI/tooling, comms, metrics, volunteer enablement.
