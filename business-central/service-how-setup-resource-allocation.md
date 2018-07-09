---
title: Set Up Resource Allocation | Microsoft Docs
description: Learn how the system can help ensure that you assign someone who has the skills required to provide a service.
services: project-madeira
documentationcenter: 
author: bholtorf
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.search.keywords: resource, skill, service, zones
ms.date: 08/22/2017
ms.author: bholtorf
ms.translationtype: HT
ms.sourcegitcommit: d7fb34e1c9428a64c71ff47be8bcff174649c00d
ms.openlocfilehash: 6dc4a059cb3bca46910a4a4be43a5940a5652c8f
ms.contentlocale: en-gb
ms.lasthandoff: 03/22/2018

---

# <a name="set-up-resource-allocation"></a>Set Up Resource Allocation
To ensure that a service task is performed well, it's important to find a resource who is qualified to do the work. You can set up [!INCLUDE[d365fin](includes/d365fin_md.md)] so that it's easy to allocate someone who has the right skills for the job. In [!INCLUDE[d365fin](includes/d365fin_md.md)], we call this _resource allocation_. You can allocate resources based on their skill, availability, or whether they are in the same service zone as the customer. 

To use resource allocation, you must set up:  
  
* The skills required to repair and maintain service items. You assign these to service items and resources.  
* Geographic regions, called zones, that you define for your market. For example, East, West, Central, and so on. You assign these to customers and resources.  
* Whether to display resource skills and zones, and whether to display a warning if someone chooses unqualified resource, or a resource that is not in the customer zone.  

## <a name="to-set-up-skills"></a>To set up skills
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Skills**, and then choose the related link.  
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-skills-to-service-items-and-resources"></a>To assign skills to service items and resources
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Items** or **Resources**, and then choose the related link.  
2. Open the card for the service item or resource, and then choose one of the following:  
  
    * For service items, choose **Resource Skills**.  
    * For resources, choose **Skills**.  

## <a name="to-set-up-zones"></a>To set up zones
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Zones**, and then choose the related link.  
2. Fill in the fields as necessary. [!INCLUDE[tooltip-inline-tip](includes/tooltip-inline-tip_md.md)]  

## <a name="to-assign-zones-to-customers-and-resources"></a>To assign zones to customers and resources 
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Customers** or **Resources**, and then choose the related link.  
2. Open the card for the service item or resource, and then choose one of the following:  
  
    * For customers, choose a zone in the **Service Zone Code** field.  
    * For resources, choose the **Service Zones** action.  

## <a name="to-specify-what-to-show-when-a-resource-is-chosen"></a>To specify what to show when a resource is chosen
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Service Setup**, and then choose the related link. 
2. In the **Resource Skills Option** field, choose one of the options described in the following table.  
  
    |**Option**|**Description**|  
    |------------|-------------|  
    |Code Shown | Displays the code only.|  
    |Warning Displayed | Shows the information and displays a warning if you choose a resource that is not qualified.|  
    |Not Used | Does not show this information.|  

## <a name="to-update-resource-capacity"></a>To update resource capacity  
You may need to change the capacity of resources.  
  
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Resource Capacity**, and then choose the related link.  
2. Choose the resource, and then choose the **Set Capacity** action.  
3. Make the changes, and then choose **Update Capacity**.  

## <a name="to-update-skills-for-items-service-items-or-service-item-groups"></a>To update skills for items, service items, or service item groups
If you want to change the skill codes assigned to items, for example from **PC** to **PCS**, you can do so either for an item, service item, or for all items in a service item group.  
  
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Items** or **Service Item**, or **Service Item Group**, and then choose the related link.  
2. Choose the entity to update, and then choose the **Resource Skills** action.  
3. On the line with the code to be changed, in the **Skill Code** field, choose the relevant skill code.  
4.  If the item has associated service items, a dialogue box opens with the following two options:  
  
    * Change the skill codes to the selected value: Select this option if you want to replace the old skill code with the new one on all the related service items.  
    * Delete the skill codes or update their relation: Select this option if you want to change the skill code on this item only. The skill code on the related service items will be reassigned, that is, the **Assigned From** field will be updated.  
  
## <a name="see-also"></a>See Also
[Allocate Resources](service-how-to-allocate-resources.md)  
[Set Up Work Hours and Service Hours](service-how-setup-work-service-hours.md)  
[Set Up Fault Reporting](service-how-setup-fault-reporting.md)  
[Set Up Codes for Standard Services](service-how-setup-service-coding.md)  
 

