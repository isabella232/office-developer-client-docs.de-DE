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
ms.openlocfilehash: 7d4877c81a52b529aa183ea552430b481c6617f1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593354"
---
# <a name="sccopynotifications"></a><span data-ttu-id="a66b8-103">ScCopyNotifications</span><span class="sxs-lookup"><span data-stu-id="a66b8-103">ScCopyNotifications</span></span>

  
  
<span data-ttu-id="a66b8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a66b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a66b8-105">Kopiert eine Gruppe von ereignisbenachrichtigungen in einen einzelnen Block Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a66b8-105">Copies a group of event notifications to a single block of memory.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a66b8-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="a66b8-106">Header file:</span></span>  <br/> |<span data-ttu-id="a66b8-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a66b8-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a66b8-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="a66b8-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a66b8-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a66b8-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a66b8-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="a66b8-110">Called by:</span></span>  <br/> |<span data-ttu-id="a66b8-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="a66b8-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="a66b8-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a66b8-112">Parameters</span></span>

 <span data-ttu-id="a66b8-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="a66b8-113">_cntf_</span></span>
  
> <span data-ttu-id="a66b8-114">[in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="a66b8-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="a66b8-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="a66b8-115">_rgntf_</span></span>
  
> <span data-ttu-id="a66b8-116">[in] Zeiger auf ein Array von **Benachrichtigung** Strukturen definieren die ereignisbenachrichtigungen kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="a66b8-116">[in] Pointer to an array of **NOTIFICATION** structures defining the event notifications to be copied.</span></span> 
    
 <span data-ttu-id="a66b8-117">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="a66b8-117">_pvDst_</span></span>
  
> <span data-ttu-id="a66b8-118">[out] Zeiger auf die zurückgegebenen Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="a66b8-118">[out] Pointer to the returned notifications.</span></span> 
    
 <span data-ttu-id="a66b8-119">_PCB_</span><span class="sxs-lookup"><span data-stu-id="a66b8-119">_pcb_</span></span>
  
> <span data-ttu-id="a66b8-120">[out] Optionaler Zeiger auf eine Variable, die die Größe in Bytes des Arrays mit der _Rgntf_ -Parameter, in dem gezeigt wird gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a66b8-120">[out] Optional pointer to a variable where the size, in bytes, of the array pointed to by the  _rgntf_ parameter is stored.</span></span> <span data-ttu-id="a66b8-121">Wenn nicht NULL-Wert der _pcb_ -Parameter wird festgelegt, um die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a66b8-121">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a66b8-122">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="a66b8-122">Return value</span></span>

<span data-ttu-id="a66b8-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="a66b8-123">S_OK</span></span>
  
> <span data-ttu-id="a66b8-124">Ereignisbenachrichtigungen wurden erfolgreich kopiert.</span><span class="sxs-lookup"><span data-stu-id="a66b8-124">Event notifications were copied successfully.</span></span>
    
<span data-ttu-id="a66b8-125">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="a66b8-125">E_INVALIDARG</span></span>
  
> <span data-ttu-id="a66b8-126">Eine ungültige Benachrichtigung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="a66b8-126">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a66b8-127">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="a66b8-127">Remarks</span></span>

<span data-ttu-id="a66b8-128">Wenn NULL in der _pcb_ -Parameter übergeben wird, wird keine kopieren ausgeführt. Wenn Sie ein nicht-Nullwert _pcb_übergeben wird, kopiert die **ScCopyNotifications** -Funktion die Größe des Arrays und das Array selbst in einen einzelnen Block Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="a66b8-128">If NULL is passed in the  _pcb_ parameter, no copying is performed; if a non-null value is passed in  _pcb_, the **ScCopyNotifications** function copies the size of the array and the array itself to a single block of memory.</span></span> <span data-ttu-id="a66b8-129">Wenn _pcb_ ungleich NULL ist, wird es auf die Anzahl von Bytes, die im Parameter _PvDst_ gespeichert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="a66b8-129">If  _pcb_ is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> <span data-ttu-id="a66b8-130">Der Parameter _PvDst_ muss groß genug für das gesamte Array sein.</span><span class="sxs-lookup"><span data-stu-id="a66b8-130">The  _pvDst_ parameter must be large enough to contain the entire array.</span></span> 
  

