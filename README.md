# Valkyrie-4 LEO Constellation
### Single-Launch Deployment & In-Plane Phasing Design
**Colorado State University — M.Eng Aerospace Engineering — Dec 2025**

---

## Mission Overview

Valkyrie-4 is a four-satellite low-Earth orbit (LEO) Earth-imaging constellation 
designed to achieve rapid-revisit coverage over a target region using a single 
launch vehicle. The mission architecture minimizes cost by eliminating plane-change 
maneuvers entirely, achieving in-plane phasing through timed loiter sequences.

| Parameter | Value |
|---|---|
| Constellation size | 4 satellites |
| Launch vehicle delivery orbit | 200 km circular parking orbit |
| Deployment orbit | 300 km circular |
| Operational orbit | 800 km circular, 28.5° inclination |
| Total spacecraft ΔV | ~266 m/s per satellite |
| Upper-stage ΔV | ~60.5 m/s |
| Phasing method | In-plane loiter (no plane change) |

---

## Mission Architecture

### Launch & Deployment Sequence
```
Launch Vehicle
     │
     ▼
200 km Parking Orbit (satellite stack)
     │
     ▼  Two-burn upper-stage transfer
300 km Deployment Orbit
     │
     ├── Satellite 1 → 1 revolution loiter → finite-burn insertion → 800 km ops orbit
     ├── Satellite 2 → 3 revolution loiter → finite-burn insertion → 800 km ops orbit  
     ├── Satellite 3 → 6 revolution loiter → finite-burn insertion → 800 km ops orbit
     └── Satellite 4 → 9 revolution loiter → finite-burn insertion → 800 km ops orbit
```

Each satellite performs a different number of loiter revolutions at the deployment 
orbit before executing a finite-burn insertion to the shared 800 km operational orbit. 
This timed phasing achieves equal angular spacing across the constellation without 
requiring any plane-change maneuvers.

---

## Tools & Methods

| Tool | Application |
|---|---|
| **STK Astrogator** | Trajectory design, finite-burn maneuver modeling |
| **STK Targeting** | Differential corrector convergence for all trajectory segments |
| **STK Coverage Analysis** | Revisit time validation over target region |
| **MATLAB** | ΔV budgeting, mission parameter trade studies |

---

## Key Results

- **In-plane phasing achieved** for all 4 satellites without plane-change maneuvers
- **Total spacecraft ΔV ≈ 266 m/s** per satellite across full deployment sequence
- **Upper-stage ΔV ≈ 60.5 m/s** for parking-to-deployment orbit transfer
- **All trajectory segments validated** using Astrogator's differential corrector targeting
- **Rapid-revisit coverage** demonstrated over target region at 800 km operational orbit

---

## Trajectory Validation

All trajectory segments were validated using STK Astrogator's differential corrector 
targeting. The targeting sequence converged for each satellite's loiter + insertion 
profile, confirming feasibility of the single-launch deployment architecture.

The differential corrector approach was chosen over impulsive maneuver approximations 
to accurately model finite-burn duration effects at the low thrust levels representative 
of small satellite propulsion systems.

---

## Mission Design Decisions

**Why single-launch?**
Reduces mission cost significantly by eliminating the need for multiple dedicated 
launches or rideshare coordination. All four satellites are delivered to the deployment 
orbit by a single upper stage.

**Why in-plane phasing via loiter?**
Plane-change maneuvers at LEO altitudes are extremely ΔV-expensive. By deploying 
all satellites into the same orbital plane and using timed loiter sequences to achieve 
angular separation, the architecture eliminates this cost entirely.

**Why 800 km operational orbit?**
Balances ground resolution requirements against orbital lifetime and radiation 
environment. 800 km provides sufficient altitude for reasonable coverage swath 
while remaining below the primary Van Allen belt.

---

## Skills Demonstrated

`STK Astrogator` `STK Targeting` `Orbital Mechanics` `Constellation Design`
`Trajectory Optimization` `ΔV Budgeting` `Finite-Burn Maneuver Modeling`
`Differential Corrector Targeting` `Coverage Analysis` `Mission Architecture`
`MATLAB` `LEO Mission Design`

---

## Project Report

Full technical report available upon request.
*Contact: faisalsyed737@gmail.com*

---

## Author

**Faisal Zohad Sayyed**
M.Eng Aerospace Engineering — Colorado State University
[LinkedIn](https://www.linkedin.com/in/faisalzsayyed/) | 
[GitHub](https://github.com/faisalzsayyed)
