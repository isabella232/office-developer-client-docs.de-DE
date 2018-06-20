---
title: IMsgStoreGetReceiveFolderTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.GetReceiveFolderTable
api_type:
- COM
ms.assetid: d115ab58-07d2-4b49-8e08-2881c2924102
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8146b5c2b9c9fb5429a9c1d46bca687c32bcf3dc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792641"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="d1b9c-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="d1b9c-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="d1b9c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1b9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1b9c-105">Bietet Zugriff auf die empfangen Ordnertabelle Tabelle Informationen zu allen der Ordner für den Nachrichtenspeicher empfangen enthält.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="d1b9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1b9c-106">Parameters</span></span>

 <span data-ttu-id="d1b9c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d1b9c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d1b9c-108">[in] Eine Bitmaske der Werte, dass Steuerelemente Access-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="d1b9c-109">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="d1b9c-109">The following flags can be set:</span></span>
    
<span data-ttu-id="d1b9c-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="d1b9c-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="d1b9c-111">Ermöglicht **GetReceiveFolderTable** erfolgreich, möglicherweise beendet, bevor die Tabelle mit dem Anrufer vollständig verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="d1b9c-112">Wenn die Tabelle nicht vollständig verfügbar ist, kann die nachfolgenden Tabelle Anrufen ein Fehler ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="d1b9c-113">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d1b9c-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d1b9c-114">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="d1b9c-115">Wenn die Option MAPI_UNICODE nicht festgelegt ist, sind die Zeichenfolgen in ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d1b9c-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="d1b9c-116">_lppTable_</span></span>
  
> <span data-ttu-id="d1b9c-117">[out] Ein Zeiger auf einen Zeiger auf den Ordner-empfangen-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d1b9c-118">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d1b9c-118">Return value</span></span>

<span data-ttu-id="d1b9c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="d1b9c-119">S_OK</span></span> 
  
> <span data-ttu-id="d1b9c-120">Die Ordner-Tabelle empfangen wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1b9c-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d1b9c-121">Remarks</span></span>

<span data-ttu-id="d1b9c-122">Die **IMsgStore::GetReceiveFolderTable** -Methode ermöglicht den Zugriff auf eine Tabelle, die anzeigt, dass die Einstellungen für alle des Nachrichtenspeicher Ordner erhalten.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d1b9c-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="d1b9c-123">Notes to implementers</span></span>

<span data-ttu-id="d1b9c-124">Eine Liste der erforderlichen Spalten in einem Ordner empfangen finden Sie unter [Ordner Tabellen erhalten](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="d1b9c-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="d1b9c-125">Implementieren der Ordner Tabellen Suchkriterien in Eigenschaft die Einstellung für die Eigenschaft **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) Unterstützung erhalten.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="d1b9c-126">Diese einfache ermöglicht den Zugriff auf bestimmte empfangen Ordner.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="d1b9c-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="d1b9c-127">Notes to callers</span></span>

<span data-ttu-id="d1b9c-128">Festlegen der Option MAPI_UNICODE im Parameter _UlFlags_ wirkt sich auf das Format der von den Methoden [IMAPITable::QueryColumns](imapitable-querycolumns.md) und [IMAPITable::QueryRows](imapitable-queryrows.md) zurückgegebenen Spalten aus.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="d1b9c-129">Dieses Kennzeichen steuert auch die Eigenschaftentypen in der Sortierreihenfolge, die von der [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d1b9c-130">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="d1b9c-130">MFCMAPI reference</span></span>

<span data-ttu-id="d1b9c-131">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d1b9c-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-132">**File**</span></span>|<span data-ttu-id="d1b9c-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-133">**Function**</span></span>|<span data-ttu-id="d1b9c-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="d1b9c-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d1b9c-135">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="d1b9c-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="d1b9c-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="d1b9c-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="d1b9c-137">MFCMAPI (engl.) verwendet die **IMsgStore::GetReceiveFolderTable** -Methode zum Abrufen der empfangen Ordnertabelle angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d1b9c-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1b9c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1b9c-138">See also</span></span>



[<span data-ttu-id="d1b9c-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="d1b9c-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="d1b9c-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="d1b9c-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="d1b9c-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="d1b9c-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="d1b9c-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="d1b9c-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="d1b9c-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="d1b9c-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="d1b9c-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="d1b9c-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

