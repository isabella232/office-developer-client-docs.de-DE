---
title: IMAPISessionGetStatusTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetStatusTable
api_type:
- COM
ms.assetid: 53428f8d-4838-46d1-a0ab-cafb194f4cc3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 48a69fa49735014dcbfffad0673f1d4da62452e7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594831"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="50598-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="50598-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="50598-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="50598-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="50598-105">Bietet Zugriff auf die Statustabelle, einer Tabelle, Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="50598-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="50598-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="50598-106">Parameters</span></span>

 <span data-ttu-id="50598-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="50598-107">_ulFlags_</span></span>
  
> <span data-ttu-id="50598-108">[in] Eine Bitmaske aus Flags, die bestimmt das Format für Spalten, die Zeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="50598-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="50598-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="50598-109">The following flag can be set:</span></span>
    
<span data-ttu-id="50598-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="50598-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="50598-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="50598-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="50598-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="50598-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="50598-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="50598-113">_lppTable_</span></span>
  
> <span data-ttu-id="50598-114">[out] Ein Zeiger auf einen Zeiger auf die Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="50598-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50598-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="50598-115">Return value</span></span>

<span data-ttu-id="50598-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="50598-116">S_OK</span></span> 
  
> <span data-ttu-id="50598-117">Die Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50598-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50598-118">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="50598-118">Remarks</span></span>

<span data-ttu-id="50598-119">Die **IMAPISession::GetStatusTable** -Methode ermöglicht den Zugriff auf die Statustabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="50598-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="50598-120">Es wird eine Zeile in der Tabelle Informationen zu MAPI-Subsystems, eine Zeile für die MAPI-Warteschlange, eine Zeile für die integrierte Adressbuch und eine Zeile für jeden Anbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="50598-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="50598-121">Eine vollständige Liste der erforderlichen und optionalen Spalten in der Tabelle "Status" finden Sie unter [Statustabellen](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="50598-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="50598-122">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus.</span><span class="sxs-lookup"><span data-stu-id="50598-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="50598-123">Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="50598-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="50598-124">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="50598-124">MFCMAPI reference</span></span>

<span data-ttu-id="50598-125">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="50598-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="50598-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="50598-126">**File**</span></span>|<span data-ttu-id="50598-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="50598-127">**Function**</span></span>|<span data-ttu-id="50598-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="50598-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="50598-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="50598-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="50598-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="50598-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="50598-131">MFCMAPI (engl.) verwendet die **IMAPISession::GetStatusTable** -Methode, um die Statustabelle zu rendernden abzurufen.</span><span class="sxs-lookup"><span data-stu-id="50598-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="50598-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50598-132">See also</span></span>



[<span data-ttu-id="50598-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="50598-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="50598-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="50598-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="50598-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="50598-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="50598-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="50598-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="50598-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="50598-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="50598-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="50598-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="50598-139">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="50598-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="50598-140">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="50598-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="50598-141">Statustabellen</span><span class="sxs-lookup"><span data-stu-id="50598-141">Status Tables</span></span>](status-tables.md)

