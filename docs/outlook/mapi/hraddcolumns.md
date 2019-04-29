---
title: HrAddColumns
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8c980257-9372-4478-b635-bd91d0a66af9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 465b685038bc3d906e468c7d7b06e9c20e1fd3c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422474"
---
# <a name="hraddcolumns"></a><span data-ttu-id="3a653-103">HrAddColumns</span><span class="sxs-lookup"><span data-stu-id="3a653-103">HrAddColumns</span></span>

  
  
<span data-ttu-id="3a653-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3a653-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3a653-105">Fügt oder verschiebt Spalten an den Anfang einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3a653-105">Adds or moves columns to the beginning of an existing table.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="3a653-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="3a653-106">Header file:</span></span>  <br/> |<span data-ttu-id="3a653-107">mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="3a653-107">mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3a653-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="3a653-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3a653-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3a653-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3a653-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="3a653-110">Called by:</span></span>  <br/> |<span data-ttu-id="3a653-111">Client Anwendungen und Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="3a653-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumns(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="3a653-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a653-112">Parameters</span></span>

 <span data-ttu-id="3a653-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="3a653-113">_lptbl_</span></span>
  
> <span data-ttu-id="3a653-114">in Zeiger auf die betroffene MAPI-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="3a653-114">[in] Pointer to the MAPI table affected.</span></span>
    
 <span data-ttu-id="3a653-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="3a653-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="3a653-116">in Zeiger auf eine **SPropTagArray** -Struktur, die ein Array von Property-Tags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3a653-116">[in] Pointer to an **SPropTagArray** structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="3a653-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="3a653-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="3a653-118">in Zeiger auf die **MAPIAllocateBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3a653-118">[in] Pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="3a653-119">Wird zum Reservieren von Arbeitsspeicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="3a653-119">Used to allocate memory.</span></span> 
    
 <span data-ttu-id="3a653-120">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="3a653-120">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="3a653-121">in Zeiger auf die **mapifreebufferfreigegeben** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="3a653-121">[in] Pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="3a653-122">Wird verwendet, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="3a653-122">Used to free memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3a653-123">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a653-123">Return value</span></span>

 <span data-ttu-id="3a653-124">**S_OK**</span><span class="sxs-lookup"><span data-stu-id="3a653-124">**S_OK**</span></span>
  
> <span data-ttu-id="3a653-125">Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3a653-125">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3a653-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a653-126">Remarks</span></span>

<span data-ttu-id="3a653-127">Die **HrAddColumns** -Funktion entspricht der Verwendung von **HrAddColumnsEx** mit _lpfnFilterColumns_ auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3a653-127">The **HrAddColumns** function is equivalent to using **HrAddColumnsEx** with  _lpfnFilterColumns_ set to NULL.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3a653-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a653-128">See also</span></span>



[<span data-ttu-id="3a653-129">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="3a653-129">HrAddColumnsEx</span></span>](hraddcolumnsex.md)
  
[<span data-ttu-id="3a653-130">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="3a653-130">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="3a653-131">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="3a653-131">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="3a653-132">SPropTagArray</span><span class="sxs-lookup"><span data-stu-id="3a653-132">SPropTagArray</span></span>](sproptagarray.md)

