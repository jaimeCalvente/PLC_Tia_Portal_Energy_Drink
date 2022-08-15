# PLC_Tia_Portal_Energy_Drink
Program designed to control an energy drink plant with modular programming in Awl, Scl and Fbd.
## Project Description
This project has been created to simulate the production plant of an energy drink.

The process consist of **three main tanks**, containing water, flavours and other conservants. Every individual tank has been implemented with a common "**FC_Tank_Level**" with a **filling** (open-close) **valve** and **discharge** (proportional) **valve** , which are in charge of filling and emptying the tanks independently of each other, depending on the level of the tank and the system`s demands.

A **conveyor belt** to transport the ingredients to a **mixer tank**, in which, the ingredients will be blended with sirupes and caffeine controlled by their own proportional valves and a **frecuency driver**.
![](EnergyDrink/Hmi_Img/GeneralProcess.png)
## Project operation walk through
The recipe contains all the necessary infomation to make the production of a specific batch. Once a recipe has been placed on the **HMI panel** and the operator validates it by pressing the "Start" button, the process can begin. In case of any mistakes when entering the recipe data, the operator can press the "Reset" button to clear the previous action and enter the new valid data.
### Tanks level management
if the tanks are empty, they will start filling to their **pre-configure setpoints** (which could be different). Once the low level has been reached, the tanks are operationally ready and the production of the batch can begin. In the meantime, the tanks will keep their valves opened until the maximum level is triggered.

**Discharge valves** are commanded by the **demands** of the system at that point in time and the **level** of every tank. If the level is **too low** the proportional valve will close. On the other hand, if the level is **whithin parameters**, the valve will open proportionally to the actual demand.

### Product weighing management
