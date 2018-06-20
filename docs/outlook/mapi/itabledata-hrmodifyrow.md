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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: a1388545597cf0000f270bf693c93f9349fb6426
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792862"
---
# <a name="itabledatahrmodifyrow"></a><span data-ttu-id="1137c-103">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="1137c-103">ITableData::HrModifyRow</span></span>

  
  
<span data-ttu-id="1137c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="1137c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="1137c-105">Fügt eine neue Tabellenzeile, die möglicherweise eine vorhandene Zeile ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1137c-105">Inserts a new table row, possibly replacing an existing row.</span></span>
  
```cpp
HRESULT HrModifyRow(
  LPSRow lpSRow
);
```

## <a name="parameters"></a><span data-ttu-id="1137c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1137c-106">Parameters</span></span>

 <span data-ttu-id="1137c-107">_lpSRow_</span><span class="sxs-lookup"><span data-stu-id="1137c-107">_lpSRow_</span></span>
  
> <span data-ttu-id="1137c-108">[in] Ein Zeiger auf eine [SRow](srow.md) -Struktur, die Zeile hinzugefügt werden soll, oder um eine vorhandene Zeile ersetzen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="1137c-108">[in] A pointer to an [SRow](srow.md) structure that describes the row to be added or to replace an existing row.</span></span> <span data-ttu-id="1137c-109">Eine der Eigenschaft Wert Strukturen auf den die **LpProps** Member der Struktur **' srow '** sollte die Indexspalte den gleichen Wert enthalten, die in der _UlPropTagIndexColumn_ -Parameter im Aufruf der [CreateTable angegeben wurde ](createtable.md)Funktion.</span><span class="sxs-lookup"><span data-stu-id="1137c-109">One of the property value structures pointed to by the **lpProps** member of the **SRow** structure should contain the index column, the same value that was specified in the  _ulPropTagIndexColumn_ parameter in the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1137c-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="1137c-110">Return value</span></span>

<span data-ttu-id="1137c-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="1137c-111">S_OK</span></span> 
  
> <span data-ttu-id="1137c-112">Die Zeile wurde erfolgreich eingefügt oder geändert.</span><span class="sxs-lookup"><span data-stu-id="1137c-112">The row was successfully inserted or modified.</span></span>
    
<span data-ttu-id="1137c-113">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1137c-113">MAPI_E_INVALID_PARAMETER</span></span> 
  
> <span data-ttu-id="1137c-114">Die Zeile übergeben in einer Indexspalte keinen.</span><span class="sxs-lookup"><span data-stu-id="1137c-114">The passed-in row does not have an index column.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1137c-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1137c-115">Remarks</span></span>

<span data-ttu-id="1137c-116">Die **ITableData::HrModifyRow** -Methode fügt die Zeile mit der **SRow** -Struktur, die auf das durch den Parameter _LpSRow_ beschrieben.</span><span class="sxs-lookup"><span data-stu-id="1137c-116">The **ITableData::HrModifyRow** method inserts the row described by the **SRow** structure pointed to by the  _lpSRow_ parameter.</span></span> <span data-ttu-id="1137c-117">Wenn eine Zeile, die den gleichen Wert für die Indexspalte der Zeile, _LpSRow_ verweist, in der Tabelle bereits vorhanden ist, wird die vorhandene Zeile ersetzt.</span><span class="sxs-lookup"><span data-stu-id="1137c-117">If a row that has the same value for its index column as the row that  _lpSRow_ points to already exists in the table, the existing row is replaced.</span></span> <span data-ttu-id="1137c-118">Wenn keine Zeile vorhanden, die in der Struktur **SRow** enthaltene übereinstimmt ist, fügt **HrModifyRow** die Zeile an das Ende der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="1137c-118">If no row exists that matches the one included in the **SRow** structure, **HrModifyRow** adds the row to the end of the table.</span></span> 
  
<span data-ttu-id="1137c-119">Alle Ansichten für die Tabelle werden geändert, um die Zeile, die auf den _LpSRow_einschließen.</span><span class="sxs-lookup"><span data-stu-id="1137c-119">All views of the table are modified to include the row pointed to by  _lpSRow_.</span></span> <span data-ttu-id="1137c-120">Jedoch, wenn eine Ansicht eine Einschränkung eingerichtet, die die Zeile ausschließt hat, es für den Benutzer sichtbar möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="1137c-120">However, if a view has a restriction in place that excludes the row, it may not be visible to the user.</span></span> 
  
<span data-ttu-id="1137c-121">Die Spalten in der Zeile, die auf den _LpSRow_ müssen nicht in derselben Reihenfolge wie die Spalten in der Tabelle werden.</span><span class="sxs-lookup"><span data-stu-id="1137c-121">The columns in the row pointed to by  _lpSRow_ do not have to be in the same order as the columns in the table.</span></span> <span data-ttu-id="1137c-122">Der Aufrufer kann auch als Spalteneigenschaften enthalten, die derzeit nicht in der Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="1137c-122">The caller can also include as columns properties that are not currently in the table.</span></span> <span data-ttu-id="1137c-123">Für vorhandene Ansichten **HrModifyRow** diesen neuen Spalten zur Verfügung umfasst aber nicht sie in der aktuellen Spalte Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1137c-123">For existing views, **HrModifyRow** makes these new columns available but does not include them in the current column set.</span></span> <span data-ttu-id="1137c-124">Für zukünftige Ansichten enthält **HrModifyRow** die neuen Spalten in der Spalte festlegen.</span><span class="sxs-lookup"><span data-stu-id="1137c-124">For future views, **HrModifyRow** includes the new columns in the column set.</span></span> 
  
<span data-ttu-id="1137c-125">Nachdem **HrModifyRow** die Zeile hinzugefügt hat, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet.</span><span class="sxs-lookup"><span data-stu-id="1137c-125">After **HrModifyRow** adds the row, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1137c-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1137c-126">See also</span></span>



[<span data-ttu-id="1137c-127">' Srow '</span><span class="sxs-lookup"><span data-stu-id="1137c-127">SRow</span></span>](srow.md)
  
[<span data-ttu-id="1137c-128">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="1137c-128">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="1137c-129">ITableData: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1137c-129">ITableData : IUnknown</span></span>](itabledataiunknown.md)

