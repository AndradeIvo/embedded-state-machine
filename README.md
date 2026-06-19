# Embedded State Machine

A simple embedded-style state machine project written in C.

This project simulates the core logic of a flight controller using states, events, and transitions. It was created to practice firmware architecture concepts commonly used in embedded systems, robotics, drones, automation, and safety-critical systems.

## Features

- Finite State Machine implementation in C
- Flight controller inspired logic
- Event-based transitions
- Failsafe handling
- Modular firmware-like architecture
- Clean separation between application and state machine logic

## States

- IDLE
- SELF_TEST
- ARMED
- TAKEOFF
- MISSION
- RETURN_HOME
- LANDING
- FAILSAFE

## Events

- START_SELF_TEST
- SELF_TEST_OK
- TAKEOFF_COMMAND
- TAKEOFF_COMPLETE
- MISSION_COMPLETE
- RETURN_HOME_COMMAND
- LAND_COMMAND
- LANDING_COMPLETE
- LOW_BATTERY
- GPS_LOST
- SYSTEM_ERROR

## State Flow
IDLE
  ↓ START_SELF_TEST
SELF_TEST
  ↓ SELF_TEST_OK
ARMED
  ↓ TAKEOFF_COMMAND
TAKEOFF
  ↓ TAKEOFF_COMPLETE
MISSION
  ↓ MISSION_COMPLETE
RETURN_HOME
  ↓ LAND_COMMAND
LANDING
  ↓ LANDING_COMPLETE
IDLE
