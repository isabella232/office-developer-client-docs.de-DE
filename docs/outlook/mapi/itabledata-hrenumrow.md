---
title: ITableDataHrEnumRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrEnumRow
api_type:
- COM
ms.assetid: b25d9f2b-9454-4983-98f7-6a051a3b8a04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 140efe0b2d1b428a94b5bb2919d461779613932a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564682"
---
# <a name="itabledatahrenumrow"></a><span data-ttu-id="20322-103">ITableData::HrEnumRow</span><span class="sxs-lookup"><span data-stu-id="20322-103">ITableData::HrEnumRow</span></span>

  
  
<span data-ttu-id="20322-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="20322-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="20322-105">Ruft eine Zeile basierend auf seine Position in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="20322-105">Retrieves a row based on its position in the table.</span></span> 
  
```cpp
HRESULT HrEnumRow(
  ULONG ulRowNumber,
  LPSRow FAR * lppSRow
);
```

## <a name="parameters"></a><span data-ttu-id="20322-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20322-106">Parameters</span></span>

 <span data-ttu-id="20322-107">_ulRowNumber_</span><span class="sxs-lookup"><span data-stu-id="20322-107">_ulRowNumber_</span></span>
  
> <span data-ttu-id="20322-108">[in] Die Anzahl der Zeilen für die Eigenschaften zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="20322-108">[in] The number of the row for which to return properties.</span></span> <span data-ttu-id="20322-109">Der Wert in der _UlRowNumber_ -Parameter kann ein beliebiger Wert von 0, sein, die die erste Zeile in der Tabelle, bis n - 1, gibt an, welche die gibt die letzte Zeile in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="20322-109">The value in the  _ulRowNumber_ parameter can be any value from 0, which indicates the first row in the table, through n - 1, which indicates the last row in the table.</span></span> 
    
 <span data-ttu-id="20322-110">_lppSRow_</span><span class="sxs-lookup"><span data-stu-id="20322-110">_lppSRow_</span></span>
  
> <span data-ttu-id="20322-111">[out] Ein Zeiger auf einen Zeiger auf eine [SRow](srow.md) -Struktur, die Zielzeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="20322-111">[out] A pointer to a pointer to an [SRow](srow.md) structure that describes the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="20322-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="20322-112">Return value</span></span>

<span data-ttu-id="20322-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="20322-113">S_OK</span></span> 
  
> <span data-ttu-id="20322-114">Die Zeile erfolgreich abgerufen wurde, oder eine Zeile für die Nummer der Zeile durch den _UlRowNumber_ -Parameter angegeben ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="20322-114">The row was retrieved successfully, or a row for the row number specified by the  _ulRowNumber_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="20322-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="20322-115">Remarks</span></span>

<span data-ttu-id="20322-116">Die **ITableData::HrEnumRow** -Methode ruft eine Zeile basierend auf eine fortlaufende Zahl.</span><span class="sxs-lookup"><span data-stu-id="20322-116">The **ITableData::HrEnumRow** method retrieves a row based on a sequential number.</span></span> <span data-ttu-id="20322-117">Diese Nummer stellt die Reihenfolge des Einfügevorgangs (0 gibt die erste Zeile und die Anzahl der Zeilen minus 1 gibt die letzte Zeile).</span><span class="sxs-lookup"><span data-stu-id="20322-117">This number represents the order of insertion (0 indicates the first row, and the number of rows minus 1 indicates the last row).</span></span> <span data-ttu-id="20322-118">MAPI behält diese Reihenfolge der Zeile eingefügt für die Lebensdauer des Table-Objekts Daten.</span><span class="sxs-lookup"><span data-stu-id="20322-118">MAPI maintains this chronological order of row insertion for the lifetime of the table data object.</span></span> 
  
<span data-ttu-id="20322-119">Wenn die Nummer im angegebenen _UlRowNumber_ nicht zu einer Zeile in der Tabelle entspricht, **HrEnumRow** gibt S_OK zurück, und der _LppSRow_ -Parameter auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="20322-119">If the number specified in  _ulRowNumber_ does not correspond to a row in the table, **HrEnumRow** returns S_OK and sets the  _lppSRow_ parameter to NULL.</span></span> 
  
<span data-ttu-id="20322-120">MAPI weist Speicher für die zurückgegebene Struktur **' srow '** mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, wenn das Table-Datenobjekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="20322-120">MAPI allocates memory for the returned **SRow** structure by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) function when the table data object is created.</span></span> <span data-ttu-id="20322-121">Der Aufrufer muss diesen Speicher Aufruf der Funktion [MAPIFreeBuffer](mapifreebuffer.md) freigeben.</span><span class="sxs-lookup"><span data-stu-id="20322-121">The caller must release this memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
<span data-ttu-id="20322-122">Um Zeilen aus einer Tabelle in der Reihenfolge abzurufen, dass sie eingefügt wurden, rufen Sie Tabelle Daten Objekt Benutzer die **HrEnumRow** -Methode.</span><span class="sxs-lookup"><span data-stu-id="20322-122">To retrieve rows from a table in the order that they were inserted, table data object users call the **HrEnumRow** method.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="20322-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20322-123">See also</span></span>



[<span data-ttu-id="20322-124">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="20322-124">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="20322-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="20322-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="20322-126">SRow</span><span class="sxs-lookup"><span data-stu-id="20322-126">SRow</span></span>](srow.md)
  
[<span data-ttu-id="20322-127">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="20322-127">ITableData : IUnknown</span></span>](itabledataiunknown.md)

