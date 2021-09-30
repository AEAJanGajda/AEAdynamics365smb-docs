---
    title: How to Set Up Electronic Invoicing [MX]
    description: Before you can send electronic documents, you must set up Business Central to ensure that the required identification numbers are in place.

    author: SorenGP

    ms.service: dynamics365-business-central
    ms.topic: conceptual
    ms.devlang: na
    ms.tgt_pltfrm: na
    ms.workload: na
    ms.search.keywords:
    ms.date: 06/18/2021
    ms.author: edupont

---
# Set Up Electronic Invoicing in the Mexican Version

Before you can send electronic documents, you must set up [!INCLUDE[prod_short](../../includes/prod_short.md)] to ensure that the tax identification number (RFC), personal identification number (CURP), and state inscription IDs are available for your company and all your customers and vendors. You also need to set up the parameters that are needed for sending electronic invoices to customers and vendors. These parameters include the certificate thumbprint, which is the certificate that you received from the Mexico tax authority (SAT).  

> [!IMPORTANT]  
> The certificate that you received from the Mexico tax authority must be installed for each user who sends electronic invoices. For more information, see the [Servicio de Administracíon Tributaria](https://go.microsoft.com/fwlink/?LinkId=242772) website.  
>
> Your company must also have SMTP mail set up for emailing electronic invoices. Depending on the configuration in your company, you may need to grant explicit SMTP permissions to each relevant user and computer. The documents will be sent from the address that is specified on the **Company Information** page.  

## To set up company information  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Company Information**, and then choose the related link.  
2. On the **Company Information** page, on the **Tax** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |------------------------------------|---------------------------------------|
    |**Tax Scheme**|Enter the tax scheme that your company uses complies with. Commonly used tax schemes are Régimen General, Régimen intermedio, and Régimen de pequeños contribuyentes (REPECOS).|
    |**RFC No.**|Enter the federal registration number for taxpayers. The Registro Federal de Contribuyentes (RFC) tax identification type can be applied to companies and to people. An RFC number for a company is 12 characters, while an RFC number for a person is 13 characters.|
    |**CURP No.**|Enter the unique fiscal card identification number. The Cédula de identification fiscal con clave única de registro de población (CURP) tax identification type can only be applied to people. A CURP number is 18 characters.|
    |**State Inscription**|Enter the tax ID number that is assigned by state tax authorities to every person or corporation.|

## To set up general ledger information  

1. Choose the ![Lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **General Ledger Setup**, and then choose the related link.  
2. On the **General Ledger Setup** page, on the **Electronic Invoice** FastTab, fill in the fields as described in the following table.  

    |Field|Description|  
    |------------------------------------|---------------------------------------|  
    |**SAT Certificate Thumbprint**|Enter the friendly name of the certificate that you want to use for issuing electronic invoices. **Note:**  A certificate is needed for each user who sends electronic invoices. To get the certificate thumbprint, see the Help for the operating system.|  
    |**Send PDF Report**|Select to include a PDF when you email electronic invoices to customers or vendors. Electronic invoices are always sent as an XML file, this option allows you to include a PDF with the XML file.|  
    |**PAC Code**|Specify the authorized service provider, PAC, that you want apply digital stamps to your electronic invoices. **Note:**  To use a PAC, you must set up web services. For more information, see [Set Up PAC Web Services](how-to-set-up-pac-web-services.md).|  
    |**PAC Environment**|Specify if your company uses electronic invoices, and if you are using the web services of your authorized service provider, PAC, in a test environment or a production environment.|  

Optionally, you can ask your Microsoft Certified Partner to modify the text that is included in the email that is sent when you send electronic invoices. The text is stored as text variables in codeunit 10145.  

## To set up customer and vendor information

Finally, you must add information about your customers and vendors. The following section section describes how to specify this information to customers, but the same fields must be specified for vendors.

1. Choose the ![A third lightbulb that opens the Tell Me feature.](../../media/ui-search/search_small.png "Tell me what you want to do") icon, enter **Customer Card**, and then choose the related link.
2. In the **Customer Card** window, on the **Invoicing** FastTab, fill in the fields as described in the following table.

    |Field|Description|
    |------------------------------------|---------------------------------------|
    |**RFC No.**|Enter the federal registration number for taxpayers. The RFC number must contain 12 digits.|
    |**CURP No.**|Enter the unique fiscal card identification number. The CURP number must contain 18 digits.|
    |**State Inscription**|Enter the tax ID number that is assigned by state tax authorities to every person or corporation.|

    > [!NOTE]
    > If you select the **Prices Including VAT** field for a customer, the electronic documents will include VAT in all amounts, including unit prices. The electronic documents will also contain a separate element for VAT. If you want to avoid any possible confusion about the amounts including VAT, you can choose to not select the **Prices Including VAT** field.

3. On the **Payments** FastTab, in the **Payment Method Code** field, specify the payment method that you want to use for this customer.

## See Also

[Electronic Invoicing](electronic-invoicing.md)  
[Generate Electronic Invoices](how-to-generate-electronic-invoices.md)  
[Mexico Local Functionality](mexico-local-functionality.md)  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]