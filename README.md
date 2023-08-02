# Tafiti Comms System

This is the repo containing contents of the Tafiti Communication System. This system is built under the sponsorship of the Kenya Space Agency.

<div style="display: flex; flex-direction: row;">
  <figure style="margin-right: 0px;">
    <img src="/COMMS/Work Images/GroundTerminal3D.png" alt="Tafiti Onboard Terminal" style="width: 500px;height:510px;">
    <figcaption>Tafiti Ground Terminal 3D Model complete</figcaption>
  </figure>
  <figure style="margin-right: 0px;">
    <img src="/COMMS/Work%20Images/ground3DBack.png" alt="Tafiti Onboard Terminal" style="width: 500px; height:510px;">
    <figcaption>Tafiti Ground Terminal 3D Model from the back</figcaption>
  </figure>
  <figure>
    <img src="/COMMS/Work%20Images/Onboard Comms 3D 2.png" alt="Tafiti Onboard Terminal" style="width: 500px; height:510px;">
    <figcaption>Tafiti Onboard Terminal 3D Model. Awaiting dimensions.</figcaption>
  </figure>
</div>

## Work Still to be done
- Get the stacking dimenisons for the onboard communication system from the Structural Engineering team.
- Adding PC104 Connectors and assigned pins from main bus.
- ~~Adding 3D models of the sx1278 Ra-02.~~ Done
- ~~Adding Logo, Subsytem name, members and more information~~
- ~~Verify accuracy and requirements fulfilment~~ Done
- ~~Confirm that the PCB meets the EMC and EMI standards and that it is well designed.~~ Done

(The above tasks should be done and marked as done beside the task)


## Hardware Designed By:
- Gerald Mbuthia - Hardware Designer

## Purpose

To provide a communication channel to transfer data to and from the Tafiti Nano-satellite.
The data to be transferred includes:
- Image data
- Housekeeping data
- Commands

## Requirements
- Receive housekeeping data from the OBC. This data will effectively be a collection of data from all other subsystems.
- Receive payload data from the Payload subsystem.
- Provide a communication link for the transfer of housekeeping data and payload data from the Cubesat to the 
ground terminal. 
- Provide a link to send telecommands from the ground to the cubesat. This will be a bi-directional communication.
- Provide an interface to view received data and key in commands.
- Allow for data storage onboard the cubesat and on the ground station.
- Provide an API to transfer data over Web.
- Should be portable.
- Data transfer rates should be fast atleast 500kB/s.
- Long range communication.
## Development procedure
### PCB Assembly:
1. Component Procurement:

Identify the required components for the PCB assembly, including PC104 connectors and other passive and active components.
Create a Bill of Materials (BOM) with detailed part numbers, quantities, and sourcing information for each component.

2. PCB Manufacturing:

Submit the finalized PCB design files, including the PC104 connectors and assigned pins, to a reputable PCB manufacturing service.
Review the design with the PCB manufacturer to ensure it meets all manufacturing requirements.

3. PCB Assembly:

Choose a reliable and experienced PCB assembly service or manufacturer.
Provide the assembled PCBs, solder paste, and all required components to the assembly service.
Ensure that the components are properly placed and soldered on the PCB according to the design guidelines.
Perform quality checks and inspections on the assembled boards to identify any defects or issues.

4. Testing and Debugging:

Develop a comprehensive test plan to verify the functionality of the assembled PCB.
Test each module individually and in combination to validate proper communication and functioning.
Use tools such as oscilloscopes, logic analyzers, and multimeters to aid in testing and debugging.

5. Packaging and Shipment:

Once the PCB assembly is successful, package the completed boards securely for shipment or further integration into the final product.
Ensure that all necessary documentation, including schematics, assembly drawings, and testing procedures, are provided along with the assembled PCBs.

## Software Development
1. Setting up Development Environment:

Install the necessary software tools and development environment for the STM32H743 board, such as STM32CubeIDE or other compatible IDEs.
Configure the development environment to support the STM32H743 microcontroller.

2. Board Bring-up:

Develop a basic firmware to initialize the STM32H743 board, including setting up clock configurations, GPIOs, and system peripherals.
Verify the board bring-up by running simple test code to ensure the microcontroller is functioning correctly.

3. Peripheral Drivers:

Implement drivers for each module on the PCB, including the SX1278 LoRa module, microSD module, UART to USB converters, and any other peripherals used.
Test each driver individually to ensure proper communication and functionality.

4. Communication Protocols:

Implement communication protocols for data exchange between different modules.
For example, set up UART communication between the STM32H743 and the UART to USB converters for debugging and communication with a PC.
Utilize the SX1278 LoRa module to establish LoRa communication between devices.
Implement LoRaWAN or any other suitable LoRa protocol as per the project requirements.

5. Data Storage and Retrieval:

Develop routines to read and write data to the microSD module, enabling data storage and retrieval capabilities.

6. User Interface:

Develop a user interface to view received data and input commands.
Implement a graphical interface or command-line interface (CLI) based on project requirements.

7. Web API Development:

Implement an API to transfer data over the Web, enabling communication between the cubesat and the ground station.

8. Power Management:

Implement power management strategies to optimize power consumption based on the system's requirements.

9. Error Handling and Debugging:

Incorporate error handling mechanisms and debugging features to facilitate the identification and resolution of software-related issues.

10. Documentation:

Maintain comprehensive documentation throughout the development process, including code comments, system architecture, and user guides.

11. Quality Assurance and Optimization:

Perform code reviews and optimize software performance to ensure efficient and reliable operation.

12. Final Testing and Deployment:

Conduct thorough testing of the integrated system to validate its functionality and stability under different scenarios.
After successful testing, deploy the software on the STM32H743 board as part of the final product.
## Testing and Data