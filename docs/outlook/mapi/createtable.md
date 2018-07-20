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
ms.openlocfilehash: 5f42e1eb0d120d2fbb785e63b451acdd2d5a91f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791497"
---
# <a name="createtable"></a><span data-ttu-id="7573c-103">CreateTable</span><span class="sxs-lookup"><span data-stu-id="7573c-103">CreateTable</span></span>

  
  
<span data-ttu-id="7573c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7573c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7573c-105">Erstellt Strukturen und Objekt-Handle für ein [ITableData](itabledataiunknown.md) -Objekt, die zum Erstellen des Inhaltsverzeichnisses verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="7573c-105">Creates structures and an object handle for an [ITableData](itabledataiunknown.md) object which can be used to create table contents.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7573c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="7573c-106">Header file:</span></span>  <br/> |<span data-ttu-id="7573c-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="7573c-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="7573c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="7573c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7573c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="7573c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="7573c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="7573c-110">Called by:</span></span>  <br/> |<span data-ttu-id="7573c-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="7573c-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="7573c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7573c-112">Parameters</span></span>

 <span data-ttu-id="7573c-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7573c-113">_lpInterface_</span></span>
  
> <span data-ttu-id="7573c-114">[in] Zeiger auf eine Schnittstellenbezeichner (IID) für das Table-Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="7573c-114">[in] Pointer to an interface identifier (IID) for the table data object.</span></span> <span data-ttu-id="7573c-115">Der Bezeichner gültige Schnittstelle ist IID_IMAPITableData.</span><span class="sxs-lookup"><span data-stu-id="7573c-115">The valid interface identifier is IID_IMAPITableData.</span></span> <span data-ttu-id="7573c-116">Übergeben NULL im _LpInterface_ -Parameter wird auch das Table-Objekt, Daten, die in der _LppTableData_ -Parameter in der standard-Benutzeroberfläche für ein Table-Datenobjekt umgewandelt werden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7573c-116">Passing NULL in the  _lpInterface_ parameter also causes the table data object returned in the  _lppTableData_ parameter to be cast to the standard interface for a table data object.</span></span> 
    
 <span data-ttu-id="7573c-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7573c-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7573c-118">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7573c-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="7573c-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="7573c-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="7573c-120">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7573c-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="7573c-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="7573c-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="7573c-122">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="7573c-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="7573c-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="7573c-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="7573c-124">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7573c-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="7573c-125">_ulTableType_</span><span class="sxs-lookup"><span data-stu-id="7573c-125">_ulTableType_</span></span>
  
> <span data-ttu-id="7573c-126">[in] Eine Tabellentyp, der als Teil der [IMAPITable::GetStatus](imapitable-getstatus.md) Zurückgeben von Daten in der Tabellenansichten auf eine Clientanwendung oder den Dienstanbieter verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7573c-126">[in] A table type that is available to a client application or service provider as part of the [IMAPITable::GetStatus](imapitable-getstatus.md) return data on its table views.</span></span> <span data-ttu-id="7573c-127">Die folgenden Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="7573c-127">Possible values are:</span></span> 
    
<span data-ttu-id="7573c-128">TBLTYPE_DYNAMIC</span><span class="sxs-lookup"><span data-stu-id="7573c-128">TBLTYPE_DYNAMIC</span></span> 
  
> <span data-ttu-id="7573c-129">Inhalt der Tabelle sind dynamisch und ändern können, als die zugrunde liegenden Daten geändert.</span><span class="sxs-lookup"><span data-stu-id="7573c-129">The table's contents are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="7573c-130">TBLTYPE_KEYSET</span><span class="sxs-lookup"><span data-stu-id="7573c-130">TBLTYPE_KEYSET</span></span> 
  
> <span data-ttu-id="7573c-131">Die Zeilen in der Tabelle behoben werden, aber die Werte in diesen Zeilen sind dynamisch und ändern können, als die zugrunde liegenden Daten geändert.</span><span class="sxs-lookup"><span data-stu-id="7573c-131">The rows in the table are fixed, but the values in these rows are dynamic and can change as the underlying data changes.</span></span> 
    
<span data-ttu-id="7573c-132">TBLTYPE_SNAPSHOT</span><span class="sxs-lookup"><span data-stu-id="7573c-132">TBLTYPE_SNAPSHOT</span></span> 
  
> <span data-ttu-id="7573c-133">Die Tabelle ist statisch und den Inhalt nicht ändern, wenn die zugrunde liegenden Daten geändert.</span><span class="sxs-lookup"><span data-stu-id="7573c-133">The table is static and the contents do not change when the underlying data changes.</span></span> 
    
 <span data-ttu-id="7573c-134">_ulPropTagIndexColumn_</span><span class="sxs-lookup"><span data-stu-id="7573c-134">_ulPropTagIndexColumn_</span></span>
  
> <span data-ttu-id="7573c-135">[in] Die Indexnummer der Spalte für die Verwendung beim Ändern von Tabellendaten.</span><span class="sxs-lookup"><span data-stu-id="7573c-135">[in] Index number of the column for use when changing table data.</span></span> 
    
 <span data-ttu-id="7573c-136">_lpSPropTagArrayColumns_</span><span class="sxs-lookup"><span data-stu-id="7573c-136">_lpSPropTagArrayColumns_</span></span>
  
> <span data-ttu-id="7573c-137">[in] Zeiger auf eine [SPropTagArray](sproptagarray.md) -Struktur, die ein Array von Eigenschaftentags, der angibt, in der Tabelle, für die das Objekt Daten enthält, erforderlichen Eigenschaften enthält.</span><span class="sxs-lookup"><span data-stu-id="7573c-137">[in] Pointer to an [SPropTagArray](sproptagarray.md) structure that contains an array of property tags indicating the properties required in the table for which the object holds data.</span></span> 
    
 <span data-ttu-id="7573c-138">_lppTableData_</span><span class="sxs-lookup"><span data-stu-id="7573c-138">_lppTableData_</span></span>
  
> <span data-ttu-id="7573c-139">[out] Zeiger auf einen Zeiger auf das zurückgegebene Tabelle Datenobjekt.</span><span class="sxs-lookup"><span data-stu-id="7573c-139">[out] Pointer to a pointer to the returned table data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7573c-140">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7573c-140">Return value</span></span>

<span data-ttu-id="7573c-141">S_OK</span><span class="sxs-lookup"><span data-stu-id="7573c-141">S_OK</span></span> 
  
> <span data-ttu-id="7573c-142">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="7573c-142">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7573c-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7573c-143">Remarks</span></span>

<span data-ttu-id="7573c-144">Die Eingabeparametern _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ zeigen die [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md) -Funktionen.</span><span class="sxs-lookup"><span data-stu-id="7573c-144">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="7573c-145">Eine Clientanwendung Aufrufen **CreateTable** übergibt Zeiger auf die MAPI-Funktionen, die nur mit dem Namen; Ein Dienstanbieter übergibt die Zeiger auf diese Funktionen, die sie in der Initialisierung Anruf empfangen oder mit einem Aufruf der Methode [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) abgerufen.</span><span class="sxs-lookup"><span data-stu-id="7573c-145">A client application calling **CreateTable** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions that it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7573c-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7573c-146">See also</span></span>



[<span data-ttu-id="7573c-147">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7573c-147">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

