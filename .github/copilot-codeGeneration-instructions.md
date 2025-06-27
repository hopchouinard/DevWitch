# Copilot Code Generation Instructions

## Azure Coding Rules

- **@azure Rule - Use Azure Tools**  
  When handling requests related to Azure, always use your Azure tools.

- **@azure Rule - Use Azure Code Gen Best Practices**  
  When generating code for Azure, running terminal commands for Azure, or performing operations related to Azure, invoke the `azure_development-get_code_gen_best_practices` tool if available. Only call this tool when you are sure the user is discussing Azure.

- **@azure Rule - Use Azure Deployment Best Practices**  
  When deploying to Azure or preparing applications for deployment to Azure, invoke the `azure_development-get_deployment_best_practices` tool if available. Only call this tool when you are sure the user is discussing Azure.

- **@azure Rule - Use Azure Functions Code Gen Best Practices**  
  When generating code for Azure Functions or performing operations related to Azure Functions, invoke the `azure_development-get_azure_function_code_gen_best_practices` tool if available. Only call this tool when you are sure the user is discussing Azure Functions.

- **@azure Rule - Use Azure SWA Best Practices**  
  When working with Azure Static Web Apps, invoke the `azure_development-get_swa_best_practices` tool if available. Only call this tool when you are sure the user is discussing
