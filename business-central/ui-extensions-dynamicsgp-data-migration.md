---
title: Migrate Data from Dynamics GP with the Data Migration Extension | Microsoft Docs
description: Use the Dynamics GP Data Migration extension to migrate customers, vendors, inventory items, and accounts from Dynamics GP to Business Central .
documentationcenter: 
author: edupont04
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms. search.keywords: app, add-in, manifest, customize, import, implement
ms.date: 03/29/2017
ms.author: edupont
ms.translationtype: HT
ms.sourcegitcommit: ad1b888d475c0523c5a905e804a3f89ab4531b28
ms.openlocfilehash: 3761bdb0d6b9a51ed309ac4189ff263de76f4679
ms.contentlocale: en-gb
ms.lasthandoff: 05/17/2018

---
# <a name="the-dynamics-gp-data-migration-extension-for-business-central"></a>The Dynamics GP Data Migration Extension for Business Central 
This extension makes it easy to migrate customers, vendors, inventory items, and accounts from Dynamics GP to [!INCLUDE[d365fin](includes/d365fin_md.md)]. If your business uses Dynamics GP today, you can export the relevant master records and then open an assisted setup guide to add the data to [!INCLUDE[d365fin](includes/d365fin_md.md)]. For more information, see [Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md).

## <a name="exporting-data-from-dynamics-gp"></a>Exporting Data from Dynamics GP
You must have exported some or all of your existing customers, vendors, inventory items, and accounts to a file, using the Dynamics GP functionality for data export. For the purposes of [!INCLUDE[d365fin](includes/d365fin_md.md)], you can export the following types of data:

* Account  
* Customer  
* Item  
* Vendor  

The Dynamics GP Data Migration extension automatically maps the exported data so that your data is quickly available to you in your new [!INCLUDE[d365fin](includes/d365fin_md.md)] company. During the process, supporting setup information is created, such as posting groups. Inventory items will be brought into the system with FIFO as the cost valuation method. Accounts will be set up as the main account segment from Dynamics GP with dimensions, because [!INCLUDE[d365fin](includes/d365fin_long_md.md)] does not have account segments.

## <a name="see-also"></a>See Also
[Importing Business Data from Other Finance Systems](across-import-data-configuration-packages.md)  
[Customizing [!INCLUDE[d365fin](includes/d365fin_md.md)] Using Extensions ](ui-extensions.md)  
