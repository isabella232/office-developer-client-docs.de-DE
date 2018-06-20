---
title: ITableDataHrInsertRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrInsertRow
api_type:
- COM
ms.assetid: e5ae37ea-81a5-49c7-9ad0-0bfac518426c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 29fdbf060576ee9309473fddf8740b06229dae9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792834"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="8ab56-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="8ab56-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="8ab56-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8ab56-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8ab56-105">Eine Tabellenzeile eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8ab56-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="8ab56-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8ab56-106">Parameters</span></span>

 <span data-ttu-id="8ab56-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="8ab56-107">_uliRow_</span></span>
  
> <span data-ttu-id="8ab56-108">[in] Eine sequenzielle Zeilennummer, die eine bestimmte Zeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="8ab56-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="8ab56-109">Nach der Zeile, der die Anzahl angibt, wird die neue Zeile platziert werden.</span><span class="sxs-lookup"><span data-stu-id="8ab56-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="8ab56-110">Der Parameter _UliRow_ können Zeile Zahlen von 0 bis n enthält, wobei n ist die Gesamtzahl der Zeilen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8ab56-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="8ab56-111">Übergeben von n in _UliRow_ fügt die Zeile an das Ende der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="8ab56-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="8ab56-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="8ab56-112">_lpSRow_</span></span>
  
> <span data-ttu-id="8ab56-113">[in] Ein Zeiger auf eine [SRow](srow.md) -Struktur, die beschreibt die Zeile eingefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ab56-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8ab56-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="8ab56-114">Return value</span></span>

<span data-ttu-id="8ab56-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8ab56-115">S_OK</span></span> 
  
> <span data-ttu-id="8ab56-116">Die Zeile wurde erfolgreich eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8ab56-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="8ab56-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8ab56-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8ab56-118">Eine Zeile, die den gleichen Wert für die Indexspalte verfügt, wie die Zeile bereits eingefügt werden in der Tabelle vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="8ab56-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8ab56-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8ab56-119">Remarks</span></span>

<span data-ttu-id="8ab56-120">Die **ITableData::HrInsertRow** -Methode fügt eine Zeile in einer Tabelle an einer bestimmten Position.</span><span class="sxs-lookup"><span data-stu-id="8ab56-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="8ab56-121">Nach der Zeile, die an der Position, die durch den Parameter _UliRow_ angegeben ist, wird die neue Zeile eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8ab56-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="8ab56-122">Wenn _UliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile am Ende der Tabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="8ab56-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="8ab56-123">Die Eigenschaft, die fungiert als Index-Spalte für die Tabelle muss in der **LpProps** Mitglied der [SRow](srow.md) -Struktur, die auf das durch den Parameter _LpSRow_ enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="8ab56-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="8ab56-124">Dieser Index-Eigenschaft in der Regel **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8ab56-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="8ab56-125">Die Spalten in der Struktur **' srow '** müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="8ab56-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="8ab56-126">Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet.</span><span class="sxs-lookup"><span data-stu-id="8ab56-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="8ab56-127">Wenn die eingefügte Zeile in der Ansicht aufgrund einer Einschränkung nicht enthalten ist, wird keine Benachrichtigung gesendet.</span><span class="sxs-lookup"><span data-stu-id="8ab56-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8ab56-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ab56-128">See also</span></span>



[<span data-ttu-id="8ab56-129">' Srow '</span><span class="sxs-lookup"><span data-stu-id="8ab56-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8ab56-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8ab56-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="8ab56-131">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8ab56-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

