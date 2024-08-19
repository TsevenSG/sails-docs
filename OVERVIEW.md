# SAILS Market Report System

## Overview

Our product leverages Generative AI (GenAI) to revolutionize the financial report generation process for investment firms. By analyzing real-time news, financial market data, and user-provided documents, our solution can produce customized daily, weekly, and monthly financial reports tailored to user specifications. This not only saves financial advisors, investors, and analysts significant time but also enhances productivity by automating a traditionally labor-intensive task. Unlike existing GenAI platforms that focus on digital marketing, our solution is uniquely designed to address the specific needs of the financial sector, providing a comprehensive and efficient reporting tool with minimal competition in this niche market.

## Technology Design

### 1. System Architecture

#### 1.1 Overview

-   **Client Side**: User interfaces for financial advisors, investors, and analysts.
-   **Server Side**: Backend services handling data processing, GenAI integration, and report generation.
-   **Database**: Storage for user data, financial data, and generated reports.
-   **External APIs**: Integration with real-time news and financial market data providers.

#### 1.2 Components

-   **Frontend**: Web application and mobile app.
-   **Backend**: RESTful API services.
-   **Database**: PostgreSQL for relational database with PGVector for Semantic search
-   **AI Engine**: GenAI model for report generation using Google Gemini model and Strategy building system [https://github.com/TsevenSG/py-strategies](https://github.com/TsevenSG/py-strategies).
-   **Data Integration Layer**: Connects to external APIs for real-time data.

### 2. Technologies

#### 2.1 Frontend

-   **Framework**: Sveltekit (Web)
-   **UI Components**: Material-UI
-   **Authentication**: Firebase Authentication / JWT / Support Google Account, Microsoft Account and Email link.

#### 2.2 Backend

-   **Language**: Python
-   **Framework**: FastAPI (Python)
-   **API Documentation**: Swagger / OpenAPI

#### 2.3 Database

-   **Primary Storage**: PostgreSQL
-   **Cache**: Redis
-   **Search**: PGVector with Gemini `textembedding-gecko@latest` model

#### 2.4 AI Engine

-   **Model**: gemini-1.5-pro
-   **Framework**: Langchain - GenAI, PyTorch - Strategy building
-   **Deployment**: Docker, Cloud Build, Cloud Run

#### 2.5 Data Integration

-   **Financial Data**: TradingView, Bloomberg, Financial Times, Seeking Alpha, Yahoo Finance
-   **Document Parsing**: Natural Language Processing (NLP) libraries spaCy, NLTK, Unstructured API

### 3. System Workflow

#### 3.1 User Interaction

1. **User Authentication**: Secure login via Firebase Authentication.
2. **Input Specifications**: Users provide preferences for report frequency and content.
3. **Data Collection**: System fetches real-time data from financial and news APIs.
4. **Document Upload**: Users can upload documents for additional context.

#### 3.2 Data Processing

1. **Data Aggregation**: Combine real-time data with user-provided documents.
2. **Data Cleaning**: Remove duplicates, handle missing values, and normalize data.

#### 3.3 Report Generation

1. **AI Analysis**: GenAI model analyzes aggregated data.
2. **Content Creation**: Generate customized reports based on user specifications.
3. **Formatting**: Apply templates for daily, weekly, and monthly reports.

#### 3.4 Delivery

1. **Notification**: Notify users via email or in-app notifications.
2. **Report Access**: Users can download or view reports within the app.

### 4. Security and Compliance

#### 4.1 Data Security

-   **Encryption**: Data encryption at rest and in transit (TLS/SSL).
-   **Access Control**: Role-based access control (RBAC).

#### 4.2 Compliance

-   **Regulations**: Ensure compliance with financial regulations (e.g., GDPR, CCPA).
-   **Audit Logs**: Maintain logs for all data access and changes.

### 5. Performance and Scalability

#### 5.1 Load Balancing

-   **Technique**: Use load balancers to distribute traffic across servers.

#### 5.2 Caching

-   **Strategy**: Implement caching for frequently accessed data using Redis.

#### 5.3 Scalability

-   **Approach**: Leverage Google Cloud to scale components.

### 6. Monitoring

#### 6.1 Monitoring

-   **Tools**: Prometheus, Grafana
-   **Metrics**: Monitor system performance, API response times, and error rates.
