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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9ca34fb2cce6e86c42e8e9525cd213f1008997d6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427479"
---
# <a name="hraddcolumnsex"></a><span data-ttu-id="7fe6a-103">HrAddColumnsEx</span><span class="sxs-lookup"><span data-stu-id="7fe6a-103">HrAddColumnsEx</span></span>

  
  
<span data-ttu-id="7fe6a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7fe6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7fe6a-105">Fügt oder verschiebt Spalten an den Anfang einer vorhandenen Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-105">Adds or moves columns to the beginning of an existing table.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7fe6a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7fe6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="7fe6a-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="7fe6a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7fe6a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7fe6a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7fe6a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7fe6a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7fe6a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7fe6a-110">Called by:</span></span>  <br/> |<span data-ttu-id="7fe6a-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7fe6a-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7fe6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7fe6a-112">Parameters</span></span>

 <span data-ttu-id="7fe6a-113">_lptbl_</span><span class="sxs-lookup"><span data-stu-id="7fe6a-113">_lptbl_</span></span>
  
> <span data-ttu-id="7fe6a-114">in Zeiger auf die betroffene MAPI-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-114">[in] Pointer to the MAPI table affected.</span></span> 
    
 <span data-ttu-id="7fe6a-115">_lpproptagColumnsNew_</span><span class="sxs-lookup"><span data-stu-id="7fe6a-115">_lpproptagColumnsNew_</span></span>
  
> <span data-ttu-id="7fe6a-116">in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Property-Tags für die Eigenschaften enthält, die hinzugefügt oder an den Anfang der Tabelle verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-116">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags for the properties to be added or moved to the beginning of the table.</span></span> 
    
 <span data-ttu-id="7fe6a-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7fe6a-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7fe6a-118">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="7fe6a-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="7fe6a-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="7fe6a-120">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="7fe6a-121">_lpfnFilterColumns_</span><span class="sxs-lookup"><span data-stu-id="7fe6a-121">_lpfnFilterColumns_</span></span>
  
> <span data-ttu-id="7fe6a-122">in Zeiger auf eine vom Aufrufer eingerichtete Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-122">[in] Pointer to a callback function furnished by the caller.</span></span> <span data-ttu-id="7fe6a-123">Wenn der _lpfnFilterColumns_ -Parameter auf NULL festgelegt ist, wird kein Rückruf vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-123">If the  _lpfnFilterColumns_ parameter is set to NULL, no callback is made.</span></span> 
    
 <span data-ttu-id="7fe6a-124">_ptaga_</span><span class="sxs-lookup"><span data-stu-id="7fe6a-124">_ptaga_</span></span>
  
> <span data-ttu-id="7fe6a-125">in Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die das Array von Property-Tags enthält, die bereits in der Tabelle vorhanden sind, bevor Eigenschaften hinzugefügt oder an den Anfang verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-125">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains the array of property tags already existing in the table before properties are added or moved to the beginning.</span></span> <span data-ttu-id="7fe6a-126">**HrAddColumnsEx** übergibt diesen Zeiger als Parameter an die Rückruffunktion, auf die durch _lpfnFilterColumns_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-126">**HrAddColumnsEx** passes this pointer as the parameter to the callback function pointed to by  _lpfnFilterColumns_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7fe6a-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7fe6a-127">Return value</span></span>

<span data-ttu-id="7fe6a-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="7fe6a-128">S_OK</span></span> 
  
> <span data-ttu-id="7fe6a-129">Der Aufruf war erfolgreich, und die angegebenen Spalten wurden verschoben oder hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-129">The call succeeded and the specified columns were moved or added.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7fe6a-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7fe6a-130">Remarks</span></span>

<span data-ttu-id="7fe6a-131">Die an **HrAddColumnsEx** übergebenen Eigenschaften werden mithilfe des _lpproptagColumnsNew_ -Parameters zu den ersten Eigenschaften, die bei nachfolgenden Aufrufen der [IMAPITable:: QueryRows](imapitable-queryrows.md) -Methode verfügbar gemacht werden.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-131">The properties passed to **HrAddColumnsEx** using the  _lpproptagColumnsNew_ parameter become the first properties exposed on subsequent calls to the [IMAPITable::QueryRows](imapitable-queryrows.md) method.</span></span> <span data-ttu-id="7fe6a-132">Alle zuvor in der Tabelle aufgeführten Eigenschaften, die nicht im _lpproptagColumnsNew_ -Parameter angegeben wurden, werden nach allen hinzugefügten und verschobenen Eigenschaften verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-132">Any properties previously in the table that were not specified in the  _lpproptagColumnsNew_ parameter are exposed after all the added and moved properties.</span></span> 
  
<span data-ttu-id="7fe6a-133">Wenn Tabelleneigenschaften nicht definiert sind, wenn **QueryRows** aufgerufen wird, werden Sie mit Eigenschafts PT_NULL und PROP_ID_NULL der Eigenschaftskennung zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-133">If any table properties are undefined when **QueryRows** is called, they are returned with property type PT_NULL and property identifier PROP_ID_NULL.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7fe6a-134">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7fe6a-134">Notes to callers</span></span>

<span data-ttu-id="7fe6a-135">Die **HrAddColumnsEx** -Funktion ermöglicht es dem Aufrufer, eine Rückruffunktion bereitzustellen, um die Spalten zu filtern, die bereits in der Tabelle enthalten sind, beispielsweise zum Konvertieren von Zeichenfolgen vom PT_UNICODE in PT_String8.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-135">The **HrAddColumnsEx** function allows the caller to furnish a callback function to filter the columns that were already in the table, for example to convert strings from property type PT_UNICODE to PT_STRING8.</span></span> <span data-ttu-id="7fe6a-136">**HrAddColumnsEx** übergibt einen Zeiger auf den zuvor vorhandenen Spaltensatz als Parameter für die Rückruffunktion.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-136">**HrAddColumnsEx** passes a pointer to the previously existing column set as the parameter to the callback function.</span></span> <span data-ttu-id="7fe6a-137">Die Callback-Funktion kann Daten im Property-Tag-Array ändern, aber keine neuen Tags hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-137">The callback function can change data in the property tag array but cannot add new tags.</span></span> 
  
 <span data-ttu-id="7fe6a-138">**HrAddColumnsEx** ruft zuerst die Callback-Funktion auf, wenn eine eingerichtet ist, fügt die angegebenen Spalten hinzu oder verschiebt Sie und ruft schließlich [IMAPITable::](imapitable-setcolumns.md)SetColumns auf.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-138">**HrAddColumnsEx** first calls the callback function if one is furnished, then adds or moves the specified columns, and finally calls [IMAPITable::SetColumns](imapitable-setcolumns.md).</span></span> 
  
<span data-ttu-id="7fe6a-139">Die _lpAllocateBuffer_ -und _lpFreeBuffer_ -Eingabeparameter zeigen auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -und die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-139">The  _lpAllocateBuffer_ and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="7fe6a-140">Die genauen Werte der an **HrAddColumnsEx** übergebenen Zeiger hängen davon ab, ob es sich bei dem Aufrufer um eine Clientanwendung oder einen Dienstanbieter handelt.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-140">The exact values of the pointers passed to **HrAddColumnsEx** depend on whether the caller is a client application or a service provider.</span></span> <span data-ttu-id="7fe6a-141">Ein Client übergibt Zeiger auf die MAPI-Funktionen mit den angegebenen Namen.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-141">A client passes pointers to the MAPI functions with the specified names.</span></span> <span data-ttu-id="7fe6a-142">Ein Dienstanbieter übergibt die Zeiger, die er bei seinem Initialisierungsaufruf erhalten hat, oder wird durch Aufrufen der [IMAPISupport:: GetMemAllocRoutines](imapisupport-getmemallocroutines.md) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7fe6a-142">A service provider passes the pointers it received in its initialization call or retrieved by calling the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7fe6a-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7fe6a-143">See also</span></span>



[<span data-ttu-id="7fe6a-144">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="7fe6a-144">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)

