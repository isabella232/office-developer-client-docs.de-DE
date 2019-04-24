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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 6d5ed20e532f0893757cc46d9ea478c7b65acc86
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348615"
---
# <a name="openimsgonistg"></a><span data-ttu-id="1488f-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="1488f-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="1488f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1488f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1488f-105">Erstellt ein neues [IMessage](imessageimapiprop.md) -Objekt über einem vorhandenen OLE- **IStorage** -Objekt, das in einer nachrichtensitzung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1488f-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1488f-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="1488f-106">Header file:</span></span>  <br/> |<span data-ttu-id="1488f-107">IMessage. h</span><span class="sxs-lookup"><span data-stu-id="1488f-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="1488f-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="1488f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1488f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1488f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1488f-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="1488f-110">Called by:</span></span>  <br/> |<span data-ttu-id="1488f-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="1488f-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="1488f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="1488f-112">Parameters</span></span>

<span data-ttu-id="1488f-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="1488f-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="1488f-114">in Zeiger auf ein Nachrichten Sitzungsobjekt, in dem das neue **IMessage**-on- **IStorage** -Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1488f-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="1488f-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="1488f-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="1488f-116">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1488f-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="1488f-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="1488f-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="1488f-118">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die zum Zuweisen von zusätzlichem Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1488f-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="1488f-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="1488f-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="1488f-120">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1488f-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="1488f-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="1488f-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="1488f-122">in Zeiger auf ein Speicher Reservierungs Objekt, das die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="1488f-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="1488f-123">Die **IMessage** -Schnittstelle muss diese Zuordnungsmethode beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream**verwenden.</span><span class="sxs-lookup"><span data-stu-id="1488f-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="1488f-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="1488f-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="1488f-125">in Optionaler Zeiger auf ein MAPI-Unterstützungsobjekt, mit dem ein Dienstanbieter die Methoden der [IMAPISupport: IUnknown](imapisupportiunknown.md) -Schnittstelle aufrufen kann.</span><span class="sxs-lookup"><span data-stu-id="1488f-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="1488f-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="1488f-126">_lpStg_</span></span>
  
> <span data-ttu-id="1488f-127">[in, out] Zeiger auf ein OLE- **IStorage** -Objekt, das geöffnet ist und über Leseberechtigung oder Lese-/Schreibzugriff verfügt.</span><span class="sxs-lookup"><span data-stu-id="1488f-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="1488f-128">Da **IMessage** keinen schreibgeschützten Zugriff unterstützt, akzeptiert **OpenIMsgOnIStg** kein im schreibgeschützten Modus geöffnetes Speicherobjekt.</span><span class="sxs-lookup"><span data-stu-id="1488f-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="1488f-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="1488f-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="1488f-130">in Optionaler Zeiger auf eine Rückruffunktion basierend auf dem [MSGCALLRELEASE](msgcallrelease.md) -Prototyp, den MAPI nach der letzten Freigabe des **IMessage**-on- **IStorage** -Objekts aufrufen soll.</span><span class="sxs-lookup"><span data-stu-id="1488f-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="1488f-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="1488f-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="1488f-132">in Von MAPI gespeicherte Anrufer-Daten mit dem **IMessage**-on- **IStorage** -Objekt und an die **MSGCALLRELEASE** -basierte Rückruffunktion übergeben.</span><span class="sxs-lookup"><span data-stu-id="1488f-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="1488f-133">Die Daten bieten Kontext über das **IMessage** -Objekt, das freigegeben wird, und das **IStorage** -Objekt, auf dem es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="1488f-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="1488f-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1488f-134">_ulFlags_</span></span>
  
> <span data-ttu-id="1488f-135">in Bitmaske der Flags, mit denen gesteuert wird, ob die OLE **IStorage:: Commit** -Methode aufgerufen wird, wenn die Clientanwendung oder der Dienstanbieter die **IMessage:: SaveChanges** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="1488f-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="1488f-136">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1488f-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="1488f-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="1488f-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="1488f-138">Die OLE-Methode **IStorage:: Commit** kann nicht aufgerufen werden, wenn der Client oder Anbieter [SaveChanges](imapiprop-savechanges.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="1488f-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="1488f-139">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1488f-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="1488f-140">Ermöglicht die Erstellung von Unicode-msg-Dateien.</span><span class="sxs-lookup"><span data-stu-id="1488f-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="1488f-141">Die resultierende [IMessage](imessageimapiprop.md) -Datei zeigt STORE_UNICODE_OK in der [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) und unterstützt Unicode-Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="1488f-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="1488f-142">Das MAPI_UNICODE-Flag wird nur in dieser Funktion in Outlook 2003 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1488f-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="1488f-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="1488f-143">_lppMsg_</span></span>
  
> <span data-ttu-id="1488f-144">Out Zeiger auf einen Zeiger auf das geöffnete **IMessage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1488f-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1488f-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1488f-145">Return value</span></span>

<span data-ttu-id="1488f-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="1488f-146">S_OK</span></span> 
  
> <span data-ttu-id="1488f-147">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="1488f-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1488f-148">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1488f-148">Remarks</span></span>

<span data-ttu-id="1488f-149">Auf Eigenschaftsattribute kann nur über Property-Objekte zugegriffen werden, also auf Objekte, die die [IMAPIProp: IUnknown](imapipropiunknown.md) -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="1488f-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="1488f-150">Um MAPI-Eigenschaften für ein OLE Structured Storage-Objekt verfügbar zu machen, erstellt **OpenIMsgOnIStg** ein [IMessage: IMAPIProp](imessageimapiprop.md) -Objekt über dem OLE- **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="1488f-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="1488f-151">Die Eigenschaftsattribute für solche Objekte können mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) festgelegt oder geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="1488f-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1488f-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1488f-152">Notes to callers</span></span>

<span data-ttu-id="1488f-153">Eine nachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1488f-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="1488f-154">Durch Angeben eines gültigen _lpMsgSess_ -Parameters stellen Sie sicher, dass die neue Nachricht innerhalb einer nachrichtensitzung erstellt wird, damit Sie geschlossen wird, wenn die Sitzung geschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="1488f-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="1488f-155">Wenn _lpMsgSess_ ist, wird die Nachricht unabhängig von einer beliebigen nachrichtensitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="1488f-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="1488f-156">Wenn die Clientanwendung oder der Dienstanbieter, der die Nachricht erstellt hat, diese nicht freigibt, sowie alle Anhänge und geöffneten Tabellen, wird der Arbeitsspeicher geleckt und kann dazu führen, dass die Anwendung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="1488f-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="1488f-157">MAPI verwendet die Funktionen, auf die durch _lpAllocateBuffer_, _lpAllocateMore_und _lpFreeBuffer_ verwiesen wird, für die meisten Speicherzuweisungen und-Aufhebungen, insbesondere für die Zuweisung von Speicher für die Verwendung durch Clientanwendungen beim Aufrufen von Objektschnittstellen wie [IMAPIProp::](imapiprop-getprops.md) GetProps und [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="1488f-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="1488f-158">Die _lpAllocateBuffer_-, _LpAllocateMore_-und _lpFreeBuffer_ -Zeiger sind optional, wenn die **OpenIMsgOnIStg** -Funktion mit einem gültigen _lpMapiSup_ -Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1488f-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="1488f-159">Da es sich um ein zugrunde liegendes OLE-Objekt handelt, muss MAPI auch die OLE-Speicherbelegung verwenden.</span><span class="sxs-lookup"><span data-stu-id="1488f-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="1488f-160">Weitere Informationen zu OLE-strukturierten Speicherobjekten und zur OLE-Speicherzuordnung finden Sie unter _OLE Programmer es Reference_.</span><span class="sxs-lookup"><span data-stu-id="1488f-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="1488f-161">Wenn für _lpMapiSup_ein gültiger Wert angegeben wird, unterstützt **IMESSAGE** die Flags MAPI_DIALOG und ATTACH_DIALOG durch aufrufen der [IMAPISupport::D oprogressdialog](imapisupport-doprogressdialog.md) -Methode, um eine Fortschritts-Benutzeroberfläche für die [IMAPIProp:: CopyTo](imapiprop-copyto.md) bereitzustellen. und [IMessage::D eleteattach](imessage-deleteattach.md) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="1488f-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="1488f-162">Außerdem versucht die [IMessage:: ModifyRecipients](imessage-modifyrecipients.md) -Methode, kurzfristige Eintrags-IDs in langfristige Eintragsbezeichner zu konvertieren, indem die [IMAPISupport:: openaddressbook](imapisupport-openaddressbook.md) -Methode aufgerufen wird und Aufrufe für das resultierende Adressbuchobjekt durchführen.</span><span class="sxs-lookup"><span data-stu-id="1488f-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="1488f-163">Wenn NULL für _lpMapiSup_übergeben wird, ignoriert **IMESSAGE** MAPI_DIALOG und ATTACH_DIALOG und speichert kurzfristige Eintragsbezeichner ohne Konvertierung.</span><span class="sxs-lookup"><span data-stu-id="1488f-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="1488f-164">Das **IStorage** -Objekt, auf das durch den _lpStg_ -Parameter verwiesen wird, muss im STGM_READ-oder STGM_READWRITE-Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="1488f-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="1488f-165">Wenn der STGM_READWRITE-Modus verwendet wird, muss auch der STGM_TRANSACTED-Modus festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="1488f-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="1488f-166">Die Rückruffunktion, auf die durch den _lpfMsgCallRelease_ -Parameter verwiesen wird, ist optional; Wenn angegeben, sollte Sie auf dem Prototyp der [MSGCALLRELEASE](msgcallrelease.md) -Funktion basieren.</span><span class="sxs-lookup"><span data-stu-id="1488f-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="1488f-167">Die **IMessage** -Schnittstelle ruft Sie auf, wenn der Verweiszähler des **IMessage**-on- **IStorage** -Objekts durch den letzten Aufruf seiner **Release** -Methode auf NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="1488f-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="1488f-168">Die Callback-Funktion wird häufig verwendet, um die zugrunde liegende **IStorage** -Schnittstelle freizugeben.</span><span class="sxs-lookup"><span data-stu-id="1488f-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="1488f-169">**IMessage** versucht nicht, auf das **IStorage** -Objekt zuzugreifen, auf das durch den _lpStg_ -Parameter verwiesen wird, nachdem der Rückruf vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="1488f-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="1488f-170">Einige Clients oder Anbieter schreiben möglicherweise zusätzliche Daten in das **IStorage** -Objekt, über die **IMessage** selbst hinaus schreibt, wenn die [SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="1488f-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="1488f-171">Der Client oder Anbieter kann das IMSG_NO_ISTG_COMMIT-Flag verwenden, um zu verhindern, dass **IMessage** beim Verarbeiten eines **SaveChanges** -Aufrufs die OLE **IStorage:: Commit** -Methode aufruft. in diesem Fall muss der Client oder Anbieter selbst das **IStorage** -Objekt übertragen, wenn die zusätzlichen Daten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="1488f-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="1488f-172">Um dies zu unterstützen, stellt die **IMessage** -Implementierung sicher, dass alle unter Speicher, die im **IStorage** -Objekt erstellt werden, beginnend mit der Zeichenfolge "__", also mit zwei unterstrichen, benannt werden.</span><span class="sxs-lookup"><span data-stu-id="1488f-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="1488f-173">Der Client oder Anbieter kann Namenskonflikte vermeiden, indem er seine unter Speichernamen aus diesem Namespace behält.</span><span class="sxs-lookup"><span data-stu-id="1488f-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="1488f-174">MAPI definiert nicht das Verhalten mehrerer geöffneter Vorgänge, die für ein Unterobjekt einer Nachricht ausgeführt werden, beispielsweise eine Anlage, einen Datenstrom oder eine eingebettete Nachricht.</span><span class="sxs-lookup"><span data-stu-id="1488f-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="1488f-175">MAPI ermöglicht derzeit, dass ein Unterobjekt, das bereits geöffnet ist, noch einmal geöffnet wird, aber MAPI führt den Öffnungsvorgang aus, indem er den Verweiszähler für das vorhandene Open-Objekt inkrementiert und an den Client oder Anbieter zurückgibt, der die IMessage:: openAttach-Funktion aufgerufen hat [. ](imessage-openattach.md)oder [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="1488f-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="1488f-176">Dies bedeutet, dass der für den ersten geöffneten Vorgang für ein Unterobjekt angeforderte Zugriff der Zugriff für alle nachfolgenden geöffneten Vorgänge ist, unabhängig davon, welcher Zugriff von den Vorgängen angefordert wird.</span><span class="sxs-lookup"><span data-stu-id="1488f-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="1488f-177">Das richtige Verfahren zum Platzieren einer Nachricht in einer Anlage besteht darin, die [IMAPIProp:: OpenProperty](imapiprop-openproperty.md) -Methode mit einem Schnittstellenbezeichner von IID_IMessage aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="1488f-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="1488f-178">**OpenProperty** unterstützt derzeit auch die Erstellung von Nachrichtenanlagen, die direkt auf der OLE- **IStorage** -Schnittstelle verfügbar sind, also mithilfe der IID_IStorage-Schnittstellenkennung.</span><span class="sxs-lookup"><span data-stu-id="1488f-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="1488f-179">**IStorage** -Zugriff wird unterstützt, um eine einfache Möglichkeit zum Einfügen eines Microsoft Word-Dokuments in eine Anlage zu ermöglichen, ohne Sie in die oder von der OLE **IStream** -Schnittstelle zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="1488f-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="1488f-180">**IMessage** reagiert möglicherweise nicht vorhersehbar, wenn **OpenIMsgOnIStg** einen **IStorage** -Zeiger auf die Anlagendaten übergeben wird und die Objekte dann in der falschen Reihenfolge freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1488f-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1488f-181">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="1488f-181">MFCMAPI reference</span></span>

<span data-ttu-id="1488f-182">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1488f-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1488f-183">**Datei**</span><span class="sxs-lookup"><span data-stu-id="1488f-183">**File**</span></span>|<span data-ttu-id="1488f-184">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="1488f-184">**Function**</span></span>|<span data-ttu-id="1488f-185">**Comment**</span><span class="sxs-lookup"><span data-stu-id="1488f-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1488f-186">Datei. cpp</span><span class="sxs-lookup"><span data-stu-id="1488f-186">File.cpp</span></span>  <br/> |<span data-ttu-id="1488f-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="1488f-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="1488f-188">MFCMAPI verwendet die **OpenIMsgOnIStg** -Methode, um eine IMessage-Schnittstelle über dem zu öffnen. MSG-Datei, sodass die Datei mit MAPI manipuliert werden kann.</span><span class="sxs-lookup"><span data-stu-id="1488f-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1488f-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1488f-189">See also</span></span>

- [<span data-ttu-id="1488f-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="1488f-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

