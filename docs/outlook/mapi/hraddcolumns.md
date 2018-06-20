---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: dc7fa8b546783819b701604a5e489f0fd030ae86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791890"
---
# <a name="hraddcolumns"></a><span data-ttu-id="ad614-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="ad614-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="ad614-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad614-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad614-105">Fügt oder Spalten an den Anfang einer vorhandenen Tabelle verschoben.</span><span class="sxs-lookup"><span data-stu-id="ad614-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ad614-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="ad614-106">Header file:</span></span>  <br/> |<span data-ttu-id="ad614-107">mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="ad614-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="ad614-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="ad614-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ad614-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ad614-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ad614-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="ad614-110">Called by:</span></span>  <br/> |<span data-ttu-id="ad614-111">Clientanwendungen und -Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="ad614-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="ad614-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad614-112">Parameters</span></span>

 <span data-ttu-id="ad614-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="ad614-113">_lptbl_</span></span>
  
> <span data-ttu-id="ad614-114">[in] Zeiger auf die MAPI-Tabelle betroffen.</span><span class="sxs-lookup"><span data-stu-id="ad614-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="ad614-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="ad614-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="ad614-116">[in] Zeiger auf eine **SPropTagArray** -Struktur, die enthält ein Array von Eigenschaftentags für die Eigenschaften hinzugefügt oder an den Anfang der Tabelle verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="ad614-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="ad614-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="ad614-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="ad614-118">[in] Zeiger auf die **MAPIAllocateBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad614-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="ad614-119">Zuweisen von Arbeitsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad614-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="ad614-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="ad614-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="ad614-121">[in] Zeiger auf die **MAPIFreeBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="ad614-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="ad614-122">Verwendet, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="ad614-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ad614-123">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ad614-123">Return value</span></span>

 <span data-ttu-id="ad614-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="ad614-124">**S_OK**</span></span>
  
> <span data-ttu-id="ad614-125">Der Aufruf war erfolgreich, und die angegebenen Spalten verschoben oder hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="ad614-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ad614-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ad614-126">Remarks</span></span>

<span data-ttu-id="ad614-127">Die Funktion **HrAddColumns** ist entspricht der Verwendung von **HrAddColumnsEx** mit _LpfnFilterColumns_ auf NULL festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ad614-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ad614-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad614-128">See also</span></span>



[<span data-ttu-id="ad614-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="ad614-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="ad614-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="ad614-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="ad614-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="ad614-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="ad614-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="ad614-132">SPropTagArray</span></span>](sproptagarray.md)

