# PLC_Tia_Portal_Energy_Drink
Program designed to control an energy drink plant with modular programming in Awl, Scl and Fbd.
## Project Description
This project has been created to simulate the production plant of an energy drink.

The process consist of **three main tanks**, containing water, flavours and other conservants. Every individual tank has been implemented with a common "**FC_Tank_Level**" with a **filling** (open-close) **valve** and **discharge** (proportional) **valve** , which are in charge of filling and emptying the tanks independently of each other, depending on the level of the tank and the system`s demands.

A **conveyor belt** to transport the ingredients to a **mixer tank**, in which, the ingredients will be blended with sirupes and caffeine controlled by their own proportional valves and a **frecuency driver**.
![](EnergyDrink/Hmi_Img/GeneralProcess.png)
