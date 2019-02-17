---
title: AEM Document Security for Microsoft Office - Release Notes
seo-title: AEM Document Security for Microsoft Office - Release Notes
description: Read the release notes before you install AEM Document Security 6.2 Extension for Microsoft Office.
seo-description: Read the release notes before you install AEM Document Security 6.2 Extension for Microsoft Office.
uuid: 73928ed8-4cee-42de-b459-53ddbd11bc86
content-type: reference
geptopics: SG_AEMFORMS/categories/document_security
topic-tags: installing
discoiquuid: 7011b6fd-7e11-4619-ab40-aba89ec5de63
index: y
internal: n
snippet: y
---

# AEM Document Security for Microsoft Office - Release Notes{#aem-document-security-for-microsoft-office-release-notes}

## What's new in AEM Document Security for Microsoft Office <br> {#what-s-new-in-aem-document-security-for-microsoft-office-br}

* **Support for Office 2016**: Document Security Extension for Microsoft Office has added support for Microsoft Office 2016. It is also expected to work with Microsoft Office 2016 desktop applications installed as part of Office 365.
* **Support for third-party authentication providers:** You can use third-party authentication providers with AEM Forms Document Security. These authentication providers help you add an additional access layer to the protected documents. AEM Forms Document Security supports following extended authentication workflows:

    * Extended authentication using default AEM Forms URL
    * Extended authentication using a custom URL
    * Default extended authentication workflow with third-party identity providers configured on AEM Forms on JEE server
    * Custom extended authentication workflow with third-party identity providers configured on AEM Forms on JEE server
    * Extended authentication using customized page for listing SAML Authentications

  For detailed steps to configure extended authentication workflows, see the [Extended Authentication Scenarios](http://blogs.adobe.com/livecycle/2011/12/extended-authentication-scenarios.html) article.

>[!NOTE]
>
>The document uses terms Adobe Experience Manager Document Security for Microsoft Office, Adobe Experience Manager Document Security Extension for Microsoft Office, and Document Security Extension for Microsoft Office interchangeably.

## Installing and Configuring AEM Document Security Extension for Microsoft Office <br> {#installing-and-configuring-aem-document-security-extension-for-microsoft-office-br}

This version of Document Security Extension for Microsoft Office is compatible with Adobe LiveCycle Rights Management ES2 and later and Document Security add-on for AEM forms.

Review the information in this document before you install AEM Document Security Extension for Microsoft Office. For detailed installation instructions, see [Installing and Configuring AEM Document Security Extension for Microsoft Office](installing-configuring-aemdsext.md) article.

## Fixed issues {#fixed-issues}

* Protected Microsoft PowerPoint and Microsoft Word files do not support video content. (Ref# CQ-108451)
* On opening an embedded file from within a protected Microsoft PowerPoint file, the process for PowerPoint remains open even after the embedded file is closed. (Ref# CQ-88580)
* In a protected Microsoft Word 2013 files, if a watermark is present, then Microsoft Word crashes on pasting any text at the beginning of the file. (Ref# CQ-89652)

## Known issues {#known-issues}

### Third-party plug-ins not supported&nbsp; {#third-party-plug-ins-not-supported-nbsp}

AEM Document Security Extension for Microsoft Office does not work with third-party plug-ins. Uninstall any third-party plug-ins for Microsoft Office before you install Document Security Extension for Microsoft Office.

### Disabled menu options in Microsoft Word, Excel, and PowerPoint {#disabled-menu-options-in-microsoft-word-excel-and-powerpoint}

AEM Document Security Extension for Microsoft Office uses built-in protection features to protect documents, worksheets, and presentations. It disables a few Excel, Word, and PowerPoint menu options.

### Restrictions for Microsoft Office 2010, 2013, and 2016 {#restrictions-for-microsoft-office-and}

In Microsoft Office, the following options are unavailable during a protected session:

* Microsoft Office 2016

    * File &gt; Save As
    * File &gt; History
    * File &gt; Share
    * File &gt; Export
    * File &gt; Publish
    * File &gt; Account
    * File &gt; Info &gt; Protect Document/Workbook/Presentation &gt; Encrypt with Password
    * File &gt; Info &gt; Protect Document &gt;Add a Digital Signature
    * File &gt; Info &gt; Protect Document &gt; Mark as Final
    * Share option on top right

* Microsoft Office 2013

    * File &gt; Save As
    * File &gt; Share
    * File &gt; Export
    * File &gt; Account
    * File &gt; Info &gt; Protect Document/Workbook/Presentation &gt; Encrypt with Password
    * File &gt; Info &gt; Protect Document &gt;Add a Digital Signature
    * File &gt; Info &gt; Protect Document &gt; Mark as Final

* Microsoft Office 2010

    * File &gt; Save and Send 
    * File &gt; Help
    * File &gt; Info &gt; Protect Document/Workbook/Presentation &gt; Encrypt with Password
    * File &gt; Info &gt; Protect Document &gt;Add a Digital Signature
    * File &gt; Info &gt; Protect Document &gt; Mark as Final

### Opening a protected document from SharePoint Server {#opening-a-protected-document-from-sharepoint-server}

Opening the protected document: If you try to open a protected document in Document Security Extension for Microsoft Office from SharePoint Server without first opening the Microsoft Office program associated with the file type, such as Microsoft Word, Microsoft Excel, or Microsoft PowerPoint, the document may not open. An error message displays indicating that you install the applicable plug-in. Hence, it is recommended that you open the associated Microsoft Office program, before you open a protected document in Document Security Extension for Microsoft Office from SharePoint Server.

(Optional) It is recommended that you clear your cache folder before opening a protected document in Document Security Extension for Microsoft Office from SharePoint Server.

When you open a protected document from SharePoint Server, all permissions on the document are disabled, regardless of the policy that was applied.

### Apply a policy with a dynamic watermark to Microsoft Excel 2010, Microsoft Excel 2013, and Microsoft Excel 2016 file with no printer installed {#apply-a-policy-with-a-dynamic-watermark-to-microsoft-excel-microsoft-excel-and-microsoft-excel-file-with-no-printer-installed}

When you apply a policy with dynamic watermark to Microsoft Excel 2010, Microsoft Excel 2013, and Microsoft Excel 2016 file on a computer that has no printers installed and then save the file, the following error appears: "Internal error while applying dynamic watermark." This error also appears when you reopen the protected file. The watermark is not applied and it is not visible from View &gt; Page Layout.

### Disable Windows Data Execution Prevention for supported Office applications {#disable-windows-data-execution-prevention-for-supported-office-applications}

It is recommended that you disable the Windows Data Execution Prevention (DEP) setting when using Document Security Extension for Microsoft Office applications.

### Shared Microsoft Office files cannot be protected using Document Security Extension&nbsp; {#shared-microsoft-office-files-cannot-be-protected-using-document-security-extension-nbsp}

When you protect any shared Microsoft Office file using Document Security Extension, an error occurs and the shared file is not secured.

### Starting Office applications on a machine containing Document Security Extension for Microsoft Office and McAfee VirusScan {#starting-office-applications-on-a-machine-containing-document-security-extension-for-microsoft-office-and-mcafee-virusscan}

To ensure that Office applications start smoothly on a machine that has Document Security installed and McAfee VirusScan with On-Access Scan enabled, disable the Buffer Overflow Protection option in the McAfee VirusScan Console.

### Installing Document Security Extension for Microsoft Office on a machine with an unsupported Microsoft Office language {#installing-document-security-extension-for-microsoft-office-on-a-machine-with-an-unsupported-microsoft-office-language}

Before you install the Document Security Extension for Microsoft Office on a machine that has a Microsoft Office application with an unsupported language, open the Office application at least once.

### Synchronize Offline button is enabled even when a user does not have offline permissions {#synchronize-offline-button-is-enabled-even-when-a-user-does-not-have-offline-permissions}

The Synchronize Offline button is available even though the user does not have offline permissions for the document. However, selecting the button does nothing.

### No support for trial versions of Microsoft Office <br> {#no-support-for-trial-versions-of-microsoft-office-br}

Document Security extension for Microsoft Office does not support trail versions of Microsoft Office. Before installing the extension, ensure that you have installed a licensed copy of Microsoft Office and it is activated.

### Unable to open a protected Microsoft Office files &nbsp; {#unable-to-open-a-protected-microsoft-office-files-nbsp}

If the protected view of the Microsoft Office is enabled, the Right Management Extension cannot open protected Microsoft Excel files (XLS, XLSX) and protected Microsoft PowerPoint (PPT) files from a remote location.

### Cells of Microsoft Excel document containing an image or background color appear on top of watermark &nbsp; {#cells-of-microsoft-excel-document-containing-an-image-or-background-color-appear-on-top-of-watermark-nbsp}

If a cell of a Microsoft Excel document contains an image or is filled with background color and a dynamic watermark policy is applied to the document, then the image or the background color filled in the cell appears on top of the watermark and cover the watermark.

### Usability issue with multiple certificates <br> {#usability-issue-with-multiple-certificates-br}

If multiple certificates are present on the client machine and the user cancels the certificate selection dialog, then the dialog appears once again and the user has to cancel the dialog twice.

### Microsoft PowerPoint allows editing protected documents {#microsoft-powerpoint-allows-editing-protected-documents}

On attempting to edit a protected document, Microsoft PowerPoint displays a message, "You are not allowed to modify this document. You will not be able to save your changes.". After closing the message, users can continue to add text or edit the document. But, the changes made to the protected documents are not saved.

The above-mentioned behavior is as expected in Microsoft PowerPoint 2010, PowerPoint 2013, and PowerPoint 2016. 

>[!MORE_LIKE_THIS]
>
>* [Introduction to AEM Document Security Extension for Microsoft Office](document-security-extension-microsoft-office.md)
>* [Installing and Configuring AEM Document Security Extension for Microsoft Office](installing-configuring-aemdsext.md)
>* [Using AEM Document Security Extension for Microsoft Office](using-aem-document-security-extension.md)
>* [AEM Document Security 6.2 for Microsoft Office - Release Notes](document-security-extension-release-notes.md)
>* [AEM Document Security end-user Help](http://help.adobe.com/en_US/AEMForms/6.1/RMHelp/index.html)
>* [Troubleshooting AEM Document Security Extension for Microsoft Office](Troubleshooting-Document-Security-Extension.md)
