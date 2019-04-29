---
title: ITableDataHrModifyRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRows
api_type:
- COM
ms.assetid: d295c896-9882-4d6f-9689-5cf40db208c0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d0074dd006fda6d44252011d0b979169e0c3d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405359"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="7a3f1-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="7a3f1-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="7a3f1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7a3f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7a3f1-105">Fügt mehrere Tabellenzeilen ein, die möglicherweise vorhandene Zeilen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="7a3f1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a3f1-106">Parameters</span></span>

 <span data-ttu-id="7a3f1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7a3f1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7a3f1-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="7a3f1-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="7a3f1-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="7a3f1-110">in Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur, die den Satz von Zeilen enthält, der hinzugefügt werden soll, und ggf. vorhandene Zeilen ersetzen.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="7a3f1-111">Eine der Eigenschaftswert Strukturen, auf die durch das **lpProps** -Element jeder [SRow](srow.md) -Struktur im Zeilensatz verwiesen wird, sollte die Indexspalte enthalten, den gleichen Wert, der im _ulPropTagIndexColumn_ -Parameter im Aufruf der [ Createable](createtable.md) -Funktion.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="7a3f1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a3f1-112">Return value</span></span>

<span data-ttu-id="7a3f1-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="7a3f1-113">S_OK</span></span> 
  
> <span data-ttu-id="7a3f1-114">Die Zeilen wurden erfolgreich eingefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="7a3f1-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="7a3f1-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="7a3f1-116">Mindestens eine der übergebenen Zeilen verfügt über keine Indexspalte.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="7a3f1-117">Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7a3f1-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7a3f1-118">Remarks</span></span>

<span data-ttu-id="7a3f1-119">Die **ITableData:: HrModifyRows** -Methode fügt die von der [SRowSet](srowset.md) -Struktur beschriebenen Zeilen ein, auf die durch den _lpSRowSet_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="7a3f1-120">Wenn der Index Spaltenwert einer Zeile im Zeilensatz mit dem Wert einer vorhandenen Zeile in der Tabelle übereinstimmt, wird die vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="7a3f1-121">Wenn keine Zeile vorhanden ist, die mit der in der **SRowSet** -Struktur übereinstimmt, fügt **HrModifyRows** die Zeile am Ende der Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="7a3f1-122">Alle Ansichten der Tabelle werden so geändert, dass Sie die Zeilen einbeziehen, auf die von _lpSRowSet_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="7a3f1-123">Wenn in einer Ansicht jedoch eine Einschränkung vorhanden ist, die eine Zeile ausschließt, ist Sie möglicherweise für den Benutzer nicht sichtbar.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="7a3f1-124">Die Spalten in den Zeilen, auf die von _lpSRowSet_ verwiesen wird, müssen sich nicht in derselben Reihenfolge wie die Spalten in der Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="7a3f1-125">Der Aufrufer kann auch als Spalteneigenschaften enthalten, die sich derzeit nicht in der Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="7a3f1-126">Bei vorhandenen Ansichten stellt **HrModifyRows** diese neuen Spalten zur Verfügung, diese werden jedoch nicht in den aktuellen Spaltensatz aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="7a3f1-127">Für zukünftige Ansichten enthält **HrModifyRows** die neuen Spalten in den Spaltensatz.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="7a3f1-128">Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="7a3f1-129">MAPI sendet TABLE_ROW_ADDED-oder TABLE_ROW_MODIFIED-Benachrichtigungen für jede Zeile, bis zu acht Zeilen.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="7a3f1-130">Wenn der **HrModifyRows** -Aufruf mehr als acht Zeilen betrifft, sendet MAPI stattdessen eine einzelne TABLE_CHANGED-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="7a3f1-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7a3f1-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a3f1-131">See also</span></span>



[<span data-ttu-id="7a3f1-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="7a3f1-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="7a3f1-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7a3f1-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

