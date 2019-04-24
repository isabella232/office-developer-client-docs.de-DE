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
ms.openlocfilehash: 303c2ef855d5cfc1d6614bda92b46c2da97717c8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317353"
---
# <a name="imsgstoregetreceivefoldertable"></a><span data-ttu-id="7f0f9-103">IMsgStore::GetReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="7f0f9-103">IMsgStore::GetReceiveFolderTable</span></span>

  
  
<span data-ttu-id="7f0f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7f0f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7f0f9-105">Ermöglicht den Zugriff auf die Tabelle Receive Folder, eine Tabelle mit Informationen zu allen Empfangs Ordnern für den Nachrichtenspeicher.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-105">Provides access to the receive folder table, a table that includes information about all of the receive folders for the message store.</span></span>
  
```cpp
HRESULT GetReceiveFolderTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable );
```

## <a name="parameters"></a><span data-ttu-id="7f0f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f0f9-106">Parameters</span></span>

 <span data-ttu-id="7f0f9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7f0f9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="7f0f9-108">in Eine Bitmaske von Flags, die den Tabellenzugriff steuert.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-108">[in] A bitmask of flags that controls table access.</span></span> <span data-ttu-id="7f0f9-109">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="7f0f9-109">The following flags can be set:</span></span>
    
<span data-ttu-id="7f0f9-110">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="7f0f9-110">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="7f0f9-111">Ermöglicht es **GetReceiveFolderTable** , erfolgreich zurückzugeben, möglicherweise bevor die Tabelle vollständig für den Aufrufer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-111">Allows **GetReceiveFolderTable** to return successfully, possibly before the table is fully available to the caller.</span></span> <span data-ttu-id="7f0f9-112">Wenn die Tabelle nicht vollständig verfügbar ist, kann durch einen nachfolgenden Tabellen Aufruf ein Fehler ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-112">If the table is not fully available, making a subsequent table call can raise an error.</span></span> 
    
<span data-ttu-id="7f0f9-113">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="7f0f9-113">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="7f0f9-114">Die zurückgegebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-114">The returned strings are in Unicode format.</span></span> <span data-ttu-id="7f0f9-115">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-115">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="7f0f9-116">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="7f0f9-116">_lppTable_</span></span>
  
> <span data-ttu-id="7f0f9-117">Out Ein Zeiger auf einen Zeiger auf die Tabelle des Empfangs Ordners.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-117">[out] A pointer to a pointer to the receive folder table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7f0f9-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f0f9-118">Return value</span></span>

<span data-ttu-id="7f0f9-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="7f0f9-119">S_OK</span></span> 
  
> <span data-ttu-id="7f0f9-120">Die Tabelle des Empfangs Ordners wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-120">The receive folder table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7f0f9-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f0f9-121">Remarks</span></span>

<span data-ttu-id="7f0f9-122">Die **IMsgStore:: GetReceiveFolderTable** -Methode ermöglicht den Zugriff auf eine Tabelle, in der die Eigenschafteneinstellungen für alle Empfangsordner des Nachrichtenspeichers angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-122">The **IMsgStore::GetReceiveFolderTable** method provides access to a table that shows the property settings for all of the message store's receive folders.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7f0f9-123">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="7f0f9-123">Notes to implementers</span></span>

<span data-ttu-id="7f0f9-124">Eine Liste der erforderlichen Spalten in einer Tabelle mit einem Receive-Ordner finden Sie unter [Receive Folder Tables](receive-folder-tables.md).</span><span class="sxs-lookup"><span data-stu-id="7f0f9-124">For a list of required columns in a receive folder table, see [Receive Folder Tables](receive-folder-tables.md).</span></span> 
  
<span data-ttu-id="7f0f9-125">Implementieren Sie die Tabellen des Empfangs Ordners, um Einstellungs Einschränkungen für die **PR_RECORD_KEY** ([pidtagrecordkey (](pidtagrecordkey-canonical-property.md))-Eigenschaft zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-125">Implement your receive folder tables to support setting property restrictions on the **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) property.</span></span> <span data-ttu-id="7f0f9-126">Dies ermöglicht den einfachen Zugriff auf bestimmte Empfangsordner.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-126">This enables easy access to particular receive folders.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="7f0f9-127">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="7f0f9-127">Notes to callers</span></span>

<span data-ttu-id="7f0f9-128">Das Festlegen des MAPI_UNICODE-Flags im _ulFlags_ -Parameter wirkt sich auf das Format der Spalten aus, die von den Methoden [IMAPITable:: QueryColumns](imapitable-querycolumns.md) und [IMAPITable:: QueryRows](imapitable-queryrows.md) zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-128">Setting the MAPI_UNICODE flag in the  _ulFlags_ parameter affects the format of the columns returned from the [IMAPITable::QueryColumns](imapitable-querycolumns.md) and [IMAPITable::QueryRows](imapitable-queryrows.md) methods.</span></span> <span data-ttu-id="7f0f9-129">Dieses Flag steuert auch die Eigenschaftentypen in der von der [IMAPITable:: QuerySortOrder](imapitable-querysortorder.md) -Methode zurückgegebenen Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-129">This flag also controls the property types in the sort order returned by the [IMAPITable::QuerySortOrder](imapitable-querysortorder.md) method.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7f0f9-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="7f0f9-130">MFCMAPI reference</span></span>

<span data-ttu-id="7f0f9-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7f0f9-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="7f0f9-132">**File**</span></span>|<span data-ttu-id="7f0f9-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="7f0f9-133">**Function**</span></span>|<span data-ttu-id="7f0f9-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="7f0f9-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7f0f9-135">MsgStoreDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="7f0f9-135">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="7f0f9-136">CMsgStoreDlg:: OnDisplayReceiveFolderTable</span><span class="sxs-lookup"><span data-stu-id="7f0f9-136">CMsgStoreDlg::OnDisplayReceiveFolderTable</span></span>  <br/> |<span data-ttu-id="7f0f9-137">MFCMAPI verwendet die **IMsgStore:: GetReceiveFolderTable** -Methode, um die anzuzeigende Ordnertabelle abzurufen.</span><span class="sxs-lookup"><span data-stu-id="7f0f9-137">MFCMAPI uses the **IMsgStore::GetReceiveFolderTable** method to get the receive folder table to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7f0f9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f0f9-138">See also</span></span>



[<span data-ttu-id="7f0f9-139">IMAPITable::QueryColumns</span><span class="sxs-lookup"><span data-stu-id="7f0f9-139">IMAPITable::QueryColumns</span></span>](imapitable-querycolumns.md)
  
[<span data-ttu-id="7f0f9-140">IMAPITable::QueryRows</span><span class="sxs-lookup"><span data-stu-id="7f0f9-140">IMAPITable::QueryRows</span></span>](imapitable-queryrows.md)
  
[<span data-ttu-id="7f0f9-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="7f0f9-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="7f0f9-142">IMAPITable::SetColumns</span><span class="sxs-lookup"><span data-stu-id="7f0f9-142">IMAPITable::SetColumns</span></span>](imapitable-setcolumns.md)
  
[<span data-ttu-id="7f0f9-143">IMsgStore: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="7f0f9-143">IMsgStore : IMAPIProp</span></span>](imsgstoreimapiprop.md)


[<span data-ttu-id="7f0f9-144">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="7f0f9-144">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

