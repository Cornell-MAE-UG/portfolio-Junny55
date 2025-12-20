---
layout: project
title: Turbocharger Analysis_MAE 2210 Thermodynamics
description: By Junseok Kang_jk2964
technologies:
image: /assets/images/A-schematic-of-a-turbocharging-system.png
image: /assets/images/Turbocharger_System%20Diagram.png
image: /assets/images/S400SX%20Turbocharger.png
image: /assets/images/S400SX_Compressor%20Maps.png
---

<span style="font-size: 2.5em;"><strong>Introduction to Turbocharger, S400SX</strong></span>\
\
A turbocharger is a centrifugal compressor powered by a turbine, designed to increase an internal combustion engine's efficiency. Turbochargers force more air into the internal combustion engine so that it produces more power under the given piston displacement of the engine, which is a form of forced induction. In this report, I analyzed the turbocharger’s process through its thermodynamic modeling using steady state energy balance, mass balance, and isentropic ideal gas relations. Specifically, I analyzed and used data of the BorgWarner S400SX, which is a turbocharger engineered to handle massive mass flow rates and high-pressure ratios and used in competitive motorsports. 

<span style="font-size: 2.5em;"><strong>Qualitative Analysis of Turbochargers and Their Usage</strong></span>\
\
In order to increase its power output and efficiency, lots of internal combustion engine uses forced induction to deliver compressed air to their intake. Gas compressors, such as turbochargers and superchargers, are used to increase the pressure, temperature, and density of air in a forced induction engine. Turbochargers are one type of compressor often used for internal combustion engines, and they recover the thermal and kinetic energy from the engine’s exhaust gases that would otherwise be wasted. In a turbocharger, two radial airfoils rotate for its operation, one of which is a turbine blade and the other is a compressor blade. The turbine blade on the turbocharger extracts thermal and kinetic energy from the exhaust gases, which have a high temperature, and convert into mechanical shaft work, delivering the work to the compressor blade through the crankshaft between the compressor blade and the turbine blade. Then, the compressor blade increases the pressure, temperature, and density of the input air into the engine’s combustion chamber, which enhances the engine’s efficiency and the magnitude of power output. 

![Schematic of a turbocharging system](/assets/images/A-schematic-of-a-turbocharging-system.png)
*Figure 1: Schematic of a turbocharger.*

Since in a naturally aspirated engine, approximately one-third of the fuel's chemical energy is lost as thermal waste through the exhaust, and turbochargers exploit the portion of this wasted enthalpy, turbochargers are used in many fields that require high performance of the internal combustion engine, such as motorsports, high-performance commercial automobiles, lightweight aircraft, and industrial fields. The BorgWarner S400SX turbocharger is commonly used in high-performance and heavy-duty engines due to its large compressor flow capacity and high-pressure ratio capability.

<span style="font-size: 2.5em;"><strong>Thermodynamic Modeling of the Turbocharger</strong></span>


![Turbocharger System Diagram](/assets/images/Turbocharger_System%20Diagram.png)
*Figure 2: Turbocharger system diagram.*

**1.	Mass & Energy Balance in the Turbocharger’s Turbine**\
Steady State Mass Balance:

$$\dot{m}_t = \dot{m}_{\text{t,in}} - \dot{m}_{\text{t,out}} = 0$$
$$\dot{m}_{\text{t,in}} = \dot{m}_{\text{t,out}} = \dot{m}_{\text{exh}}$$


Steady State Energy Balance, assuming the turbocharger’s turbine is in an adiabatic process and assuming \( c_p \) is constant for the air in the process:

$$\dot{Q}_t = 0$$
$$\dot{E}_t = \dot{Q}_t - \dot{W}_t + \dot{m}_{\text{exh}} (h_{\text{t,in}} - h_{\text{t,out}}) = -\dot{W}_t + \dot{m}_{\text{exh}} c_p (T_{\text{t,in}} - T_{\text{t,out}}) = 0$$

 /
Thus, we can see that the turbine power comes from exhaust enthalpy:

$$\dot{W}_t = \dot{m}_{\text{exh}} c_p (T_{\text{t,in}} - T_{\text{t,out}})$$

For a turbocharger, since the turbine and the compressor are directly connected through a crankshaft, the mechanical work will be transferred from the turbine to the compressor. Moreover, since the turbine power output is the power input for the compressor, the sign is positive for turbine power but should be negative for the compressor power:

$$\dot{W}_t \approx -\dot{W}_c$$

**2. Mass & Energy Balance in the Turbocharger’s Compressor**\
Steady State Mass Balance:

$$\dot{m}_c = \dot{m}_{\text{c,in}} - \dot{m}_{\text{c,out}} = 0$$

$$\dot{m}_{\text{c,in}} = \dot{m}_{\text{c,out}} = \dot{m}_a$$

Steady State Energy Balance, assuming the compressor is in an adiabatic process and assuming \( c_p \) is constant for the air:

$$\dot{Q}_c = 0$$

$$\dot{E}_c = \dot{Q}_c - \dot{W}_c + \dot{m}_a (h_1 - h_2) = -\dot{W}_c + \dot{m}_a c_p (T_1 - T_2) = 0$$

Thus, we can write the actual compressor work and convert it into an equation about \( T_2 \), which is the compressor outlet temperature:

$$\dot{W}_c = \dot{m}_a c_p (T_1 - T_2) = -\dot{m}_{\text{exh}} c_p (T_{\text{t,in}} - T_{\text{t,out}})$$

$$T_2 = T_1 - \frac{\dot{m}_{\text{exh}}}{\dot{m}_a} (T_{\text{t,in}} - T_{\text{t,out}})$$

**3. Calculate Compressor Outlet Temperature**\
Let’s assume adiabatic compression in the turbocharger compressor as above, and assume the air in the process acts like an ideal gas. Therefore, we can use the isentropic ideal gas relation to calculate the isentropic compressor output temperature based on the pressure ratio of the turbocharger and the specific heat ratio of the air.\
Isentropic compressor outlet temperature:

$$T_{2s} = T_1 \Pi_c^{\frac{k-1}{k}}$$

Since the compressor process in the turbocharger won’t be reversible in real life, using the isentropic of the compressor, the actual compressor outlet temperature can be written like the following equation, where \( k \approx 1.4 \) for air and \( \eta_c \) can be taken directly from the compressor map:

$$T_2 = T_1 \left[ 1 + \frac{1}{\eta_c} \left( \Pi_c^{\frac{k-1}{k}} - 1 \right) \right] = T_1 - \frac{\dot{m}_{\text{exh}}}{\dot{m}_a} (T_{\text{t,in}} - T_{\text{t,out}})$$

Since S400SX maps use corrected airflow, I had to convert the corrected airflow into the actual airflow that is input to the turbocharger compressor, where 

$T_{\text{ref}} = 288 \text{ K}$ and $P_{\text{ref}} = 101.3 \text{ kPa}$:

$$\dot{m}_{\text{corr}} = \dot{m}_a \sqrt{\frac{T_{\text{c,in}}}{T_{\text{ref}}}} \cdot \left( \frac{P_{\text{ref}}}{P_{\text{c,in}}} \right)$$

$$\dot{m}_a = \dot{m}_{\text{corr}} \sqrt{\frac{T_{\text{ref}}}{T_{\text{c,in}}}} \cdot \left( \frac{P_{\text{c,in}}}{P_{\text{ref}}} \right)$$

<span style="font-size: 2.5em;"><strong>Specific Turbocharger, S400SX, Data and Modeling</strong></span>
 \
 \
The turbocharger’s steady-state thermodynamic model, which I’ve elaborated above, can be applied to the S400SX turbocharger using publicly available compressor map data. Key physical quantities of the turbocharger, such as mass flow rate, compressor outlet temperature, compressor power, and required turbine power, can be calculated using the thermodynamic model above.\

![S400SX Turbocharger](/assets/images/S400SX%20Turbocharger.png)
*Figure 3: BorgWarner S400SX turbocharger.*

![S400SX Compressor Maps](/assets/images/S400SX_Compressor%20Maps.png)
*Figure 4: S400SX compressor maps.*

From the S400SX compressor map available online, I could select a typical mid-efficiency operating point (400-900HP):
$$\Pi_c = 3.2$$
$$\dot{m}_{\mathrm{corr}} = 72 \, \frac{\mathrm{lb}}{\mathrm{min}} = 0.54 \, \frac{\mathrm{kg}}{\mathrm{s}}$$
$$\eta_c = 0.74$$

Initial conditions I set:
$$P_1 = 1 \, \mathrm{atm} = 101.3 \, \mathrm{kPa}$$
$$T_1 = 25^\circ \mathrm{C} = 298 \, \mathrm{K}$$
$$P_{\mathrm{ref}} = 101.3 \, \mathrm{kPa}, \, T_{\mathrm{ref}} = 288 \, \mathrm{K}$$

Thermodynamic constants I used, assuming the air in the process acts like an ideal gas, so that the ratio of specific heats and specific heats are constant:
$$k = 1.4$$
$$c_p = 1005 \, \frac{\mathrm{J}}{\mathrm{kg} \cdot \mathrm{K}}$$

Actual Compressor mass flow:
$$\dot{m}_a = \dot{m}_{\mathrm{corr}} \sqrt{\frac{T_{\mathrm{ref}}}{T_1}} \frac{P_1}{P_{\mathrm{ref}}} = 0.54 \sqrt{\frac{288}{298}} \cdot 1 = 0.53 \, \frac{\mathrm{kg}}{\mathrm{s}}$$

Isentropic outlet temperature:
$$T_{2s} = T_1 \Pi_c^{\frac{k - 1}{k}} = 298 \cdot 3.2^{\frac{0.4}{1.4}} = 415 \, \mathrm{K}$$

Actual outlet temperature, considering the compressor efficiency:
$$T_2 = T_1 \left[1 + \frac{1}{\eta_c} \left( \Pi_c^{\frac{k - 1}{k}} - 1 \right) \right] = 298 \left[1 + \frac{1}{0.74} (1.364 - 1)\right] = 445.7 \, \mathrm{K}$$

Compressor power needed for the S400SX turbocharger to operate at the selected operating point:
$$W_c = \dot{m}_a c_p (T_2 - T_1) = 0.53 \cdot 1005 \cdot (445.7 - 298) = 78.7 \, \mathrm{kW}$$

Assuming exhaust mass flow is approximately equal to intake air flow:
$$\dot{m}_{\mathrm{exh}} \approx \dot{m}_a = 0.53 \, \frac{\mathrm{kg}}{\mathrm{s}}$$
$$\dot{W}_c = \dot{m}_a c_p (T_1 - T_2) = -\dot{W}_t = -\dot{m}_{\mathrm{exh}} c_p (T_{(t,\mathrm{in})} - T_{(t,\mathrm{out})})$$

Solving for exhaust temperature drop, which represents recovered exhaust enthalpy that would otherwise be wasted in a naturally aspirated engine:
$$\Delta T_t = T_{(t,\mathrm{in})} - T_{(t,\mathrm{out})} = \frac{W_t}{\dot{m}_{\mathrm{exh}} c_p} = \frac{78.7 \cdot 1000}{0.53 \cdot 1005} = 147.8 \, \mathrm{K}$$

Engine inlet gas temperature increases due to the compression in the turbocharger, which can be calculated as follows:
$$\Delta T_c = T_2 - T_1 = 445.7 - 298 = 146.5 \, \mathrm{K} \approx \Delta T_t = 147.8 \, \mathrm{K}$$

This calculation shows that the exhaust temperature drop due to the turbocharger turbine and the inlet gas temperature increases due to the turbocharger compressor match their value, which was expected by the model. Furthermore, the exhaust temperature drop due to the turbocharger usually ranges between 150K and 200K, which implies that the thermodynamic model of the turbocharger in this report is plausible. 
