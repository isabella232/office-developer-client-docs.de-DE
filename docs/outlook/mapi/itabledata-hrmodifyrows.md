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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 15d98183548d4b73c35368d690ef63d5c3dfd9af
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792856"
---
# <a name="itabledatahrmodifyrows"></a><span data-ttu-id="6862c-103">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="6862c-103">ITableData::HrModifyRows</span></span>

  
  
<span data-ttu-id="6862c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6862c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6862c-105">Mehrere Tabellenzeilen, möglicherweise Ersetzen der vorhandene Zeilen eingefügt.</span><span class="sxs-lookup"><span data-stu-id="6862c-105">Inserts multiple table rows, possibly replacing existing rows.</span></span>
  
```cpp
HRESULT HrModifyRows(
  ULONG ulFlags,
  LPSRowSet lpSRowSet
);
```

## <a name="parameters"></a><span data-ttu-id="6862c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6862c-106">Parameters</span></span>

 <span data-ttu-id="6862c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6862c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6862c-108">[in] Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6862c-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="6862c-109">_lpSRowSet_</span><span class="sxs-lookup"><span data-stu-id="6862c-109">_lpSRowSet_</span></span>
  
> <span data-ttu-id="6862c-110">[in] Ein Zeiger auf eine [SRowSet](srowset.md) -Struktur enthält, die den Satz von Zeilen hinzugefügt werden soll, Ersetzen von vorhandenen Zeilen bei Bedarf.</span><span class="sxs-lookup"><span data-stu-id="6862c-110">[in] A pointer to an [SRowSet](srowset.md) structure that contains the set of rows to be added, replacing existing rows if necessary.</span></span> <span data-ttu-id="6862c-111">Eine der Eigenschaft Wert Strukturen zum Festlegen anhand der **LpProps** Member jeder [SRow](srow.md) Struktur in der Zeile gezeigt sollte die Indexspalte den gleichen Wert enthalten, die in der _UlPropTagIndexColumn_ -Parameter im Aufruf der [angegeben wurde CreateTable](createtable.md) Funktion.</span><span class="sxs-lookup"><span data-stu-id="6862c-111">One of the property value structures pointed to by the **lpProps** member of each [SRow](srow.md) structure in the row set should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="6862c-112">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6862c-112">Return value</span></span>

<span data-ttu-id="6862c-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="6862c-113">S_OK</span></span> 
  
> <span data-ttu-id="6862c-114">Die Zeilen wurden erfolgreich eingefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="6862c-114">The rows were successfully inserted or modified.</span></span>
    
<span data-ttu-id="6862c-115">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="6862c-115">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="6862c-116">Eine oder mehrere Zeilen übergebenen verfügt nicht über eine Indexspalte.</span><span class="sxs-lookup"><span data-stu-id="6862c-116">One or more of the passed-in rows does not have an index column.</span></span> <span data-ttu-id="6862c-117">Wenn dieser Fehler zurückgegeben wird, werden keine Zeilen geändert.</span><span class="sxs-lookup"><span data-stu-id="6862c-117">If this error is returned, no rows are changed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6862c-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6862c-118">Remarks</span></span>

<span data-ttu-id="6862c-119">Die **ITableData::HrModifyRows** -Methode fügt die Zeilen, die durch die [SRowSet](srowset.md) -Struktur, die auf das durch den Parameter _LpSRowSet_ beschrieben.</span><span class="sxs-lookup"><span data-stu-id="6862c-119">The **ITableData::HrModifyRows** method inserts the rows described by the [SRowSet](srowset.md) structure pointed to by the  _lpSRowSet_ parameter.</span></span> <span data-ttu-id="6862c-120">Wenn der Wert von Column Index einer Zeile in der Zeile Set der Wert für eine vorhandene Zeile in der Tabelle entspricht, wird die vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="6862c-120">If the index column value of a row in the row set matches the value for an existing row in the table, the existing row is replaced.</span></span> <span data-ttu-id="6862c-121">Wenn keine Zeile vorhanden, die in der Struktur **SRowSet** enthaltene übereinstimmt ist, fügt **HrModifyRows** die Zeile an das Ende der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="6862c-121">If no row exists that matches the one included in the **SRowSet** structure, **HrModifyRows** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="6862c-122">Alle Ansichten für die Tabelle werden geändert, um die Zeilen, die auf den _LpSRowSet_enthalten.</span><span class="sxs-lookup"><span data-stu-id="6862c-122">All views of the table are modified to include the rows pointed to by  _lpSRowSet_.</span></span> <span data-ttu-id="6862c-123">Jedoch, wenn eine Ansicht eine Einschränkung eingerichtet, die eine Zeile ausschließt hat, es für den Benutzer sichtbar möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="6862c-123">However, if a view has a restriction in place that excludes a row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="6862c-124">Die Spalten in den Zeilen auf den _LpSRowSet_ müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle werden.</span><span class="sxs-lookup"><span data-stu-id="6862c-124">The columns in the rows pointed to by  _lpSRowSet_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="6862c-125">Der Aufrufer kann auch als Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="6862c-125">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="6862c-126">Für vorhandene Ansichten **HrModifyRows** diesen neuen Spalten zur Verfügung umfasst aber nicht sie in der aktuellen Spalte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="6862c-126">For existing views, **HrModifyRows** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="6862c-127">Für zukünftige Ansichten enthält **HrModifyRows** die neuen Spalten in der Spalte festlegen.</span><span class="sxs-lookup"><span data-stu-id="6862c-127">For future views, **HrModifyRows** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="6862c-128">Nachdem **HrModifyRows** die Zeilen hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet.</span><span class="sxs-lookup"><span data-stu-id="6862c-128">After **HrModifyRows** has added the rows, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="6862c-129">MAPI sendet TABLE_ROW_ADDED oder TABLE_ROW_MODIFIED Benachrichtigungen für jede Zeile, bis zu acht Zeilen.</span><span class="sxs-lookup"><span data-stu-id="6862c-129">MAPI sends TABLE_ROW_ADDED or TABLE_ROW_MODIFIED notifications for each row, up to eight rows.</span></span> <span data-ttu-id="6862c-130">Wenn mehr als acht Zeilen betroffen sind durch den Aufruf von **HrModifyRows** sendet MAPI eine einzelne TABLE_CHANGED Benachrichtigung stattdessen.</span><span class="sxs-lookup"><span data-stu-id="6862c-130">If more than eight rows are affected by the **HrModifyRows** call, MAPI sends a single TABLE_CHANGED notification instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6862c-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6862c-131">See also</span></span>



[<span data-ttu-id="6862c-132">SRowSet</span><span class="sxs-lookup"><span data-stu-id="6862c-132">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="6862c-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6862c-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

