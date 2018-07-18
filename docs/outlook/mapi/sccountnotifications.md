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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c27472a309c26882051744a23fbe05e41c36aa3f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795460"
---
# <a name="sccountnotifications"></a><span data-ttu-id="2207e-103">ScCountNotifications</span><span class="sxs-lookup"><span data-stu-id="2207e-103">ScCountNotifications</span></span>

  
  
<span data-ttu-id="2207e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2207e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2207e-105">Bestimmt die Größe in Bytes, der ein Array von ereignisbenachrichtigungen, und das Array zugeordneten Arbeitsspeicher überprüft.</span><span class="sxs-lookup"><span data-stu-id="2207e-105">Determines the size, in bytes, of an array of event notifications, and validates the memory associated with the array.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="2207e-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="2207e-106">Header file:</span></span>  <br/> |<span data-ttu-id="2207e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="2207e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="2207e-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="2207e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="2207e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="2207e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="2207e-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="2207e-110">Called by:</span></span>  <br/> |<span data-ttu-id="2207e-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="2207e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCountNotifications(
  int cntf,
  LPNOTIFICATION rgntf,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="2207e-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="2207e-112">Parameters</span></span>

 <span data-ttu-id="2207e-113">_cntf_</span><span class="sxs-lookup"><span data-stu-id="2207e-113">_cntf_</span></span>
  
> <span data-ttu-id="2207e-114">[in] Anzahl der [Benachrichtigung](notification.md) Strukturen in das Array, das durch den Parameter _Rgntf_ angegeben.</span><span class="sxs-lookup"><span data-stu-id="2207e-114">[in] Count of [NOTIFICATION](notification.md) structures in the array indicated by the  _rgntf_ parameter.</span></span> 
    
 <span data-ttu-id="2207e-115">_rgntf_</span><span class="sxs-lookup"><span data-stu-id="2207e-115">_rgntf_</span></span>
  
> <span data-ttu-id="2207e-116">[in] Zeiger auf das Array von **Benachrichtigung** Strukturen, deren Größe ist bestimmt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2207e-116">[in] Pointer to the array of **NOTIFICATION** structures whose size is to be determined.</span></span> 
    
 <span data-ttu-id="2207e-117">_PCB_</span><span class="sxs-lookup"><span data-stu-id="2207e-117">_pcb_</span></span>
  
> <span data-ttu-id="2207e-118">[out] Optional Zeiger auf die Größe des Arrays auf das durch den Parameter _Rgntf_ in Bytes.</span><span class="sxs-lookup"><span data-stu-id="2207e-118">[out] Optional pointer to the size, in bytes, of the array pointed to by the  _rgntf_ parameter.</span></span> <span data-ttu-id="2207e-119">Wenn NULL, überprüft **ScCountNotifications** das Array von Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="2207e-119">If NULL, **ScCountNotifications** validates the array of notifications.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="2207e-120">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="2207e-120">Return value</span></span>

<span data-ttu-id="2207e-121">S_OK</span><span class="sxs-lookup"><span data-stu-id="2207e-121">S_OK</span></span>
  
> <span data-ttu-id="2207e-122">Count wurde erfolgreich bestimmt.</span><span class="sxs-lookup"><span data-stu-id="2207e-122">Count was determined successfully.</span></span>
    
<span data-ttu-id="2207e-123">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2207e-123">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="2207e-124">Eine ungültige Benachrichtigung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="2207e-124">An invalid notification was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2207e-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2207e-125">Remarks</span></span>

<span data-ttu-id="2207e-126">Wenn NULL in der _pcb_ -Parameter übergeben wird, überprüft die Funktion **ScCountNotifications** nur das Array von Benachrichtigungen, aber keine Zählung abgeschlossen ist. Wenn ein Wert ungleich Null in _pcb_übergeben wird, bestimmt die Größe des Arrays und speichert die Ursache **ScCountNotifications** _pcb_.</span><span class="sxs-lookup"><span data-stu-id="2207e-126">If NULL is passed in the  _pcb_ parameter, the **ScCountNotifications** function only validates the array of notifications but no counting is done; if a non-null value is passed in  _pcb_, **ScCountNotifications** determines the size of the array and stores the cause  _pcb_.</span></span> <span data-ttu-id="2207e-127">Der Parameter _pcb_ muss groß genug für das gesamte Array sein.</span><span class="sxs-lookup"><span data-stu-id="2207e-127">The  _pcb_ parameter must be large enough to contain the entire array.</span></span> 
  

