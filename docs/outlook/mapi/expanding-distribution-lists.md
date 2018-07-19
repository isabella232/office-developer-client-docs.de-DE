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
ms.openlocfilehash: 47a37683ac54bef72ebd50aaaa11a36bdfd28659
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791648"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="a8000-103">Erweitern von Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="a8000-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="a8000-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a8000-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="a8000-105">**Erweitern eine Verteilerliste MAPI aufgefordert.**</span><span class="sxs-lookup"><span data-stu-id="a8000-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="a8000-106">Legen Sie dessen **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))-Eigenschaft auf MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="a8000-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="a8000-107">MAPI wird vor dem Senden der Nachricht an der Adressbuchhierarchie Adressen mit diesem Typ erweitert.</span><span class="sxs-lookup"><span data-stu-id="a8000-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

