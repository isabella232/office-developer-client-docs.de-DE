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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2709ac612fc9e2edaa57b280d52c0a5229ee9978
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278806"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="75e45-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="75e45-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="75e45-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="75e45-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="75e45-105">Fügt eine Tabellenzeile ein.</span><span class="sxs-lookup"><span data-stu-id="75e45-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="75e45-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="75e45-106">Parameters</span></span>

 <span data-ttu-id="75e45-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="75e45-107">_uliRow_</span></span>
  
> <span data-ttu-id="75e45-108">in Eine sequenzielle Zeilennummer, die eine bestimmte Zeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="75e45-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="75e45-109">Die neue Zeile wird nach der Zeile, die die Zahl angibt.</span><span class="sxs-lookup"><span data-stu-id="75e45-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="75e45-110">Der _uliRow_ -Parameter kann Zeilenzahlen von 0 bis n enthalten, wobei n die Gesamtanzahl der Zeilen in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="75e45-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="75e45-111">Beim Übergeben von n in _uliRow_ wird die Zeile am Ende der Tabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="75e45-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="75e45-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="75e45-112">_lpSRow_</span></span>
  
> <span data-ttu-id="75e45-113">in Ein Zeiger auf eine [SRow](srow.md) -Struktur, die die einzufügende Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="75e45-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="75e45-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75e45-114">Return value</span></span>

<span data-ttu-id="75e45-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="75e45-115">S_OK</span></span> 
  
> <span data-ttu-id="75e45-116">Die Zeile wurde erfolgreich eingefügt.</span><span class="sxs-lookup"><span data-stu-id="75e45-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="75e45-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="75e45-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="75e45-118">Eine Zeile, die den gleichen Wert für die Indexspalte hat wie die einzufügende Zeile, ist bereits in der Tabelle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="75e45-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="75e45-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75e45-119">Remarks</span></span>

<span data-ttu-id="75e45-120">Die **ITableData:: HrInsertRow** -Methode fügt eine Zeile an einer bestimmten Position in eine Tabelle ein.</span><span class="sxs-lookup"><span data-stu-id="75e45-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="75e45-121">Die neue Zeile wird nach der Zeile eingefügt, die sich in der durch den _uliRow_ -Parameter angegebenen Position befindet.</span><span class="sxs-lookup"><span data-stu-id="75e45-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="75e45-122">Wenn _uliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile am Ende der Tabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="75e45-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="75e45-123">Die Eigenschaft, die als Indexspalte für die Tabelle fungiert, muss im **lpProps** -Element der [SRow](srow.md) -Struktur enthalten sein, auf die durch den _lpSRow_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="75e45-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="75e45-124">Diese Index Eigenschaft, normalerweise **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md)), wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="75e45-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="75e45-125">Die Eigenschaftenspalten in der **SRow** -Struktur müssen nicht in der gleichen Reihenfolge wie die Eigenschaftenspalten in der Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="75e45-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="75e45-126">Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="75e45-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="75e45-127">Es wird keine Benachrichtigung gesendet, wenn die eingefügte Zeile aufgrund einer Einschränkung nicht in der Ansicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="75e45-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="75e45-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75e45-128">See also</span></span>



[<span data-ttu-id="75e45-129">SRow</span><span class="sxs-lookup"><span data-stu-id="75e45-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="75e45-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="75e45-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="75e45-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="75e45-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

