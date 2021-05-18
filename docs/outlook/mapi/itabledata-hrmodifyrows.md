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
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="1f711-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="1f711-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="1f711-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f711-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f711-105">Fügt mehrere Tabellenzeilen ein und ersetzt möglicherweise vorhandene Zeilen.</span><span class="sxs-lookup"><span data-stu-id="1f711-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="1f711-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1f711-106">Parameters</span></span>

 <span data-ttu-id="1f711-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1f711-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1f711-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="1f711-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1f711-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="1f711-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="1f711-110">[in] Ein Zeiger auf eine [SRowSet-Struktur,](srowset.md) die die zu hinzufügende Gruppe von Zeilen enthält und bei Bedarf vorhandene Zeilen ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1f711-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="1f711-111">Eine der Eigenschaftenwertstrukturen, auf die das **lpProps-Element** jeder [SRow-Struktur](srow.md) im Zeilensatz verweist, sollte die Indexspalte enthalten, denselben Wert, der im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion](createtable.md) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="1f711-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1f711-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1f711-112">Return value</span></span>

<span data-ttu-id="1f711-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="1f711-113">S_OK</span></span> 
  
> <span data-ttu-id="1f711-114">Die Zeilen wurden erfolgreich eingefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="1f711-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="1f711-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1f711-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1f711-116">Mindestens eine der übergebenen Zeilen verfügt nicht über eine Indexspalte.</span><span class="sxs-lookup"><span data-stu-id="1f711-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="1f711-117">Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.</span><span class="sxs-lookup"><span data-stu-id="1f711-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1f711-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1f711-118">Remarks</span></span>

<span data-ttu-id="1f711-119">Die **ITableData::HrModifyRows-Methode** fügt die Zeilen ein, die von der [SRowSet-Struktur](srowset.md) beschrieben werden, auf die der  _lpSRowSet-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="1f711-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="1f711-120">Wenn der Indexspaltenwert einer Zeile im Zeilensatz dem Wert für eine vorhandene Zeile in der Tabelle entspricht, wird die vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1f711-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="1f711-121">Wenn keine Zeile vorhanden ist, die der in der **SRowSet-Struktur** enthaltenen Zeile entspricht, fügt **HrModifyRows** die Zeile am Ende der Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="1f711-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="1f711-122">Alle Ansichten der Tabelle werden so geändert, dass sie die Zeilen enthalten, auf die _von lpSRowSet verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="1f711-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="1f711-123">Wenn eine Ansicht jedoch eine Einschränkung hat, die eine Zeile ausschließt, ist sie möglicherweise nicht für den Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="1f711-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="1f711-124">Die Spalten in den Zeilen, auf die  _von lpSRowSet_ verwiesen wird, müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="1f711-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="1f711-125">Der Aufrufer kann auch Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1f711-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="1f711-126">Für vorhandene Ansichten **stellt HrModifyRows** diese neuen Spalten zur Verfügung, schließt sie jedoch nicht in den aktuellen Spaltensatz ein.</span><span class="sxs-lookup"><span data-stu-id="1f711-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="1f711-127">Für zukünftige Ansichten **enthält HrModifyRows** die neuen Spalten im Spaltensatz.</span><span class="sxs-lookup"><span data-stu-id="1f711-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="1f711-128">Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="1f711-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="1f711-129">MAPI sendet TABLE_ROW_ADDED oder TABLE_ROW_MODIFIED Benachrichtigungen für jede Zeile, bis zu acht Zeilen.</span><span class="sxs-lookup"><span data-stu-id="1f711-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="1f711-130">Wenn mehr als acht Zeilen vom **HrModifyRows-Aufruf** betroffen sind, sendet MAPI stattdessen eine TABLE_CHANGED Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1f711-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1f711-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f711-131">See also</span></span>



[<span data-ttu-id="1f711-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="1f711-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="1f711-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1f711-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

