---
title: ScRelocNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocNotifications
api_type:
- COM
ms.assetid: 22de5d38-7be6-48b3-90a7-bc553dcdb042
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 81da4b77f0d2162a1119b7945b1e0ceb87ba9fb8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415201"
---
# <a name="screlocnotifications"></a><span data-ttu-id="236d2-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="236d2-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="236d2-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="236d2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="236d2-105">Passt einen Zeiger innerhalb eines angegebenen Ereignisbenachrichtigungsarrays an.</span><span class="sxs-lookup"><span data-stu-id="236d2-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="236d2-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="236d2-106">Header file:</span></span>  <br/> |<span data-ttu-id="236d2-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="236d2-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="236d2-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="236d2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="236d2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="236d2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="236d2-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="236d2-110">Called by:</span></span>  <br/> |<span data-ttu-id="236d2-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="236d2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="236d2-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="236d2-112">Parameters</span></span>

 <span data-ttu-id="236d2-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="236d2-113">_cntf_</span></span>
  
> <span data-ttu-id="236d2-114">[in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, das durch den  _rgntf-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="236d2-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="236d2-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="236d2-115">_rgntf_</span></span>
  
> <span data-ttu-id="236d2-116">[in] Zeiger auf das Array von **NOTIFICATION-Strukturen,** in dem Ereignisbenachrichtigungen definiert werden, innerhalb derer ein Zeiger angepasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="236d2-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="236d2-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="236d2-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="236d2-118">[in] Zeiger auf die ursprüngliche Basisadresse des Arrays, die durch den  _rgntf-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="236d2-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="236d2-119">_pvBaseNeu_</span><span class="sxs-lookup"><span data-stu-id="236d2-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="236d2-120">[in] Der Speicherort, an den **ScRelocNotifications** die neue Basisadresse des arrays schreibt, das durch den  _rgntf-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="236d2-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="236d2-121">_leiterplatte_</span><span class="sxs-lookup"><span data-stu-id="236d2-121">_pcb_</span></span>
  
> <span data-ttu-id="236d2-122">[out] Zeiger auf die Größe des durch den  _parameter pvBaseNew_ angegebenen Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="236d2-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="236d2-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="236d2-123">Return value</span></span>

<span data-ttu-id="236d2-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="236d2-124">S_OK</span></span>
  
> <span data-ttu-id="236d2-125">Ein Zeiger wurde erfolgreich angepasst.</span><span class="sxs-lookup"><span data-stu-id="236d2-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="236d2-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="236d2-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="236d2-127">Es wurde eine ungültige Benachrichtigung gefunden.</span><span class="sxs-lookup"><span data-stu-id="236d2-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="236d2-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="236d2-128">Remarks</span></span>

<span data-ttu-id="236d2-129">Der  _Parameter "pcb"_ für die **ScRelocNotifications-Funktion** ist optional.</span><span class="sxs-lookup"><span data-stu-id="236d2-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="236d2-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="236d2-130">See also</span></span>



[<span data-ttu-id="236d2-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="236d2-131">ScRelocProps</span></span>](screlocprops.md)

