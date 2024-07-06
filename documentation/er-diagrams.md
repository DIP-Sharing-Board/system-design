# ER Diagrams

## Overview

This document contains the Entity-Relationship (ER) diagrams for the database schema used in our system. The ER diagrams illustrate the structure of the database, including the entities, attributes, and relationships.

## ER Diagram

![ER Diagram](/detailed-design/er-diagrams/er-diagram.svg)

## Entities

### Competition
- **id**: INTEGER (Primary Key)
  - Acts as the unique identifier for each competition entry.
- **link**: TEXT
  - The URL link for the competition.
- **topic**: TEXT
  - The topic or subject of the competition.
- **imageUrl**: TEXT
  - The URL link to an image representing the competition.
- **deadline**: DATETIME
  - The deadline date and time for the competition.
- **createAt**: DATETIME
  - The date and time when the competition entry was created.
- **isActive**: BOOLEAN
  - Indicates if the competition is still active. `true` if the deadline has not passed, `false` if it has.

### Camp
- **id**: INTEGER (Primary Key)
  - Acts as the unique identifier for each camp entry.
- **link**: TEXT
  - The URL link for the camp.
- **topic**: TEXT
  - The topic or subject of the camp.
- **imageUrl**: TEXT
  - The URL link to an image representing the camp.
- **deadline**: DATETIME
  - The deadline date and time for the camp.
- **createAt**: DATETIME
  - The date and time when the camp entry was created.
- **isActive**: BOOLEAN
  - Indicates if the camp is still active. `true` if the deadline has not passed, `false` if it has.

### Other
- **id**: INTEGER (Primary Key)
  - Acts as the unique identifier for each other activity entry.
- **link**: TEXT
  - The URL link for the other activity.
- **topic**: TEXT
  - The topic or subject of the other activity.
- **imageUrl**: TEXT
  - The URL link to an image representing the other activity.
- **deadline**: DATETIME
  - The deadline date and time for the other activity.
- **createAt**: DATETIME
  - The date and time when the other activity entry was created.
- **isActive**: BOOLEAN
  - Indicates if the other activity is still active. `true` if the deadline has not passed, `false` if it has.