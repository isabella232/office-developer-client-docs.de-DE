---
title: Zugreifen auf die Mitglieder von Verteilerlisten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f724cac8-2d5d-42bc-a15e-99f77a99ce21
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 21975482c458998cbe158a84d535f911156ac392
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791258"
---
# <a name="accessing-the-members-of-a-distribution-list"></a><span data-ttu-id="573ec-103">Zugreifen auf die Mitglieder von Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="573ec-103">Accessing the Members of a Distribution List</span></span>

  
  
<span data-ttu-id="573ec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="573ec-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="573ec-105">**Zum Abrufen der Mitglieder einer Verteilerliste**</span><span class="sxs-lookup"><span data-stu-id="573ec-105">**To get the members of a distribution list**</span></span>
  
1. <span data-ttu-id="573ec-106">Erstellen Sie ein Größe Eigenschaft Tag-Array mit den Eigenschaften der Elemente aus, wie **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_DISPLAY_TYPE** ([ abgerufen werden sollen. PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="573ec-106">Create a sized property tag array with the properties of the members you would like to retrieve, such as **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), and **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).</span></span>
    
2. <span data-ttu-id="573ec-107">Rufen Sie [IAddrBook::OpenEntry](iaddrbook-openentry.md) , um die Verteilerliste zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="573ec-107">Call [IAddrBook::OpenEntry](iaddrbook-openentry.md) to open the distribution list.</span></span> 
    
3. <span data-ttu-id="573ec-108">Rufen Sie die Verteilerliste **IABContainer::GetContentsTable** -Methode zum Zugriff auf die Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="573ec-108">Call the distribution list's **IABContainer::GetContentsTable** method to access its contents table.</span></span> 
    
4. <span data-ttu-id="573ec-109">Rufen Sie [HrQueryAllRows](hrqueryallrows.md) zum Abrufen aller Zeilen der Tabelle, die Mitglieder der Verteilerliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="573ec-109">Call [HrQueryAllRows](hrqueryallrows.md) to retrieve all of the table's rows representing the members of the distribution list.</span></span> 
    

