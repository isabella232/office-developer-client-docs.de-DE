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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412387"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="b4b99-103">Zugreifen auf die Mitglieder einer Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="b4b99-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="b4b99-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b4b99-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="b4b99-105">**So erhalten Sie die Mitglieder einer Verteilerliste**</span><span class="sxs-lookup"><span data-stu-id="b4b99-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="b4b99-106">Erstellen Sie ein #A0 der Größe mit den Eigenschaften der Elemente, die Sie abrufen möchten, z. B. **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b4b99-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="b4b99-107">Rufen [Sie IAddrBook::OpenEntry auf,](iaddrbook-openentry.md) um die Verteilerliste zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="b4b99-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="b4b99-108">Rufen Sie die **IABContainer::GetContentsTable-Methode** der Verteilerliste auf, um auf die Inhaltstabelle zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b4b99-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="b4b99-109">Rufen [Sie HrQueryAllRows auf,](hrqueryallrows.md) um alle Zeilen der Tabelle abzurufen, die die Mitglieder der Verteilerliste darstellen.</span><span class="sxs-lookup"><span data-stu-id="b4b99-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

