---
title: OpenIMsgOnIStg
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OpenIMsgOnIStg
api_type:
- HeaderDef
ms.assetid: a98b0b26-9b19-44ca-9b4e-0ad4d1c54325
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406521"
---
# <a name="openimsgonistg"></a><span data-ttu-id="0157c-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="0157c-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="0157c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0157c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0157c-105">Erstellt ein neues [IMessage-Objekt](imessageimapiprop.md) auf einem vorhandenen OLE **IStorage-Objekt,** das in einer Nachrichtensitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0157c-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0157c-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0157c-106">Header file:</span></span>  <br/> |<span data-ttu-id="0157c-107">Imessage.h</span><span class="sxs-lookup"><span data-stu-id="0157c-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="0157c-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0157c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0157c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0157c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0157c-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0157c-110">Called by:</span></span>  <br/> |<span data-ttu-id="0157c-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0157c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE OpenIMsgOnIStg(
  LPMSGSESS lpMsgSess,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  LPMALLOC lpmalloc,
  LPVOID lpMapiSup,
  LPSTORAGE lpStg,
  MSGCALLRELEASE FAR * lpfMsgCallRelease,
  ULONG ulCallerData,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMsg
);
```

## <a name="parameters"></a><span data-ttu-id="0157c-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0157c-112">Parameters</span></span>

<span data-ttu-id="0157c-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="0157c-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="0157c-114">[in] Zeiger auf ein Nachrichtensitzungsobjekt, in dem das neue IMessage-on-IStorage-Objekt erstellt werden soll.  </span><span class="sxs-lookup"><span data-stu-id="0157c-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="0157c-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="0157c-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="0157c-116">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0157c-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="0157c-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="0157c-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="0157c-118">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die zum Zuordnen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0157c-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="0157c-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="0157c-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="0157c-120">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0157c-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="0157c-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="0157c-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="0157c-122">[in] Zeiger auf ein Speicherzuweisungsobjekt, das die OLE **IMalloc-Schnittstelle verfügbar** machen soll.</span><span class="sxs-lookup"><span data-stu-id="0157c-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="0157c-123">Die **IMessage-Schnittstelle** muss diese Zuordnungsmethode beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream verwenden.**</span><span class="sxs-lookup"><span data-stu-id="0157c-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="0157c-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="0157c-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="0157c-125">[in] Optionaler Zeiger auf ein MAPI-Unterstützungsobjekt, das ein Dienstanbieter zum Aufrufen der Methoden der [IMAPISupport : IUnknown-Schnittstelle verwenden](imapisupportiunknown.md) kann.</span><span class="sxs-lookup"><span data-stu-id="0157c-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="0157c-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="0157c-126">_lpStg_</span></span>
  
> <span data-ttu-id="0157c-127">[in, out] Zeiger auf ein OLE **IStorage-Objekt,** das geöffnet ist und über schreibgeschützte Oder Lese-/Schreibberechtigungen verfügt.</span><span class="sxs-lookup"><span data-stu-id="0157c-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="0157c-128">Da **IMessage** keinen Schreibzugriff unterstützt, akzeptiert **OpenIMsgOnIStg** kein Speicherobjekt, das im Schreibmodus geöffnet wird.</span><span class="sxs-lookup"><span data-stu-id="0157c-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="0157c-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="0157c-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="0157c-130">[in] Optionaler Zeiger auf eine Rückruffunktion basierend auf dem [MSGCALLRELEASE-Prototyp,](msgcallrelease.md) den MAPI nach der letzten Version des **IMessage**-on-IStorage-Objekts **aufrufen** soll.</span><span class="sxs-lookup"><span data-stu-id="0157c-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="0157c-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="0157c-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="0157c-132">[in] Aufruferdaten, die von MAPI mit dem IMessage-on-IStorage-Objekt **gespeichert** und an die **MSGCALLRELEASE-basierte** Rückruffunktion übergeben werden. </span><span class="sxs-lookup"><span data-stu-id="0157c-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="0157c-133">Die Daten bieten Kontext zum **freigegebenen IMessage-Objekt** und zum **IStorage-Objekt,** auf dem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="0157c-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="0157c-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0157c-134">_ulFlags_</span></span>
  
> <span data-ttu-id="0157c-135">[in] Bitmaske von Flags, die verwendet werden, um zu steuern, ob die OLE **IStorage::Commit-Methode** aufgerufen wird, wenn die Clientanwendung oder der Dienstanbieter die **IMessage::SaveChanges-Methode** aufruft.</span><span class="sxs-lookup"><span data-stu-id="0157c-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="0157c-136">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="0157c-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="0157c-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="0157c-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="0157c-138">Die **OLE-Methode IStorage::Commit** darf nicht aufgerufen werden, wenn der Client oder Anbieter [SaveChanges aufruft.](imapiprop-savechanges.md)</span><span class="sxs-lookup"><span data-stu-id="0157c-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="0157c-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0157c-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="0157c-140">Ermöglicht das Erstellen von Unicode-MSG-Dateien.</span><span class="sxs-lookup"><span data-stu-id="0157c-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="0157c-141">Die resultierende [IMessage-Datei](imessageimapiprop.md) STORE_UNICODE_OK in ihrer [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="0157c-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="0157c-142">Das MAPI_UNICODE wird nur in dieser Funktion unter Outlook 2003 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0157c-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="0157c-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="0157c-143">_lppMsg_</span></span>
  
> <span data-ttu-id="0157c-144">[out] Zeiger auf einen Zeiger auf das geöffnete **IMessage-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="0157c-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="0157c-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0157c-145">Return value</span></span>

<span data-ttu-id="0157c-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="0157c-146">S_OK</span></span> 
  
> <span data-ttu-id="0157c-147">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="0157c-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0157c-148">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0157c-148">Remarks</span></span>

<span data-ttu-id="0157c-149">Auf Eigenschaftsattribute kann nur auf Eigenschaftsobjekte zugegriffen werden, d. h. auf Objekte, die die [IMAPIProp : IUnknown-Schnittstelle](imapipropiunknown.md) implementieren.</span><span class="sxs-lookup"><span data-stu-id="0157c-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="0157c-150">Um MAPI-Eigenschaften für ein strukturiertes OLE-Speicherobjekt verfügbar zu machen, erstellt **OpenIMsgOnIStg** ein [IMessage : IMAPIProp-Objekt](imessageimapiprop.md) über dem OLE **IStorage-Objekt.**</span><span class="sxs-lookup"><span data-stu-id="0157c-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="0157c-151">Die Eigenschaftenattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit [GetAttribIMsgOnIStg abgerufen werden.](getattribimsgonistg.md)</span><span class="sxs-lookup"><span data-stu-id="0157c-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0157c-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="0157c-152">Notes to callers</span></span>

<span data-ttu-id="0157c-153">Eine Nachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0157c-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="0157c-154">Wenn Sie einen gültigen  _lpMsgSess-Parameter_ angeben, wird sichergestellt, dass die neue Nachricht innerhalb einer Nachrichtensitzung erstellt wird, sodass sie geschlossen wird, wenn die Sitzung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="0157c-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="0157c-155">Wenn  _lpMsgSess_ NULL ist, wird die Nachricht unabhängig von jeder Nachrichtensitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="0157c-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="0157c-156">Wenn die Clientanwendung oder der Dienstanbieter, von der die Nachricht erstellt wurde, sie nicht sowie alle Anlagen und geöffneten Tabellen veröffentlicht, ist Arbeitsspeicher nicht mehr verfügbar und kann dazu führen, dass die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0157c-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="0157c-157">MAPI verwendet die Funktionen, auf die  _von lpAllocateBuffer_,  _lpAllocateMore_ und  _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und Deallocation, insbesondere zum Zuordnen von Arbeitsspeicher für Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="0157c-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="0157c-158">Die  _Zeiger lpAllocateBuffer,_  _lpAllocateMore_ und  _lpFreeBuffer_ sind optional, wenn die **OpenIMsgOnIStg-Funktion** mit einem gültigen  _lpMapiSup-Parameter_ aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0157c-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="0157c-159">Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI auch die OLE-Speicherzuordnung verwenden.</span><span class="sxs-lookup"><span data-stu-id="0157c-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="0157c-160">Weitere Informationen zu strukturierten OLE-Speicherobjekten und der OLE-Speicherzuweisung finden Sie unter  _OLE Programmer's Reference_.</span><span class="sxs-lookup"><span data-stu-id="0157c-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="0157c-161">Wenn ein gültiger Wert für  _lpMapiSup_ angegeben wird, unterstützt **IMessage** die MAPI_DIALOG- und ATTACH_DIALOG-Flags, indem die [IMAPISupport::D oProgressDialog-Methode](imapisupport-doprogressdialog.md) aufruft, um eine Statusbenutzeroberfläche für die [Methoden IMAPIProp::CopyTo](imapiprop-copyto.md) und [IMessage::D eleteAttach](imessage-deleteattach.md) zu liefern.</span><span class="sxs-lookup"><span data-stu-id="0157c-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="0157c-162">Darüber hinaus versucht die [IMessage::ModifyRecipients-Methode,](imessage-modifyrecipients.md) kurzfristige Eintragsbezeichner durch Aufrufen der [IMAPISupport::OpenAddressBook-Methode](imapisupport-openaddressbook.md) und Aufrufen des resultierenden Adressbuchobjekts in langfristige Eintragsbezeichner zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0157c-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="0157c-163">Wenn NULL für  _lpMapiSup_ übergeben wird, ignoriert **IMessage** MAPI_DIALOG und ATTACH_DIALOG und speichert kurzfristige Eintragsbezeichner ohne Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="0157c-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="0157c-164">Das **IStorage-Objekt,** auf das der  _lpStg-Parameter_ verweist, muss entweder im STGM_READ- oder STGM_READWRITE geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="0157c-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="0157c-165">Wenn der STGM_READWRITE verwendet wird, muss auch STGM_TRANSACTED festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="0157c-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="0157c-166">Die Rückruffunktion, auf die der  _lpfMsgCallRelease-Parameter_ verweist, ist optional. Sofern angegeben, sollte es auf dem [MSGCALLRELEASE-Funktionsprototyp](msgcallrelease.md) basieren.</span><span class="sxs-lookup"><span data-stu-id="0157c-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="0157c-167">Die **IMessage-Schnittstelle** ruft sie auf, wenn die Referenzanzahl des IMessage-on-IStorage-Objekts durch den letzten Aufruf der **Release-Methode** auf Null festgelegt ist.  </span><span class="sxs-lookup"><span data-stu-id="0157c-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="0157c-168">Die Rückruffunktion wird häufig verwendet, um die zugrunde liegende **IStorage-Schnittstelle frei** zu geben.</span><span class="sxs-lookup"><span data-stu-id="0157c-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="0157c-169">**IMessage** versucht nach dem Rückruf nicht, auf das **IStorage-Objekt** zu zugreifen, auf das der  _lpStg-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="0157c-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="0157c-170">Einige Clients oder Anbieter schreiben möglicherweise zusätzliche Daten in das **IStorage-Objekt** über das hinaus, was **IMessage** selbst schreibt, wenn seine [SaveChanges-Methode](imapiprop-savechanges.md) aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="0157c-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="0157c-171">Der Client oder Anbieter kann das IMSG_NO_ISTG_COMMIT verwenden, um zu verhindern, dass **IMessage** die OLE **IStorage::Commit-Methode** aufruft, während er einen **SaveChanges-Aufruf** verarbeitet. In diesem Fall muss der Client oder Anbieter selbst ein Commit für das **IStorage-Objekt** erstellen, wenn die zusätzlichen Daten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="0157c-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="0157c-172">Um dies zu unterstützen, garantiert die **IMessage-Implementierung,** alle substorages zu benennen, die im **IStorage-Objekt** erstellt werden, beginnend mit der Zeichenfolge "__", d. h. mit zwei Unterstrichen.</span><span class="sxs-lookup"><span data-stu-id="0157c-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="0157c-173">Der Client oder Anbieter kann Namenskollision vermeiden, indem er seine Unternamen aus diesem Namespace heraushalten.</span><span class="sxs-lookup"><span data-stu-id="0157c-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="0157c-174">MAPI definiert nicht das Verhalten mehrerer geöffneter Vorgänge, die für ein Unterobjekt einer Nachricht ausgeführt werden, z. B. eine Anlage, ein Datenstrom oder eine eingebettete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="0157c-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="0157c-175">MapI ermöglicht derzeit, dass ein bereits geöffnetes Unterobjekt erneut geöffnet wird, aber MAPI führt den open-Vorgang aus, indem die Referenzanzahl für das vorhandene open-Objekt erhöht und an den Client oder Anbieter zurückgezahlt wird, der die [IMessage::OpenAttach-](imessage-openattach.md) oder [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="0157c-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="0157c-176">Dies bedeutet, dass der für den ersten geöffneten Vorgang für ein Unterobjekt angeforderte Zugriff der Zugriff ist, der für alle nachfolgenden geöffneten Vorgänge bereitgestellt wird, unabhängig vom von den Vorgängen angeforderten Zugriff.</span><span class="sxs-lookup"><span data-stu-id="0157c-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="0157c-177">Das richtige Verfahren zum Platzieren einer Nachricht in einer Anlage ist das Aufrufen der [IMAPIProp::OpenProperty-Methode](imapiprop-openproperty.md) mit dem Schnittstellenbezeichner IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="0157c-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="0157c-178">**OpenProperty** unterstützt derzeit auch das Erstellen von Nachrichtenanlagen, die direkt auf der OLE **IStorage-Schnittstelle** verfügbar sind, d. h. mithilfe IID_IStorage Bezeichners.</span><span class="sxs-lookup"><span data-stu-id="0157c-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="0157c-179">**Der IStorage-Zugriff** wird unterstützt, um eine einfache Möglichkeit zu ermöglichen, ein Microsoft Word-Dokument in eine Anlage zu speichern, ohne es in die **OLE-IStream-Schnittstelle** oder von dieser zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="0157c-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="0157c-180">**IMessage** verhält sich jedoch möglicherweise nicht vorhersagbar, wenn **OpenIMsgOnIStg** einen **IStorage-Zeiger** auf die Anlagendaten übergeben wird und die Objekte dann in der falschen Reihenfolge freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0157c-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0157c-181">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="0157c-181">MFCMAPI reference</span></span>

<span data-ttu-id="0157c-182">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="0157c-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0157c-183">**Datei**</span><span class="sxs-lookup"><span data-stu-id="0157c-183">**File**</span></span>|<span data-ttu-id="0157c-184">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="0157c-184">**Function**</span></span>|<span data-ttu-id="0157c-185">**Comment**</span><span class="sxs-lookup"><span data-stu-id="0157c-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0157c-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="0157c-186">File.cpp</span></span>  <br/> |<span data-ttu-id="0157c-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="0157c-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="0157c-188">MFCMAPI verwendet die **OpenIMsgOnIStg-Methode,** um eine IMessage-Schnittstelle über der zu öffnen. MSG-Datei, damit die Datei mit MAPI bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0157c-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0157c-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0157c-189">See also</span></span>

- [<span data-ttu-id="0157c-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="0157c-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

