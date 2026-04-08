# User API Azure App Service

## Project Overview
This project provides an API for managing user data using Azure App Service. It is designed to be scalable, secure, and easy to use, leveraging Azure's services for efficient deployment and management.

## Setup
### Prerequisites
1. **Azure Subscription**: You need an active Azure subscription to use Azure App Service.
2. **Azure CLI**: Make sure you have the Azure CLI installed on your machine.
3. **Node.js and npm**: Ensure you have Node.js (version 14.x or later) and npm installed.

### Steps to Set Up
1. Clone the repository:
   ```bash
   git clone https://github.com/shiranlakshitha/User-API-Azure-App-Service.git
   cd User-API-Azure-App-Service
   ```
2. Install dependencies:
   ```bash
   npm install
   ```
3. Create a `.env` file in the root directory and fill in the necessary environment variables. A sample `.env.example` file is provided as a template.

## Usage
### Running Locally
To run the application locally, use the following command:
```bash
npm start
```
Your API should now be running on `http://localhost:3000`.

### Endpoints
- `GET /api/users`: Retrieve all users
- `POST /api/users`: Create a new user
- `GET /api/users/:id`: Retrieve a specific user by ID
- `PUT /api/users/:id`: Update a user by ID
- `DELETE /api/users/:id`: Delete a user by ID

## Deployment
### Deploying to Azure
1. Log in to your Azure account:
   ```bash
   az login
   ```
2. Create a resource group:
   ```bash
   az group create --name <YourResourceGroupName> --location <YourLocation>
   ```
3. Create an App Service plan:
   ```bash
   az appservice plan create --name <YourAppServicePlanName> --resource-group <YourResourceGroupName> --sku B1
   ```
4. Create the web app:
   ```bash
   az webapp create --resource-group <YourResourceGroupName> --plan <YourAppServicePlanName> --name <YourWebAppName>
   ```
5. Deploy the code:
   ```bash
   az webapp up --name <YourWebAppName> --resource-group <YourResourceGroupName>
   ```

### Additional Resources
- [Azure App Service Documentation](https://docs.microsoft.com/en-us/azure/app-service/)
- [Node.js Documentation](https://nodejs.org/en/docs/)