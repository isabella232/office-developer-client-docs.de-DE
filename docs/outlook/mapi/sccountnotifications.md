---
title: ScCountNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCountNotifications
api_type:
- COM
ms.assetid: 13e80bdc-cb59-47a5-8de0-404e22f87f82
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f5298620239d1e42e4ba613c22a98f0cf6f7d457
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437994"
---
# <a name="sccountnotifications"></a><span data-ttu-id="61c97-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="61c97-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="61c97-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61c97-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61c97-105">Bestimmt die Größe eines Arrays von Ereignisbenachrichtigungen in Byte und überprüft den dem Array zugeordneten Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="61c97-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="61c97-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="61c97-106">Header file:</span></span>  <br/> |<span data-ttu-id="61c97-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="61c97-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="61c97-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="61c97-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="61c97-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="61c97-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="61c97-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="61c97-110">Called by:</span></span>  <br/> |<span data-ttu-id="61c97-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="61c97-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="61c97-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="61c97-112">Parameters</span></span>

 <span data-ttu-id="61c97-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="61c97-113">_cntf_</span></span>
  
> <span data-ttu-id="61c97-114">in Die Anzahl [](notification.md) der Benachrichtigungs Strukturen im durch den _rgntf_ -Parameter angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="61c97-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="61c97-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="61c97-115">_rgntf_</span></span>
  
> <span data-ttu-id="61c97-116">in Zeiger auf das Array der **Benachrichtigungs** Strukturen, dessen Größe bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="61c97-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="61c97-117">_PCB_</span><span class="sxs-lookup"><span data-stu-id="61c97-117">_pcb_</span></span>
  
> <span data-ttu-id="61c97-118">Out Optionaler Zeiger auf die Größe des Arrays, auf das durch den _rgntf_ -Parameter verwiesen wird, in Bytes.</span><span class="sxs-lookup"><span data-stu-id="61c97-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="61c97-119">Wenn der Wert NULL ist, überprüft **ScCountNotifications** das Array der Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="61c97-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="61c97-120">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61c97-120">Return value</span></span>

<span data-ttu-id="61c97-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="61c97-121">S_OK</span></span>
  
> <span data-ttu-id="61c97-122">Count wurde erfolgreich ermittelt.</span><span class="sxs-lookup"><span data-stu-id="61c97-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="61c97-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="61c97-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="61c97-124">Es wurde eine ungültige Benachrichtigung gefunden.</span><span class="sxs-lookup"><span data-stu-id="61c97-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="61c97-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61c97-125">Remarks</span></span>

<span data-ttu-id="61c97-126">Wenn NULL im _PCB_ -Parameter übergeben wird, überprüft die **ScCountNotifications** -Funktion nur das Array der Benachrichtigungen, aber es wird keine Zählung durchgeführt; Wenn ein Wert ungleich NULL in _PCB_übergeben wird, bestimmt **ScCountNotifications** die Größe des Arrays und speichert die Ursache _PCB_.</span><span class="sxs-lookup"><span data-stu-id="61c97-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="61c97-127">Der _PCB_ -Parameter muss so hoch sein, dass er das gesamte Array enthält.</span><span class="sxs-lookup"><span data-stu-id="61c97-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

