# Multi-Skill Agent Example

## Scenario

User: "Build a secure web dashboard that reads data from an IoT device with custom PCB"

## Project Type

Cross-domain: Web application + IoT hardware

## Skills Selection

- **Primary:** `web-development` – Dashboard UI, API, auth, data display
- **Primary/Supporting:** `pcb-engineering` – Custom PCB for IoT sensor/device
- **Secondary:** `electronics` – Circuit analysis if needed
- **Secondary:** `embedded-systems` – Firmware context (if mentioned in future)
- **Cross-cutting:** `security` – Auth, API security, secure comms

## Orchestration Steps

1. **Understand** – Split into web + hardware domains. Identify shared requirements (data format, comms).
2. **Plan** – Unified plan with clear boundaries. Define API contract between device and dashboard.
3. **Build** – Domain-specific work per skills. Keep interfaces consistent.
4. **Integrate** – Ensure PCB outputs align with embedded comms; API matches frontend.
5. **Test** – Domain tests + integration check (conceptual for hardware).
6. **Review** – QA each skill + cross-domain coherence + priority compliance.
7. **Deliver** – Unified response with honest status per domain.

## Priority Application

- Safety/security first (hardware safety + web security)
- User requirements and shared contract
- Resolve conflicts by priority
- Avoid duplication

## Notes

- Each domain states its own status honestly (hardware: design only unless tested)
- Composition respects boundaries
- Minimal skill set selected

---

*Demonstrates PROJECT_SKILL_TEMPLATE principles.*