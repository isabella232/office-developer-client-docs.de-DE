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
ms.openlocfilehash: cc0039cf2210446704d25b2156bd4ff50041a524
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586277"
---
# <a name="imapisessiongetmsgstorestable"></a><span data-ttu-id="206e2-103">IMAPISession::GetMsgStoresTable</span><span class="sxs-lookup"><span data-stu-id="206e2-103">IMAPISession::GetMsgStoresTable</span></span>

  
  
<span data-ttu-id="206e2-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="206e2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="206e2-105">Bietet Zugriff auf die Nachricht Store Tabelle mit Informationen zu allen Nachrichtenspeichern im Profil der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="206e2-105">Provides access to the message store table that contains information about all the message stores in the session profile.</span></span>
  
```cpp
HRESULT GetMsgStoresTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="206e2-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="206e2-106">Parameters</span></span>

 <span data-ttu-id="206e2-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="206e2-107">_ulFlags_</span></span>
  
> <span data-ttu-id="206e2-108">[in] Eine Bitmaske aus Flags, die bestimmt das Format für Spalten, die Zeichenfolgen sind.</span><span class="sxs-lookup"><span data-stu-id="206e2-108">[in] A bitmask of flags that determines the format for columns that are character strings.</span></span> <span data-ttu-id="206e2-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="206e2-109">The following flag can be set:</span></span>
    
<span data-ttu-id="206e2-110">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="206e2-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="206e2-111">Die Zeichenfolgenspalten sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="206e2-111">The string columns are in Unicode format.</span></span> <span data-ttu-id="206e2-112">Wenn die Option MAPI_UNICODE nicht festgelegt ist, werden die Zeichenfolgenspalten im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="206e2-112">If the MAPI_UNICODE flag is not set, the string columns are in ANSI format.</span></span>
    
 <span data-ttu-id="206e2-113">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="206e2-113">_lppTable_</span></span>
  
> <span data-ttu-id="206e2-114">[out] Ein Zeiger auf einen Zeiger auf die Nachricht Store-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="206e2-114">[out] A pointer to a pointer to the message store table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="206e2-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="206e2-115">Return value</span></span>

<span data-ttu-id="206e2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="206e2-116">S_OK</span></span> 
  
> <span data-ttu-id="206e2-117">Die Tabelle wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="206e2-117">The table was successfully returned.</span></span>
    
<span data-ttu-id="206e2-118">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="206e2-118">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="206e2-119">Die Option MAPI_UNICODE wurde festgelegt, und die Sitzung Unicode nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="206e2-119">The MAPI_UNICODE flag was set and the session does not support Unicode.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="206e2-120">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="206e2-120">Remarks</span></span>

<span data-ttu-id="206e2-121">Die **IMAPISession::GetMsgStoresTable** -Methode ruft einen Zeiger auf die Nachricht Store-Tabelle, eine Tabelle von MAPI verwaltet wird, enthält Informationen zu jeder geöffneten Nachrichtenspeicher im Profil.</span><span class="sxs-lookup"><span data-stu-id="206e2-121">The **IMAPISession::GetMsgStoresTable** method retrieves a pointer to the message store table, a table maintained by MAPI that contains information about each open message store in the profile.</span></span> 
  
<span data-ttu-id="206e2-122">Speichern Sie eine vollständige Liste der erforderlichen und optionalen Spalten in der Nachricht Tabelle, finden Sie unter [Nachricht speichern Tabellen](message-store-tables.md).</span><span class="sxs-lookup"><span data-stu-id="206e2-122">For a complete list of required and optional columns in the message store table, see [Message Store Tables](message-store-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="206e2-123">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="206e2-123">Notes to callers</span></span>

<span data-ttu-id="206e2-124">Da MAPI die Tabelle Store während der Sitzung aktualisiert immer Änderungen auftreten, rufen Sie die **Advise** -Methode der Nachricht Store Tabelle registrieren, um diese Änderungen benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="206e2-124">Because MAPI updates the message store table during the session whenever changes occur, call the **Advise** method of the message store table to register to be notified of these changes.</span></span> <span data-ttu-id="206e2-125">Mögliche Änderungen zählen das Hinzufügen von neuen Nachrichtenspeicher, Entfernen vorhandener speichert und in der Standard-Informationsspeichers geändert.</span><span class="sxs-lookup"><span data-stu-id="206e2-125">Possible changes include the addition of new message stores, removal of existing stores, and changes to the default store.</span></span> 
  
<span data-ttu-id="206e2-126">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus.</span><span class="sxs-lookup"><span data-stu-id="206e2-126">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="206e2-127">Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="206e2-127">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="206e2-128">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="206e2-128">MFCMAPI reference</span></span>

<span data-ttu-id="206e2-129">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="206e2-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="206e2-130">**Datei**</span><span class="sxs-lookup"><span data-stu-id="206e2-130">**File**</span></span>|<span data-ttu-id="206e2-131">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="206e2-131">**Function**</span></span>|<span data-ttu-id="206e2-132">**Comment**</span><span class="sxs-lookup"><span data-stu-id="206e2-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="206e2-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="206e2-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="206e2-134">CMainDlg::OnOpenMessageStoreTable</span><span class="sxs-lookup"><span data-stu-id="206e2-134">CMainDlg::OnOpenMessageStoreTable</span></span>  <br/> |<span data-ttu-id="206e2-135">MFCMAPI (engl.) verwendet die **IMAPISession::GetMsgStoresTable** -Methode, um die Nachricht Store-Tabelle zu erhalten, damit es im Hauptdialogfeld von MFCMAPI (engl.) gerendert werden kann.</span><span class="sxs-lookup"><span data-stu-id="206e2-135">MFCMAPI uses the **IMAPISession::GetMsgStoresTable** method to obtain the message store table so that it can be rendered in the main dialog box of MFCMAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="206e2-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="206e2-136">See also</span></span>



[<span data-ttu-id="206e2-137">IMAPISession::OpenMsgStore</span><span class="sxs-lookup"><span data-stu-id="206e2-137">IMAPISession::OpenMsgStore</span></span>](imapisession-openmsgstore.md)
  
[<span data-ttu-id="206e2-138">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="206e2-138">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)
  
[<span data-ttu-id="206e2-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="206e2-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="206e2-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="206e2-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="206e2-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="206e2-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="206e2-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="206e2-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="206e2-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="206e2-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="206e2-144">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="206e2-144">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="206e2-145">MFCMAPI als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="206e2-145">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="206e2-146">Nachrichtenspeichertabellen</span><span class="sxs-lookup"><span data-stu-id="206e2-146">Message Store Tables</span></span>](message-store-tables.md)

