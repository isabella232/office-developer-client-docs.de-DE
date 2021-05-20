---
title: IMAPISessionGetMsgStoresTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.GetMsgStoresTable
api_type:
- COM
ms.assetid: 77db2dff-4534-440f-a05c-635711cbc2c3
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 5fced633023ebf00efaf5b667dc7994eeb5de316
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428137"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="78011-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="78011-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="78011-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="78011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="78011-105">Bietet Zugriff auf die Nachrichtenspeichertabelle, die Informationen zu allen Nachrichtenspeichern im Sitzungsprofil enthält.</span><span class="sxs-lookup"><span data-stu-id="78011-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="78011-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="78011-106">Parameters</span></span>

 <span data-ttu-id="78011-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="78011-107">_ulFlags_</span></span>
  
> <span data-ttu-id="78011-108">[in] Eine Bitmaske mit Flags, die das Format für Spalten bestimmt, die Zeichenzeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="78011-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="78011-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="78011-109">The following flag can be set:</span></span>
    
<span data-ttu-id="78011-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="78011-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="78011-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="78011-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="78011-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="78011-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="78011-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="78011-113">_lppTable_</span></span>
  
> <span data-ttu-id="78011-114">[out] Ein Zeiger auf einen Zeiger auf die Nachrichtenspeichertabelle.</span><span class="sxs-lookup"><span data-stu-id="78011-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="78011-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="78011-115">Return value</span></span>

<span data-ttu-id="78011-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="78011-116">S_OK</span></span> 
  
> <span data-ttu-id="78011-117">Die Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="78011-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="78011-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="78011-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="78011-119">Das MAPI_UNICODE wurde festgelegt, und die Sitzung unterstützt Unicode nicht.</span><span class="sxs-lookup"><span data-stu-id="78011-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="78011-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78011-120">Remarks</span></span>

<span data-ttu-id="78011-121">Die **IMAPISession::GetMsgStoresTable-Methode** ruft einen Zeiger auf die Nachrichtenspeichertabelle ab, eine von MAPI verwaltete Tabelle, die Informationen zu jedem geöffneten Nachrichtenspeicher im Profil enthält.</span><span class="sxs-lookup"><span data-stu-id="78011-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="78011-122">Eine vollständige Liste der erforderlichen und optionalen Spalten in der Nachrichtenspeichertabelle finden Sie unter [Message Store Tables](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="78011-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="78011-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="78011-123">Notes to callers</span></span>

<span data-ttu-id="78011-124">Da MAPI die Nachrichtenspeichertabelle während der Sitzung aktualisiert, wenn Änderungen auftreten, rufen Sie die **Advise-Methode** der Nachrichtenspeichertabelle auf, um sich zu registrieren, um über diese Änderungen benachrichtigt zu werden.</span><span class="sxs-lookup"><span data-stu-id="78011-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="78011-125">Mögliche Änderungen sind das Hinzu- und Entfernen von neuen Nachrichtenspeichern, das Entfernen vorhandener Speicher und Änderungen am Standardspeicher.</span><span class="sxs-lookup"><span data-stu-id="78011-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="78011-126">Das Festlegen MAPI_UNICODE im  _ulFlags-Parameter_ wirkt sich auf das Format der Spalten aus, die von den [Methoden IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="78011-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="78011-127">Dieses Flag steuert auch die Eigenschaftstypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder-Methode zurückgegeben](imapitable-querysortorder.md) wird.</span><span class="sxs-lookup"><span data-stu-id="78011-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="78011-128">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="78011-128">MFCMAPI reference</span></span>

<span data-ttu-id="78011-129">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="78011-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="78011-130">**Datei**</span><span class="sxs-lookup"><span data-stu-id="78011-130">**File**</span></span>|<span data-ttu-id="78011-131">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="78011-131">**Function**</span></span>|<span data-ttu-id="78011-132">**Comment**</span><span class="sxs-lookup"><span data-stu-id="78011-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="78011-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="78011-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="78011-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="78011-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="78011-135">MFCMAPI verwendet die **IMAPISession::GetMsgStoresTable-Methode,** um die Nachrichtenspeichertabelle zu erhalten, sodass sie im Hauptdialogfeld von MFCMAPI gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="78011-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78011-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78011-136">See also</span></span>



[<span data-ttu-id="78011-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="78011-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="78011-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78011-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="78011-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="78011-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="78011-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="78011-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="78011-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="78011-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="78011-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="78011-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="78011-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="78011-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="78011-144">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="78011-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="78011-145">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="78011-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="78011-146">Nachrichten Store Tabellen</span><span class="sxs-lookup"><span data-stu-id="78011-146">Message Store Tables</span></span>](message-store-tables.md)

