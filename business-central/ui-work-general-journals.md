---
title: Using General Journals to Post Directly to G/L| Microsoft Docs
description: Learn about using general journals to post financial transactions to general ledger accounts and other accounts, such as bank and vendor accounts.
author: SorenGP
ms.service: dynamics365-business-central
ms.topic: article
ms.devlang: na
ms.tgt_pltfrm: na
ms.workload: na
ms.date: 02/23/2018
ms.author: sgroespe
ms.translationtype: HT
ms.sourcegitcommit: e7dcdc0935a8793ae226dfc2f9709b5b8f487a62
ms.openlocfilehash: 090a0141583795757a0d59b358ba4d553100d976
ms.contentlocale: en-gb
ms.lasthandoff: 03/22/2018

---
# <a name="working-with-general-journals"></a>Working with General Journals
Most financial transactions are posted to the general ledger through dedicated business documents, such as purchase invoices and sales orders. For business activities that are not represented by a document in [!INCLUDE[d365fin](includes/d365fin_md.md)], such as smaller expenses or cash receipts, you can create the related transactions by posting journal lines in the **General Journal** window. For more information, see [Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md).

For example, you can post employees' expenditure of own money on business-related expenses, for later reimbursement. For more information, see [Record and Reimburse Employees' Expenses](finance-how-record-reimburse-employee-expenses.md).

You use general journals to post financial transactions directly to general ledger accounts and other accounts, such as bank, customer, vendor, and employee accounts. Posting with a general journal always creates entries on general ledger accounts. This is true even when, for example, you post a journal line to a customer account, because an entry is posted to a general ledger receivables account through a posting group.

The information that you enter in a journal is temporary and can be changed while it is in the journal. When you post the journal, the information is transferred to entries on individual accounts, where it cannot be changed. You can, however, unapply posted entries, and you can post reversing or correcting entries. For more information, see [Reverse Postings](finance-how-reverse-journal-posting.md).

## <a name="using-journal-templates-and-batches"></a>Using Journal Templates and Batches
There are several general journal templates. Each journal template is represented by a dedicated window with particular functions and the fields that are required to support those functions, such as the **Payment Reconciliation Journal** window to process bank payments and the **Payment Journal** window to pay your vendors or reimburse your employees. For more information, see [Make Payments](payables-make-payments.md) and [Reconcile Customer Payments Manually](receivables-how-apply-sales-transactions-manually.md).

For each journal template, you can set up your own personal journal as a journal batch. For example, you can define your own journal batch for the payment journal that has your personal layout and settings. The following tip is an example of how to personalise a journal.

> [!TIP]  
> If you select the **Suggest Balancing Amount** check box on the line for your batch in the **General Journal Batches** window, then the **Amount** field on, for example, general journal lines for the same document number is automatically prefilled with the value that is required to balance the document. For more information, see [Letting [!INCLUDE[d365fin](includes/d365fin_md.md)] Suggest Values](ui-let-system-suggest-values.md).

## <a name="understanding-main-accounts-and-balancing-accounts"></a>Understanding Main Accounts and Balancing Accounts
If you have set up default balancing accounts for the journal batches on the **General Journals** page, the balancing account will be filled in automatically when you fill in the **Account No.** field. Otherwise, fill in both the **Account No.** field and the **Bal. Account No.** field manually. A positive amount in the **Amount** field is debited to the main account and credited to the balancing account. A negative amount is credited to the main account and debited to the balancing account.

> [!NOTE]  
>   VAT is calculated separately for the main account and the balancing account, so they can use different VAT percentage rates.

## <a name="working-with-recurring-journals"></a>Working with Recurring Journals
A recurring journal is a general journal with specific fields for managing transactions that you post frequently with few or no changes, such as rent, subscriptions, electricity, and heat. Using these fields for recurring transactions, you can post both fixed and variable amounts. You can also specify automatic reversal entries for the day after the posting date. You can also use allocation keys to divide the recurring entries among various accounts. For more information, see the "Allocating Recurring Journal Amounts to Several Accounts" section.

With a recurring journal, entries that will be posted regularly need to be typed in only once. That is, the accounts, dimensions and dimension values and so on that you enter will be remain in the journal after posting. If any adjustments are necessary, you can make them with each posting.

### <a name="recurring-method-field"></a>Recurring Method field
This field determines how the amount on the journal line is treated after posting. For example, if you will use the same amount every time you post the line, you can let the amount remain. If you will use the same accounts and text on the line but the amount will vary every time you post, you can choose to delete the amount after posting.

| To | See |
| --- | --- |
|Fixed|The amount on the journal line will remain after posting.|
|Variable|The amount on the journal line will be deleted after posting.|
|Balance|The posted amount on the account on the line will be allocated among the accounts specified for the line in the Gen. Jnl. Allocation table. The balance on the account will thus be set to zero. Remember to fill in the **Allocation %** field in the **Allocations** window. For more information, see the "Allocating Recurring Journal Amounts to Several Accounts" section.|
|Reversing Fixed|The amount on the journal line will remain after posting, and a balancing entry will be posted on the next day.|
|Reversing Variable|The amount on the journal line will be deleted after posting, and a balancing entry will be posted on the next day.|
|Reversing Balance|The posted amount on the account on the line will be allocated among the accounts specified for the line in the **Allocations** window. The balance on the account will be set to zero, and a balancing entry is posted on the next day.|

> [!NOTE]  
>  The VAT fields can be filled in on either the recurring journal line or on the allocation journal line but not on both. That is, they can be filled in in the **Allocations** window only if the corresponding lines in the recurring journal are not filled in.

### <a name="recurring-frequency-field"></a>Recurring Frequency field
This field determines how often the entry on the journal line will be posted. It is a date formula field, and it must be filled in for recurring journal lines. For more information, see the "Using Date Formulas" section in [Entering Data](ui-enter-data.md).

#### <a name="examples"></a>Examples
If the journal line must be posted every month, enter "1M". After every posting, the date in the **Posting Date** field will be updated to the same date in the next month.

If you want to post an entry on the last day of every month, you can do one of the following:

- Post the first entry on the last day of a month by entering 1D+1M-1D (1 day + 1 month - 1 day). With this formula, the posting date is calculated correctly regardless of how many days there are in the month.

- Post the first entry on any arbitrary day of a month by entering 1M+CM. With this formula, the posting date will be after one full month + the remaining days of the current month.

### <a name="expiration-date-field"></a>Expiration Date field
This field determines the date on which the line will be posted for the last time. The line will not be posted after this date.

The advantage of using the field is that the line will not be deleted from the journal immediately and you can always replace the present expiration date with a later one so that you can use the line further into the future.

If the field is blank, the line will be posted every time you post until it is deleted from the journal.

### <a name="allocating-recurring-journal-amounts-to-several-accounts"></a>Allocating Recurring Journal Amounts to Several Accounts
In the **Recurring General Journal** window, you can choose the **Allocations** action to see or manage how amounts on the recurring journal line are allocated to several accounts and dimensions. Note that an allocation functions as balancing account line to the recurring journal line.

Just as in a recurring journal, you need to enter an allocation only once. The allocation will remain in the allocation journal after posting, so you do not need to enter amounts and allocations every time you post the recurring journal line.

If the recurring method in the recurring journal is set to **Balance** or **Reversing Balance**, then any dimension value codes in the recurring journal are disregarded when the account is set to zero. So if you allocate a recurring line to various dimension values in the **Allocations** window, then only one reversing entry will be created. Therefore, if you allocate a recurring journal line that contains a dimension value code, then you must not enter the same code in the **Allocations** window. If you do, the dimension values will be incorrect.

####<a name="example-allocating-rent-payments-to-different-departments"></a>Example: Allocating Rent Payments to Different Departments
You pay rent every month, so you have entered the rent amount on the cash account on a recurring journal line. In the **Allocations** window, you can divide the expense among several departments (Department dimension) according to the number of square feet that each one occupies. The calculation is based on the allocation percentage on each line. You can enter various accounts on different allocation lines (if rent will also be divided among several accounts), or you can enter the same account but with various dimension value codes for the Department dimension on each line.


## <a name="working-with-standard-journals"></a>Working with Standard Journals
When you have created journal lines which you know you are likely to create again later, you can save them as a standard journal before you post the journal. This functionality applies to item journals and general journals.

> [!NOTE]  
>   The following procedure refers to the item journal, but the information also applies to the general journal.

### <a name="to-save-a-standard-journal"></a>To save a standard journal
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Journals**, and then choose the related link.
2. Enter one or more journal lines.
3. Select the journal lines that you want to reuse.
4. Choose the **Save as Standard Journal** action.
5. In the **Save as Standard Item Journal** request window, define a new or existing standard item journal that the lines should be saved in.

    If you have already created one or more standard item journals and you want to replace one of these with the new set of item journal lines, in the Code field, select the code you want.
6. Choose the **OK** button to verify that you want to overwrite the existing standard item journal and replace all its content.
7. Select the **Save Unit Amount** field if you want to save the values in the **Unit Amount** field of the standard item journal.
8. Select the **Save Quantity** field if you want the program to save the values in the **Quantity** field.
9. Choose the **OK** button to save the standard item journal.

When you have finished saving the standard item journal, the Item Journal window is displayed so you can proceed to post it, knowing that it can easily be recreated next time you need to post the same or similar lines.

### <a name="to-reuse-a-standard-journal"></a>To reuse a standard journal
1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **Item Journals**, and then choose the related link.
2. Choose the **Get Standard Journals** action.

    The Standard Item Journals window opens showing codes and descriptions for all existing standard item journals.
3. To review a standard item journal before you select it for reuse, choose the **Show Journal** action.

    Any changes you make in a standard item journal are implemented right away. They will be there next time you open or reuse the standard item journal in question. You should therefore be sure that the change is important enough to apply generally. Otherwise, make the specific change in the item journal after the standard item journal lines have been inserted. See step 4 below.
4. In the **Standard Item Journals** window, select the standard item journal you want to reuse, and then choose the **OK** button.

    Now the item journal is filled with the lines you saved as the standard item journal. If journal lines already existed in the item journal, the inserted lines will be placed under the existing journal lines.

    If you did not check the **Save Unit Amount** field when you used the **Save as Standard Item Journal** function job, then the **Unit Amount** field on lines that are inserted from the standard journal is automatically filled with the item’s current value, copied from the **Unit Cost** field on the item card.

    > [!NOTE]  
    >   If you selected the **Save Unit Amount** or **Save Quantity** fields, you should now make sure the inserted values are correct for this particular inventory adjustment before you post the item journal.

    If the inserted item journal lines contain saved unit amounts that you do not want to post, you can quickly adjust it to the current value of the item as follows.

6. Select the item journal lines you want to adjust, and then choose the **Recalculate Unit Amount** action. This will update the Unit Amount field with the current unit cost of the item.
7. Choose the **post** action.

## <a name="to-renumber-document-numbers-in-journals"></a>To renumber document numbers in journals
To make sure that you do not receive posting errors because of the document number order, you can use the **Renumber Document Numbers** function before you post a journal.

In all journals that are based on the general journal, the **Document No.** field is editable so that you can specify different document numbers for different journal lines or the same document number for related journal lines.

If the **No. Series** field on the journal batch is filled, then the posting function in general journals requires that the document number on individual or grouped journal lines be in sequential order. To make sure that you do not receive posting errors because of the document number order, you can use the **Renumber Document Numbers** function before you post the journal. If related journal lines were grouped by document number before you used the function, they will remain grouped but may be assigned a different document number.

This function also works on filtered views.

Any renumbering of document numbers will respect related applications, such as a payment application that has been made from the document on the journal line to a vendor account. Accordingly, the **Applies-to ID** and **Applies-to Doc. No.** fields on the affected ledger entries may be updated.

The following procedure is based on the **General Journal** window, but applies to all other journals that are based on the general journal, such as the **Payment Journal** window.

1. Choose the ![Search for Page or Report](media/ui-search/search_small.png "Search for Page or Report icon") icon, enter **General Journals**, and then choose the related link.
2. When you are ready to post the journal, choose the **Renumber Document Numbers** action.

Values in the **Document No.** field are changed, where required, so that the document number on individual or grouped journal lines are in sequential order. After documents are renumbered, you can proceed to post the journal.

## <a name="see-also"></a>See Also
[Post Transactions Directly to the General Ledger](finance-how-post-transactions-directly.md)  
[Reverse Postings](finance-how-reverse-journal-posting.md)  
[Allocate Costs and Income](year-allocate-costs-income.md)  
[Finance](finance.md)  
[Working with [!INCLUDE[d365fin](includes/d365fin_md.md)]](ui-work-product.md)
