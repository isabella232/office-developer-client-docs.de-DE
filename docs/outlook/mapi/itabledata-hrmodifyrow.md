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
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="28d52-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="28d52-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="28d52-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="28d52-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="28d52-105">Fügt eine neue Tabellenzeile ein, die möglicherweise eine vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="28d52-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="28d52-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="28d52-106">Parameters</span></span>

 <span data-ttu-id="28d52-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="28d52-107">_lpSRow_</span></span>
  
> <span data-ttu-id="28d52-108">in Ein Zeiger auf eine [SRow](srow.md) -Struktur, die die hinzuzufügende Zeile beschreibt oder eine vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="28d52-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="28d52-109">Eine der Eigenschaftswert Strukturen, auf die durch das **lpProps** -Element der **SRow** -Struktur verwiesen wird, sollte die Index-Spalte enthalten, den gleichen Wert, der im _ulPropTagIndexColumn_ -Parameter im Aufruf der Create-Basis angegeben wurde. [ ](createtable.md)-Funktion.</span><span class="sxs-lookup"><span data-stu-id="28d52-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="28d52-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="28d52-110">Return value</span></span>

<span data-ttu-id="28d52-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="28d52-111">S_OK</span></span> 
  
> <span data-ttu-id="28d52-112">Die Zeile wurde erfolgreich eingefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="28d52-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="28d52-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="28d52-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="28d52-114">Die übergebene Zeile hat keine Indexspalte.</span><span class="sxs-lookup"><span data-stu-id="28d52-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="28d52-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28d52-115">Remarks</span></span>

<span data-ttu-id="28d52-116">Die **ITableData:: HrModifyRow** -Methode fügt die durch die **SRow** -Struktur beschriebene Zeile ein, auf die durch den _lpSRow_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="28d52-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="28d52-117">Wenn eine Zeile, die den gleichen Wert für die Indexspalte hat, wie die Zeile, auf die _lpSRow_ verweist, in der Tabelle bereits vorhanden ist, wird die vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="28d52-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="28d52-118">Wenn keine Zeile vorhanden ist, die mit der in der **SRow** -Struktur übereinstimmt, fügt **HrModifyRow** die Zeile am Ende der Tabelle hinzu.</span><span class="sxs-lookup"><span data-stu-id="28d52-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="28d52-119">Alle Ansichten der Tabelle werden so geändert, dass Sie die Zeile einbeziehen, auf die von _lpSRow_verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="28d52-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="28d52-120">Wenn in einer Ansicht jedoch eine Einschränkung vorhanden ist, die die Zeile ausschließt, ist Sie möglicherweise nicht für den Benutzer sichtbar.</span><span class="sxs-lookup"><span data-stu-id="28d52-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="28d52-121">Die Spalten in der Zeile, auf die durch _lpSRow_ verwiesen wird, müssen sich nicht in derselben Reihenfolge wie die Spalten in der Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="28d52-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="28d52-122">Der Aufrufer kann auch als Spalteneigenschaften enthalten, die sich derzeit nicht in der Tabelle befinden.</span><span class="sxs-lookup"><span data-stu-id="28d52-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="28d52-123">Bei vorhandenen Ansichten stellt **HrModifyRow** diese neuen Spalten zur Verfügung, diese werden jedoch nicht in den aktuellen Spaltensatz aufgenommen.</span><span class="sxs-lookup"><span data-stu-id="28d52-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="28d52-124">Für zukünftige Ansichten enthält **HrModifyRow** die neuen Spalten in den Spaltensatz.</span><span class="sxs-lookup"><span data-stu-id="28d52-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="28d52-125">Nachdem **HrModifyRow** die Zeile hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter gesendet, die über eine Tabellenansicht verfügen und die [IMAPITable:: Advise](imapitable-advise.md) -Methode der Tabelle aufgerufen haben, um sich für Benachrichtigungen zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="28d52-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="28d52-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28d52-126">See also</span></span>



[<span data-ttu-id="28d52-127">SRow</span><span class="sxs-lookup"><span data-stu-id="28d52-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="28d52-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="28d52-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="28d52-129">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="28d52-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

