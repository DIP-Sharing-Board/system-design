# Sequence Diagram

## Overview

This document contains the sequence diagrams for the system, illustrating how objects interact in specific scenarios.


## Sharer

![Sharer Sequence Diagram](/low-level-design\sequence-diagrams\sharer-sequence-diagram.svg)

### Description

1. **Sharer Posts Message in Discord**:
    - **Actor**: Sharer
    - **Description**: The sharer posts a message containing a link in a specified Discord channel.
    - **Interaction**: The sharer sends a `msg` to Discord.
    - **Outcome**: The message is posted in the Discord channel.

2. **Discord Bot Retrieves Message**:
    - **Actor**: Discord Bot
    - **Description**: The Discord Bot monitors the specified Discord channel and retrieves the posted message.
    - **Interaction**: The Discord Bot sends a `getMessage()` request to Discord and receives `msgData` in response.
    - **Outcome**: The Discord Bot has the data of the posted message.

3. **Discord Bot Requests Content from Other Website**:
    - **Actor**: Discord Bot
    - **Description**: The Discord Bot extracts the link from the message data and sends a request to the specified website to retrieve content.
    - **Interaction**: The Discord Bot sends a `getContent()` request to the other website and receives `contentData` in response.
    - **Outcome**: The Discord Bot retrieves the content data from the specified website.

4. **Discord Bot Stores Data in Database**:
    - **Actor**: Discord Bot
    - **Description**: The Discord Bot processes the retrieved content data and inserts it into the database.
    - **Interaction**: The Discord Bot sends an `insertData` request to the database with the content data.
    - **Outcome**: The content data is stored in the database.

This sequence of interactions ensures that the data shared in Discord is retrieved, processed, and stored in the database for further use.

## Client

![Client Sequence Diagram](/low-level-design\sequence-diagrams\client-sequence-diagram.svg)

### Description

1. **Client Requests Activity Data**:
    - **Actor**: Client
    - **Description**: The client initiates a request to the `Activity Data Service` to retrieve activity data.
    - **Interaction**: The client sends a `GET` request to the `Activity Data Service` with the parameters `type` (activity type) and `lastId` (for pagination).
    - **Outcome**: The request is received by the `Activity Data Service`.

2. **Activity Data Service Queries Database**:
    - **Actor**: Activity Data Service
    - **Description**: Upon receiving the client's request, the `Activity Data Service` queries the database for the requested activity data.
    - **Interaction**: The `Activity Data Service` sends a `query activity` request to the database.
    - **Outcome**: The database processes the query and retrieves the relevant activity data.

3. **Database Returns Activity Data**:
    - **Actor**: Database
    - **Description**: The database returns the retrieved activity data to the `Activity Data Service`.
    - **Interaction**: The database sends the `activityData` back to the `Activity Data Service`.
    - **Outcome**: The `Activity Data Service` receives the activity data.

4. **Activity Data Service Responds to Client**:
    - **Actor**: Activity Data Service
    - **Description**: The `Activity Data Service` sends the retrieved activity data back to the client.
    - **Interaction**: The `Activity Data Service` sends the `activityData` to the client.
    - **Outcome**: The client receives the activity data.

This sequence of interactions ensures that the client can successfully retrieve the required activity data from the `Activity Data Service`.