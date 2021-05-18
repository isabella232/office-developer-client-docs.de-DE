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
ms.openlocfilehash: 17e936093536f548d16021523d9434f09777c6d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407137"
---
# <a name="imapisessiongetstatustable"></a><span data-ttu-id="d68b8-103">IMAPISession::GetStatusTable</span><span class="sxs-lookup"><span data-stu-id="d68b8-103">IMAPISession::GetStatusTable</span></span>

  
  
<span data-ttu-id="d68b8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d68b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d68b8-105">Bietet Zugriff auf die Statustabelle, eine Tabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="d68b8-105">Provides access to the status table, a table that contains information about all the MAPI resources in the session.</span></span>
  
```cpp
HRESULT GetStatusTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="d68b8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d68b8-106">Parameters</span></span>

 <span data-ttu-id="d68b8-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d68b8-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d68b8-108">[in] Eine Bitmaske mit Flags, die das Format für Spalten bestimmt, die Zeichenzeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="d68b8-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="d68b8-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d68b8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="d68b8-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d68b8-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d68b8-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d68b8-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="d68b8-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d68b8-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="d68b8-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d68b8-113">_lppTable_</span></span>
  
> <span data-ttu-id="d68b8-114">[out] Ein Zeiger auf einen Zeiger auf die Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="d68b8-114">[out] A pointer to a pointer to the status table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d68b8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d68b8-115">Return value</span></span>

<span data-ttu-id="d68b8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="d68b8-116">S_OK</span></span> 
  
> <span data-ttu-id="d68b8-117">Die Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d68b8-117">The table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d68b8-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d68b8-118">Remarks</span></span>

<span data-ttu-id="d68b8-119">Die **IMAPISession::GetStatusTable-Methode** bietet Zugriff auf die Statustabelle, die Informationen zu allen MAPI-Ressourcen in der Sitzung enthält.</span><span class="sxs-lookup"><span data-stu-id="d68b8-119">The **IMAPISession::GetStatusTable** method provides access to the status table that contains information about all of the MAPI resources in the session.</span></span> <span data-ttu-id="d68b8-120">Die Tabelle enthält eine Zeile mit Informationen zum MAPI-Subsystem, eine Zeile für den MAPI-Spooler, eine Zeile für das integrierte Adressbuch und eine Zeile für jeden Dienstanbieter im Profil.</span><span class="sxs-lookup"><span data-stu-id="d68b8-120">There is one row in the table for information about the MAPI subsystem, one row for the MAPI spooler, one row for the integrated address book, and one row for each service provider in the profile.</span></span> 
  
<span data-ttu-id="d68b8-121">Eine vollständige Liste der erforderlichen und optionalen Spalten in der Statustabelle finden Sie unter [Status Tables](status-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d68b8-121">For a complete list of required and optional columns in the status table, see [Status Tables](status-tables.md).</span></span> 
  
<span data-ttu-id="d68b8-122">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d68b8-122">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="d68b8-123">Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird.</span><span class="sxs-lookup"><span data-stu-id="d68b8-123">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d68b8-124">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="d68b8-124">MFCMAPI reference</span></span>

<span data-ttu-id="d68b8-125">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d68b8-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d68b8-126">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d68b8-126">**File**</span></span>|<span data-ttu-id="d68b8-127">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d68b8-127">**Function**</span></span>|<span data-ttu-id="d68b8-128">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d68b8-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d68b8-129">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d68b8-129">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="d68b8-130">CMainDlg::OnStatusTable</span><span class="sxs-lookup"><span data-stu-id="d68b8-130">CMainDlg::OnStatusTable</span></span>  <br/> |<span data-ttu-id="d68b8-131">MFCMAPI verwendet die **IMAPISession::GetStatusTable-Methode,** um die Statustabelle zu erhalten, die gerendert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d68b8-131">MFCMAPI uses the **IMAPISession::GetStatusTable** method to obtain the status table to be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d68b8-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d68b8-132">See also</span></span>



[<span data-ttu-id="d68b8-133">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d68b8-133">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="d68b8-134">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="d68b8-134">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="d68b8-135">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d68b8-135">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="d68b8-136">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="d68b8-136">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="d68b8-137">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d68b8-137">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="d68b8-138">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="d68b8-138">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="d68b8-139">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d68b8-139">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="d68b8-140">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d68b8-140">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d68b8-141">Statustabellen</span><span class="sxs-lookup"><span data-stu-id="d68b8-141">Status Tables</span></span>](status-tables.md)

