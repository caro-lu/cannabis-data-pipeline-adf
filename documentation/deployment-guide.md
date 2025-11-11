# Deployment Guide

## Prerequisites
- Azure subscription with Data Factory service enabled
- Azure Data Lake Storage Gen2 account  
- Snowflake account with appropriate permissions
- Source database access credentials

## Deployment Steps

### 1. Deploy ARM Template
```bash
# Using Azure CLI
az deployment group create \
  --resource-group your-resource-group \
  --template-file arm-templates/ARMTemplateForFactory.json \
  --parameters @arm-templates/ARMTemplateParametersForFactory.json
```

### 2. Configure Connections
1. Update all connection strings in the parameters file
2. Store sensitive credentials in Azure Key Vault
3. Test all linked service connections

### 3. Validate Deployment  
1. Run test pipeline execution
2. Verify data flow to destinations
3. Check monitoring and alerting setup
