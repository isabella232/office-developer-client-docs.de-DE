---
title: ITableDataHrDeleteRow
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrDeleteRow
api_type:
- COM
ms.assetid: 670c2291-d5b6-4dcf-9046-9125272dd8f8
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 37d0ce65e125b2420af775d61ead51db189758ca
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792839"
---
# <a name="itabledatahrdeleterow"></a><span data-ttu-id="42b28-103">ITableData::HrDeleteRow</span><span class="sxs-lookup"><span data-stu-id="42b28-103">ITableData::HrDeleteRow</span></span>

  
  
<span data-ttu-id="42b28-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="42b28-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="42b28-105">Löscht eine Tabellenzeile.</span><span class="sxs-lookup"><span data-stu-id="42b28-105">Deletes a table row.</span></span>
  
```cpp
HRESULT HrDeleteRow(
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="42b28-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="42b28-106">Parameters</span></span>

 <span data-ttu-id="42b28-107">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="42b28-107">_lpSPropValue_</span></span>
  
> <span data-ttu-id="42b28-108">[in] Ein Zeiger auf eine Eigenschaft-Wert-Struktur, die beschreibt die Indexspalte für die Zeile gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="42b28-108">[in] A pointer to a property value structure that describes the index column for the row to be deleted.</span></span> <span data-ttu-id="42b28-109">Der **UlPropTag** Member der Eigenschaft Wert Struktur sollte das gleiche Eigenschafts-Tag als _UlPropTagIndexColumn_ -Parameter aus dem Aufruf der Funktion [CreateTable](createtable.md) enthalten.</span><span class="sxs-lookup"><span data-stu-id="42b28-109">The **ulPropTag** member of the property value structure should contain the same property tag as the  _ulPropTagIndexColumn_ parameter from the call to the [CreateTable](createtable.md) function.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="42b28-110">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="42b28-110">Return value</span></span>

<span data-ttu-id="42b28-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="42b28-111">S_OK</span></span> 
  
> <span data-ttu-id="42b28-112">Die Zeile wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="42b28-112">The row was successfully deleted.</span></span>
    
<span data-ttu-id="42b28-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="42b28-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="42b28-114">Die-Eigenschaft auf das durch den Parameter _LpSPropValue_ wird eine Zeile in der Tabelle nicht identifiziert.</span><span class="sxs-lookup"><span data-stu-id="42b28-114">The property pointed to by the  _lpSPropValue_ parameter does not identify a row in the table.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42b28-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="42b28-115">Remarks</span></span>

<span data-ttu-id="42b28-116">Die **ITableData::HrDeleteRow** -Methode entfernt Tabellenzeile, die die Spalte enthält, die-Eigenschaft auf das durch den Parameter _LpSPropValue_ übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="42b28-116">The **ITableData::HrDeleteRow** method removes the table row that contains the column that matches the property pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="42b28-117">Die Daten für die Zeile werden gelöscht, und die Zeile aus alle geöffneten Ansichten entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="42b28-117">The data for the row is deleted and the row is removed from all open views.</span></span> 
  
<span data-ttu-id="42b28-118">Nachdem die Zeile gelöscht wurde, werden Benachrichtigungen an alle Clients oder Dienstanbieter, die eine Ansicht der Tabelle und aufgerufen, die die Tabelle [IMAPITable::Advise](imapitable-advise.md) -Methode zum Registrieren für Benachrichtigungen, gesendet.</span><span class="sxs-lookup"><span data-stu-id="42b28-118">After the row is deleted, notifications are sent to all clients or service providers that have a view of the table and that have called the table's [IMAPITable::Advise](imapitable-advise.md) method to register for notifications.</span></span> 
  
<span data-ttu-id="42b28-119">Löschen einer Zeile wird nicht reduziert die Spalte festlegen, die verfügbar ist, vorhandene Ansichten oder Ansichten, anschließend geöffnet, auch wenn die gelöschte Zeile die letzte Zeile ist, die einen Wert für eine bestimmte Spalte verfügt.</span><span class="sxs-lookup"><span data-stu-id="42b28-119">Deleting a row does not reduce the column set that is available to existing views or subsequently opened views, even if the deleted row is the last row that has a value for a specific column.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="42b28-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42b28-120">See also</span></span>



[<span data-ttu-id="42b28-121">CreateTable</span><span class="sxs-lookup"><span data-stu-id="42b28-121">CreateTable</span></span>](createtable.md)
  
[<span data-ttu-id="42b28-122">ITableData::HrDeleteRows</span><span class="sxs-lookup"><span data-stu-id="42b28-122">ITableData::HrDeleteRows</span></span>](itabledata-hrdeleterows.md)
  
[<span data-ttu-id="42b28-123">ITableData::HrModifyRow</span><span class="sxs-lookup"><span data-stu-id="42b28-123">ITableData::HrModifyRow</span></span>](itabledata-hrmodifyrow.md)
  
[<span data-ttu-id="42b28-124">SPropValue</span><span class="sxs-lookup"><span data-stu-id="42b28-124">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="42b28-125">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="42b28-125">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="42b28-126">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="42b28-126">ITableData : IUnknown</span></span>](itabledataiunknown.md)

