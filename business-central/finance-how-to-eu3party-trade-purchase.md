---
title: EU third-party purchase transactions
description: This article topic explains how to set up and use European Union (EU) third-party purchase transactions.
author: altotovi
ms.topic: conceptual
ms.devlang: al
ms.search.form: '50, 51, 52, 187, 317'
ms.search.keywords: 'EU3P, EU 3-P, EU 3-Party'
ms.date: 07/07/2023
ms.author: altotovi
ms.service: dynamics-365-business-central
ms.reviewer: bholtorf
---

# <a name="eu-third-party-purchase-transactions"></a>EU third-party purchase transactions

European Union (EU) third-party trade occurs when you receive a purchase invoice from a customer in one EU country/region, and the products are sent to a different EU country/region without entering the country of residence. The transaction amount can be identified and reported separately to comply with some EU countries'/regions' value-added tax (VAT) reporting and VAT Information Exchange System (VIES) requirements. Microsoft Dynamics 365 Business Central enables purchase transactions to be set up as EU third-party trade. Posted EU third-party transactions can be filtered in VAT statements and excluded from the amount in the **Sales to Customer** column of the **VAT-VIES Declaration Tax Auth** report.

Even if the feature is preinstalled as an extension, it isn't activated by default. Follow these steps to activate the feature.

1. Select the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, go to the **Feature Management** workspace, and then select the related link.
2. In the list, find and select **Feature update: Replace the existing EU 3-Party Purchase functionality with the new EU 3-Party Trade Purchase extension**.
3. In the **Enabled for** column, select **All users**.

## <a name="enable-eu-third-party-trade-functionality-for-a-purchase"></a>Enable EU third-party trade functionality for a purchase

1. Select the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Setup**, and then select the related link.
2. On the **VAT Setup** page, mark the **Enable EU 3-Party Purchase** field.

## <a name="use-eu-third-party-trade-functionality"></a>Use EU third-party trade functionality

1. Select the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Purchase Invoice** (or another purchase document), and then select the related link.
2. Select an existing purchase invoice, or select **New** to create a new one.
3. On the **Invoice Details** FastTab, select the **EU 3-Party Trade** checkbox.
4. Select **OK**.

## <a name="include-or-exclude-eu-third-party-trade-records-on-the-vat-statement"></a>Include or exclude EU third-party trade records on the VAT statement

1. Select the ![Lightbulb that opens the Tell Me feature.](media/ui-search/search_small.png "Tell me what you want to do") icon, enter **VAT Statement**, and then select the related link.
2. On the **VAT Statement** page, select one of the following options to show EU third-party trade records by using the **EU 3-Party Trade Filter** field.

    | Option | Description |
    |--------|-------------|
    | All | Show all records, regardless of whether the **EU 3-Party Trade** field in documents was marked. |
    | EU3 | Show only records where the **EU 3-Party Trade** field in documents was marked. |
    | Non-EU3 | Show only records where the **EU 3-Party Trade** field in documents wasn't marked. |


## <a name="see-also"></a>See also
[Financial Management](finance.md)  
[Work with Business Central](ui-work-product.md)

[!INCLUDE[footer-include](includes/footer-banner.md)]
