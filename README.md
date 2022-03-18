# Azure Firewall

Azure Firewall is a cloud-native and intelligent network firewall security service that provides the best of breed threat protection for your cloud workloads running in Azure. It's a fully stateful, firewall as a service with built-in high availability and unrestricted cloud scalability

# Azure Firewall Standard

Azure Firewall Standard provides L3-L7 filtering and threat intelligence feeds directly from Microsoft Cyber Security. Threat intelligence-based filtering can alert and deny traffic from/to known malicious IP addresses and domains which are updated in real time to protect against new and emerging attacks.


# Azure Firewall Premium

Azure Firewall Premium provides advanced capabilities include signature-based IDPS to allow rapid detection of attacks by looking for specific patterns. These patterns can include byte sequences in network traffic, or known malicious instruction sequences used by malware. There are more than 58,000 signatures in over 50 categories which are updated in real time to protect against new and emerging exploits. The exploit categories include malware, phishing, coin mining, and Trojan attacks.

## Target audience

- Infrastructure Architect
- Security Team
- Network Administrator
- Cloud Solution Architect

# Create an Azure Firewall

The [Template.bicep](https://github.com/DavidArayaSanabria/Deploy_Azure_Firewall_and_enable_monitoring/blob/df95b2d460fe26358f2da51bc362f7e114f4bf96/Deployment%20Templates/Template.bicep) Azure Bicep template will help you automatically deploy an Azure Firewall

# Monitor Azure Firewall logs and metrics

## Create a Log Analytics Workspace using CloudShell and Azure CLI:

```
az monitor log-analytics workspace create --resource-group
                                          --workspace-name
                                          [--capacity-reservation-level]
                                          [--ingestion-access {Disabled, Enabled}]
                                          [--location]
                                          [--no-wait]
                                          [--query-access {Disabled, Enabled}]
                                          [--quota]
                                          [--retention-time]
                                          [--sku]
                                          [--subscription]
                                          [--tags]
```                                          

## Example
```
az monitor log-analytics workspace create -g MyResourceGroup -n MyWorkspace
```

## Select the Diagnostic Settings balde option

![alt image](https://github.com/DavidArayaSanabria/Deploy_Azure_Firewall_and_enable_monitoring/blob/b76192dc7cf842bc02dd2571df23ef7bd5c96e21/Images/Diagnostic%20setting.png)

Select the Logs and Metrics you would like to store in your Log Analytics Workspace

## Use the Metrics blade option

![alt image](https://github.com/DavidArayaSanabria/Deploy_Azure_Firewall_and_enable_monitoring/blob/b76192dc7cf842bc02dd2571df23ef7bd5c96e21/Images/Metrics.png)

Gather and filter relevant Firewall's metrics/

## Query Logs

Use ready-made Kusto Query Language (KQL) queries for your Firewall's logs

![alt image](https://github.com/DavidArayaSanabria/Deploy_Azure_Firewall_and_enable_monitoring/blob/b76192dc7cf842bc02dd2571df23ef7bd5c96e21/Images/pre-defined%20KQL%20queires.png)

Use your own KQL queries

![alt image](https://github.com/DavidArayaSanabria/Deploy_Azure_Firewall_and_enable_monitoring/blob/b76192dc7cf842bc02dd2571df23ef7bd5c96e21/Images/custom%20query.png)


## Azure services and related products

- Azure Monitor
- KQL
- Log Analytics
- VNET

## Related references
- https://docs.microsoft.com/en-us/azure/aks/intro-kubernetes
- https://docs.microsoft.com/en-us/azure/aks/private-clusters
- https://blog.baeke.info/2021/07/01/dns-options-for-private-azure-kubernetes-service/
- https://docs.microsoft.com/en-us/azure/aks/coredns-custom
- https://docs.microsoft.com/en-us/azure/templates/microsoft.containerservice/managedclusters?tabs=bicep
- https://docs.microsoft.com/en-us/azure/firewall/protect-azure-kubernetes-service
- https://docs.microsoft.com/en-us/azure/active-directory/managed-identities-azure-resources/how-managed-identities-work-vm#user-assigned-managed-identity
- https://github.com/marcusbakker/KQL
