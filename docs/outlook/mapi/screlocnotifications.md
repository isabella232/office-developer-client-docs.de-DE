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
ms.openlocfilehash: 4117558d27d64444cdac62651584fe6cfe8ff061
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583967"
---
# <a name="screlocnotifications"></a><span data-ttu-id="18aaf-103">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="18aaf-103">ScRelocNotifications</span></span>

  
  
<span data-ttu-id="18aaf-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18aaf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18aaf-105">Einen Zeiger in ein bestimmtes Ereignis Benachrichtigung Array passt.</span><span class="sxs-lookup"><span data-stu-id="18aaf-105">Adjusts a pointer within a specified event notification array.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18aaf-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="18aaf-106">Header file:</span></span>  <br/> |<span data-ttu-id="18aaf-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="18aaf-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="18aaf-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="18aaf-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="18aaf-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="18aaf-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="18aaf-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="18aaf-110">Called by:</span></span>  <br/> |<span data-ttu-id="18aaf-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="18aaf-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="18aaf-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="18aaf-112">Parameters</span></span>

 <span data-ttu-id="18aaf-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="18aaf-113">_cntf_</span></span>
  
> <span data-ttu-id="18aaf-114">[in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="18aaf-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="18aaf-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="18aaf-115">_rgntf_</span></span>
  
> <span data-ttu-id="18aaf-116">[in] Zeiger auf das Array von **Benachrichtigung** Strukturen definieren von ereignisbenachrichtigungen in denen ein Zeiger ist angepasst werden.</span><span class="sxs-lookup"><span data-stu-id="18aaf-116">[in] Pointer to the array of **NOTIFICATION** structures defining event notifications within which a pointer is to be adjusted.</span></span> 
    
 <span data-ttu-id="18aaf-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="18aaf-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="18aaf-118">[in] Zeiger auf die ursprüngliche Basisadresse des Arrays durch den Parameter _Rgntf_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="18aaf-118">[in] Pointer to the original base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="18aaf-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="18aaf-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="18aaf-120">[in] Der Speicherort, auf das die neue Basisadresse des durch den Parameter _Rgntf_ angegebenen Arrays von **ScRelocNotifications** schreibt.</span><span class="sxs-lookup"><span data-stu-id="18aaf-120">[in] The location to which **ScRelocNotifications** writes the new base address of the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="18aaf-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="18aaf-121">_pcb_</span></span>
  
> <span data-ttu-id="18aaf-122">[out] Zeiger auf die Größe des durch den Parameter _PvBaseNew_ angegebenen Arrays in Bytes.</span><span class="sxs-lookup"><span data-stu-id="18aaf-122">[out] Pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18aaf-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="18aaf-123">Return value</span></span>

<span data-ttu-id="18aaf-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="18aaf-124">S_OK</span></span>
  
> <span data-ttu-id="18aaf-125">Ein Zeiger wurde erfolgreich korrigiert.</span><span class="sxs-lookup"><span data-stu-id="18aaf-125">A pointer was adjusted successfully.</span></span>
    
<span data-ttu-id="18aaf-126">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="18aaf-126">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="18aaf-127">Eine ungültige Benachrichtigung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="18aaf-127">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18aaf-128">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="18aaf-128">Remarks</span></span>

<span data-ttu-id="18aaf-129">Der Parameter _pcb_ an die Funktion **ScRelocNotifications** ist optional.</span><span class="sxs-lookup"><span data-stu-id="18aaf-129">The  _pcb_ parameter to the **ScRelocNotifications** function is optional.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="18aaf-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="18aaf-130">See also</span></span>



[<span data-ttu-id="18aaf-131">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="18aaf-131">ScRelocProps</span></span>](screlocprops.md)

