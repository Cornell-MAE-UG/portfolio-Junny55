---
layout: project
title: MAE2250 Open Design Project
subtitle: Group project focusing on the lanternfly infestation and their effects on the grape industry
date: 2026-02-20
image: /assets/images/portfolio-placeholder.jpg
---

## Overview

This is a group engineering design project focused on addressing the **spotted lanternfly infestation** problem and its significant impact on the grape industry. The project applies open design principles to develop innovative solutions to mitigate the economic and environmental damage caused by these invasive pests.

---

## Project Details

### Type
Group Engineering Design Project

### Status
**Proposal Phase** - Client requirements and design brief established

### Semester
Spring 2026

---

## Team & Clients

Team: Pest Control  
Clients: Cornell CALS Extension / E&J Gallo Winery / National Grape

## Problem

Viticulturalists in New York State are affected by the spotted lantern fly infestation, an invasive species that contaminates the harvest. Batches are rejected from juiceries and wineries, resulting in economic loss. Traditional pest-control methods are insufficient. Pesticides come with high economic and environmental costs. Egg removal proves too difficult because of the massive scale of laying locations, costing too much in labor.

## Impact

Reducing SLF contamination in harvest improves economic output. Currently, farmers rely on insecticide rotations, but a mechanical device would offer a low-chemical alternative and reduce the cost of expensive sprays while meeting the growing consumer demand. 

---

## Solution

Centrifugal Density Separator - A high-speed rotation device that separates harvested grapes from SLF by density, removing them from the desired product.

## How to Implement

Harvest is loaded into the device, and an internal drum spins at a calculated RPM. Heavier grapes are pushed out furthest, sliding down the angled outer walls into a collection bin. Lighter insects get pulled into a secondary bag. This way, grape pulp is conserved without contamination.

## Why It's Better Than the Status Quo

Pesticides leave a taint on the wine's taste profile and contaminate the organic integrity of the grapes. Manual sorting is slow, costly, and prone to human error/inconsistencies. Our solution is non-chemical and efficient on a large scale.

## End-of-Semester Proof-of-Concept

A benchtop rotating drum prototype using grapes and 3D printed SLF accurate to weight and size, allowing us to optimize RPM. Success is determined by comparing the percentage of pests (SLF models) successfully sorted with the percentage of harvest lost.

## Key Risks/Unknowns

### Damage to Grapes

A high RPM exerts a force on the grape skin, possibly causing the grapes to break apart. Assessing the damage to grapes requires a physical "Burst Test," spinning grapes at incremental RPMs to identify when skins rupture, then comparing our results to the RPM needed to separate SLF.

### Mass Variation and Obstructions

While a dry lanternfly is less dense than a grape, a lanternfly soaked in grape juice is much denser. Similarly, an SLF wedged inside a tight cluster might not separate easily, resulting in less effective separation. We can test this by using "weighted" objects (3D-printed bugs with adhesive, SLF tucked inside dense clusters or higher-density SLF), measuring SLF removed per cycle at various degrees of obstruction.

### Processing Time

A centrifuge is often a batch process, and if the device takes too long to load, spin, and unload, farmers will reject it in favor of faster methods. To address this, we will test the time the cycle duration of our prototype, and calculate the throughput to compare it to standard manual sorting speeds.

## Questions for the Client

**How much material other than grapes, like stems and leaves, typically remains in the bin after your primary harvest?** This changes our separation threshold and testing parameters based on what we want to separate/how much grapes weigh.

**What is the maximum holding time allowed between the grape being picked and it reaching the crusher before you worry about quality loss?** This determines the constraints of our time trials and whether or not our product is viable in the time scale of grape processing.

**Do the SLF tend to stay on the surface of the grape clusters when disturbed, or do they retreat deep into the center of the bunch?** This affects the "ramping profile" (i.e. how fast we accelerate) based on how hard SLF tends to stay on grapes, and also how we simulate SLF in our separation experiments.

**What reservations does this idea leave you with as a client?** (Any issues we haven't thought of?)

---

## References

Penn State Agricultural Division. "Spotted Lanternfly." Penn State Extension, extension.psu.edu/spotted-lanternfly.

Penn State Agricultural Division, "Spotted Lanternfly Management in Vineyards." Penn State Extension, extension.psu.edu/spotted-lanternfly-management-in-vineyards.

Department of Environmental Conservation, NYS. "Spotted Lanternfly - NYDEC." Dec.ny.gov, 16 Mar. 2017, dec.ny.gov/nature/animals-fish-plants/spotted-lanternfly.

---

## Contact & Questions

For inquiries about this project:
- **Email**: [jk2964@cornell.edu](mailto:jk2964@cornell.edu)
- **Phone**: +949 945 0352

---

*This portfolio entry is part of Junseok Kang's MAE undergraduate portfolio and demonstrates the application of open design principles to real-world agricultural engineering challenges.*
