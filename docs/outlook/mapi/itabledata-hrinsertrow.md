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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435439"
---
# <a name="itabledatahrinsertrow"></a><span data-ttu-id="8b845-103">ITableData::HrInsertRow</span><span class="sxs-lookup"><span data-stu-id="8b845-103">ITableData::HrInsertRow</span></span>

  
  
<span data-ttu-id="8b845-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8b845-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8b845-105">Fügt eine Tabellenzeile ein.</span><span class="sxs-lookup"><span data-stu-id="8b845-105">Inserts a table row.</span></span> 
  
```cpp
HRESULT HrInsertRow(
  ULONG uliRow,
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="8b845-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b845-106">Parameters</span></span>

 <span data-ttu-id="8b845-107">_uliRow_</span><span class="sxs-lookup"><span data-stu-id="8b845-107">_uliRow_</span></span>
  
> <span data-ttu-id="8b845-108">[in] Eine sequenzielle Zeilennummer, die eine bestimmte Zeile darstellt.</span><span class="sxs-lookup"><span data-stu-id="8b845-108">[in] A sequential row number that represents a specific row.</span></span> <span data-ttu-id="8b845-109">Die neue Zeile wird hinter der Zeile platziert, die die Zahl angibt.</span><span class="sxs-lookup"><span data-stu-id="8b845-109">The new row will be placed after the row that the number indicates.</span></span> <span data-ttu-id="8b845-110">Der  _Parameter uliRow_ kann Zeilennummern von 0 bis n enthalten, wobei n die Gesamtanzahl der Zeilen in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="8b845-110">The  _uliRow_ parameter can contains row numbers from 0 through n, where n is the total number of rows in the table.</span></span> <span data-ttu-id="8b845-111">Durch Übergeben von n in  _uliRow_ wird die Zeile am Ende der Tabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="8b845-111">Passing n in  _uliRow_ appends the row to the end of the table.</span></span> 
    
 <span data-ttu-id="8b845-112">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="8b845-112">_lpSRow_</span></span>
  
> <span data-ttu-id="8b845-113">[in] Ein Zeiger auf eine [SRow-Struktur,](srow.md) die die eingefügte Zeile beschreibt.</span><span class="sxs-lookup"><span data-stu-id="8b845-113">[in] A pointer to an [SRow](srow.md) structure that describes the row to be inserted.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8b845-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b845-114">Return value</span></span>

<span data-ttu-id="8b845-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="8b845-115">S_OK</span></span> 
  
> <span data-ttu-id="8b845-116">Die Zeile wurde erfolgreich eingefügt.</span><span class="sxs-lookup"><span data-stu-id="8b845-116">The row was successfully inserted.</span></span>
    
<span data-ttu-id="8b845-117">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8b845-117">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="8b845-118">Eine Zeile mit demselben Wert für die Indexspalte wie die zu einfügende Zeile ist bereits in der Tabelle vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8b845-118">A row that has the same value for its index column as the row to be inserted already exists in the table.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8b845-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b845-119">Remarks</span></span>

<span data-ttu-id="8b845-120">Die **ITableData::HrInsertRow-Methode** fügt eine Zeile in eine Tabelle an einer bestimmten Position ein.</span><span class="sxs-lookup"><span data-stu-id="8b845-120">The **ITableData::HrInsertRow** method inserts a row into a table at a particular position.</span></span> <span data-ttu-id="8b845-121">Die neue Zeile wird nach der Zeile eingefügt, die sich an der durch den  _Parameter uliRow angegebenen Position_ befindet.</span><span class="sxs-lookup"><span data-stu-id="8b845-121">The new row is inserted after the row that is in the position specified by the  _uliRow_ parameter.</span></span> 
  
<span data-ttu-id="8b845-122">Wenn  _uliRow_ auf die Anzahl der Zeilen in der Tabelle festgelegt ist, wird die neue Zeile am Ende der Tabelle angefügt.</span><span class="sxs-lookup"><span data-stu-id="8b845-122">If  _uliRow_ is set to the number of rows in the table, the new row is appended to the end of the table.</span></span> 
  
<span data-ttu-id="8b845-123">Die Eigenschaft, die als Indexspalte für die Tabelle fungiert, muss im **lpProps-Element** der [SRow-Struktur](srow.md) enthalten sein, auf die der  _lpSRow-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="8b845-123">The property that acts as the index column for the table must be included in the **lpProps** member of the [SRow](srow.md) structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="8b845-124">Diese Indexeigenschaft, normalerweise **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), wird verwendet, um die Zeile für zukünftige Wartungsaufgaben eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8b845-124">This index property, typically **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)), is used to uniquely identify the row for future maintenance tasks.</span></span>
  
<span data-ttu-id="8b845-125">Die Eigenschaftenspalten in der **SRow-Struktur** müssen nicht in derselben Reihenfolge wie die Eigenschaftenspalten in der Tabelle liegen.</span><span class="sxs-lookup"><span data-stu-id="8b845-125">The property columns in the **SRow** structure do not have to be in the same order as the property columns in the table.</span></span> 
  
<span data-ttu-id="8b845-126">Nachdem die Zeile eingefügt wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="8b845-126">After the row is inserted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> <span data-ttu-id="8b845-127">Es wird keine Benachrichtigung gesendet, wenn die eingefügte Zeile aufgrund einer Einschränkung nicht in der Ansicht enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="8b845-127">No notification is sent if the inserted row is not included in the view due to a restriction.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b845-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b845-128">See also</span></span>



[<span data-ttu-id="8b845-129">SRow</span><span class="sxs-lookup"><span data-stu-id="8b845-129">SRow</span></span>](srow.md)
  
[<span data-ttu-id="8b845-130">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="8b845-130">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="8b845-131">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b845-131">ITableData : IUnknown</span></span>](itabledataiunknown.md)

