---
title: CreateTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CreateTable
api_type:
- HeaderDef
ms.assetid: 106ce3d8-d0bf-4a0e-9a15-dc8988d0eb58
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e8c399569e68b8cb55d803733ed93105ea0be799
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435012"
---
# <a name="createtable"></a><span data-ttu-id="f052c-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="f052c-103">CreateTable</span></span>

  
  
<span data-ttu-id="f052c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f052c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f052c-105">Erstellt Strukturen und ein Objekthandle für ein [ITableData-Objekt,](itabledataiunknown.md) das zum Erstellen von Tabelleninhalten verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="f052c-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f052c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f052c-106">Header file:</span></span>  <br/> |<span data-ttu-id="f052c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f052c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f052c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f052c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f052c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f052c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f052c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f052c-110">Called by:</span></span>  <br/> |<span data-ttu-id="f052c-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f052c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateTable(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  ULONG ulTableType,
  ULONG ulPropTagIndexColumn,
  LPSPropTagArray lpSPropTagArrayColumns,
  LPTABLEDATA FAR * lppTableData
);
```

## <a name="parameters"></a><span data-ttu-id="f052c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f052c-112">Parameters</span></span>

 <span data-ttu-id="f052c-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="f052c-113">_lpInterface_</span></span>
  
> <span data-ttu-id="f052c-114">[in] Zeiger auf eine Schnittstellen-ID (Interface Identifier, IID) für das Tabellendatenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f052c-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="f052c-115">Der gültige Schnittstellenbezeichner wird IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="f052c-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="f052c-116">Das Übergeben von NULL im  _lpInterface-Parameter_ bewirkt auch, dass das im  _lppTableData-Parameter_ zurückgegebene Tabellendatenobjekt in die Standardschnittstelle für ein Tabellendatenobjekt übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="f052c-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="f052c-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f052c-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f052c-118">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f052c-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="f052c-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="f052c-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="f052c-120">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f052c-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="f052c-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="f052c-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="f052c-122">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f052c-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="f052c-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="f052c-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="f052c-124">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="f052c-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="f052c-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="f052c-125">_ulTableType_</span></span>
  
> <span data-ttu-id="f052c-126">[in] Ein Tabellentyp, der einer Clientanwendung oder einem Dienstanbieter als Teil der [IMAPITable::GetStatus-Rückgabedaten](imapitable-getstatus.md) in den Tabellenansichten zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="f052c-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="f052c-127">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="f052c-127">Possible values are:</span></span> 
    
<span data-ttu-id="f052c-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="f052c-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="f052c-129">Der Inhalt der Tabelle ist dynamisch und kann sich ändern, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="f052c-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="f052c-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="f052c-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="f052c-131">Die Zeilen in der Tabelle sind fest, aber die Werte in diesen Zeilen sind dynamisch und können sich ändern, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="f052c-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="f052c-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="f052c-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="f052c-133">Die Tabelle ist statisch, und der Inhalt ändert sich nicht, wenn sich die zugrunde liegenden Daten ändern.</span><span class="sxs-lookup"><span data-stu-id="f052c-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="f052c-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="f052c-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="f052c-135">[in] Indexnummer der Spalte, die beim Ändern von Tabellendaten verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f052c-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="f052c-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="f052c-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="f052c-137">[in] Zeiger auf eine [SPropTagArray-Struktur,](sproptagarray.md) die ein Array von Eigenschaftstags enthält, die die eigenschaften angeben, die in der Tabelle erforderlich sind, für die das Objekt Daten enthält.</span><span class="sxs-lookup"><span data-stu-id="f052c-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="f052c-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="f052c-138">_lppTableData_</span></span>
  
> <span data-ttu-id="f052c-139">[out] Zeiger auf einen Zeiger auf das zurückgegebene Tabellendatenobjekt.</span><span class="sxs-lookup"><span data-stu-id="f052c-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f052c-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f052c-140">Return value</span></span>

<span data-ttu-id="f052c-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="f052c-141">S_OK</span></span> 
  
> <span data-ttu-id="f052c-142">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="f052c-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f052c-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f052c-143">Remarks</span></span>

<span data-ttu-id="f052c-144">Die _Eingabeparameter lpAllocateBuffer,_ _lpAllocateMore_ und _lpFreeBuffer_ verweisen auf die [Funktionen MAPIAllocateBuffer,](mapiallocatebuffer.md) [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="f052c-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="f052c-145">Eine Clientanwendung, die **CreateTable** aufruft, übergibt Zeiger auf die gerade benannten #A0 . Ein Dienstanbieter übergibt die Zeiger an diese Funktionen, die er beim Initialisierungsaufruf empfangen oder mit einem Aufruf der [IMAPISupport::GetMemAllocRoutines-Methode abgerufen](imapisupport-getmemallocroutines.md) hat.</span><span class="sxs-lookup"><span data-stu-id="f052c-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f052c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f052c-146">See also</span></span>



[<span data-ttu-id="f052c-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f052c-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

