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
ms.openlocfilehash: 00662d7a5bf1c2addc5c4e0b39d657abd7073753
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792835"
---
# <a name="itabledatahrdeleterows"></a><span data-ttu-id="d3500-103">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="d3500-103">ITableData::HrDeleteRows</span></span>

  
  
<span data-ttu-id="d3500-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d3500-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d3500-105">Löscht mehrere Tabellenzeilen.</span><span class="sxs-lookup"><span data-stu-id="d3500-105">Deletes multiple table rows.</span></span>
  
```cpp
HRESULT HrDeleteRows(
  ULONG ulFlags,
  LPSRowSet lprowsetToDelete,
  ULONG FAR * cRowsDeleted
);
```

## <a name="parameters"></a><span data-ttu-id="d3500-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3500-106">Parameters</span></span>

 <span data-ttu-id="d3500-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d3500-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d3500-108">[in] Eine Bitmaske aus Flags, die den Löschvorgang steuert.</span><span class="sxs-lookup"><span data-stu-id="d3500-108">[in] A bitmask of flags that controls the deletion.</span></span> <span data-ttu-id="d3500-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d3500-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d3500-110">TAD_ALL_ROWS</span><span class="sxs-lookup"><span data-stu-id="d3500-110">TAD_ALL_ROWS</span></span> 
  
> <span data-ttu-id="d3500-111">Löscht alle Zeilen aus der Tabelle und alle zugehörigen Ansichten eine einzelne TABLE_RELOAD-Benachrichtigung senden.</span><span class="sxs-lookup"><span data-stu-id="d3500-111">Deletes all rows from the table and all corresponding views, sending a single TABLE_RELOAD notification.</span></span>
    
 <span data-ttu-id="d3500-112">_lprowsetToDelete_</span><span class="sxs-lookup"><span data-stu-id="d3500-112">_lprowsetToDelete_</span></span>
  
> <span data-ttu-id="d3500-113">[in] Ein Zeiger auf ein Rowset fest, die die zu löschenden Zeilen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d3500-113">[in] A pointer to a row set that describes the rows to be deleted.</span></span> <span data-ttu-id="d3500-114">Der Parameter _LprowsetToDelete_ kann NULL sein, wenn das Flag TAD_ALL_ROWS im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d3500-114">The  _lprowsetToDelete_ parameter can be NULL if the TAD_ALL_ROWS flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d3500-115">_cRowsDeleted_</span><span class="sxs-lookup"><span data-stu-id="d3500-115">_cRowsDeleted_</span></span>
  
> <span data-ttu-id="d3500-116">[out] Die Anzahl der gelöschten Zeilen.</span><span class="sxs-lookup"><span data-stu-id="d3500-116">[out] The count of the deleted rows.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d3500-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d3500-117">Return value</span></span>

<span data-ttu-id="d3500-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="d3500-118">S_OK</span></span> 
  
> <span data-ttu-id="d3500-119">Zeilen der Tabelle gelöscht wurden.</span><span class="sxs-lookup"><span data-stu-id="d3500-119">The table rows were successfully deleted.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d3500-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d3500-120">Remarks</span></span>

<span data-ttu-id="d3500-121">Die **ITableData::HrDeleteRows** -Methode sucht und entfernt die Zeilen der Tabelle, die die Spalten enthalten, die die-Eigenschaft zum Festlegen anhand der **LpProps** Member der einzelnen **aRow** Einträge in der Zeile gezeigt entsprechen.</span><span class="sxs-lookup"><span data-stu-id="d3500-121">The **ITableData::HrDeleteRows** method locates and removes the table rows that contain the columns that match the property pointed to by the **lpProps** member of each **aRow** entry in the row set.</span></span> <span data-ttu-id="d3500-122">Eine Indexspalte wird verwendet, um jede Zeile zu identifizieren. Diese Spalte muss das gleiche Eigenschafts-Tag als das Eigenschafts-Tag im _UlPropTagIndexColumn_ -Parameter im Aufruf der [CreateTable](createtable.md) -Funktion übergeben haben.</span><span class="sxs-lookup"><span data-stu-id="d3500-122">An index column is used to identify each row; this column must have the same property tag as the property tag passed in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
  
<span data-ttu-id="d3500-123">Die Anzahl der Zeilen, die tatsächlich gelöscht wurden, wird in _cRowsDeleted_zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3500-123">The number of rows that were actually deleted is returned in  _cRowsDeleted_.</span></span> <span data-ttu-id="d3500-124">Es wird kein Fehler zurückgegeben, wenn eine oder mehrere Zeilen nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="d3500-124">No error is returned if one or more rows could not be found.</span></span> 
  
<span data-ttu-id="d3500-125">Nachdem die Zeilen gelöscht werden, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet.</span><span class="sxs-lookup"><span data-stu-id="d3500-125">After the rows are deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="d3500-126">Löschen von Zeilen, verringert sich nicht auf die Spalten der vorhandenen Tabelle Ansichten oder Tabellenansichten anschließend geöffnet werden, selbst wenn gelöschten Zeilen der letzten, die Werte für eine bestimmte Spalte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="d3500-126">Deleting rows does not reduce the columns available to existing table views or subsequently opened table views, even if the deleted rows are the last that have values for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d3500-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d3500-127">See also</span></span>



[<span data-ttu-id="d3500-128">CreateTable</span><span class="sxs-lookup"><span data-stu-id="d3500-128">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="d3500-129">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="d3500-129">ITableData::HrDeleteRow</span></span>](itabledata-hrdeleterow.md)
  
[<span data-ttu-id="d3500-130">ITableData::HrModifyRows</span><span class="sxs-lookup"><span data-stu-id="d3500-130">ITableData::HrModifyRows</span></span>](itabledata-hrmodifyrows.md)
  
[<span data-ttu-id="d3500-131">SRowSet</span><span class="sxs-lookup"><span data-stu-id="d3500-131">SRowSet</span></span>](srowset.md)
  
[<span data-ttu-id="d3500-132">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="d3500-132">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="d3500-133">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d3500-133">ITableData : IUnknown</span></span>](itabledataiunknown.md)

