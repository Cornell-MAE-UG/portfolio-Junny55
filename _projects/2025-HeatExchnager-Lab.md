---
layout: project
title: Heat Exchnager Lab
description: Class project
technologies:
image: /fa25-portfolio-Junny55/assets/images/Picture1.png
---

The plate heat exchanger used in this activity consists of two separate flow paths, labeled 1–2 and 3–4, through which hot and cold water circulate without mixing. Hot water from a bucket heated by the heater is pumped through one flow path, while cold water from an ice-cooled reservoir flows through the other. The fluids pass through alternating channels separated by thin metal plates, allowing heat to transfer through conduction across the plates and convection within each flowing stream. Thermometers placed in each reservoir measures the inlet and outlet temperatures, and food dye helps distinguish the two streams. When the pumps run, heat flows from the hotter water to the colder water, increasing the cold stream’s temperature while decreasing the hot stream’s temperature.

The operation of the heat exchanger can be described using a steady state CV model. Because there is no mass mixing and no mechanical work, the mass flow entering each side equals the mass flow exiting, and the heat lost by the hot stream equals the heat gained by the cold stream. This energy balance takes the form:
m ̇_h c_p (T_(h,in)-T_(h,out))=m ̇_c c_p (T_(c,out)-T_(c,in))

Entropy generation is determined by the entropy changes of each stream and is minimized when the temperature difference between the fluids is maintained efficiently along the exchanger. The two possible flow arrangements—parallel flow (same direction) and counter-flow (opposite directions)—create different temperature profiles, which strongly influence heat-transfer effectiveness.

The experimental results show that counter-flow operation is significantly more effective. In counter-flow, the cold stream warmed from 6.5°C to 26.5°C while the hot stream cooled from 45.5°C to 21.5°C, yielding large temperature changes and strong heat transfer. In parallel flow, the cold stream warmed only from 7.6°C to 23°C and the hot stream cooled from 41.6°C to 26.5°C. Counter-flow maintains a larger and more uniform temperature difference along the exchanger, producing a greater log-mean temperature difference and lower entropy generation, which enhances performance. Thus, changing the operating mode from parallel to counter-flow directly improves the exchanger’s thermal effectiveness and demonstrates the importance of flow configuration in heat-exchanger design.

Test Result [Unit:Celcius]:
    Counter Flow:
        T_cold_initial = 6.5
        T_hot_initial = 45.5

        T_cold_final = 26.5
        T_hot_finial = 21.5

    Parallel Flow:
        T_cold_initial = 7.6
        T_hot_initial = 41.6

        T_cold_final = 23
        T_hot_finial = 26.5


        