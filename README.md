# Generic Opinion Collector

Generic Opinion Collector is a comprehensive software solution designed for collecting written opinions, poll responses, and survey answers from users through web forms distributed via links. This versatile system allows for efficient opinion data collection, management, and analysis across various campaigns and user details.

## Overview

The Generic Opinion Collector system consists of several key components:

1. **Web Form Frontend**: A user-friendly interface for participants to submit their written responses.
2. **Campaign Creator**: A tool for setting up and managing opinion collection campaigns.
3. **Dashboard**: A real-time monitoring interface for live events and campaign progress.
4. **Backend System**: Manages data storage, retrieval, and processing of written responses and associated metadata.

## Key Features

- **Flexible Campaign Management**: Create and customize opinion collection campaigns with varying levels of detail and user information.
- **Scalable Data Collection**: Collect user opinions from a wide range of participants through easily shareable web forms.
- **Customizable Privacy Settings**: Configure campaigns to collect detailed user information, regional data only, or maintain complete anonymity.
- **Real-time Monitoring**: Track campaign progress and live events through an intuitive dashboard.
- **Data Analysis and Reporting**: Generate insights and reports based on collected user opinions and associated metadata.

## Use Cases

- 📝 **Market Research**: Gather user opinions for market research, sentiment analysis, and user feedback.

## Technology Stack

- 🌐 **Frontend**: HTML5, CSS3, and JavaScript
- 💻 **Backend**: Go, MongoDB
- 🐳 **Infrastructure**: 
  - Docker: Containerized deployment
  - Portable: Standalone executable for quick setup on various platforms

## Url Structure

### Minumum

Url: https://example.org/v1/fjZdS0lD?x=WQ7cVlxQ0Q

- `v1`: Version of the API being used (e.g., v1, v2).
- `fjZdS0lD`: Unique campaign identifier.
- `x`: Signature for data integrity and security (mandatory for data submission).

### With optional tracing details

Url: https://example.org/v1/fjZdS0lD?i=1234567890&s=tx&r=5&x=WQ7cVlxQ0Q

- `v1`: Version of the API being used (e.g., v1, v2).
- `fjZdS0lD`: Unique campaign identifier.
- `i`: User identifier (optional tracing details).
- `s`: State (optional tracing details).
- `r`: Room (optional tracing details).
- `x`: Signature for data integrity and security (mandatory for data submission).

## Use Cases

### Simple

1. The role "campaign creator" goes to the dashboard and creates a new campaign.
2. The campaign creator sets up the campaign details, such as the campaign name, tracing details, description, and privacy settings.
3. The campaign creator customizes the web form. This may include adding questions, setting response types, and configuring privacy settings.
4. The campaign creator shares the web form link with participants
5. Participants submit their written opinions, poll responses, or survey answers through the web form, which is then stored in the backend system for further analysis and reporting.
   1. They can choose which tracing details they want to share
6. The campaign creator can monitor the campaign's progress and live events through the dashboard.
7. Once the campaign is complete, the campaign creator can generate insights and reports based on the collected user opinions and associated metadata.
