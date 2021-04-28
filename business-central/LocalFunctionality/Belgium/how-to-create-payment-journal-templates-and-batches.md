---
title: How to Create Payment Journal Templates and Batches
description: In the Belgian version of Business Central, payment suggestions are generated and posted in payment journals. The structure of the payment journal is similar to the structure of other journal types.
author: SorenGP

ms.service: dynamics365-business-central
ms.topic: conceptual
ms.search.keywords:
ms.date: 04/01/2021
ms.author: edupont

---
# Create Payment Journal Templates and Batches
In [!INCLUDE[prod_short](../../includes/prod_short.md)], payment suggestions are generated and posted in payment journals. The structure of the payment journal is similar to the structure of other journal types. However, the payment journal contains some fields that are specific for processing payments. Before you can start generating payment suggestions, you have to set up a payment journal template and a payment journal batch.  

If you assign a bank account to the payment journal template, the bank account will be inserted on all payment journal batches and payment journal lines that are created by using this template. By specifying a bank account for the journal template, you can reduce the time that is required for checking the payment suggestions.  

## To create a payment journal template  

1. Choose the ![Lightbulb that opens the Tell Me feature](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Payment Journal Templates**, and then choose the related link.  
2. Choose the **New** action.  
3. On the **EB Payment Journal Templates** page, fill in the fields.  

    [!INCLUDE [tooltip-inline-tip_md](../../includes/tooltip-inline-tip_md.md)]

    > [!IMPORTANT]
    > If the **Page ID** and **Test Report ID** fields are not shown, you must add them through personalization. The fields must be filled in before you continue. For more information, see [Personalize Your Workspace](../../ui-personalization-user.md).
4. Repeat step 2 for any additional templates.

5. Choose the **OK** button.  

## To add payment journal batches to the journal template  

1.  On the **Payment Journal Templates** page, choose the **Batches** action.  
2.  On the **Paym. Journal Batch** page, fill in the fields as described in the following table.  

    |Field|Description|  
    |---------------------------------|---------------------------------------|  
    |**Name**|Enter a unique name for the journal batch.<br /><br /> **NOTE:** To have the journal name update numerically, include a number in the journal batch name. For example, the name KBC1 will increment by one number with every posting to KBC2, KBC3, and so on.|  
    |**Description**|Enter a description for the journal batch.|  
    |**Reason Code**|Optionally, specify the reason code that is linked to this journal batch.|  
    |**Status**|Specifies the status of the batch.|

Next, you can test the configuration. For more information, see [Test Electronic Payments](how-to-test-electronic-payments.md).  

3.  Choose the **OK** button.  

## See Also  
 [Belgian Electronic Payments](belgian-electronic-payments.md)   
 [Set Up Electronic Banking](how-to-set-up-electronic-banking.md)   
 [Set Up IBLC-BLWI Transaction Codes](how-to-set-up-iblc-blwi-transaction-codes.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]