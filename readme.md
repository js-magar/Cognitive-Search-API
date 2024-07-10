# Cognitive Search API - SharePoint Data Source

This repository contains the code and instructions to create a link between SharePoint and AI services using Azure Cognitive Search API.

## Description

This project demonstrates how to integrate SharePoint with Azure Cognitive Search using API services. The process includes creating a data source, index, and indexer to facilitate the search functionality.

## Prerequisites

1. Azure subscription with appropriate permissions.
2. Postman installed on your machine.
3. GitHub repository with the necessary code (this repository).

## Setup Instructions

### 1. App Registration

1. Create an app registration in Azure Active Directory.
2. Assign `Read all` permissions for Sites and Files.
3. Generate a client secret and store it in Azure Key Vault for secure access.

### 2. AI Service

1. Create an AI service in Azure (must be higher than the freee tier to act as a data source for Azure Open AI).

### 3. Postman Setup

1. Download and install Postman.
2. Import the necessary code from this GitHub repository into Postman.

### 4. GitHub Repository

The repository for the necessary code is available [here](https://github.com/js-magar/Cognitive-Search-API). Please ensure to edit the secrets as they are not included in the repo for security reasons. Ensure that all variables are correct and edit if needed.

## Usage Instructions

1. Clone the repository: 

    ```bash
    git clone https://github.com/js-magar/Cognitive-Search-API.git
    ```

2. Follow the order of operations for the Postman requests:

    1. **Create Data Source**
    2. **Create Index**
    3. **Create Indexer**
    4. **Get Indexer Status**
    
    - Log in using the Status Link
    - Return to Indexer to see completion

    If the process isn't working, ensure that you have created a system managed instance or included a tenant id in the data source. Note that System Managed Identity requires a higher tier than the free plan.

## Creating Azure Open AI Instance

1. Create an Azure Open AI Instance.
2. Navigate to **Model Deployments** > **Manage Deployments** > **Chat** > **Create new deployment**.
3. Create a GPT model.
4. Click **Add your data**.
5. Add Azure AI Search as a data source.

## Acknowledgements

- Some code adapted from GitHub - [Cognitive Search API - SharePoint Data Source.](https://gist.github.com/Zerg00s/6e239aabd54ea6346d6db8133e99be2d)