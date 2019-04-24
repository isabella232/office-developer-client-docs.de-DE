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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: ddb730ed92db4c8d281e7c8d5d9b18bc44505598
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346396"
---
# <a name="iabcontainercopyentries"></a><span data-ttu-id="6303b-103">IABContainer::CopyEntries</span><span class="sxs-lookup"><span data-stu-id="6303b-103">IABContainer::CopyEntries</span></span>

  
  
<span data-ttu-id="6303b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6303b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6303b-105">Kopiert einen oder mehrere Einträge, in der Regel Messagingbenutzer oder Verteilerlisten.</span><span class="sxs-lookup"><span data-stu-id="6303b-105">Copies one or more entries, typically messaging users or distribution lists.</span></span>
  
```cpp
HRESULT CopyEntries(
  LPENTRYLIST lpEntries,
  ULONG_PTR ulUIParam,
  LPMAPIPROGRESS lpProgress,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6303b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6303b-106">Parameters</span></span>

 <span data-ttu-id="6303b-107">_lpEntries_</span><span class="sxs-lookup"><span data-stu-id="6303b-107">_lpEntries_</span></span>
  
> <span data-ttu-id="6303b-108">in Ein Zeiger auf ein Array von [entrylist](entrylist.md) -Strukturen, das die Eintragsbezeichner der zu kopierende Einträge enthält.</span><span class="sxs-lookup"><span data-stu-id="6303b-108">[in] A pointer to an array of [ENTRYLIST](entrylist.md) structures that contains the entry identifiers of the entries to copy.</span></span> 
    
 <span data-ttu-id="6303b-109">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="6303b-109">_ulUIParam_</span></span>
  
> <span data-ttu-id="6303b-110">in Das Handle für das übergeordnete Fenster aller von dieser Methode angezeigten Dialogfelder oder Fenster.</span><span class="sxs-lookup"><span data-stu-id="6303b-110">[in] The handle to the parent window of any dialog boxes or windows that this method displays.</span></span> <span data-ttu-id="6303b-111">Der _ulUIParam_ -Parameter muss NULL sein, wenn das AB_NO_DIALOG-Flag im _ulFlags_ -Parameter festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6303b-111">The  _ulUIParam_ parameter must be zero if the AB_NO_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="6303b-112">_lpProgress_</span><span class="sxs-lookup"><span data-stu-id="6303b-112">_lpProgress_</span></span>
  
> <span data-ttu-id="6303b-113">in Ein Zeiger auf ein Progress-Objekt, das eine Statusanzeige oder NULL anzeigt.</span><span class="sxs-lookup"><span data-stu-id="6303b-113">[in] A pointer to a progress object that displays a progress indicator, or NULL.</span></span> <span data-ttu-id="6303b-114">Wenn _lpProgress_ ist, sollte eine Statusanzeige mithilfe des von MAPI über die [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode bereitgestellten Progress-Objekts angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="6303b-114">If  _lpProgress_ is NULL, a progress indicator should be displayed by using the progress object supplied by MAPI through the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method.</span></span> <span data-ttu-id="6303b-115">Der _lpProgress_ -Parameter wird ignoriert, wenn das AB_NO_DIALOG-Flag in _ulFlags_festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6303b-115">The  _lpProgress_ parameter is ignored if the AB_NO_DIALOG flag is set in  _ulFlags_.</span></span>
    
 <span data-ttu-id="6303b-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6303b-116">_ulFlags_</span></span>
  
> <span data-ttu-id="6303b-117">in Eine Bitmaske von Flags, die die Ausführung des Kopiervorgangs steuert.</span><span class="sxs-lookup"><span data-stu-id="6303b-117">[in] A bitmask of flags that controls how the copy operation is performed.</span></span> <span data-ttu-id="6303b-118">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="6303b-118">The following flags can be set:</span></span>
    
<span data-ttu-id="6303b-119">AB_NO_DIALOG</span><span class="sxs-lookup"><span data-stu-id="6303b-119">AB_NO_DIALOG</span></span> 
  
> <span data-ttu-id="6303b-120">UnterDrückt die Anzeige einer Statusanzeige.</span><span class="sxs-lookup"><span data-stu-id="6303b-120">Suppresses display of a progress indicator.</span></span> <span data-ttu-id="6303b-121">Wenn dieses Flag nicht festgelegt ist, wird eine Statusanzeige angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6303b-121">If this flag is not set, a progress indicator is displayed.</span></span>
    
<span data-ttu-id="6303b-122">CREATE_CHECK_DUP_LOOSE</span><span class="sxs-lookup"><span data-stu-id="6303b-122">CREATE_CHECK_DUP_LOOSE</span></span> 
  
> <span data-ttu-id="6303b-123">Gibt an, dass eine Überprüfung der doppelten Eingabe durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6303b-123">Indicates that a loose level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="6303b-124">Die Implementierung von Loose Duplicate entry checking ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="6303b-124">The implementation of loose duplicate entry checking is provider specific.</span></span> <span data-ttu-id="6303b-125">Ein Anbieter kann beispielsweise eine lockere Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6303b-125">For example, a provider can define a loose match as any two entries that have the same display name.</span></span>
    
<span data-ttu-id="6303b-126">CREATE_CHECK_DUP_STRICT</span><span class="sxs-lookup"><span data-stu-id="6303b-126">CREATE_CHECK_DUP_STRICT</span></span> 
  
> <span data-ttu-id="6303b-127">Gibt an, dass eine strikte doppelte Eingabeüberprüfung durchgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6303b-127">Indicates that a strict level of duplicate entry checking should be performed.</span></span> <span data-ttu-id="6303b-128">Die Implementierung einer strengen doppelten Eintrags Überprüfung ist Anbieter spezifisch.</span><span class="sxs-lookup"><span data-stu-id="6303b-128">The implementation of strict duplicate entry checking is provider specific.</span></span> <span data-ttu-id="6303b-129">Ein Anbieter kann beispielsweise eine strikte Übereinstimmung als zwei Einträge definieren, die den gleichen Anzeigenamen und die gleiche Messaging Adresse aufweisen.</span><span class="sxs-lookup"><span data-stu-id="6303b-129">For example, a provider can define a strict match as any two entries that have both the same display name and messaging address.</span></span>
    
<span data-ttu-id="6303b-130">CREATE_REPLACE</span><span class="sxs-lookup"><span data-stu-id="6303b-130">CREATE_REPLACE</span></span> 
  
> <span data-ttu-id="6303b-131">Gibt an, dass ein neuer Eintrag eine vorhandene ersetzen soll, wenn festgestellt wird, dass die beiden Duplikate sind.</span><span class="sxs-lookup"><span data-stu-id="6303b-131">Indicates that a new entry should replace an existing one if it is determined that the two are duplicates.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6303b-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6303b-132">Return value</span></span>

<span data-ttu-id="6303b-133">S_OK</span><span class="sxs-lookup"><span data-stu-id="6303b-133">S_OK</span></span> 
  
> <span data-ttu-id="6303b-134">Der Kopiervorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="6303b-134">The copy operation succeeded.</span></span>
    
<span data-ttu-id="6303b-135">MAPI_W_PARTIAL_COMPLETION</span><span class="sxs-lookup"><span data-stu-id="6303b-135">MAPI_W_PARTIAL_COMPLETION</span></span> 
  
> <span data-ttu-id="6303b-136">Der Kopiervorgang war insgesamt erfolgreich, aber mindestens einer der Einträge konnte nicht kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="6303b-136">The copy operation succeeded overall, but one or more of the entries could not be copied.</span></span> <span data-ttu-id="6303b-137">Wenn dieser Wert zurückgegeben wird, sollte der Aufruf als erfolgreich behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="6303b-137">When this value is returned, the call should be handled as successful.</span></span> <span data-ttu-id="6303b-138">Verwenden Sie das **HR_FAILED** -Makro, um diesen Wert zu testen.</span><span class="sxs-lookup"><span data-stu-id="6303b-138">To test for this value, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="6303b-139">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="6303b-139">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6303b-140">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6303b-140">Remarks</span></span>

<span data-ttu-id="6303b-141">Die **IABContainer:: CopyEntries** -Methode kopiert Einträge aus demselben Container oder aus einem anderen Container.</span><span class="sxs-lookup"><span data-stu-id="6303b-141">The **IABContainer::CopyEntries** method copies entries from the same container or a different container.</span></span> <span data-ttu-id="6303b-142">Ein Aufruf von **CopyEntries** ist funktionell gleichbedeutend mit der folgenden Aufrufe für jeden Eintrag kopiert werden:</span><span class="sxs-lookup"><span data-stu-id="6303b-142">A call to **CopyEntries** is functionally equivalent to making the following calls for each entry to be copied:</span></span> 
  
1. <span data-ttu-id="6303b-143">Die [IABContainer:: CreateEntry](iabcontainer-createentry.md) -Methode zum Erstellen des neuen Eintrags.</span><span class="sxs-lookup"><span data-stu-id="6303b-143">The [IABContainer::CreateEntry](iabcontainer-createentry.md) method to create the new entry.</span></span> 
    
2. <span data-ttu-id="6303b-144">Die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode zum Lesen von Eigenschaften aus dem zu kopierenden Eintrag.</span><span class="sxs-lookup"><span data-stu-id="6303b-144">The [IMAPIProp::GetProps](imapiprop-getprops.md) method to read properties from the entry to be copied.</span></span> 
    
3. <span data-ttu-id="6303b-145">Die [IMAPIProp::](imapiprop-setprops.md) SetProps-Methode zum Schreiben von Eigenschaften in den neuen Eintrag.</span><span class="sxs-lookup"><span data-stu-id="6303b-145">The [IMAPIProp::SetProps](imapiprop-setprops.md) method to write properties to the new entry.</span></span> 
    
4. <span data-ttu-id="6303b-146">Die [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) -Methode des neuen Eintrags zum Durchführen eines Speichers.</span><span class="sxs-lookup"><span data-stu-id="6303b-146">The new entry's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method to perform a save.</span></span> 
    
5. <span data-ttu-id="6303b-147">Die [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) -Methode des neuen Eintrags zum Freigeben des Container-Verweises.</span><span class="sxs-lookup"><span data-stu-id="6303b-147">The new entry's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28VS.85%29.aspx) method to release the container's reference.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="6303b-148">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="6303b-148">Notes to implementers</span></span>

<span data-ttu-id="6303b-149">Alle Container, die die **IABContainer:: CopyEntries** -Methode unterstützen, müssen geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="6303b-149">All containers that support the **IABContainer::CopyEntries** method must be modifiable.</span></span> <span data-ttu-id="6303b-150">Legen Sie das AB_MODIFIABLE-Flag ihres Containers in seiner **PR_CONTAINER_FLAGS** ([pidtagcontainerflags (](pidtagcontainerflags-canonical-property.md))-Eigenschaft fest, um anzugeben, dass es veränderbar ist.</span><span class="sxs-lookup"><span data-stu-id="6303b-150">Set your container's AB_MODIFIABLE flag in its **PR_CONTAINER_FLAGS** ([PidTagContainerFlags](pidtagcontainerflags-canonical-property.md)) property to indicate that it is modifiable.</span></span> 
  
<span data-ttu-id="6303b-151">Sie müssen alle Flags unterstützen. die Interpretation und Verwendung dieser Flags ist jedoch implementierungsspezifisch, d. h., Sie können bestimmen, welche Semantik die Flags CREATE_CHECK_DUP_LOOSE und CREATE_CHECK_DUP_STRICT im Kontext ihrer Implementierung bedeuten.</span><span class="sxs-lookup"><span data-stu-id="6303b-151">You must support all of the flags; however, the interpretation and use of these flags is implementation specific—that is, you can determine what the semantics of the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags mean in the context of your implementation.</span></span> <span data-ttu-id="6303b-152">Wenn Sie nicht feststellen können, ob ein Eintrag ein Duplikat ist, können Sie immer zulassen, dass der Eintrag kopiert wird.</span><span class="sxs-lookup"><span data-stu-id="6303b-152">If you cannot or do not determine whether an entry is a duplicate, always allow the entry to be copied.</span></span> 
  
<span data-ttu-id="6303b-153">Wenn das CREATE_REPLACE-Flag festgelegt ist, kopieren Sie den Eintrag immer unabhängig davon, ob CREATE_CHECK_DUP_LOOSE oder CREATE_CHECK_DUP_STRICT festgelegt ist und ob der Eintrag ein Duplikat ist.</span><span class="sxs-lookup"><span data-stu-id="6303b-153">If the CREATE_REPLACE flag is set, always copy the entry regardless of whether CREATE_CHECK_DUP_LOOSE or CREATE_CHECK_DUP_STRICT is set and whether the entry is a duplicate.</span></span> 
  
<span data-ttu-id="6303b-154">Wenn CREATE_REPLACE nicht festgelegt ist und CREATE_CHECK_DUP_STRICT festgelegt ist, überprüfen Sie, ob Duplikate vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="6303b-154">If CREATE_REPLACE is not set and CREATE_CHECK_DUP_STRICT is set, check for duplicates.</span></span> <span data-ttu-id="6303b-155">Wenn ein Eintrag als Duplikat festgelegt wurde, kopieren Sie den Eintrag nicht.</span><span class="sxs-lookup"><span data-stu-id="6303b-155">If an entry is determined to be a duplicate, do not copy the entry.</span></span> 
  
<span data-ttu-id="6303b-156">Sie müssen CREATE_REPLACE nicht unterstützen; nicht die Unterstützung von CREATE_REPLACE, dass Sie Sie bedenkenlos ignorieren und immer eine Kopie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="6303b-156">You do not need to support CREATE_REPLACE; not supporting CREATE_REPLACE means that you can safely ignore it and always perform a copy.</span></span> 
  
<span data-ttu-id="6303b-157">Geben Sie die Warnung MAPI_W_PARTIAL_COMPLETION nur dann zurück, wenn ein nicht doppelter Eintrag nicht kopiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="6303b-157">Return the warning MAPI_W_PARTIAL_COMPLETION only if a nonduplicate entry cannot be copied.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6303b-158">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="6303b-158">Notes to callers</span></span>

<span data-ttu-id="6303b-159">Verwenden Sie die CREATE_CHECK_DUP_LOOSE-und CREATE_CHECK_DUP_STRICT-Flags, um dem Anbieter anzuzeigen, wie der Container die Überprüfung durch doppelte Eingabe ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="6303b-159">Use the CREATE_CHECK_DUP_LOOSE and CREATE_CHECK_DUP_STRICT flags to indicate to the provider how you want the container to perform duplicate-entry checking.</span></span> <span data-ttu-id="6303b-160">Wenn ein Eintrag hinzugefügt werden muss, unabhängig davon, ob es sich um ein Duplikat handelt, legen Sie entweder keine dieser Flags fest oder legen Sie das CREATE_REPLACE-Flag fest.</span><span class="sxs-lookup"><span data-stu-id="6303b-160">If you need to have an entry added regardless of whether it is a duplicate, either do not set either of these flags or set the CREATE_REPLACE flag.</span></span> <span data-ttu-id="6303b-161">CREATE_REPLACE gibt an, dass es Ihnen egal ist, ob ein Eintrag ein Duplikat ist; Sie möchten immer, dass der ursprüngliche Eintrag ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="6303b-161">CREATE_REPLACE indicates that you do not care if an entry is a duplicate; you always want it to replace the original entry.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6303b-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6303b-162">See also</span></span>



[<span data-ttu-id="6303b-163">ENTRYLIST</span><span class="sxs-lookup"><span data-stu-id="6303b-163">ENTRYLIST</span></span>](entrylist.md)
  
[<span data-ttu-id="6303b-164">IABContainer::CreateEntry</span><span class="sxs-lookup"><span data-stu-id="6303b-164">IABContainer::CreateEntry</span></span>](iabcontainer-createentry.md)
  
[<span data-ttu-id="6303b-165">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6303b-165">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="6303b-166">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="6303b-166">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="6303b-167">IABContainer : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="6303b-167">IABContainer : IMAPIContainer</span></span>](iabcontainerimapicontainer.md)

