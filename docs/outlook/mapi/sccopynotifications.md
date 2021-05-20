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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 08b9b954f856d64214947d81cf700adee42bcce4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435922"
---
# <a name="sccopynotifications"></a><span data-ttu-id="22c30-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="22c30-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="22c30-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22c30-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22c30-105">Kopiert eine Gruppe von Ereignisbenachrichtigungen in einen einzelnen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="22c30-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22c30-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="22c30-106">Header file:</span></span>  <br/> |<span data-ttu-id="22c30-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="22c30-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="22c30-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="22c30-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="22c30-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="22c30-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="22c30-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="22c30-110">Called by:</span></span>  <br/> |<span data-ttu-id="22c30-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="22c30-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="22c30-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="22c30-112">Parameters</span></span>

 <span data-ttu-id="22c30-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="22c30-113">_cntf_</span></span>
  
> <span data-ttu-id="22c30-114">[in] Anzahl der [NOTIFICATION-Strukturen](notification.md) im Array, das durch den  _rgntf-Parameter angegeben_ wird.</span><span class="sxs-lookup"><span data-stu-id="22c30-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="22c30-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="22c30-115">_rgntf_</span></span>
  
> <span data-ttu-id="22c30-116">[in] Zeiger auf ein Array von **NOTIFICATION-Strukturen,** die die zu kopierenden Ereignisbenachrichtigungen definieren.</span><span class="sxs-lookup"><span data-stu-id="22c30-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="22c30-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="22c30-117">_pvDst_</span></span>
  
> <span data-ttu-id="22c30-118">[out] Zeiger auf die zurückgegebenen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="22c30-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="22c30-119">_leiterplatte_</span><span class="sxs-lookup"><span data-stu-id="22c30-119">_pcb_</span></span>
  
> <span data-ttu-id="22c30-120">[out] Optionaler Zeiger auf eine Variable, in der die Größe des Arrays in Bytes gespeichert wird, auf das der  _rgntf-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="22c30-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="22c30-121">Wenn nicht NULL, wird  _der Parameter "pcb"_ auf die Anzahl der Bytes festgelegt, die im  _pvDst-Parameter gespeichert_ sind.</span><span class="sxs-lookup"><span data-stu-id="22c30-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="22c30-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="22c30-122">Return value</span></span>

<span data-ttu-id="22c30-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="22c30-123">S_OK</span></span>
  
> <span data-ttu-id="22c30-124">Ereignisbenachrichtigungen wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="22c30-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="22c30-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="22c30-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="22c30-126">Es wurde eine ungültige Benachrichtigung gefunden.</span><span class="sxs-lookup"><span data-stu-id="22c30-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22c30-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="22c30-127">Remarks</span></span>

<span data-ttu-id="22c30-128">Wenn NULL im  _#A0 übergeben_ wird, wird kein Kopieren ausgeführt. Wenn ein Nicht-Null-Wert  _in_ einer Leiterplatte übergeben wird, kopiert die **ScCopyNotifications-Funktion** die Größe des Arrays und des Arrays selbst in einen einzelnen Speicherblock.</span><span class="sxs-lookup"><span data-stu-id="22c30-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="22c30-129">Wenn  _die Leiterplatte_ nicht NULL ist, wird sie auf die Anzahl der Bytes festgelegt, die im  _pvDst-Parameter gespeichert_ sind.</span><span class="sxs-lookup"><span data-stu-id="22c30-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="22c30-130">Der  _pvDst-Parameter_ muss groß genug sein, um das gesamte Array enthalten zu können.</span><span class="sxs-lookup"><span data-stu-id="22c30-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

