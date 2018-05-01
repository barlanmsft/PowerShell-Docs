---
ms.date:  03/27/2018
contributor:  JKeithB
ms.topic:  conceptual
keywords:  gallery,powershell,psgallery,GDPR
title:  PowerShell Gallery GDPR Compliance
---

# PowerShell Gallery GDPR Compliance

## Overview

In May 2018, a European privacy law, the General Data Protection Regulation (GDPR), will take effect.
The GDPR imposes new rules on companies, government agencies, non-profits,
and other organizations that offer goods and services to people in the European Union (EU),
or that collect and analyze data tied to EU residents. The GDPR applies no matter where you are located.

Read more about Microsoft Privacy policy at [Trust Center](https://www.microsoft.com/trustcenter).

The PowerShell Gallery stores the following information that may be provided by users, which may contain personal information:

* PowerShell Gallery account
* Items published to the PowerShell Gallery
* Email correspondence with the PowerShell Gallery team

Most users do not create a PowerShell Gallery account.
An account is not required unless you are going to publish an item
or use the "Contact Owner" feature in the PowerShell Gallery.
Other than email correspondence initiated by the user, the PowerShell Gallery does not store
personally identifiable data for users who have not created an account.

Users who create a PowerShell Gallery account can publish items to the PowerShell Gallery.
Those items are expected to be PowerShell code, but may contain other information including personal information.
The information below will show how you can get all the items you have published to the PowerShell Gallery.

## DSR Export of PowerShell Gallery Data

The following sections describe how the PowerShell Gallery supports data subject requests (DSR).
by explaining how to export information stored in the PowerShell Gallery, and how to request deletion of this information.

### Email

Email correspondence may include any of the following:

* Email sent to the owners of PowerShell Gallery items if the code analysis scans detected an issue with any item they have published to the PowerShell Gallery
* Email sent by anyone to the PowerShell Gallery team using the email address in the "Contact Us" page (cgadmin@microsoft.com)
* Registered users who use the "Contact Owner" feature in the PowerShell Gallery to send email to the owner of an item in the PowerShell Gallery

Emails sent by or to the PowerShell Gallery have a retention policy of 90 days to support
possible security investigations should malicious code be discovered on the PowerShell Gallery.
Emails are deleted by policy after 90 days.

You may request copies of all emails sent to or from your email address and the PowerShell Gallery within the previous 90 days.
To request this correspondence, send an email to cgadmin@microsoft.com, with the title: "DSR Request for emails relating to this account".
In the body of the message, state what information you are requesting (for example: Please send all emails sent to or received from this email address.)
All emails involving your email address within 90 days of the request will be sent within 7 business days.

### PowerShell Gallery Account Information

If you have created a PowerShell Gallery account, you can find all personal information that has been stored in PowerShell Gallery by taking the following steps:

1. Sign in to the PowerShell Gallery, then click on your username
2. The next page displayed is the Account page, which shows the email address used for the PowerShell Gallery account

If you have created more than one account in the PowerShell Gallery, you will need to repeat these steps for each account.

### Items in the PowerShell Gallery

To facilitate exporting items published to the PowerShell Gallery,
we have published the script "GetPSGalleryItemsForAuthor" to the PowerShell Gallery.
This script exports a copy of every version of every item put into the PowerShell Gallery based
on the author information stored in the item.

> [!NOTE]
> The Author is stored in the item manifest when you publish your item.
> There is no guarantee that the Author is the same identity as the account you use in the PowerShell Gallery.
> If you use some other value in the Author field, you will need to supply that value when using this script.

You may download the script by using the following PowerShell command:

```powershell
Save-Script GetPSGalleryItemsForAuthor -path <local folder location> -repository psgallery
```

You can then run the script directly, by running the following PowerShell commands:

```powershell
cd <local folder location >
.\GetPSGalleryItemsForAuthor.ps1
```

You will be prompted to supply the Author and a folder on your system where you want the items to be saved.

## Deleting Personal Data From The PowerShell Gallery

To delete your PowerShell Gallery account or any item you own in the PowerShell Gallery,
send email to cgadmin@microsoft.com with the title: "GDPR Request for items relating to this account".
In the body of the message state what information you want deleted. For example:

* Please delete version x.y.z of my item "item name"
* Please delete all versions of my item "item name"
* Please delete my PowerShell Gallery account

The PowerShell Gallery administrators will reply within 7 business days.
The items specified will be deleted within 30 days after the request is sent.