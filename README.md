# Siemens-Multibay-Automated-Car-wash-
A fully simulated 3-Bay Car Wash system using S7-1200 and KTP700 HMI controlled via SCL state machines

# 🚗 Automatic Multi-Bay Car Wash System

## Project Overview
This project simulates a commercial 3-bay car wash system using Siemens TIA Portal V16. It demonstrates complex state machine logic, HMI visualization, and hardware configuration.

## 🛠 Tech Stack
* **Software:** Siemens TIA Portal V16
* **PLC:** CPU 1214C DC/DC/DC (S7-1200)
* **HMI:** KTP700 Basic PN
* **Languages:** SCL (Structured Control Language) for logic, LAD for counters.

### Logic Snippet (SCL)
<img width="719" height="446" alt="image" src="https://github.com/user-attachments/assets/0bc54654-c732-47d1-a04a-ab550a66756e" />
*Description: A CASE statement handles the state machine (Idle -> Wash -> Dry -> Complete).*

## 🧠 Logic Breakdown
The system uses a **State Machine** architecture:
1.  **State 0 (Idle):** Waits for "Start" command.
2.  **State 10 (Selection):** Operator chooses Basic, Premium, or Ultra.
3.  **State 12-14 (Wash Cycle):** Timers control water/soap application.
4.  **State 50 (Complete):** Resets counters and waits for exit.

