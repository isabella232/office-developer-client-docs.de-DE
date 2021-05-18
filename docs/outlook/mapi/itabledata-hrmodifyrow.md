---
title: ITableDataHrModifyRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrModifyRow
api_type:
- COM
ms.assetid: 9e255b3e-dd17-4528-ba4e-c3a1aef32b04
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44ecf095ad24dd266dc5f603ace9c7b9f21c1b41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408999"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="07fcc-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="07fcc-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="07fcc-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="07fcc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="07fcc-105">Fügt eine neue Tabellenzeile ein und ersetzt möglicherweise eine vorhandene Zeile.</span><span class="sxs-lookup"><span data-stu-id="07fcc-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="07fcc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07fcc-106">Parameters</span></span>

 <span data-ttu-id="07fcc-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="07fcc-107">_lpSRow_</span></span>
  
> <span data-ttu-id="07fcc-108">[in] Ein Zeiger auf eine [SRow-Struktur,](srow.md) in der die zu hinzufügende Zeile oder das Ersetzen einer vorhandenen Zeile beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="07fcc-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="07fcc-109">Eine der Eigenschaftenwertstrukturen, auf die das **lpProps-Element** der **SRow-Struktur** verweist, sollte die Indexspalte enthalten, denselben Wert, der im  _ulPropTagIndexColumn-Parameter_ im Aufruf der [CreateTable-Funktion](createtable.md) angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="07fcc-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="07fcc-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07fcc-110">Return value</span></span>

<span data-ttu-id="07fcc-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="07fcc-111">S_OK</span></span> 
  
> <span data-ttu-id="07fcc-112">Die Zeile wurde erfolgreich eingefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="07fcc-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="07fcc-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="07fcc-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="07fcc-114">Die übergebene Zeile verfügt nicht über eine Indexspalte.</span><span class="sxs-lookup"><span data-stu-id="07fcc-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07fcc-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="07fcc-115">Remarks</span></span>

<span data-ttu-id="07fcc-116">Die **ITableData::HrModifyRow-Methode** fügt die durch die **SRow-Struktur** beschriebene Zeile ein, auf die der  _lpSRow-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="07fcc-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="07fcc-117">Wenn eine Zeile mit demselben Wert für die Indexspalte wie die Zeile, auf die  _lpSRow_ verweist, bereits in der Tabelle vorhanden ist, wird die vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="07fcc-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="07fcc-118">Wenn keine Zeile vorhanden ist, die mit der in der **SRow-Struktur** enthaltenen Zeile entspricht, fügt **HrModifyRow** die Zeile am Ende der Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="07fcc-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="07fcc-119">Alle Ansichten der Tabelle werden so geändert, dass sie die Zeile enthält, auf die _von lpSRow verwiesen wird._</span><span class="sxs-lookup"><span data-stu-id="07fcc-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="07fcc-120">Wenn eine Ansicht jedoch über eine Einschränkung verfügt, die die Zeile ausschließt, ist sie möglicherweise nicht für den Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="07fcc-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="07fcc-121">Die Spalten in der Zeile, auf die  _lpSRow_ verweist, müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle sein.</span><span class="sxs-lookup"><span data-stu-id="07fcc-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="07fcc-122">Der Aufrufer kann auch Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="07fcc-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="07fcc-123">Für vorhandene Ansichten **stellt HrModifyRow** diese neuen Spalten zur Verfügung, schließt sie jedoch nicht in den aktuellen Spaltensatz ein.</span><span class="sxs-lookup"><span data-stu-id="07fcc-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="07fcc-124">Für zukünftige Ansichten **enthält HrModifyRow** die neuen Spalten im Spaltensatz.</span><span class="sxs-lookup"><span data-stu-id="07fcc-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="07fcc-125">Nachdem **HrModifyRow** die Zeile hinzufügt, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Ansicht der Tabelle verfügen und die die [IMAPITable::Advise-Methode](imapitable-advise.md) der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="07fcc-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="07fcc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="07fcc-126">See also</span></span>



[<span data-ttu-id="07fcc-127">SRow</span><span class="sxs-lookup"><span data-stu-id="07fcc-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="07fcc-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="07fcc-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="07fcc-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="07fcc-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

