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
- `i`: User identifier (example for an optional tracing details).
- `s`: State (example for an optional tracing details).
- `r`: Room (example for an optional tracing details).
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

## Database Structure

This provided structure is a conceptual representation of how you might design your MongoDB documents. 

```
// Campaign Collection
{
  _id: ObjectId("..."),
  campaignId: "fjZdS0lD",
  name: "Summer Product Feedback",
  description: "Collecting user opinions on our new summer product line",
  createdAt: ISODate("2023-06-01T00:00:00Z"),
  updatedAt: ISODate("2023-06-01T00:00:00Z"),
  status: "active",
  privacySettings: {
    collectUserInfo: true,
    collectRegionalData: true,
    anonymity: false
  },
  tracingDetails: [
    {
      key: "i",
      name: "Identifier",
      description: "Unique identifier for the respondent",
      isRequired: false
    },
    {
      key: "s",
      name: "Source",
      description: "Source of the response",
      isRequired: false
    },
    {
      key: "r",
      name: "Reference",
      description: "Additional reference information",
      isRequired: false
    }
  ],
  questions: [
    {
      questionId: "q1",
      text: "What do you think about our new summer t-shirt design?",
      type: "text"
    },
    {
      questionId: "q2",
      text: "How likely are you to purchase this product?",
      type: "scale",
      min: 1,
      max: 5
    }
  ],
  statistics: {
    totalResponses: 1000,
    completionRate: 0.85,
    averageTimeToComplete: 180, // in seconds
    responsesBySource: {
      "email": 500,
      "social": 300,
      "website": 200
    },
    questionStats: {
      "q1": {
        responseCount: 950,
        averageLength: 50 // for text responses, average character count
      },
      "q2": {
        responseCount: 980,
        averageRating: 4.2,
        ratingDistribution: {
          "1": 50,
          "2": 80,
          "3": 150,
          "4": 300,
          "5": 400
        }
      }
    },
    lastUpdated: ISODate("2023-06-15T14:30:00Z")
  }
}

// Response Collection
{
  _id: ObjectId("..."),
  campaignId: "fjZdS0lD",
  submittedAt: ISODate("2023-06-15T14:30:00Z"),
  tracingDetails: {
    i: "1234567890",  // Generic identifier
    s: "email",       // Generic source
    r: "promo_456"    // Generic reference
  },
  responses: [
    {
      questionId: "q1",
      answer: "I love the vibrant colors and modern design!"
    },
    {
      questionId: "q2",
      answer: 4
    }
  ],
  metadata: {
    userAgent: "Mozilla/5.0 ...",
    ipAddress: "192.168.1.1",  // Stored if allowed by privacy settings
    region: "Texas, USA",      // Stored if allowed by privacy settings
    timeToComplete: 165        // in seconds
  }
}

// User Collection (Optional, based on privacy settings)
{
  _id: ObjectId("..."),
  userId: "1234567890",
  name: "John Doe",
  email: "john.doe@example.com",
  demographics: {
    age: 30,
    gender: "male",
    occupation: "engineer"
  },
  createdAt: ISODate("2023-06-01T00:00:00Z"),
  updatedAt: ISODate("2023-06-15T14:30:00Z")
}
```
