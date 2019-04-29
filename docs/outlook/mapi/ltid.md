---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2ea877c9328279322de0f15e5755096e74819425
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419436"
---
# <a name="ltid"></a><span data-ttu-id="cf5cb-103">LTID</span><span class="sxs-lookup"><span data-stu-id="cf5cb-103">LTID</span></span>

  
  
<span data-ttu-id="cf5cb-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf5cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf5cb-105">Generische Langzeit-ID eines Objekts in einem Outlook-Speicher.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cf5cb-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cf5cb-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="cf5cb-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="cf5cb-107">Members</span></span>

 <span data-ttu-id="cf5cb-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="cf5cb-108">_guid_</span></span>
  
- <span data-ttu-id="cf5cb-109">Out Die GUID des Servers, der das Objekt erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="cf5cb-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="cf5cb-110">_globcnt_</span></span>
  
- <span data-ttu-id="cf5cb-111">Out Eine eindeutige 6-Byte-Zahl, die das Objekt innerhalb des Outlook-Speichers identifiziert.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="cf5cb-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="cf5cb-112">_wLevel_</span></span>
  
- <span data-ttu-id="cf5cb-113">Out Die Hierarchieebene der Eintrags-ID für einen öffentlichen Exchange-Ordner.</span><span class="sxs-lookup"><span data-stu-id="cf5cb-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cf5cb-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf5cb-114">See also</span></span>



[<span data-ttu-id="cf5cb-115">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="cf5cb-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="cf5cb-116">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="cf5cb-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="cf5cb-117">FEID</span><span class="sxs-lookup"><span data-stu-id="cf5cb-117">FEID</span></span>](feid.md)

