---
title: Exploring and Navigating Pages and Reports per Role
description: 'You can get an overview of all the business features that are available for your role, and for other roles, with the Role Explorer.'
author: jswymer
ms.topic: conceptual
ms.devlang: al
ms.search.keywords: 'role explorer, find features, navigate'
ms.search.form: 'RoleExplorer, 9020, 9022, 9027, 9024'
ms.date: 08/01/2021
ms.author: jswymer
ms.service: dynamics-365-business-central
ms.reviewer: jswymer
---

# <a name="finding-pages-and-reports-with-the-role-explorer"></a>Finding pages and reports with the role explorer

You can get an overview of all the business features that are available for your role, and for other roles if you go a step further. This article refers to the feature overview as the *role explorer*.

Each element on the role explorer is an action that opens a page or report. Accordingly, you can also use the role explorer as a means to navigate in [!INCLUDE[prod_short](includes/prod_short.md)].

[!INCLUDE [about-ui-learn](includes/about-ui-learn.md)]

## <a name="open-the-role-explorer"></a>Open the role explorer

You can open the role explorer from the role centre and all list pages and from the **Tell Me** window.

- On your role centre or any list page, choose the ![Menu button.](media/ui_menu_button.png "Menu button") button to the right of the navigation bar, or select <kbd>Shift</kbd>+<kbd>F12</kbd>.
- In the **Tell Me** window, choose the **exploring** action at the bottom.

When you first open the role centre, it shows links to most features available for your role.

## <a name="open-the-role-explorer-filtered-to-show-reports"></a>Open the role explorer filtered to show reports

You can open the role explorer in a view that's filtered to show reports from the role centre and all list pages and from the **Tell Me** window:

- On your Role Centre or any list page, choose the **All Reports** link to the right of the navigation bar.
- In the **Tell Me** window, choose the **exploring reports** action at the bottom.

## <a name="navigate-features"></a>Navigate features

The actions that open pages or reports are organised under nodes named after the features or application areas. You can collapse or expand each node individually, or all nodes together.

- To expand/collapse an individual node, choose the node. This applies to top-level nodes and sub nodes.
- To expand/collapse all top-level nodes on the page, but leave the sub-nodes as they are, choose **...** at the top, then choose **Expand** or **Collapse**.
- To expand/collapse all top-levels node and all sub nodes under it, choose **...** at the top, then choose the **Expand All** or **Collapse All** action.

## <a name="search-for-features"></a>Search for features

To quickly locate features, select **Find**, then enter a word or phrase for the feature your trying to find. The role centre highlights any matching text. If a feature is hidden in a collapsed node, the collapsed node is marked with a dot. 

## <a name="explore-other-roles"></a>Explore other roles

To explore roles other than your own, select **Explore more roles**. The role centre displays each role under its own heading, with links to its features. You can find and go to features just like you do when exploring your role.

> [!NOTE]
> You'll only access roles that are set up to show in the role explorer. If a role isn't available, it's probably not set up for it. For more information, see [Manage Profiles](admin-users-profiles-roles.md). 

When exploring other roles, you can also narrow down the exploration by using the **Report & Analysis** and **Administration** actions at the top of the role centre.

- **Report & Analysis** shows only those features that are categorised as reports and analysis features.
- **Administration** shows only those features that are categorised as administration features.

> [!TIP]
> For developers, you categorise pages and reports by setting the [UsageCategory property](/dynamics365/business-central/dev-itpro/developer/properties/devenv-usagecategory-property) in the object's AL code.
<!--
 
## <a name="role-explorer-actions"></a>Role explorer actions

There a several actions along the top of the role explorer to help you locate features of your role and other roles.

|Action|Description|
|------|------|
|**All**|Shows all features that are related to the role.|
|**Find**|Lets you enter a word or phrase to quickly locate feature names that match.|
|**Explore more roles**|All business features that are available for all roles including your own. When exploring all roles, the other actions work the same way, except for all roles shown. **NOTE:** You can only access roles that are set up to show in role explorer. For more information, see [Manage Profiles](admin-users-profiles-roles.md).  |
|**Report & Analysis**|This action Shows only those features that are categorized as reports and analysis features.|
|**Administration**|Shows only those features that are categorized as administration features.|



<!--
Choose the **Find** action at the top of the role explorer to quickly locate feature names that contain a certain term.

Choose the **Explore more roles** action at the top of the role explorer to get an overview of all business features that are available for all roles including your own.

> [!NOTE]
> Only Role Center actions for profiles where the **Show in Role Explorer** check box is selected will appear on the extended version of the role explorer (shown with the **Explore more roles** action). For more information, see [Manage Profiles](admin-users-profiles-roles.md).
-->

## <a name="expand-and-collapse-nodes-on-the-role-explorer"></a>Expand and collapse nodes on the role explorer

The actions that open pages are organised under nodes named after the features or application areas. Each node can be collapsed or expanded individually and you can collapse/expand all nodes together.

- To expand/collapse a node, choose the node. This applies to top-level nodes and sub nodes.
- To expand/collapse all top-level nodes on the page, choose the **Expand** or **Collapse** action in the top-right corner.
- To expand/collapse all top-levels node and all sub nodes under it, do one of the following steps:
  - Select the <kbd>Ctrl</kbd>+<kbd>Shift</kbd> keys while you choose the **Expand** or **Collapse** action in the top-right corner.
  - Choose **...** in the top-right corner, then choose the **Expand All** or **Collapse All** action.

## <a name="see-also"></a>See Also

[Finding Pages and Information with Tell Me](ui-search.md)  
[Manage Profiles](admin-users-profiles-roles.md)  
[Work with [!INCLUDE[prod_short](includes/prod_short.md)]](ui-work-product.md)  

[!INCLUDE[footer-include](includes/footer-banner.md)]
