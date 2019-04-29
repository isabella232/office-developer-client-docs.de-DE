---
title: IMAPISessionSetDefaultStore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.SetDefaultStore
api_type:
- COM
ms.assetid: 456c207f-5d41-4d0c-94b6-0c58893a6bed
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f4ff2a3897306ebe4f77c08630782c5f2c7d5d3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426107"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="bd409-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="bd409-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="bd409-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bd409-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bd409-105">Richtet einen Nachrichtenspeicher als Standardnachrichtenspeicher für die Sitzung ein.</span><span class="sxs-lookup"><span data-stu-id="bd409-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="bd409-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bd409-106">Parameters</span></span>

 <span data-ttu-id="bd409-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bd409-107">_ulFlags_</span></span>
  
> <span data-ttu-id="bd409-108">in Eine Bitmaske von Flags, die die Einstellung des Standardnachrichten Speichers steuert.</span><span class="sxs-lookup"><span data-stu-id="bd409-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="bd409-109">Diese Flags schließen sich gegenseitig aus; nur eines der folgenden Flags kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="bd409-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="bd409-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="bd409-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="bd409-111">Richtet den Nachrichtenspeicher als Sitzungs Standard ein.</span><span class="sxs-lookup"><span data-stu-id="bd409-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="bd409-112">Aktualisiert die Statustabellen Zeile des Nachrichtenspeichers, indem das STATUS_DEFAULT_STORE-Flag in der **PR_RESOURCE_FLAGS** ([pidtagresourceflags (](pidtagresourceflags-canonical-property.md))-Spalte festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd409-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="bd409-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="bd409-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="bd409-114">Richtet den Nachrichtenspeicher als den bei der Anmeldung zu verwendenden Speicher ein.</span><span class="sxs-lookup"><span data-stu-id="bd409-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="bd409-115">Wenn es sich bei dem Nachrichtenspeicher nicht um den Standardspeicher handelt, sollten Clients diesen standardmäßig festlegen.</span><span class="sxs-lookup"><span data-stu-id="bd409-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="bd409-116">Aktualisiert die Statustabellen Zeile des Nachrichtenspeichers, indem das STATUS_PRIMARY_STORE-Flag in der **PR_RESOURCE_FLAGS** -Spalte festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd409-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="bd409-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="bd409-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="bd409-118">Richtet den Nachrichtenspeicher als den bei der Anmeldung zu verwendenden Speicher ein, wenn der primäre Nachrichtenspeicher nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="bd409-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="bd409-119">Wenn ein Client den primären Speicher nicht öffnen kann, sollte er den sekundären Speicher öffnen und als Standard festlegen.</span><span class="sxs-lookup"><span data-stu-id="bd409-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="bd409-120">Aktualisiert die Statustabellen Zeile des Nachrichtenspeichers, indem das STATUS_SECONDARY_STORE-Flag in der **PR_RESOURCE_FLAGS** -Spalte festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="bd409-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="bd409-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="bd409-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="bd409-122">Legt das STATUS_SIMPLE_STORE-Flag in der **PR_RESOURCE_FLAGS** -Eigenschaft des Nachrichtenspeichers in der Zeile Status Tabelle, Nachrichtenspeicher-Tabellenzeile und im Sitzungsprofil fest.</span><span class="sxs-lookup"><span data-stu-id="bd409-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="bd409-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="bd409-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="bd409-124">Legt das STATUS_SIMPLE_STORE-Flag in der **PR_RESOURCE_FLAGS** -Eigenschaft des Nachrichtenspeichers in der Zeile Status Tabelle und Nachrichtenspeichertabelle fest.</span><span class="sxs-lookup"><span data-stu-id="bd409-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="bd409-125">Das Profil wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="bd409-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="bd409-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="bd409-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="bd409-127">in Die Anzahl der Bytes in der Eintrags-ID, auf die durch den _lpEntryID_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bd409-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="bd409-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="bd409-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="bd409-129">in Ein Zeiger auf die Eintrags-ID des Nachrichtenspeichers, der als Standard verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bd409-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="bd409-130">Wenn ein Client in _LPENTRYID_NULL übergibt, wird kein Nachrichtenspeicher als Standard ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="bd409-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bd409-131">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bd409-131">Return value</span></span>

<span data-ttu-id="bd409-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="bd409-132">S_OK</span></span> 
  
> <span data-ttu-id="bd409-133">Der Aufruf war erfolgreich, und der erwartete Wert oder die Werte wurden zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd409-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bd409-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd409-134">Remarks</span></span>

<span data-ttu-id="bd409-135">Mit der **IMAPISession:: SetDefaultStore** -Methode wird ein Nachrichtenspeicher als einer der folgenden festgelegt:</span><span class="sxs-lookup"><span data-stu-id="bd409-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="bd409-136">Der standardmäßige Nachrichtenspeicher für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bd409-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="bd409-137">Der primäre Nachrichtenspeicher für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bd409-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="bd409-138">Der sekundäre Nachrichtenspeicher für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bd409-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="bd409-139">Zum Einrichten eines Nachrichtenspeichers als Standard muss für den Nachrichtenspeicher die folgenden Flags in der **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festgelegt sein:</span><span class="sxs-lookup"><span data-stu-id="bd409-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="bd409-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="bd409-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="bd409-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="bd409-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="bd409-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="bd409-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="bd409-143">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="bd409-143">Notes to callers</span></span>

<span data-ttu-id="bd409-144">Sie können den standardmäßigen Nachrichtenspeicher für die Sitzung bestimmen, indem Sie die Statustabelle abrufen und nach der Einstellung des STATUS_DEFAULT_STORE-Flags in der **PR_RESOURCE_FLAGS** -Spalte suchen.</span><span class="sxs-lookup"><span data-stu-id="bd409-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="bd409-145">Die Zeile mit dieser Einstellung stellt den Nachrichtenspeicher dar, der als Sitzungs Standard festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="bd409-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="bd409-146">Wenn das MAPI_DEFAULT_STORE-oder das MAPI_SIMPLE_STORE_PERMANENT-Flag festgelegt ist, aktualisiert MAPI das Profil, die Nachrichtenspeichertabelle und die Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="bd409-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="bd409-147">Bei jeder Änderung der Standardeinstellung für den Nachrichtenspeicher werden die folgenden Benachrichtigungen generiert:</span><span class="sxs-lookup"><span data-stu-id="bd409-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="bd409-148">Für jede betroffene Zeile in der Nachrichtenspeicher-und Statustabelle wird eine **fnevTableModified** -Ereignisbenachrichtigung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd409-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="bd409-149">Eine interne Benachrichtigung wird an den MAPI-Spooler ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="bd409-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="bd409-150">Vorgänge, die bereits ausgeführt werden, werden ohne Änderung abgeschlossen. neue Vorgänge, die den standardmäßigen Nachrichtenspeicher betreffen, wie das Herunterladen von Nachrichten, werden für den neuen Standardspeicher verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="bd409-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="bd409-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="bd409-151">MFCMAPI reference</span></span>

<span data-ttu-id="bd409-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bd409-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bd409-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="bd409-153">**File**</span></span>|<span data-ttu-id="bd409-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="bd409-154">**Function**</span></span>|<span data-ttu-id="bd409-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="bd409-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bd409-156">MainDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="bd409-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="bd409-157">CMainDlg:: OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="bd409-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="bd409-158">MFCMAPI verwendet die **IMAPISession:: SetDefaultStore** -Methode, um den ausgewählten Speicher als Standardspeicher festzulegen.</span><span class="sxs-lookup"><span data-stu-id="bd409-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bd409-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bd409-159">See also</span></span>



[<span data-ttu-id="bd409-160">Kanonische Pidtagresourceflags (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bd409-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="bd409-161">Kanonische PidTagStoreSupportMask-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="bd409-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="bd409-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="bd409-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="bd409-163">IMAPISession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bd409-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="bd409-164">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="bd409-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

