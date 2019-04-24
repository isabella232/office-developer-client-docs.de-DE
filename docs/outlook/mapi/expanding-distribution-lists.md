---
title: Erweitern von Verteilerlisten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5731a35b5d570669d8606be6dd6ca1a23fb87e88
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334986"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="75105-103">Erweitern von Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="75105-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="75105-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75105-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="75105-105">**So fordern Sie MAPI zum Erweitern einer Verteilerliste an**</span><span class="sxs-lookup"><span data-stu-id="75105-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="75105-106">Legen Sie die **PR_ADDRTYPE** ([pidtagaddresstype (](pidtagaddresstype-canonical-property.md))-Eigenschaft auf MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="75105-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="75105-107">MAPI erweitert die Adressen mit diesem Typ vor dem Senden der Nachricht an den Transportanbieter.</span><span class="sxs-lookup"><span data-stu-id="75105-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

