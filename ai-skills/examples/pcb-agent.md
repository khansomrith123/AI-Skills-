# PCB Agent Example

## Scenario

User: "Design a simple ESP32 sensor breakout PCB with I2C sensor"

## Expected Behavior

1. **Analyze** → PCB hardware design
2. **Discover** → `pcb-engineering` matches
3. **Load** → Read full skill
4. **Understand** → Electrical specs, size, interfaces, constraints
5. **Plan** → Schematic blocks, power, decoupling, stackup, design rules
6. **Build** → Schematic + layout, footprints verified, DRC-aware
7. **Review** → Safety, DFM, grounding, BOM
8. **Deliver** → Explicit status. Must state: Designed and Reviewed. Simulated/Tested/Manufactured only if actually done.

## Critical

Engineering honesty: Agent must never claim physical testing or manufacturing. Should state "This is a design only; electrical validation requires physical prototyping."

## Skills Used

- Primary: `pcb-engineering` (v1.0.0)
- Secondary (if circuit analysis deep): `electronics` (optional)

---

*Example demonstrates hardware design with strict honesty requirements.*