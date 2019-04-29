---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Zuletzt geändert: 02 Juli, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409811"
---
# <a name="feid"></a><span data-ttu-id="93eb9-103">FEID</span><span class="sxs-lookup"><span data-stu-id="93eb9-103">FEID</span></span>

 
  
<span data-ttu-id="93eb9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="93eb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="93eb9-105">Bezeichner für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="93eb9-105">Identifier for a folder.</span></span> <span data-ttu-id="93eb9-106">Sie enthält eine Eintrags-ID und andere relevante Informationen.</span><span class="sxs-lookup"><span data-stu-id="93eb9-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="93eb9-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="93eb9-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="93eb9-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="93eb9-108">Members</span></span>

 <span data-ttu-id="93eb9-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="93eb9-109">_abFlags_</span></span>
  
> <span data-ttu-id="93eb9-110">4-Byte-Eintrags-ID für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="93eb9-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="93eb9-111">Weitere Informationen zu MAPI-Eintrags Bezeichnern **[](entryid.md)** finden Sie Untereintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="93eb9-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="93eb9-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="93eb9-112">_muid_</span></span>
  
> <span data-ttu-id="93eb9-113">GUID, die den Informationsspeicher Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="93eb9-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="93eb9-114">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="93eb9-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="93eb9-115">_Platzhalter_</span><span class="sxs-lookup"><span data-stu-id="93eb9-115">_placeholder_</span></span>
  
> <span data-ttu-id="93eb9-116">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93eb9-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="93eb9-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="93eb9-117">_ltid_</span></span>
  
> <span data-ttu-id="93eb9-118">Langfristige ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="93eb9-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="93eb9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93eb9-119">See also</span></span>



[<span data-ttu-id="93eb9-120">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="93eb9-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="93eb9-121">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="93eb9-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="93eb9-122">LTID</span><span class="sxs-lookup"><span data-stu-id="93eb9-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="93eb9-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="93eb9-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="93eb9-124">SYNCHRONISIERUNGS</span><span class="sxs-lookup"><span data-stu-id="93eb9-124">SYNC</span></span>](sync.md)

