---
title: Introduction to AEM Document Security Extension for Microsoft Office
seo-title: Introduction to AEM Document Security Extension for Microsoft Office
description: Using document Security Extension for Microsoft Office, you can apply predefined confidentiality settings to your Microsoft Office files. 
seo-description: Using document Security Extension for Microsoft Office, you can apply predefined confidentiality settings to your Microsoft Office files. 
uuid: a5428c50-fae3-4823-9e6f-0f5306e7248f
content-type: reference
topic-tags: using
geptopics: SG_AEMFORMS/categories/document_security
discoiquuid: cf93f9f5-1fb6-4909-815e-0ffb8c6ea6d1
index: y
internal: n
snippet: y
---

# Introduction to AEM Document Security Extension for Microsoft Office{#introduction-to-aem-document-security-extension-for-microsoft-office}

Adobe® Experience Manager Document Security Extension for Microsoft® Office ensures that only the people you authorize can use Word, Excel, and PowerPoint files that contain your intellectual property. By using Document Security Extension for Microsoft Office, you can apply predefined confidentiality settings to your files.

Document Security Extension for Microsoft Office extends LiveCycle Rights Management and Document Security add-on for Adobe Experience Manager Forms to protect Word, Excel, and PowerPoint files and to allow authorized users who have this software installed to use policy-protected files according to the confidentiality settings established in the policy.

## How Document Security protects intellectual property {#how-document-security-protects-intellectual-property}

Document Security ensures that only the people you authorize can use files that contain your intellectual property. Using Document Security, you can protect files by using confidentiality policies. A *policy* is a collection of information that includes confidentiality settings and a list of authorized users. The settings you specify in a policy determine how a recipient can use a file to which you apply the policy. For example, you can specify whether recipients can print or copy text or save changes.

Document Security administrators and users create policies. Administrators create organizational policies that are available to all authorized users. Administrators or policy set coordinators can also create groups of policies called *policy sets* that are available to a subset of users. Users can create their own policies, which only they can use. Administrators, policy set coordinators, and users create policies by using the Document Security web pages.

Although policies are stored on Document Security, you apply them to files through Word, Excel, or PowerPoint. When you apply a policy to a file, the information that the file contains is protected by the confidentiality settings that are specified in the policy. When you distribute the policy-protected file, only the recipients who are authorized by the policy can access the file’s contents.

Using a policy to protect a file gives you ongoing control over that file, even after you distribute it. You can audit events to track when and how recipients are using your file, make changes to the policy, prevent users from continuing to access the file, and change the policy that is attached to the file.

## How policies work {#how-policies-work}

Policies contain information about the authorized users and the confidentiality settings to apply to intellectual property. Users can be any user who is recognized by Document Security through inclusion in a linked LDAP or Active Directory list. Users can also be people who were invited to register with Document Security or for whom the administrator created an account.

The confidentiality settings in a policy determine how the recipients can use files that are protected by the policy. For example, policies specify whether recipients can print files, copy content to other files, or save changes to protected files. Policies can also specify different confidentiality settings for various users.

When you apply a policy to a file, the information that the file contains is protected by the confidentiality settings that are specified in the policy. When you distribute the file, Document Security authenticates the recipients who attempt to open the file and authorizes access according to the privileges specified in the policy.

After a policy is applied to a file, the confidentiality settings of the policy can be changed at any time, allowing you to add or remove authorized users or change the privileges for users after they received the file. The policy applied to the file can be changed, and access to the file can be revoked so that anyone with a copy of the file can no longer open it.

If the policy permits offline access, recipients can also use policy-protected files offline (without an active Internet or network connection) for the time period specified in the policy.

## How policy-protected files work {#how-policy-protected-files-work}

For a user to open and use policy-protected Word, Excel, and PowerPoint files, the policy must include the user as a recipient or allow anonymous access, and the user must have Document Security Extension for Microsoft Office installed. To give a policy-protected file to someone who does not have Document Security Extension for Microsoft Office, either give them a copy of the software or tell them how to download it from your website. If you do not have the installer, you can download it from the [download page](https://www.adobe.com/products/livecycle/rightsmanagement/extension/downloads.html).

When a user attempts to open a policy-protected file, Document Security Extension for Microsoft Office connects to Document Security to authenticate the user. If Document Security is configured to audit file usage, the user sees a notification indicating that the file usage is being audited. Document Security determines which file permissions to grant the user and the user can then use the file according to the policy settings, under these conditions:

* For the validity period that is specified in the policy. 
* Until an administrator or the person who applied the policy either revokes the access to the file or changes the policy.

  If the person who applied the policy changes the policy or revokes access to the file, the user’s permissions for the file are changed or removed even though the user already has the file. If the file itself was revoked, a URL may be provided to the user to get an updated copy.

  Policy-protected files can be opened offline (without an Internet or network connection), if the policy permits offline access, for the duration of the offline lease period that is specified in the policy. When the offline lease period ends, the user must go online and synchronize with Document Security, which starts a new lease period.

  If the policy allows the file to be saved and a user saves a copy of the policy-protected file, the policy is automatically applied and enforced for the saved file. Events, such as attempts to open the new file, are also audited and recorded the same as for the original file.

## Using Document Security to protect your files {#using-document-security-to-protect-your-files}

You can use policies to protect your files in various situations.

For example, a manufacturer is accepting bids from vendors who will provide parts for a new product. The manufacturer must provide the bidders with proprietary information that they need to finalize their submissions. The manufacturer uses Document Security to protect the files with a policy that allows the bidders to open the files and view the information. However, bidders are prevented from changing, printing, or copying the files and anyone who does not have permission is prevented from opening the files.

After accepting one of the bids, the manufacturer updates the policy to give the successful bidder permissions to print, copy, and save changes locally, and to remove the unsuccessful bidders so that they no longer have permission to open the files.

While working with the successful bidder, the manufacturer’s engineers change some of the design specifications in the files. To publish the new specifications, the manufacturer revokes access to some of the files and publishes new versions. When engineers for the successful bidder attempt to open the file, they see a message that access to the file was revoked. The message contains a URL where they can download a new version of the file.

## Additional Information {#additional-information}

The resources in this table can help you learn more about AEM Document Security: 

<table cellpadding="4" cellspacing="0"> 
 <tbody>
  <tr>
   <th class="cellrowborder" valign="top" width="NaN%"><p>For information about</p> </th> 
   <th class="cellrowborder" valign="top" width="NaN%"><p>See</p> </th> 
  </tr>
  <tr>
   <td class="cellrowborder" headers="d19e326 " valign="top" width="NaN%"><p>AEM forms Administrator Help</p> </td> 
   <td class="cellrowborder" headers="d19e329 " valign="top" width="NaN%"><p><a data-disable-query="false" href="http://www.adobe.com/go/learn_aemforms_admin_65">Administrator Help</a> or, on the Document Security administration pages, click the Help link in the upper-right corner of a page.</p> </td> 
  </tr>
  <tr>
   <td class="cellrowborder" headers="d19e326 " valign="top" width="NaN%"><p>Patch updates, technical notes, and additional information about this product version</p> </td> 
   <td class="cellrowborder" headers="d19e329 " valign="top" width="NaN%"><p><a href="https://helpx.adobe.com/marketing-cloud/contact-support.html">Marketing Cloud Technical Support</a></p> </td> 
  </tr>
 </tbody>
</table>

