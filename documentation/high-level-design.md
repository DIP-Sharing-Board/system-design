# High-Level Design

## Overview

This document provides a high-level overview of the system architecture, major components, and their interactions.

## Architecture Diagram

![High-Level Design](/high-level-design\architecture-diagrams\architecture-diagram.svg)

### Components

- **Client**: Interacts with the server to request and display activity data.
- **Server**: Processes client requests, interacts with the database, performs webscraping, sends request to Discord to receive shared links, retrieves data from external sources like Discord and other websites.
- **Database**: Stores activity data including competitions, camps, and other activities.
- **Discord**: Source of shared links.
- **Other Websites**: Additional sources of activity data.

##  Description
Detailed documentation of system design, components, and architecture overviews.

- [Detailed Documentation](/high-level-design\descriptions\system-design-description.md).