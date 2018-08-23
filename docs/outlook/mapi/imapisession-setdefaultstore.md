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
ms.openlocfilehash: c7eda7089515942cb38a941bab863b3adf971bdc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587845"
---
# <a name="imapisessionsetdefaultstore"></a><span data-ttu-id="f8073-103">IMAPISession::SetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="f8073-103">IMAPISession::SetDefaultStore</span></span>

  
  
<span data-ttu-id="f8073-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f8073-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f8073-105">Stellt einen Nachrichtenspeicher als Standard-Informationsspeicher für die Sitzung her.</span><span class="sxs-lookup"><span data-stu-id="f8073-105">Establishes a message store as the default message store for the session.</span></span>
  
```cpp
HRESULT SetDefaultStore(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="f8073-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8073-106">Parameters</span></span>

 <span data-ttu-id="f8073-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f8073-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f8073-108">[in] Eine Bitmaske aus Flags, die die Einstellung der Standard-Informationsspeicher steuert.</span><span class="sxs-lookup"><span data-stu-id="f8073-108">[in] A bitmask of flags that controls the setting of the default message store.</span></span> <span data-ttu-id="f8073-109">Diese Flags schließen sich gegenseitig aus; Es kann nur eine der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="f8073-109">These flags are mutually exclusive; only one of the following flags can be set:</span></span>
    
<span data-ttu-id="f8073-110">MAPI_DEFAULT_STORE</span><span class="sxs-lookup"><span data-stu-id="f8073-110">MAPI_DEFAULT_STORE</span></span>
  
> <span data-ttu-id="f8073-111">Stellt den Nachrichtenspeicher unverändert Sitzung her.</span><span class="sxs-lookup"><span data-stu-id="f8073-111">Establishes the message store as the session default.</span></span> <span data-ttu-id="f8073-112">Aktualisiert den Nachrichtenspeicher Status Tabellenzeile durch das Flag STATUS_DEFAULT_STORE in der Spalte **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8073-112">Updates the message store's status table row by setting the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md)) column.</span></span>
    
<span data-ttu-id="f8073-113">MAPI_PRIMARY_STORE</span><span class="sxs-lookup"><span data-stu-id="f8073-113">MAPI_PRIMARY_STORE</span></span>
  
> <span data-ttu-id="f8073-114">Richtet den Nachrichtenspeicher als Speicher, die bei der Anmeldung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8073-114">Establishes the message store as the store to be used at logon.</span></span> <span data-ttu-id="f8073-115">Wenn der Nachrichtenspeicher nicht des Standard-Informationsspeichers ist, sollte Clients die Standardeinstellung ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f8073-115">If the message store is not the default store, clients should make it the default.</span></span> <span data-ttu-id="f8073-116">Aktualisiert den Nachrichtenspeicher Status Tabellenzeile durch das Flag STATUS_PRIMARY_STORE in der Spalte **PR_RESOURCE_FLAGS** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8073-116">Updates the message store's status table row by setting the STATUS_PRIMARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="f8073-117">MAPI_SECONDARY_STORE</span><span class="sxs-lookup"><span data-stu-id="f8073-117">MAPI_SECONDARY_STORE</span></span>
  
> <span data-ttu-id="f8073-118">Richtet den Nachrichtenspeicher als Speicher bei der Anmeldung verwendet werden, wenn der primäre Nachrichtenspeicher nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f8073-118">Establishes the message store as the store to be used at logon if the primary message store is not available.</span></span> <span data-ttu-id="f8073-119">Wenn ein Client den primären Speicher nicht öffnen kann, sollten sie den sekundären Speicher öffnen und als Standard festlegen.</span><span class="sxs-lookup"><span data-stu-id="f8073-119">If a client cannot open the primary store, it should open the secondary store and set it as the default.</span></span> <span data-ttu-id="f8073-120">Aktualisiert den Nachrichtenspeicher Status Tabellenzeile durch das Flag STATUS_SECONDARY_STORE in der Spalte **PR_RESOURCE_FLAGS** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8073-120">Updates the message store's status table row by setting the STATUS_SECONDARY_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> 
    
<span data-ttu-id="f8073-121">MAPI_SIMPLE_STORE_PERMANENT</span><span class="sxs-lookup"><span data-stu-id="f8073-121">MAPI_SIMPLE_STORE_PERMANENT</span></span>
  
> <span data-ttu-id="f8073-122">Das Flag STATUS_SIMPLE_STORE festgelegt in den Nachrichtenspeicher **PR_RESOURCE_FLAGS** -Eigenschaft in dessen Status Tabellenzeile Nachricht Store Tabellenzeile, und das Sitzungsprofil.</span><span class="sxs-lookup"><span data-stu-id="f8073-122">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row, message store table row, and in the session profile.</span></span> 
    
<span data-ttu-id="f8073-123">MAPI_SIMPLE_STORE_TEMPORARY</span><span class="sxs-lookup"><span data-stu-id="f8073-123">MAPI_SIMPLE_STORE_TEMPORARY</span></span>
  
> <span data-ttu-id="f8073-124">Legt das Flag STATUS_SIMPLE_STORE in den Nachrichtenspeicher **PR_RESOURCE_FLAGS** -Eigenschaft in den Status Tabellenzeile und Nachricht Store Tabellenzeile fest.</span><span class="sxs-lookup"><span data-stu-id="f8073-124">Sets the STATUS_SIMPLE_STORE flag in the message store's **PR_RESOURCE_FLAGS** property in its status table row and message store table row.</span></span> <span data-ttu-id="f8073-125">Das Profil wird nicht geändert.</span><span class="sxs-lookup"><span data-stu-id="f8073-125">The profile is not modified.</span></span> 
    
 <span data-ttu-id="f8073-126">_cbEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8073-126">_cbEntryID_</span></span>
  
> <span data-ttu-id="f8073-127">[in] Die Byteanzahl von in die Eintrags-ID auf den durch den Parameter _LpEntryID_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="f8073-127">[in] The byte count in the entry identifier pointed to by the  _lpEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="f8073-128">_lpEntryID_</span><span class="sxs-lookup"><span data-stu-id="f8073-128">_lpEntryID_</span></span>
  
> <span data-ttu-id="f8073-129">[in] Ein Zeiger auf die Eintrags-ID des Nachrichtenspeichers, das als Standard vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f8073-129">[in] A pointer to the entry identifier of the message store that is intended as the default.</span></span> <span data-ttu-id="f8073-130">Wenn ein Client NULL _LpEntryID_übergibt, wird keine Nachrichtenspeicher als Standard ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="f8073-130">If a client passes NULL in  _lpEntryID_, no message store is selected as the default.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f8073-131">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="f8073-131">Return value</span></span>

<span data-ttu-id="f8073-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="f8073-132">S_OK</span></span> 
  
> <span data-ttu-id="f8073-133">Der Aufruf erfolgreich ausgeführt und der erwartete Wert oder Werte zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8073-133">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f8073-134">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="f8073-134">Remarks</span></span>

<span data-ttu-id="f8073-135">Die **IMAPISession::SetDefaultStore** -Methode legt einen Nachrichtenspeicher als eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="f8073-135">The **IMAPISession::SetDefaultStore** method establishes a message store as one of the following:</span></span> 
  
- <span data-ttu-id="f8073-136">Die Standard-Nachrichtenspeicher für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f8073-136">The default message store for the session.</span></span>
    
- <span data-ttu-id="f8073-137">Die primäre Nachrichtenspeicher für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f8073-137">The primary message store for the session.</span></span>
    
- <span data-ttu-id="f8073-138">Die sekundäre Nachrichtenspeicher für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f8073-138">The secondary message store for the session.</span></span>
    
<span data-ttu-id="f8073-139">Zum Einrichten eines Nachrichtenspeichers als Standard muss der Nachrichtenspeicher folgender Flags in seiner **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))-Eigenschaft festlegen können:</span><span class="sxs-lookup"><span data-stu-id="f8073-139">To establish a message store as the default, the message store must have the following flags set in its **PR_STORE_SUPPORT_MASK** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md)) property:</span></span>
  
- <span data-ttu-id="f8073-140">STORE_SUBMIT_OK</span><span class="sxs-lookup"><span data-stu-id="f8073-140">STORE_SUBMIT_OK</span></span>
    
- <span data-ttu-id="f8073-141">STORE_CREATE_OK</span><span class="sxs-lookup"><span data-stu-id="f8073-141">STORE_CREATE_OK</span></span>
    
- <span data-ttu-id="f8073-142">STORE_MODIFY_OK</span><span class="sxs-lookup"><span data-stu-id="f8073-142">STORE_MODIFY_OK</span></span>
    
## <a name="notes-to-callers"></a><span data-ttu-id="f8073-143">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f8073-143">Notes to callers</span></span>

<span data-ttu-id="f8073-144">Sie können Standard-Informationsspeicher für die Sitzung bestimmen, indem Status abrufen und für die Einstellung des STATUS_DEFAULT_STORE-Flags in der Spalte **PR_RESOURCE_FLAGS** suchen.</span><span class="sxs-lookup"><span data-stu-id="f8073-144">You can determine the default message store for the session by retrieving the status table and searching for the setting of the STATUS_DEFAULT_STORE flag in the **PR_RESOURCE_FLAGS** column.</span></span> <span data-ttu-id="f8073-145">Die Zeile, die diese Einstellung hat stellt den Nachrichtenspeicher, der als Sitzung Standardproxy festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f8073-145">The row that has this setting represents the message store that is designated as the session default.</span></span> 
  
<span data-ttu-id="f8073-146">Wenn die MAPI_DEFAULT_STORE oder das MAPI_SIMPLE_STORE_PERMANENT-Flag festgelegt ist, aktualisiert MAPI Profil, Nachricht Store Tabelle und Statustabelle.</span><span class="sxs-lookup"><span data-stu-id="f8073-146">When either the MAPI_DEFAULT_STORE or the MAPI_SIMPLE_STORE_PERMANENT flag is set, MAPI updates the profile, message store table, and status table.</span></span> 
  
<span data-ttu-id="f8073-147">Wenn die Nachricht Store Standardeinstellung eine Änderung vorgenommen wird, werden die folgenden Benachrichtigungen generiert:</span><span class="sxs-lookup"><span data-stu-id="f8073-147">Whenever a change is made to the message store default setting, the following notifications are generated:</span></span>
  
- <span data-ttu-id="f8073-148">Für jede betroffene Zeile in der Nachricht Store und den Status der Tabelle wird eine Benachrichtigung bei **FnevTableModified** ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8073-148">An **fnevTableModified** event notification is issued for each affected row in both the message store and status table.</span></span> 
    
- <span data-ttu-id="f8073-149">Eine interne Benachrichtigung wird an die Warteschlange MAPI ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="f8073-149">An internal notification is issued to the MAPI spooler.</span></span> <span data-ttu-id="f8073-150">Bereits in Bearbeitung befindlichen Vorgänge werden ohne Änderung ausgefüllt. neue Vorgänge mit Standard-Informationsspeicher, wie etwa Nachricht herunterladen, werden für den neuen Standardspeicher verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f8073-150">Operations already in progress are completed without change; new operations that involve the default message store, such as message downloading, are processed for the new default store.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="f8073-151">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="f8073-151">MFCMAPI reference</span></span>

<span data-ttu-id="f8073-152">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="f8073-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f8073-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="f8073-153">**File**</span></span>|<span data-ttu-id="f8073-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="f8073-154">**Function**</span></span>|<span data-ttu-id="f8073-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="f8073-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f8073-156">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f8073-156">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="f8073-157">CMainDlg::OnSetDefaultStore</span><span class="sxs-lookup"><span data-stu-id="f8073-157">CMainDlg::OnSetDefaultStore</span></span>  <br/> |<span data-ttu-id="f8073-158">MFCMAPI (engl.) verwendet die **IMAPISession::SetDefaultStore** -Methode, um der ausgewählten Speicher als Standard-Informationsspeicher festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f8073-158">MFCMAPI uses the **IMAPISession::SetDefaultStore** method to set the selected store as the default store.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f8073-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f8073-159">See also</span></span>



[<span data-ttu-id="f8073-160">PidTagResourceFlags (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f8073-160">PidTagResourceFlags Canonical Property</span></span>](pidtagresourceflags-canonical-property.md)
  
[<span data-ttu-id="f8073-161">PidTagStoreSupportMask (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="f8073-161">PidTagStoreSupportMask Canonical Property</span></span>](pidtagstoresupportmask-canonical-property.md)
  
[<span data-ttu-id="f8073-162">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="f8073-162">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="f8073-163">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f8073-163">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="f8073-164">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="f8073-164">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

