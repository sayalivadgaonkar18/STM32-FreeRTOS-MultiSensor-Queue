# STM32 FreeRTOS Multi-Sensor Queue Communication

## Project Overview

This project demonstrates **inter-task communication using FreeRTOS queues** on STM32.

Three independent producer tasks simulate different sensors:

- Temperature Sensor
- Humidity Sensor
- Pressure Sensor

All sensor tasks send data to a **shared FreeRTOS queue** using a **structure-based messaging system**.

A dedicated UART consumer task receives the messages from the queue and prints the sensor values to a serial terminal.

This project demonstrates a real-world **Producer → Queue → Consumer** RTOS architecture commonly used in embedded systems.


# Hardware & Software Used

## Hardware
- STM32 NUCLEO-G474RE
- ST-Link Debugger
- USB UART Serial Terminal

## Software
- STM32CubeIDE
- STM32CubeMX
- FreeRTOS (CMSIS V2 API)
- TeraTerm


# RTOS Concepts Covered

## Task Management
- Multiple producer tasks
- Single consumer task
- Independent task execution

## Queue Communication
- Shared queue communication
- FIFO data transfer
- Inter-task synchronization

## Blocking Mechanism
- `osWaitForever`
- BLOCKED task state
- Efficient CPU utilization

## Structure-Based Messaging
- Sensor packet transfer
- Scalable communication design

## Task Scheduling
- Different task execution periods
- RTOS scheduler behavior


# System Architecture

Temperature Task -----\
                       \
Humidity Task ----------> Shared Queue --------> UART Task
                       /
Pressure Task --------/