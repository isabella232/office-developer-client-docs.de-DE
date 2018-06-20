---
title: IABContainerCopyEntries
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABContainer.CopyEntries
api_type:
- COM
ms.assetid: 4e775228-5ceb-4002-9b68-999fb5889b86
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 44a31e46c43a065c720564f2aa193913dbfd9a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791950"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="c4045-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="c4045-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="c4045-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c4045-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c4045-105">Kopiert eine oder mehrere Einträge, in der Regel messaging Benutzer oder Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="c4045-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c4045-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c4045-106">Parameters</span></span>

 <span data-ttu-id="c4045-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="c4045-107">_lpEntries_</span></span>
  
> <span data-ttu-id="c4045-108">[in] Ein Zeiger auf ein Array von [ENTRYLIST](entrylist.md) -Strukturen, die Einträge zum Kopieren von Eintragsbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="c4045-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="c4045-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c4045-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="c4045-110">[in] Das Handle für das übergeordnete Fenster für alle Dialogfelder oder Windows, die diese Methode anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c4045-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="c4045-111">Der Parameter _UlUIParam_ muss NULL sein, wenn das Flag AB_NO_DIALOG im _UlFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4045-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="c4045-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="c4045-112">_lpProgress_</span></span>
  
> <span data-ttu-id="c4045-113">[in] Ein Zeiger auf ein Fortschritt-Objekt, eine Statusanzeige oder NULL anzeigt.</span><span class="sxs-lookup"><span data-stu-id="c4045-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="c4045-114">Wenn _LpProgress_ NULL ist, sollte eine Statusanzeige mithilfe von MAPI bereitgestellt wird, über die [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode des Fortschritts-Objekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c4045-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="c4045-115">Der Parameter _LpProgress_ wird ignoriert, wenn das Flag AB_NO_DIALOG in _UlFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="c4045-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="c4045-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c4045-116">_ulFlags_</span></span>
  
> <span data-ttu-id="c4045-117">[in] Eine Bitmaske aus Flags, die steuert, wie der Kopiervorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c4045-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="c4045-118">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c4045-118">The following flags can be set:</span></span>
    
<span data-ttu-id="c4045-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="c4045-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="c4045-120">Unterdrückt die Anzeige einer Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="c4045-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="c4045-121">Wenn dieses Flag nicht festgelegt ist, wird eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c4045-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="c4045-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="c4045-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="c4045-123">Gibt an, dass eine weit Ebene der doppelten Eintrag Überprüfung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4045-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c4045-124">Die Implementierung der weit doppelter Eintrag Überprüfung ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="c4045-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c4045-125">Beispielsweise kann ein Anbieter eine niedrigen Übereinstimmung definieren, wie alle zwei Einträge, die den gleichen Namen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4045-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="c4045-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="c4045-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="c4045-127">Gibt an, dass eine strikt doppelter Eintrag überprüfen ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4045-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="c4045-128">Die Implementierung der exakte doppelter Eintrag Überprüfung ist anbieterspezifisch.</span><span class="sxs-lookup"><span data-stu-id="c4045-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="c4045-129">Ein Anbieter kann beispielsweise eine exakte Übereinstimmung definieren, wie alle zwei Einträge, die beide den gleichen Namen und die messaging-Adresse anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="c4045-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="c4045-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="c4045-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="c4045-131">Gibt an, dass ein neuer Eintrag eine vorhandene ersetzen soll, wenn festgestellt wird, dass die beiden Duplikate sind.</span><span class="sxs-lookup"><span data-stu-id="c4045-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c4045-132">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c4045-132">Return value</span></span>

<span data-ttu-id="c4045-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="c4045-133">S_OK</span></span> 
  
> <span data-ttu-id="c4045-134">Der Kopiervorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c4045-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="c4045-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="c4045-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="c4045-136">Der Kopiervorgang insgesamt erfolgreich, aber eine oder mehrere Einträge konnte nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4045-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="c4045-137">Wenn dieser Wert zurückgegeben wird, sollte der Anruf als erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c4045-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="c4045-138">Verwenden Sie das Makro **HR_FAILED** , um für diesen Wert zu testen.</span><span class="sxs-lookup"><span data-stu-id="c4045-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="c4045-139">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="c4045-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c4045-140">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c4045-140">Remarks</span></span>

<span data-ttu-id="c4045-141">Die **IABContainer::CopyEntries** -Methode kopiert die Einträge aus der gleichen Container oder einen anderen Container.</span><span class="sxs-lookup"><span data-stu-id="c4045-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="c4045-142">Ein Aufruf von **CopyEntries** entspricht der folgenden Aufrufe für jeden Eintrag kopiert werden:</span><span class="sxs-lookup"><span data-stu-id="c4045-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="c4045-143">Die [IABContainer::CreateEntry](iabcontainer-createentry.md) -Methode, um den neuen Eintrag erstellen.</span><span class="sxs-lookup"><span data-stu-id="c4045-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="c4045-144">Die [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Lesen von Eigenschaften aus den Eintrag kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4045-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="c4045-145">Die [IMAPIProp::SetProps](imapiprop-setprops.md) -Methode zum Schreiben von Eigenschaften in den neuen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="c4045-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="c4045-146">Den neuen Eintrag [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c4045-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="c4045-147">Den neuen Eintrag [IUnknown](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) -Methode, die den Container Verweis freigeben.</span><span class="sxs-lookup"><span data-stu-id="c4045-147">The new entry's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="c4045-148">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c4045-148">Notes to implementers</span></span>

<span data-ttu-id="c4045-149">Alle Container, die die **IABContainer::CopyEntries** -Methode unterstützen müssen geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c4045-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="c4045-150">Festlegen des Containers AB_MODIFIABLE Flag in seiner **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md))-Eigenschaft, um anzugeben, dass es geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="c4045-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="c4045-151">Sie müssen alle Kennzeichen unterstützen. die Interpretation und die Verwendung dieser Flags Implementierung ist jedoch bestimmte – d. h., können Sie ermitteln, Bedeutung der Semantik der CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT-Kennzeichen im Zusammenhang mit der Implementierung.</span><span class="sxs-lookup"><span data-stu-id="c4045-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="c4045-152">Wenn Sie nicht oder nicht bestimmen, ob ein Eintrag vorhanden ist, immer zulassen Sie den Eintrag kopiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="c4045-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="c4045-153">Wenn das Flag CREATE_REPLACE festgelegt ist, kopieren Sie den Eintrag unabhängig davon, ob CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT festgelegt ist und ob der Eintrag ein Duplikat ist immer.</span><span class="sxs-lookup"><span data-stu-id="c4045-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="c4045-154">Wenn CREATE_REPLACE nicht festgelegt ist und CREATE_CHECK_DUP_STRICT festgelegt ist, Duplikate überprüft.</span><span class="sxs-lookup"><span data-stu-id="c4045-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="c4045-155">Wenn Sie ein Eintrag ermittelt wird, dass ein Duplikat ist, kopieren Sie den Eintrag nicht.</span><span class="sxs-lookup"><span data-stu-id="c4045-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="c4045-156">Sie müssen nicht CREATE_REPLACE unterstützen. nicht unterstützt, CREATE_REPLACE bedeutet, dass Sie Sie ignorieren, und führen stets eine Kopie.</span><span class="sxs-lookup"><span data-stu-id="c4045-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="c4045-157">Die Warnung MAPI_W_PARTIAL_COMPLETION nur zurück, wenn ein Eintrag nicht duplizierte kann nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="c4045-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c4045-158">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c4045-158">Notes to callers</span></span>

<span data-ttu-id="c4045-159">Verwenden Sie die Kennzeichen CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT, um auf den Anbieter anzugeben, wie den Container doppelter Eintrag Überprüfung ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="c4045-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="c4045-160">Wenn Sie benötigen, einen Eintrag hinzugefügt werden, unabhängig davon, ob es sich um ein Duplikat handelt, entweder nicht legen Sie einen der folgenden Kennzeichen oder legen Sie das CREATE_REPLACE-Flag.</span><span class="sxs-lookup"><span data-stu-id="c4045-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="c4045-161">CREATE_REPLACE gibt an, dass Sie nicht wichtig ist, wenn der Eintrag ein Duplikat ist; Möchten sie den ursprünglichen Eintrag ersetzen.</span><span class="sxs-lookup"><span data-stu-id="c4045-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c4045-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c4045-162">See also</span></span>



[<span data-ttu-id="c4045-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="c4045-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="c4045-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="c4045-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="c4045-165">IMAPIProgress: IUnknown</span><span class="sxs-lookup"><span data-stu-id="c4045-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="c4045-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c4045-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c4045-167">IABContainer: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c4045-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

