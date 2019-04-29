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
# <a name="screlocnotifications"></a><span data-ttu-id="d8951-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="d8951-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="d8951-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8951-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8951-105">Passt einen Zeiger in einem angegebenen Ereignis Benachrichtigungs Array an.</span><span class="sxs-lookup"><span data-stu-id="d8951-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d8951-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="d8951-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8951-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="d8951-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d8951-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="d8951-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8951-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8951-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8951-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="d8951-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8951-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="d8951-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="d8951-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="d8951-112">Parameters</span></span>

 <span data-ttu-id="d8951-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="d8951-113">_cntf_</span></span>
  
> <span data-ttu-id="d8951-114">in Die Anzahl [](notification.md) der Benachrichtigungs Strukturen im durch den _rgntf_ -Parameter angegebenen Array.</span><span class="sxs-lookup"><span data-stu-id="d8951-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d8951-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="d8951-115">_rgntf_</span></span>
  
> <span data-ttu-id="d8951-116">in Zeiger auf das Array von **Benachrichtigungs** Strukturen, die Ereignisbenachrichtigungen definieren, innerhalb derer ein Zeiger angepasst werden soll.</span><span class="sxs-lookup"><span data-stu-id="d8951-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="d8951-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="d8951-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="d8951-118">in Zeiger auf die ursprüngliche Basisadresse des vom _rgntf_ -Parameter angegebenen Arrays.</span><span class="sxs-lookup"><span data-stu-id="d8951-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d8951-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="d8951-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="d8951-120">in Der Speicherort, an den **ScRelocNotifications** die neue Basisadresse des durch den _rgntf_ -Parameter angegebenen Arrays schreibt.</span><span class="sxs-lookup"><span data-stu-id="d8951-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="d8951-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="d8951-121">_pcb_</span></span>
  
> <span data-ttu-id="d8951-122">Out Zeiger auf die Größe des vom _pvBaseNew_ -Parameter angegebenen Arrays in Byte.</span><span class="sxs-lookup"><span data-stu-id="d8951-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d8951-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d8951-123">Return value</span></span>

<span data-ttu-id="d8951-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d8951-124">S_OK</span></span>
  
> <span data-ttu-id="d8951-125">Ein Zeiger wurde erfolgreich angepasst.</span><span class="sxs-lookup"><span data-stu-id="d8951-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="d8951-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d8951-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="d8951-127">Es wurde eine ungültige Benachrichtigung gefunden.</span><span class="sxs-lookup"><span data-stu-id="d8951-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d8951-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d8951-128">Remarks</span></span>

<span data-ttu-id="d8951-129">Der _PCB_ -Parameter für die **ScRelocNotifications** -Funktion ist optional.</span><span class="sxs-lookup"><span data-stu-id="d8951-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d8951-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d8951-130">See also</span></span>



[<span data-ttu-id="d8951-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="d8951-131">ScRelocProps</span></span>](screlocprops.md)

