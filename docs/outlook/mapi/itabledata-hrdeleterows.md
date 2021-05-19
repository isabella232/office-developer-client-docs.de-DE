---
title: ITableDataHrDeleteRows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRows
api_type:
- COM
ms.assetid: 7b351eec-9624-4b38-9978-5d0b67b64687
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fdd6f40b4d7aa7f65bf1a46d3d9a4f18472b19f7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416454"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="78b57-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="78b57-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="78b57-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78b57-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78b57-105">Löscht mehrere Tabellenzeilen.</span><span class="sxs-lookup"><span data-stu-id="78b57-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="78b57-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78b57-106">Parameters</span></span>

 <span data-ttu-id="78b57-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78b57-107">_ulFlags_</span></span>
  
> <span data-ttu-id="78b57-108">[in] Eine Bitmaske mit Flags, die den Löschvorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="78b57-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="78b57-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="78b57-109">The following flag can be set:</span></span>
    
<span data-ttu-id="78b57-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="78b57-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="78b57-111">Löscht alle Zeilen aus der Tabelle und allen entsprechenden Ansichten und sendet eine TABLE_RELOAD Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="78b57-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="78b57-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="78b57-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="78b57-113">[in] Ein Zeiger auf einen Zeilensatz, der die zu löschende Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="78b57-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="78b57-114">Der  _lprowsetToDelete-Parameter_ kann NULL sein, wenn TAD_ALL_ROWS im  _ulFlags-Parameter festgelegt_ ist.</span><span class="sxs-lookup"><span data-stu-id="78b57-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="78b57-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="78b57-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="78b57-116">[out] Die Anzahl der gelöschten Zeilen.</span><span class="sxs-lookup"><span data-stu-id="78b57-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78b57-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78b57-117">Return value</span></span>

<span data-ttu-id="78b57-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="78b57-118">S_OK</span></span> 
  
> <span data-ttu-id="78b57-119">Die Tabellenzeilen wurden erfolgreich gelöscht.</span><span class="sxs-lookup"><span data-stu-id="78b57-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78b57-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78b57-120">Remarks</span></span>

<span data-ttu-id="78b57-121">Die **ITableData::HrDeleteRows-Methode** sucht und entfernt die Tabellenzeilen, die die Spalten enthalten, die mit der Eigenschaft übereinstimmen, auf die das **lpProps-Mitglied** jedes **aRow-Eintrags** im Zeilensatz verweist.</span><span class="sxs-lookup"><span data-stu-id="78b57-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="78b57-122">Zum Identifizieren jeder Zeile wird eine Indexspalte verwendet. Diese Spalte muss das gleiche Eigenschaftstag wie das Eigenschaftstag haben, das im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion übergeben](createtable.md) wird.</span><span class="sxs-lookup"><span data-stu-id="78b57-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="78b57-123">Die Anzahl der Zeilen, die tatsächlich gelöscht wurden, wird in _cRowsDeleted zurückgegeben._</span><span class="sxs-lookup"><span data-stu-id="78b57-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="78b57-124">Es wird kein Fehler zurückgegeben, wenn eine oder mehrere Zeilen nicht gefunden wurden.</span><span class="sxs-lookup"><span data-stu-id="78b57-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="78b57-125">Nachdem die Zeilen gelöscht wurden, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="78b57-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="78b57-126">Durch das Löschen von Zeilen werden die Spalten, die vorhandenen Tabellenansichten oder anschließend geöffneten Tabellenansichten zur Verfügung stehen, nicht reduziert, auch wenn die gelöschten Zeilen die letzten sind, die Werte für eine bestimmte Spalte enthalten.</span><span class="sxs-lookup"><span data-stu-id="78b57-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="78b57-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78b57-127">See also</span></span>



[<span data-ttu-id="78b57-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="78b57-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="78b57-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="78b57-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="78b57-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="78b57-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="78b57-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="78b57-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="78b57-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="78b57-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="78b57-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78b57-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

