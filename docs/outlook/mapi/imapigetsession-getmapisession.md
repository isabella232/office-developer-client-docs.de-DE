---
title: IMAPIGetSessionGetMAPISession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession.GetMAPISession
api_type:
- COM
ms.assetid: 581db5d9-35f7-43ad-aef3-a5d5da310150
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: dbf9f9f73d9e3860b482f81fb942673e6d373267
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321553"
---
# <a name="imapigetsessiongetmapisession"></a><span data-ttu-id="ef5db-103">IMAPIGetSession::GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="ef5db-103">IMAPIGetSession::GetMAPISession</span></span>

  
  
<span data-ttu-id="ef5db-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ef5db-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ef5db-105">Gibt einen Verweis auf die MAPI-Sitzung zurück, die dem MAPI-Unterstützungsobjekt zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="ef5db-105">Returns a pointer to the MAPI session associated with the MAPI support object.</span></span>
  
```cpp
HRESULT GetMAPISession(
  LPUNKNOWN *  lppSession
);
```

## <a name="parameters"></a><span data-ttu-id="ef5db-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef5db-106">Parameters</span></span>

 <span data-ttu-id="ef5db-107">_lppSession_</span><span class="sxs-lookup"><span data-stu-id="ef5db-107">_lppSession_</span></span>
  
> <span data-ttu-id="ef5db-108">Out Ein Zeiger auf die aktuelle MAPI-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="ef5db-108">[out] A pointer to the current MAPI session.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ef5db-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef5db-109">See also</span></span>



[<span data-ttu-id="ef5db-110">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef5db-110">IMAPIGetSession : IUnknown</span></span>](imapigetsessioniunknown.md)


[<span data-ttu-id="ef5db-111">Übersicht über das Support Objekt</span><span class="sxs-lookup"><span data-stu-id="ef5db-111">Support Object Overview</span></span>](support-object-overview.md)

