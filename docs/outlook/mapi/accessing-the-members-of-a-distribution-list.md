---
title: Zugreifen auf die Mitglieder einer Verteilerliste
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2944a53d27bc916ccafcfa649d79e3c00afaf622
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331241"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="6af8d-103">Zugreifen auf die Mitglieder einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="6af8d-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="6af8d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6af8d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="6af8d-105">**So rufen Sie die Mitglieder einer Verteilerliste ab**</span><span class="sxs-lookup"><span data-stu-id="6af8d-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="6af8d-106">Erstellen Sie ein Array mit den Eigenschaften der Elemente, die Sie abrufen möchten, wie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([ PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="6af8d-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="6af8d-107">Rufen Sie [IAddrBook:: OpenEntry](iaddrbook-openentry.md) auf, um die Verteilerliste zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="6af8d-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="6af8d-108">Rufen Sie die **IABContainer::** getcontentable-Methode der Verteilerliste auf, um auf Ihre Inhaltstabelle zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="6af8d-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="6af8d-109">Rufen Sie [HrQueryAllRows](hrqueryallrows.md) auf, um alle Tabellenzeilen abzurufen, die die Mitglieder der Verteilerliste darstellen.</span><span class="sxs-lookup"><span data-stu-id="6af8d-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

