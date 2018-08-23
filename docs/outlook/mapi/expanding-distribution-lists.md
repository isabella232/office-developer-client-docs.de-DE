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
ms.openlocfilehash: c7c0043ed898a827b2ea8c65b20837c571f88883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582056"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="89bf6-103">Erweitern von Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="89bf6-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="89bf6-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89bf6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="89bf6-105">**Erweitern eine Verteilerliste MAPI aufgefordert.**</span><span class="sxs-lookup"><span data-stu-id="89bf6-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="89bf6-106">Legen Sie dessen **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft auf MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="89bf6-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="89bf6-107">MAPI wird vor dem Senden der Nachricht an der Adressbuchhierarchie Adressen mit diesem Typ erweitert.</span><span class="sxs-lookup"><span data-stu-id="89bf6-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

