---
title: HrAddColumnsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.HrAddColumnsEx
api_type:
- COM
ms.assetid: c0a65d2b-a9b8-4477-a1c7-18c8478126f6
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: c79d9ebb5be1d8af6c9136514d8a2b695513f755
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791896"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="7c078-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="7c078-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="7c078-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c078-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c078-105">Fügt oder Spalten an den Anfang einer vorhandenen Tabelle verschoben.</span><span class="sxs-lookup"><span data-stu-id="7c078-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7c078-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7c078-106">Header file:</span></span>  <br/> |<span data-ttu-id="7c078-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7c078-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7c078-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7c078-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7c078-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7c078-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7c078-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7c078-110">Called by:</span></span>  <br/> |<span data-ttu-id="7c078-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7c078-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrAddColumnsEx(
  LPMAPITABLE lptbl,
  LPSPropTagArray lpproptagColumnsNew,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPFREEBUFFER lpFreeBuffer,
  void (FAR * lpfnFilterColumns)(
  LPSPropTagArray ptaga)
);
```

## <a name="parameters"></a><span data-ttu-id="7c078-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c078-112">Parameters</span></span>

 <span data-ttu-id="7c078-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="7c078-113">_lptbl_</span></span>
  
> <span data-ttu-id="7c078-114">[in] Zeiger auf die MAPI-Tabelle betroffen.</span><span class="sxs-lookup"><span data-stu-id="7c078-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="7c078-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="7c078-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="7c078-116">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die enthält ein Array von Eigenschaftentags für die Eigenschaften hinzugefügt oder an den Anfang der Tabelle verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7c078-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="7c078-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7c078-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7c078-118">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c078-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="7c078-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="7c078-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="7c078-120">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7c078-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="7c078-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="7c078-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="7c078-122">[in] Zeiger auf eine Rückruffunktion, die vom Anrufer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="7c078-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="7c078-123">Wenn der _LpfnFilterColumns_ -Parameter auf NULL festgelegt ist, erfolgt kein Rückruf.</span><span class="sxs-lookup"><span data-stu-id="7c078-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="7c078-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="7c078-124">_ptaga_</span></span>
  
> <span data-ttu-id="7c078-125">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die enthält das Array von Eigenschaftentags bereits in der Tabelle, bevor Eigenschaften hinzugefügt oder an den Anfang verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7c078-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="7c078-126">**HrAddColumnsEx** übergibt diese Zeiger als Parameter an den Callback-Funktion mit _LpfnFilterColumns_gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7c078-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c078-127">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="7c078-127">Return value</span></span>

<span data-ttu-id="7c078-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c078-128">S_OK</span></span> 
  
> <span data-ttu-id="7c078-129">Der Aufruf war erfolgreich, und die angegebenen Spalten verschoben oder hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="7c078-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c078-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7c078-130">Remarks</span></span>

<span data-ttu-id="7c078-131">Die Eigenschaften **HrAddColumnsEx** mit dem _LpproptagColumnsNew_ -Parameter übergeben werden die ersten Eigenschaften für nachfolgende Aufrufe [der QueryRows](imapitable-queryrows.md) verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="7c078-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="7c078-132">Alle Eigenschaften zuvor in der Tabelle, die nicht im _LpproptagColumnsNew_ -Parameter angegeben wurden, werden nach alle Eigenschaften hinzugefügten und verschobenen verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="7c078-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="7c078-133">Wenn alle Tabelleneigenschaften **QueryRows** aufgerufen wird nicht definiert sind, werden diese mit Eigenschaftentyp PT_NULL und Eigenschaftenbezeichner PROP_ID_NULL zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7c078-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7c078-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7c078-134">Notes to callers</span></span>

<span data-ttu-id="7c078-135">Die **HrAddColumnsEx** -Funktion kann der Aufrufer erhalten Sie vom Netzwerkadministrator eine Callback-Funktion, um die Spalten zu filtern, die bereits in der Tabelle, beispielsweise Zeichenfolgen aus Eigenschaftentyp PT_UNICODE in PT_STRING8 konvertiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7c078-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="7c078-136">**HrAddColumnsEx** übergibt einen Zeiger auf die zuvor vorhandenen Spalte als Parameter an die Rückruffunktion festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7c078-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="7c078-137">Die Callback-Funktion kann Daten in dem Array der Tag-Eigenschaft geändert, neue Tags kann nicht hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="7c078-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="7c078-138">**HrAddColumnsEx** ruft zunächst die Callback-Funktion, wenn eine ausgestattet ist, und klicken Sie dann hinzugefügt oder die angegebenen Spalten verschiebt und schließlich [IMAPITable::SetColumns ruft](imapitable-setcolumns.md).</span><span class="sxs-lookup"><span data-stu-id="7c078-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="7c078-139">Die Eingabeparametern _LpAllocateBuffer_ und _LpFreeBuffer_ zeigen Sie jeweils auf die Funktionen [MAPIAllocateBuffer](mapiallocatebuffer.md) und [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="7c078-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="7c078-140">Die genauen Werte Zeiger an **HrAddColumnsEx** übergeben, hängt davon ab, ob der Anrufer eine Clientanwendung oder einem Dienstanbieter ist.</span><span class="sxs-lookup"><span data-stu-id="7c078-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="7c078-141">Ein Client übergibt Zeiger an die MAPI-Funktionen mit den angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="7c078-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="7c078-142">Ein Dienstanbieter übergibt die Zeiger, die es in seinem Initialisierungsaufruf empfangen oder durch Aufrufen der Methode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7c078-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c078-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7c078-143">See also</span></span>



[<span data-ttu-id="7c078-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="7c078-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

