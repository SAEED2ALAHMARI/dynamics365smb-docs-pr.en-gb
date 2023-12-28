---
title: Copilot data movement across geographies
description: Learn how data that's used in copilot features in Dynamics 365 Business Central moves across geographies where Azure OpenAI Service isn't available by default.
author: jswymer
ms.author: jswymer
ms.reviewer: jswymer
ms.topic: conceptual
ms.collection: null
ms.date: 11/30/2023
ms.custom: bap-template
---

# <a name="copilot-data-movement-across-geographies"></a>Copilot data movement across geographies

Copilot is available in all supported [Business Central countries/regions](/dynamics365/business-central/dev-itpro/compliance/apptest-countries-and-translations). However, Copilot uses Microsoft Azure OpenAI Service, which is currently available for Business Central in some geographical regions only. This means that if your environment is located elsewhere, data from the Copilot and generative AI features must be transmitted outside of your geographical region and might be processed and stored outside your compliance boundary. Data includes the AI prompts and your business data that's used by or generated by Copilot. In this case, you must opt in to allow data movement to an Azure OpenAI Service in another geography. <!--For a list of geographies, refer to the [Azure OpenAI Service geographies](#azure-openai-service-geographies) section that follows.-->

> [!IMPORTANT]
> If your environment is located in same Azure region as the Azure OpenAI Service, it automatically connects to Azure OpenAI Service, there's no option and no one-time configuration is required.

> [!NOTE]
> Individual Copilot and generative AI features might not be available in all Business Central environment countries/regions. Consult with the publisher of each capability to understand availability.
> 
> Copilot and generative AI features from non-Microsoft publishers, such as those originating from customisations or AppSource apps you install, each define their own specific Azure OpenAI Service regions. Consult with the extension publisher to understand which regional Azure services are used by the extension. 

### <a name="azure-openai-service-geographies"></a>Azure OpenAI Service geographies

The following table shows the Azure OpenAI Service's geography used by Copilot, based on the Azure region of a Business Central environment. This information is important when deciding whether to opt in for data movement across geographies. You can identify the Azure region for your environment in the Business Central admin centre (see [Managing environments in the admin centre](/dynamics365/business-central/dev-itpro/administration/tenant-admin-center-environments)).

| Environment Azure region| Azure OpenAI Service geography|Admin action required to unlock Copilot| 
| - | - | - |
|Asia (East, South East) |United States|Yes|
|Australia (South East)| United States |Yes |
|Brazil (South) |United States|Yes|
|Canada (Central, East)|United States|Yes|
|Europe (West, North)| Sweden or Switzerland |Yes|
|France (Central, South)| Sweden or Switzerland |Yes|
|Germany (North, West Central)| Sweden or Switzerland |Yes|
|India (Central, South)|United States|Yes|
|Japan (East, West)|United States|Yes|
|Korea (Central, South)|United States|Yes|
|Norway (East, West)|Sweden or Switzerland |Yes|
|South Africa (North, West)|United States|Yes|
|Switzerland (North, West) |Sweden or Switzerland |Yes|
|United Arab Emirates (North, West)|United States|Yes|
|United Kingdom (South, West)|United Kingdom|Yes|
|United States (Central, East, North Central, South Central, West) |United States|No|

> [!NOTE]
> Once an Azure OpenAI Service becomes available in your  Business Central geography, your environment will automatically transition to use the Azure OpenAI Service and opting in isn't required or even possible.  
<!--

BC geos base on https://dynamics.microsoft.com/en-us/availability-reports/georeport/
case "AUSTRALIAEAST":
            case "AUSTRALIASOUTHEAST":
                return new CapiRegion("au", 2);
            case "BRAZILSOUTH":
                return new CapiRegion("br", 2);
            case "CANADACENTRAL":
            case "CANADAEAST":
                return new CapiRegion("ca", 2);
            case "CENTRALINDIA":
            case "SOUTHINDIA":
                return new CapiRegion("in", 1);
            case "EASTASIA":
                return new CapiRegion("as", 2);
            case "EASTUS":
            case "EASTUS2":
            case "SOUTHCENTRALUS":
            case "CENTRALUS":
            case "NORTHCENTRALUS":
            case "WESTUS":
            case "US":
                return new CapiRegion("us", 9, HasGpt4InGeo: true, HasTurboInGeo: true);
            case "FRANCECENTRAL":
            case "FRANCESOUTH":
                return new CapiRegion("fr", 1);
            case "GERMANYNORTH":
            case "GERMANYWESTCENTRAL":
                return new CapiRegion("de", 1);
            case "JAPANEAST":
            case "JAPANWEST":
                return new CapiRegion("jp", 1);
            case "KOREACENTRAL":
            case "KOREASOUTH":
                return new CapiRegion("kr", 1);
            case "NORWAYEAST":
            case "NORWAYWEST":
                return new CapiRegion("no", 1);
            case "SOUTHAFRICANORTH":
            case "SOUTHWESTAFRICA":
                return new CapiRegion("za", 1);
            case "SOUTHEASTASIA":
                return new CapiRegion("sg", 1);
            case "SWITZERLANDNORTH":
            case "SWITZERLANDWEST":
                return new CapiRegion("ch", 1, HasTurboInGeo: true);
            case "UKSOUTH":
            case "UKWEST":
                return new CapiRegion("uk", 2);
            case "NORTHEUROPE":
            case "WESTEUROPE":
                return new CapiRegion("eu", 10);
            case "UAENORTH":
            case "UAECENTRAL":
                return new CapiRegion("ae", 1);

-->

## <a name="next-steps"></a>Next steps

You opt in to allow data movement across geographies from the [Copilot & AI Capabilities](https://businesscentral.dynamics.com/?page=7775) page. To learn more, go to [Allow data movement across geographies](enable-ai.md#allow-data-movement-across-geographies).