---
title: ScCopyNotifications
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyNotifications
api_type:
- COM
ms.assetid: ac31cf65-a2bc-4c8e-91a4-d2903aa98776
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 28a802ffc43b08d3e2ec2be26dd98fa78f474d91
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795434"
---
# <a name="sccopynotifications"></a><span data-ttu-id="c543b-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="c543b-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="c543b-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c543b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c543b-105">Kopiert eine Gruppe von ereignisbenachrichtigungen in einen einzelnen Block Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c543b-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c543b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c543b-106">Header file:</span></span>  <br/> |<span data-ttu-id="c543b-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c543b-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c543b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c543b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c543b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c543b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c543b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c543b-110">Called by:</span></span>  <br/> |<span data-ttu-id="c543b-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c543b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="c543b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c543b-112">Parameters</span></span>

 <span data-ttu-id="c543b-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="c543b-113">_cntf_</span></span>
  
> <span data-ttu-id="c543b-114">[in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="c543b-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="c543b-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="c543b-115">_rgntf_</span></span>
  
> <span data-ttu-id="c543b-116">[in] Zeiger auf ein Array von **Benachrichtigung** Strukturen definieren die ereignisbenachrichtigungen kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c543b-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="c543b-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="c543b-117">_pvDst_</span></span>
  
> <span data-ttu-id="c543b-118">[out] Zeiger auf die zurückgegebenen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="c543b-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="c543b-119">_PCB_</span><span class="sxs-lookup"><span data-stu-id="c543b-119">_pcb_</span></span>
  
> <span data-ttu-id="c543b-120">[out] Optionaler Zeiger auf eine Variable, die die Größe in Bytes des Arrays mit der _Rgntf_ -Parameter, in dem gezeigt wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c543b-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="c543b-121">Wenn nicht NULL-Wert der _pcb_ -Parameter wird festgelegt, um die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c543b-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c543b-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c543b-122">Return value</span></span>

<span data-ttu-id="c543b-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="c543b-123">S_OK</span></span>
  
> <span data-ttu-id="c543b-124">Ereignisbenachrichtigungen wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="c543b-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="c543b-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="c543b-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="c543b-126">Eine ungültige Benachrichtigung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c543b-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c543b-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c543b-127">Remarks</span></span>

<span data-ttu-id="c543b-128">Wenn NULL in der _pcb_ -Parameter übergeben wird, wird keine kopieren ausgeführt. Wenn Sie ein nicht-Nullwert _pcb_übergeben wird, kopiert die **ScCopyNotifications** -Funktion die Größe des Arrays und das Array selbst in einen einzelnen Block Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="c543b-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="c543b-129">Wenn _pcb_ ungleich NULL ist, wird es auf die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="c543b-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="c543b-130">Der Parameter _PvDst_ muss groß genug für das gesamte Array sein.</span><span class="sxs-lookup"><span data-stu-id="c543b-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

