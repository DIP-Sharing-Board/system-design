# System Design Description

## 1. System Overview

### Introduction
The system aims to collect and display information about activities and events shared on Discord channels related to various categories such as camps, competitions/events, and other innovations or funding news.

### Purpose and Goals
- Collect links shared in Discord channels.
- Perform web scraping on the links to extract project details such as project name, poster image (if available), and application deadline.
- Store extracted data in a database for further retrieval and display.

### Architecture Overview
The system consists of two main components:
1. **Activity Data Service**: Provides an API to retrieve activity data from the database.
2. **Discord Bot**: Collects links shared in Discord channels, performs web scraping, and stores data in the database.

## 2. Component Details

### Activity Data Service
- **Functionality**:
  - Exposes an API endpoint to query activity data.
  - Retrieves and serves the latest activity information to clients.

### Discord Bot
- **Functionality**:
  - Monitors specified Discord channels for shared links.
  - Performs web scraping on the shared links to extract project details.
  - Stores extracted project details in the database.

## 3. Conclusion

### Summary of System Design
The system efficiently collects and presents activity information from Discord channels through automated link monitoring and web scraping. It provides a streamlined approach for users to discover and engage with relevant activities based on their interests.

### Future Plans or Considerations
- Implementing a dashboard to visualize the collected activity data.
- Enhancing the web scraping module to handle various formats and sources.