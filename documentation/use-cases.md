# Use Cases

## Overview

This document outlines the use cases for the system, describing how users interact with the system to achieve specific goals.

## Use Case Diagram

![Use Case Diagram](/low-level-design\use-case-diagrams\use-case-diagram.svg)


## Actors:
1. **User**: This actor is someone looking for information about various activities.
2. **Sharer**: This actor is responsible for sharing links to different channels on Discord.

## Use Cases:


### **Actor**: Sharer
1. **Share link to camps channel**:
    - **Actor**: Sharer
    - **Description**: The sharer shares a link related to camps in the respective Discord channel.
    - **Interaction**: The sharer posts the link to the Discord channel for camps.
    - **Outcome**: The link is shared in the Discord channel.

2. **Share link to competitions channel**:
    - **Actor**: Sharer
    - **Description**: The sharer shares a link related to competitions in the respective Discord channel.
    - **Interaction**: The sharer posts the link to the Discord channel for competitions.
    - **Outcome**: The link is shared in the Discord channel.

3. **Share link to others channel**:
    - **Actor**: Sharer
    - **Description**: The sharer shares a link related to other activities in the respective Discord channel.
    - **Interaction**: The sharer posts the link to the Discord channel for other activities.
    - **Outcome**: The link is shared in the Discord channel.

### **Actor**: User
1. **Looking for a camp**:
    - **Actor**: User
    - **Description**: The user searches for information about camps.
    - **Interaction**: The user sends a request to the `ActivityDataService` with parameters `activity(camp, lastId)`.
    - **Outcome**: The system retrieves and sends the relevant camp data back to the user.

2. **Looking for a competition**:
    - **Actor**: User
    - **Description**: The user searches for information about competitions.
    - **Interaction**: The user sends a request to the `ActivityDataService` with parameters `activity(comp, lastId)`.
    - **Outcome**: The system retrieves and sends the relevant competition data back to the user.

3. **Looking for other activities**:
    - **Actor**: User
    - **Description**: The user searches for information about other activities.
    - **Interaction**: The user sends a request to the `ActivityDataService` with parameters `activity(other, lastId)`.
    - **Outcome**: The system retrieves and sends the relevant data for other activities back to the user.