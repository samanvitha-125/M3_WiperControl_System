# WIPER CONTROL SYSTEM

# ABSTRACT

Rainwater, dust, and exhaust gas compounds from vehicles that adhere to the surface of an automobile windshield are unlikely to be a problem as long as the driver has a clear view of the road. 
However, if the adhering chemicals are not dealt with, they will pose a danger to travel safety.

A windshield wiper system consists of two wiper arms and a wiper drive. The drive drives the two wiper arms over the windshield at an angle to give the driver and passenger a good view. 
The ideal cleaning outcome is ensured by an uniquely formed rubber wiping lip. 

Wipers are extremely important for driver visibility. If the wipers aren't working, the car is considered unsafe. The front wiper motor and transmission mechanism (linkage) are located underneath the windshield, under the cowl panel cover.

## DESCRIPTION

 - A Wiper Control System for an automotive wiper controls the operational speed of a wiper in accordance with rain conditions.It useful in the automotive unit the main purpose of the system is to clean the windscreen sufficiently to provide suitable visibility at all times.

# INTRODUCTION

 Wiper is an essential component that is used to wipe raindrops or any water from the windscreen. Wipers are designed and made to clear the water from a windscreen. Most cars have two wipers on the windscreen, one on the rear window and the other on each headlight. The wiper parts visible from outside the car are the rubber blade, the wiper arm holding the blade, a spring linkage, and parts of the wiper pivots. The wiper itself has about six parts called pressure points or claws that are small arms under the wiper
 
The existing system uses a control stalk to activate the wiper and the process of pulling up the wiper is difficult.r needs to switch on and off the control stalk and it will reduce the driver’s concentration during the driving. Thus, this system is proposed to solve all these problems. The concept of this wiper system is similar to other conventional wipers, yet this system will be upgraded to an automatic control system by using a controller.When water hits a dedicated sensor located on the windscreen, it triggers the wiper motor to move. is not detected by sensor, the wiper will automatically stop. This will help the driver to give more concentration and reduce the car accident probability. 

In this project, there were two innovations reviewed as the literature review. The two were designed with different concepts and operating mechanism however with same objective of working principle of the car wiper. The rain sensor was a highly versatile device for automatic wiping of vehicle windscreen when it is wet due to moisture, raindrops or even mud. It worked by reflecting harmonious light beams within the windscreen. When raindrops fall onto the windscreen, this harmony light is disturbed and creating a drop in the light beam intensity. The system then activated the wipers to be operated in full automatic mode. It has a response time of 0.1 seconds. It allowed for a quick reaction when it is a sudden splashes of water that will make the driver totally ‘blinds’ when the situation happened. With the automatic wiper, the driver can avert the risk of an accident. The automatic wiper is important during heavy traffic, e.g. in town, city, school zone and other public places. A driver may be subjected to many distractions with bad weather, dangerous road conditions and fatigue. The Rain Sensor reduced the driver’s burden by making driving more comfortable. Trailing a wet car is no longer a nuisance as detection of even 0.005 milliliters of water is possible. 

## COMPONENTS AND SUPPLIES:

1. STM32F407 Discovery Board
2. Push Button
3. LEDs
4. Resistors
5. Power Supply

## ADVANTAGES :

1. During rainy seasons, the irrigation system can be switched off to save money. As a result, electricity bills are reduced.
2. Water is saved during rain events by rain sensors, so water is available during summer and winter.
3. As a result, rain sensor-based systems such as car wipers and irrigation.
4. systems last longer by only running when necessary.
5. It is very simple to operate.
6. As a result, it uses less energy.
7. Installation of rain sensor based systems are very much simple.
8. Individual rain sensor costs very less.

## DISADVANTAGES :

 1. The rain sensor based system functions when water falls on the sensor directly.
 2. The cost of overall system increases as additional components are needed along with rain sensor.
 3. In order to avoid false detection of rain, it requires rain sensors to take decision after few minutes.


# Exploring STM32F407 Discovery Board

The main purpose of this project is to get an insight into the STM32F407 Discovery Board, which is an ARM Cortex M4 based Microcontroller. As I started working on STM32F07 Discovery Board, initially it was difficult and confusing to understand and program this microcontroller because understanding internal structures and working of the microcontroller using data sheet of STM32F407VGT MCU is difficult especially if one is a beginner.

                                                  Figure 1 : STM32F407 Discovery Board
![STM32 trun OFF](https://user-images.githubusercontent.com/101395036/167911226-a6e681ca-9aaf-40b8-9f76-92a28865968b.png)

This project gives almost all the basic information needed to get started with STM32F407 Discovery Board and also development of driver code.
1. Hardware Used : STM32F4 DISCOVERY kit, for more information visit: [STM32F4 DISCOVERY](https://www.st.com/en/evaluation-tools/stm32f4discovery.html)
2. Software Tool : STM32cubeIDE, for more information visit: [STM32CubeIDE](https://www.st.com/en/development-tools/stm32cubeide.html)
3. For installation of STM32CubeIDE refer [Youtube](https://www.youtube.com/watch?v=KOh-X_xpfC8&t=215s&ab_channel=RADAS)

Note : As this microcontroller has many advanced features and the main aim of this project is to get all basic insights, during the driver development only the required functionalities are added and other advanced functionality is not added. I may update the driver and other functionality in the future.

Please find the STM32F4 Discovery User Manual,STM32F4xxx Reference Manual (RM0090) and other related documents inside a folder called Documents. I will be referring to these documents for information such as block diagrams, register details ect.

## Overview of STM32F407VGT6 Microcontroller

 Please refer : Figure 6. STM32F407VGT6 block diagram from 'STM32F4 Discovery User Manual' (Page 12).
 
 ![Figure_6_STM32F407VGT6_block_diagram](https://user-images.githubusercontent.com/101395036/167913344-4b240f0f-2b6d-4031-bf15-5ce021f42794.png)
 
The STM32F407 Discovery board uses STM32F407VGT6 Microcontroller which has ARM Cortex-M4F Processor, which is capable of running upto 168Mhz. This MCU has many peripherals such as GPIO ports, TIMERS, ADCs, DACs, Flash Memory, SRAM, SPI, UART ect. The processor and peripherals talk via BUS-Interface. There are three busses available 
1. I-BUS (Instruction Bus)
2. D-BUS (Data Bus)
3. S-BUS (System Bus)

I-BUS This bus connects the Instruction bus of the Cortex®-M4 with FPU(Floating point unit) core to the BusMatrix. This bus is used by the core to fetch instructions. The target of this bus is a memory containing code (internal Flash memory/SRAM or external memories through the FSMC/FMC).

D-BUS This bus connects the databus of the Cortex®-M4 with FPU to the 64-Kbyte CCM data RAM to the BusMatrix. This bus is used by the core for literal load and debug access. The target of this bus is a memory containing code or data (internal Flash memory or external memories through the FSMC/FMC).

S-BUS This bus connects the system bus of the Cortex®-M4 with FPU core to a BusMatrix. This bus is used to access data located in a peripheral or in SRAM. Instructions may also be fetched on this bus (less efficient than ICode). The targets of this bus are the internal SRAM1, SRAM2 and SRAM3, the AHB1 peripherals including the APB peripherals, the AHB2 peripherals and the external memories through the FSMC/FMC.

So instructions and data use I-bus and D-bus respectively, All the other peripheral uses System bus. The Cortex-M4 processor contains three external Advanced High-performance Bus (AHB)-Lite bus interface and one Advanced Peripheral Bus (APB) interface. The GPIOs are connected to AHB1 bus which has a maximum speed of 150Mhz and is divided into two buses as APB1 and APB2. APB1 runs at 42Mhz(max) and APB2 runs at 82Mhz(max). The different peripherals such as SPI, UART, TIMERs, ADCs, DACs, etc are connected to either APB1/APB2 buses. And the AHB2(168Mhz max) is connected to Camera and USB OTG interfaces, AHB3 is connected to External memory controller.

## Bus Matrix

Please refer : Figure 7. System architecture from 'Using the STM32F2 and STM32F4 DMA controller(AN4031)' (page 18).

![Figure_7_System architecture](https://user-images.githubusercontent.com/101395036/167913975-9ae91c12-22b4-430f-9433-97d34114ee1b.png)

Refering to the figure 7, The Yellow blocks are Master and blocks in Green are Slaves, there are lots of connected dots which actually says that there is path from master to slave for communication. In Microcontroller , the communication between the processors and the peripherals is seen in the scope of communication between master and slave. Here the processor ARM Cortex-M4 itself is a master, and it may have other masters such as Ethernet, High Speed USB 2.0, DMA1 and DMA2.

## Clock

STM32F407VGT6 Micorcontroller has 3 main clock sources:
 1. Crystal Oscillator(HSE) - This is external clock source which can be connected to MCU based on requirements. HSE standas fro High speed External. If you want to       use HSE as system clock an external crystal oscillator(whose frequency must be in range 4 to 26Mhz ) has to be connected. In this board, the manufacturer has           connected 8Mhz crystal.
 2. RC Oscillator (HSI) - All modern MCU comes with internal RC Oscillator, which can be just activated to use. HSI stands for High Speed Internal .After Reset, by         default HSI is used to provide a clock to MCU, which means by default MCU select HSI as the clock. This clock is internal to MCU and its value is 16Mhz in             STM32F407 MCU. The HSI internal oscillator has the advantage of providing a clock at a low cost, as no external component is required to use this clock. It also       has a faster start-up time than the external crystal oscillator however, frequency is less accurate when compared to the external crystal oscillator.
 3. PLL(Phase locked loop) - It is also Implemented internally in MCU, it uses low frequency sources to generate high frequency clock (PLLCLK).The power of PLL lies in     producing high-frequency clocks of various programmable range. By using PLL you can boost the HCLK(AHB) up to 168Mhz in STM32F4xx MCU. All the modern MCU has PLL.     If you want to use MCU-buses at their maximum speed then we have to use PLL only. You have to feed either HSI or HSE to the PLL as input frequency. Then by using       all PLL circuitry settings, it produces a PLL output clock in the range of 100's of Mhz. So to Run STM32F407 at its maximum frequency(168Hhz) you have to use PLL.
Please refer : Figure 21. Clock tree from 'STM32F4xxx Reference Manual (RM0090)' (Page 216).
Note : If your using STM32 CubeIED tool, then select STM32F407 board and goto clock configuration for a much better clock tree representation.(I prefer to use this clock representation for easier understanding).

 ![Figure_Clock_Tree](https://user-images.githubusercontent.com/101395036/167915117-8f24c500-4d62-4155-a88d-cce70ed842ed.png)

From above clock tree we can see that HSI RC is 16Mhz internal Clock, and an external oscillator (4Mhz to 26Mhz) has to be connected to HSE input and PLL takes HSI/HSE as input to produce various other clocks. All 3 of these clock sources are given to SYSTEM CLOCK MULTIPLEXER where we can select clock source, Output of this MUX is SYSCLK(i.e, System Clock).
1. SYSCLK : This is the Main clock of MCU, using this other clocks are derived (Ex: Peripheral, Bus clocks ect). SYSCLK is given directly to Ethernet PTP Clock.
2. HCLK : HCLK is derived from SYSCLK with a Prescaler in between , which brings down the clock frequency. HCLK goes directly to AHB bus, core, memory and DMA. HCLK      goes to Cortex System Timer with prescalar in between and HCLK goes directly to Cortex Processor (FCLK Cortex Clock).
3. PCLK : PCLK1 and PCLK2 are derived from HCLK, PCLK1 goes to APB1 peripheral clock and APB1 Timer Clock and PCLK2 goes to APB2 peripheral clock and APB2 Timer Clock.
By default MCU uses HSI (i.e internal RC Oscillator) as SYSCLK, Which means after reset HSI is used as SYSCLK Source. Before using any peripheral its clock should be enabled. Referring MUC Block Diagram, all different peripheral drives the clock from bus which it is connected. By default almost all the peripheral are deactive, which means there clocks are not enabled. RCC(Reset and clock Control) engine of MCU gives various registers to enable and disable various peripheral clocks. For more information refer RCC section of STM32F4xxx Reference Manual (RM0090), page-213.

## Clocking the MCU using External Crystal Oscillator

As explained before, you can connect (4 to 26Mhz) crystal oscillator to MCU. In STM32 board manufacturer has connected 8Mhz Crystal. Even though it is connected its useless as its disabled. Before using an external oscillator, we need to enable it by using RCC Clock Control Register(RCC_CR). Refer 7.3.1 RCC clock control register (RCC_CR) (page 224 of RM0090). Referring to the RCC_CR Register:

  * Bit 17 and 16 are HSERDY and HSE ON respectively
  * To enable HSE, HSEON bit is made 1, then you have to wait until the HSERDY flag becomes 1, which indicates the HSE oscillator is ready to use. It important to wait     until HSERDY flag is set.
  * Now HSE is ready but it is not yet set as SYSCLK(System Clock).
So to set HSE as System clock, RCC clock configuration register (RCC_CFGR) is used. Refer 7.3.3 RCC clock configuration register (RCC_CFGR)(page 228 of RM0090). Referring RCC_CFGR, bit 0 and 1 are used to switch system clock.
  * If Bit1:0 SW = 01, then HSE oscillator selected as the system clock .
  * Once we do this HSE will be used as a system clock
 
## Vector Table

 It is a table of Vectors. Generally, Vectors are related to directions. We know that VECTORS in physics has both magnitude and direction. In our context we can        compare pointers and direction, as pointers will point to certain addresses. So we can say that Vector table is a table which holds the specific addresses. It contains the addresses of Exception Handlers. Here system exceptions(these are MCU internally generated) and Interrupts(Which are external) are collectively called as exceptions.
Referring : Table 61. Vector table for STM32F405xx/07xx and STM32F415xx/17xx (Page 372 of RM0090)

 <img width="420" alt="Table_61_VectorTable (1)" src="https://user-images.githubusercontent.com/101395036/167916534-d079c0fe-421c-4e0f-9fe6-8294f8714ed0.png">
Above Vector table is not the complete table, it's just a part of it. Please refer the RM0090 for complete vector table. There are 6 columns in Vector Table: Position, Priority, Type of priority, Acronym, Description, and Address.

 1. Position: We can see that position is kept empty for all the system exceptions, system exceptions come from the processor end and vendor ST does not have control       over system exceptions. These positions are with respect to NVIC(Nested vectored interrupt controller). For example, Window Watchdog interrupt is at Position 0         w.r.t to NVIC. Another name for the position is IRQ Number.
2. Priority: This column gives the priority of exceptions and interrupts. From the table, we can see that Reset has the highest priority of -3.
   Type of Priority: This column tells us that whether the priority of exceptions can be changed or not. Here Reset, NMI and Hard Fault has fixed priority type and the    remaining exceptions have settable priority type which means its priority can be changed.
3. Address: This column tells that where exactly in the processor memory map you have to keep the corresponding exception handler. A handler is just a C function which    takes care of that exception. for example, if we have implemented a function to handle NMI exception in your program then address of that handler must be kept at      0x0000 0008, that is function pointer should be kept in this addresses. The very first address that is 0x00000000 is reserved and it has special data known as STACK    Pointer value in Cortex Processor. Before coming to the Reset handler, the processor loads the value stored in 0x00000000 location into stack pointer. Because          always stack pointer must be initialized before entering into any handler. So we must keep a valid value at this address. All these initializations are handled in      startup code.

## NVIC(Nested vectored interrupt controller)

Interrupts are a common feature supported by almost all microcontrollers. They are typically generated by hardware, for example peripherals or external input pins. When a peripheral or hardware needs service from the processor, this will lead to changes in program flow control outside the normal programmed sequence. Typically, the following sequences would occur:

1. The peripheral asserts an interrupt request to the processor.
2. The currently running task is suspended by the processor.
3. The processor executes an Interrupt Service Routine (ISR) to service the peripheral, and optionally the interrupt request is cleared by software if needed.
4. The processor resumes the previously suspended task. For every interrupt there must be a program associated with it. When an interrupt occurs, this program is          executed to perform certain service for the interrupt. This program is usually named as Interrupt Service Routine (ISR) or interrupt handler.

![Figure_NVIC_Cortex_M4](https://user-images.githubusercontent.com/101395036/167917548-ddac3914-eb9f-4e4c-a12f-2de529526bca.png)

As the above figure shows every Cortex-M4 processor provides a Nested Vectored Interrupt Controller (NVIC) for interrupt handling. NVIC facilitates low-latency exception and interrupts handling, controls power management and implements System Control Registers. The NVIC and the processor core interface are closely coupled, which enables low latency to interrupt processing and efficient processing of late arriving interrupts.

For this microcontroller, the NVIC receives interrupt requests from various sources. In addition to interrupt requests, ther are some other events which need servicing. They are called “exceptions” (which are MCU internally generated). For Cortex-M4 processor, exceptions include resets, software interrupts and hardware interrupts. Each exception has an associated 32-bit vector that stores the memory location where the ISR that handles the exception is located. These vectors are stored in ROM at the beginning of memory. As explained earlier Vector table holds the location of ISR. The Cortex-M4 NVIC supports up to 240 interrupt requests (IRQs), a non-maskable interrupt (NMI), a SysTick timer interrupt and a number of system exceptions. Most of these IRQs are generated by peripherals such as timers, GPIO ports and communication interfaces such as UARTs.

## You can find more details about the different peripherals of STM32F407 MCU below.

1. [GPIO](https://github.com/SharathN25/STM32F407-Discovery/tree/master/GPIO_Driver) - Serial Peripheral Interface]- General Purpose Input and Output
2. [SPI](https://github.com/SharathN25/STM32F407-Discovery/tree/master/SPI_Driver) - Serial Peripheral Interface]
3. [USART/UART](https://github.com/SharathN25/STM32F407-Discovery/blob/master/UART_Driver/README.md#usartuniversal-synchronous-asynchronous-receiver-transmitter-and-uartuniversal-asynchronous-receiver-transmitter) - Universal Synchronous/Asynchronous Receiver Transmitter
4. [I2C](https://github.com/SharathN25/STM32F407-Discovery/tree/master/I2C_Driver)  - Inter-Integrated Circuit

for more details refer to: [GitHub](https://github.com/SharathN25)

## Features

 * If the User button is pressed Once, the red LED will be on    
 
 * If the User Button is pressed TWICE, Blue,Green,Orange LED's come ON at a time with set of frequency

 * If the User Button is pressed THIRD time, ON All LED's in CLOCKWISE manner an speeed will increase 

 * If the User Button is pressed FOURTH time ,all LED's on anticlock manner

 * If the User Button is pressed FIFTH time, the red LED will be off 

![Screenshot (105)](https://user-images.githubusercontent.com/62429376/167068935-6c3e8f17-1708-4a77-9bd0-ddd2fd4e5171.png)

## State of art

 * The main focus point is seeing the wiper control of the car.
 * And also seeing the seep of the wiper system in the car
 * Now this two features are explained in these project

# 5W's & 1H  

![Screenshot (104)](https://user-images.githubusercontent.com/62429376/167068196-569dce68-9ded-4259-8ef5-8cd52300e01f.png)

#  SWOT ANALYSIS 

![Screenshot (103)](https://user-images.githubusercontent.com/62429376/167066480-c12c3086-1d1b-426f-99c4-815b6db4368f.png)

# High Level Requirements

| ID | Description | Requirement | Status | 
| ----- | ----- | ------- | ---------|
| HR01 | SSD or HARD DRIVE  | 1GB TO 20 GB | IMPLEMENTED | 
| HR02 | OPERATING SYSTEM  | WINDOWS |  IMPLEMENTED  |
| HR03 | PROGRAMMING LANGUAGE | EMBEDDED C |  IMPLEMENTED  |
| HR04 | ARM BASED MICROCONTROLLER | STM32F407VGT6 BOARD  |  IMPLEMENTED  |

# Low Level Requirements

| ID | Description | REQUIREMENT | Status |
| ------ | --------- | ------ | ----- |
| LR01 | WIPER COMES TO INITIAL POSITION AFTER HIS WORK | LED |  IMPLEMENTED  |
| LR02 | PROPER SUPPLY TO PINS AND BOARD | POWER SUPPLY | IMPLEMENTED |
| LR03 | ON AND OFF SWITCH MECHANISM FOR ACTIVATION AND DEACTIVATION OF WIPER BLADES  | SWITCH | IMPLEMENTED |

## Best Methods To Be Followed

* Used functions to decrease dependency on main function
* Used Functions to accept the inputs from environmental conditions and store the values which helped in creating easy design of the system.
* comments have been placed only wherever necessary to avoid confusions
* Created header file so that the fuctions can be used else where ever required without any difficulty

# Behavioural Diagram

![Untitled Diagram (3)](https://user-images.githubusercontent.com/101981165/167299441-5cf2d7cb-178a-4b59-ab6f-e27c3c1b9f5a.jpg)

# Flow Chart

![Untitled Diagram (1)](https://user-images.githubusercontent.com/101981165/167257805-e125bf7a-42f8-46af-871d-20dfd1506e33.jpg)

# Structural Diagram

![Untitled Diagram (2)](https://user-images.githubusercontent.com/101981165/167301261-91f3b1ad-1115-4165-bc73-fb114441ef25.jpg)

## Introduction

* Rainwater, dust, and exhaust gas compounds from vehicles that adhere to the surface of an automobile windshield are unlikely to be a problem as long as the driver has a clear view of the road. However, if the adhering chemicals are not dealt with, they will pose a danger to travel safety. A windshield wiper system consists of two wiper arms and a wiper drive. The drive drives the two wiper arms over the windshield at an angle to give the driver and passenger a good view. The ideal cleaning outcome is ensured by an uniquely formed rubber wiping lip. Wipers are extremely important for driver visibility. If the wipers aren't working, the car is considered unsafe. The front wiper motor and transmission mechanism (linkage) are located underneath the windshield, under the cowl panel cover.

## Implementation

* If the User button is pressed Once, the red LED will be on    
 
 * If the User Button is pressed TWICE, Blue,Green,Orange LED's come ON at a time with set of frequency

 * If the User Button is pressed THIRD time, ON All LED's in CLOCKWISE manner an speeed will increase 

 * If the User Button is pressed FOURTH time ,all LED's on anticlock manner

 * If the User Button is pressed FIFTH time, the red LED will be off 

## High Level Test Plan

| ID | Description | Requirement | Status | 
| ----- | ----- | ------- | ---------|
| HL01 | SSD or HARD DRIVE  | 1GB TO 20 GB | IMPLEMENTED | 
| HL02 | OPERATING SYSTEM  | WINDOWS |  IMPLEMENTED  |
| HL03 | PROGRAMMING LANGUAGE | EMBEDDED C |  IMPLEMENTED  |
| HL04 | ARM BASED MICROCONTROLLER | STM32F407VGT6 BOARD  |  IMPLEMENTED  |

## Low Level Test Plan

| ID | Description | REQUIREMENT | Status |
| ------ | --------- | ------ | ----- |
| LL01 | WIPER COMES TO INITIAL POSITION AFTER HIS WORK | LED |  IMPLEMENTED  |
| LL02 | PROPER SUPPLY TO PINS AND BOARD | POWER SUPPLY | IMPLEMENTED |
| LL03 | ON AND OFF SWITCH MECHANISM FOR ACTIVATION AND DEACTIVATION OF WIPER BLADES  | SWITCH | IMPLEMENTED |

# OUTPUT VIDEO

https://user-images.githubusercontent.com/62429376/167387308-8435a9da-6f4e-4c11-9b20-61ad71fd8822.mp4

# OUTPUT DIAGRAM

## Switch turned off

![Screenshot (106)](https://user-images.githubusercontent.com/62429376/167388539-46c3632a-74a7-4bb7-98e7-c61324d76512.png)

## Switch turned on 

![Screenshot (107)](https://user-images.githubusercontent.com/62429376/167388545-68d0f225-2156-428b-b6a4-75d02bdfbbe0.png)

## Wiper turned on

![Screenshot (118)](https://user-images.githubusercontent.com/62429376/167388551-79b6e314-6096-4fb6-b4f4-e77c11f0b8f7.png)

![Screenshot (108)](https://user-images.githubusercontent.com/62429376/167388573-d8571493-41e5-4ee0-bc5c-880269ca364c.png)

![Screenshot (109)](https://user-images.githubusercontent.com/62429376/167388580-201eabda-fc25-4392-a033-f771ac987651.png)

![Screenshot (111)](https://user-images.githubusercontent.com/62429376/167388586-f24716fb-45ff-431e-99f5-8524efe7ee65.png)

![Screenshot (113)](https://user-images.githubusercontent.com/62429376/167388591-113e5008-3f21-4928-9edf-5aa9fde7c836.png)

![Screenshot (114)](https://user-images.githubusercontent.com/62429376/167388596-ccefc6a7-1a24-4d43-86cf-8208a7d20ff7.png)

## Wiper turned off

![Screenshot (106)](https://user-images.githubusercontent.com/62429376/167388539-46c3632a-74a7-4bb7-98e7-c61324d76512.png)
