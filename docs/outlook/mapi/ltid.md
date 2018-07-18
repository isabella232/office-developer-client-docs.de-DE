---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792909"
---
# <a name="ltid"></a><span data-ttu-id="cb48b-103">LTID</span><span class="sxs-lookup"><span data-stu-id="cb48b-103">LTID</span></span>

  
  
<span data-ttu-id="cb48b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cb48b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cb48b-105">Generische lange Ausdrucks-ID eines Objekts in einem Outlook-Speicher.</span><span class="sxs-lookup"><span data-stu-id="cb48b-105">Generic Long Term ID of an object in an Outlook store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb48b-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cb48b-106">Quick info</span></span>

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a><span data-ttu-id="cb48b-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="cb48b-107">Members</span></span>

 <span data-ttu-id="cb48b-108">_guid_</span><span class="sxs-lookup"><span data-stu-id="cb48b-108">_guid_</span></span>
  
- <span data-ttu-id="cb48b-109">[out] Die GUID des Servers, der das Objekt erstellt.</span><span class="sxs-lookup"><span data-stu-id="cb48b-109">[out] The GUID of the server that created the object.</span></span>
    
 <span data-ttu-id="cb48b-110">_globcnt_</span><span class="sxs-lookup"><span data-stu-id="cb48b-110">_globcnt_</span></span>
  
- <span data-ttu-id="cb48b-111">[out] Eine 6-Byte eindeutige Zahl, die das Objekt in der Outlook-Speicher angibt.</span><span class="sxs-lookup"><span data-stu-id="cb48b-111">[out] A 6-byte unique number that identifies the object within the Outlook store.</span></span>
    
 <span data-ttu-id="cb48b-112">_wLevel_</span><span class="sxs-lookup"><span data-stu-id="cb48b-112">_wLevel_</span></span>
  
- <span data-ttu-id="cb48b-113">[out] Die Ebene der die Eintrags-ID für einen bevorzugten öffentlichen Exchange-Ordner.</span><span class="sxs-lookup"><span data-stu-id="cb48b-113">[out] The hierarchy level of the entry ID for an Exchange Favorite Public folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="cb48b-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb48b-114">See also</span></span>



[<span data-ttu-id="cb48b-115">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="cb48b-115">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="cb48b-116">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="cb48b-116">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="cb48b-117">FEID</span><span class="sxs-lookup"><span data-stu-id="cb48b-117">FEID</span></span>](feid.md)

