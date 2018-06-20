---
title: SYNCCONT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7b4307a3-5a8c-89bf-1113-2549556a7fe7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 82923895353cf600c4d0b78b9a6e16fc7d57e466
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795681"
---
# <a name="synccont"></a><span data-ttu-id="3db76-103">SYNCCONT</span><span class="sxs-lookup"><span data-stu-id="3db76-103">SYNCCONT</span></span>

<span data-ttu-id="3db76-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3db76-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3db76-105">Informationen für den Inhalt der angegebenen Ordner in einem lokalen Speicher mit dem Server synchronisieren, während der [Inhalt Zustand synchronisieren](synchronize-contents-state.md).</span><span class="sxs-lookup"><span data-stu-id="3db76-105">Information for synchronizing the contents of specified folders in a local store with the server during the [synchronize contents state](synchronize-contents-state.md).</span></span> <span data-ttu-id="3db76-106">Dieser Schritt umfasst das soeben hochladen oder eine vollständige Synchronisierung im Zusammenhang mit Upload und klicken Sie dann auf Download.</span><span class="sxs-lookup"><span data-stu-id="3db76-106">This involves just uploading, or a full synchronization involving an upload and then a download.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="3db76-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="3db76-107">Quick info</span></span>

```cpp
struct SYNCCONT 
{ 
   ULONG   ulFlags; 
   UINT   iEnt; 
   UINT   cEnt; 
   LPVOID    pvReserved; 
   LPSPropTagArray   ptagaReserved; 
   LPSSortOrderSet   psosReserved; 
};
```

## <a name="members"></a><span data-ttu-id="3db76-108">Members</span><span class="sxs-lookup"><span data-stu-id="3db76-108">Members</span></span>

<span data-ttu-id="3db76-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3db76-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3db76-110">[in] Kennzeichen, die um das entsprechende Verhalten während der Synchronisierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="3db76-110">[in] Flags to determine the appropriate behavior during synchronization.</span></span>
    
  - <span data-ttu-id="3db76-111">UPC_OK</span><span class="sxs-lookup"><span data-stu-id="3db76-111">UPC_OK</span></span>
    
  - <span data-ttu-id="3db76-112">[in] Hochladen oder vollständige Synchronisierung war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="3db76-112">[in] Upload or full synchronization was successful.</span></span> <span data-ttu-id="3db76-113">Der Client legt dies nach Informationen mit dem Server synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3db76-113">The client sets this after synchronizing information with the server.</span></span>
    
<span data-ttu-id="3db76-114">_iEnt_</span><span class="sxs-lookup"><span data-stu-id="3db76-114">_iEnt_</span></span>
  
> <span data-ttu-id="3db76-115">[out] Index zum Nachverfolgen der Inhalt in die Anzahl von _cEnt_angegebenen Ordner zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="3db76-115">[out] Index to track synchronizing the contents in the number of folders specified by  _cEnt_.</span></span>
    
<span data-ttu-id="3db76-116">_cEnt_</span><span class="sxs-lookup"><span data-stu-id="3db76-116">_cEnt_</span></span>
  
> <span data-ttu-id="3db76-117">[out] Anzahl der Ordner repliziert werden.</span><span class="sxs-lookup"><span data-stu-id="3db76-117">[out] Number of folders to be replicated.</span></span>
    
<span data-ttu-id="3db76-118">_pvReserved_</span><span class="sxs-lookup"><span data-stu-id="3db76-118">_pvReserved_</span></span>
  
> <span data-ttu-id="3db76-119">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3db76-119">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3db76-120">_ptagaReserved_</span><span class="sxs-lookup"><span data-stu-id="3db76-120">_ptagaReserved_</span></span>
  
> <span data-ttu-id="3db76-121">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3db76-121">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
<span data-ttu-id="3db76-122">_psosReserved_</span><span class="sxs-lookup"><span data-stu-id="3db76-122">_psosReserved_</span></span>
  
> <span data-ttu-id="3db76-123">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3db76-123">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="3db76-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3db76-124">See also</span></span>

- [<span data-ttu-id="3db76-125">Über die API-Replikation</span><span class="sxs-lookup"><span data-stu-id="3db76-125">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="3db76-126">Informationen zu den Replikationsstatus Computer</span><span class="sxs-lookup"><span data-stu-id="3db76-126">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="3db76-127">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3db76-127">MAPI Constants</span></span>](mapi-constants.md)

