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
ms.openlocfilehash: 27a5978d85cf06a31f583b82cd39d0001852876b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793308"
---
# <a name="openimsgonistg"></a><span data-ttu-id="b721d-103">OpenIMsgOnIStg</span><span class="sxs-lookup"><span data-stu-id="b721d-103">OpenIMsgOnIStg</span></span>

<span data-ttu-id="b721d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b721d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b721d-105">Erstellt ein neues [IMessage](imessageimapiprop.md) -Objekt auf der Basis ein vorhandenes OLE **IStorage** -Objekt in einer Nachricht Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-105">Builds a new [IMessage](imessageimapiprop.md) object on top of an existing OLE **IStorage** object, to be used within a message session.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b721d-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="b721d-106">Header file:</span></span>  <br/> |<span data-ttu-id="b721d-107">IMessage.h</span><span class="sxs-lookup"><span data-stu-id="b721d-107">Imessage.h</span></span>  <br/> |
|<span data-ttu-id="b721d-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="b721d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b721d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b721d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b721d-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="b721d-110">Called by:</span></span>  <br/> |<span data-ttu-id="b721d-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="b721d-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="b721d-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="b721d-112">Parameters</span></span>

<span data-ttu-id="b721d-113">_lpMsgSess_</span><span class="sxs-lookup"><span data-stu-id="b721d-113">_lpMsgSess_</span></span>
  
> <span data-ttu-id="b721d-114">[in] Zeiger auf ein Objekt "Message" Sitzung innerhalb dessen ist die neue **IMessage**- auf - **IStorage** -Objekt erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b721d-114">[in] Pointer to a message session object within which the new **IMessage**-on- **IStorage** object is to be created.</span></span> 
    
<span data-ttu-id="b721d-115">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="b721d-115">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="b721d-116">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b721d-116">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
<span data-ttu-id="b721d-117">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="b721d-117">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="b721d-118">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
<span data-ttu-id="b721d-119">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="b721d-119">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="b721d-120">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="b721d-120">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
<span data-ttu-id="b721d-121">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="b721d-121">_lpMalloc_</span></span>
  
> <span data-ttu-id="b721d-122">[in] Zeiger auf ein Speicherobjekt-Zuweisung die OLE **IMalloc** -Schnittstelle verfügbar macht.</span><span class="sxs-lookup"><span data-stu-id="b721d-122">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="b721d-123">Die **IMessage** -Schnittstelle muss beim Arbeiten mit Schnittstellen wie **IStorage** und **IStream**diese Zuordnungsmethode verwenden.</span><span class="sxs-lookup"><span data-stu-id="b721d-123">The **IMessage** interface needs to use this allocation method when working with interfaces such as **IStorage** and **IStream**.</span></span> 
    
<span data-ttu-id="b721d-124">_lpMapiSup_</span><span class="sxs-lookup"><span data-stu-id="b721d-124">_lpMapiSup_</span></span>
  
> <span data-ttu-id="b721d-125">[in] Optionaler Zeiger auf ein MAPI-Support-Objekt, das ein Dienstanbieter verwenden kann, die Methoden des Aufrufen der [IMAPISupport: IUnknown](imapisupportiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b721d-125">[in] Optional pointer to a MAPI support object that a service provider can use to call the methods of the [IMAPISupport : IUnknown](imapisupportiunknown.md) interface.</span></span> 
    
<span data-ttu-id="b721d-126">_lpStg_</span><span class="sxs-lookup"><span data-stu-id="b721d-126">_lpStg_</span></span>
  
> <span data-ttu-id="b721d-127">[in, out] Zeiger auf ein OLE- **IStorage** -Objekt, das geöffnet ist und hat schreibgeschützte oder Lese-/Schreibberechtigung.</span><span class="sxs-lookup"><span data-stu-id="b721d-127">[in, out] Pointer to an OLE **IStorage** object that is open and has read-only or read/write permission.</span></span> <span data-ttu-id="b721d-128">Da **IMessage** lesegeschützt nicht unterstützt werden, akzeptiert **OpenIMsgOnIStg** kein Speicherobjekt im Schreibzugriff-Modus geöffnet.</span><span class="sxs-lookup"><span data-stu-id="b721d-128">Because **IMessage** does not support write-only access, **OpenIMsgOnIStg** does not accept a storage object opened in write-only mode.</span></span> 
    
<span data-ttu-id="b721d-129">_lpfMsgCallRelease_</span><span class="sxs-lookup"><span data-stu-id="b721d-129">_lpfMsgCallRelease_</span></span>
  
> <span data-ttu-id="b721d-130">[in] Optional Zeiger auf eine Rückruffunktion, die basierend auf den [MSGCALLRELEASE](msgcallrelease.md) Prototyp, die MAPI nach der letzten Version für die **IMessage**- auf - **IStorage** -Objekt aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b721d-130">[in] Optional pointer to a callback function based on the [MSGCALLRELEASE](msgcallrelease.md) prototype that MAPI is to call following the last release on the **IMessage**-on- **IStorage** object.</span></span> 
    
<span data-ttu-id="b721d-131">_ulCallerData_</span><span class="sxs-lookup"><span data-stu-id="b721d-131">_ulCallerData_</span></span>
  
> <span data-ttu-id="b721d-132">[in] Anrufer-Daten von MAPI mit dem **IMessage**- auf - **IStorage** -Objekt gespeichert und an die **MSGCALLRELEASE** übergebenen basieren Callback-Funktion.</span><span class="sxs-lookup"><span data-stu-id="b721d-132">[in] Caller data saved by MAPI with the **IMessage**-on- **IStorage** object and passed to the **MSGCALLRELEASE** based callback function.</span></span> <span data-ttu-id="b721d-133">Die Daten enthält Kontext zu den **IMessage** -Objekts, das freigegeben und das **IStorage** -Objekt auf der Basis, das es erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="b721d-133">The data provides context about the **IMessage** object being released and the **IStorage** object on top of which it was built.</span></span> 
    
<span data-ttu-id="b721d-134">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b721d-134">_ulFlags_</span></span>
  
> <span data-ttu-id="b721d-135">[in] Bitmaske von Flags Steuerelement, ob die OLE- **IStorage::Commit** -Methode aufgerufen wird, wenn die Clientanwendung oder -Dienstanbieter die **IMessage::SaveChanges** -Methode aufruft.</span><span class="sxs-lookup"><span data-stu-id="b721d-135">[in] Bitmask of flags used to control whether the OLE **IStorage::Commit** method is called when the client application or service provider calls the **IMessage::SaveChanges** method.</span></span> <span data-ttu-id="b721d-136">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="b721d-136">The following flags can be set:</span></span> 
    
<span data-ttu-id="b721d-137">IMSG_NO_ISTG_COMMIT</span><span class="sxs-lookup"><span data-stu-id="b721d-137">IMSG_NO_ISTG_COMMIT</span></span> 
  
> <span data-ttu-id="b721d-138">Die OLE-Methode **IStorage::Commit** darf nicht aufgerufen werden, wenn der Client oder Anbieter [SaveChanges](imapiprop-savechanges.md)aufruft.</span><span class="sxs-lookup"><span data-stu-id="b721d-138">The OLE method **IStorage::Commit** is not to be called when the client or provider calls [SaveChanges](imapiprop-savechanges.md).</span></span> 
    
<span data-ttu-id="b721d-139">PARAMETER MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b721d-139">MAPI_UNICODE</span></span>
  
> <span data-ttu-id="b721d-140">Ermöglicht die Erstellung von Unicode-MSG-Dateien.</span><span class="sxs-lookup"><span data-stu-id="b721d-140">Enables creation of Unicode .msg files.</span></span> <span data-ttu-id="b721d-141">Die resultierende [IMessage](imessageimapiprop.md) Datei zeigt STORE_UNICODE_OK in seiner [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) und Unicode-Eigenschaften unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b721d-141">The resulting [IMessage](imessageimapiprop.md) file shows STORE_UNICODE_OK in its [PR_STORE_SUPPORT_MASK](pidtagstoresupportmask-canonical-property.md) and supports Unicode properties.</span></span> 
    
  > [!NOTE]
  > <span data-ttu-id="b721d-142">Die Option MAPI_UNICODE wird nur in dieser Funktion auf Outlook 2003 oder höher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="b721d-142">The MAPI_UNICODE flag is only supported in this function on Outlook 2003 or higher.</span></span> 
  
<span data-ttu-id="b721d-143">_lppMsg_</span><span class="sxs-lookup"><span data-stu-id="b721d-143">_lppMsg_</span></span>
  
> <span data-ttu-id="b721d-144">[out] Zeiger auf einen Zeiger auf das geöffnete **IMessage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b721d-144">[out] Pointer to a pointer to the opened **IMessage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b721d-145">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b721d-145">Return value</span></span>

<span data-ttu-id="b721d-146">S_OK</span><span class="sxs-lookup"><span data-stu-id="b721d-146">S_OK</span></span> 
  
> <span data-ttu-id="b721d-147">Der Aufruf erfolgreich ausgef�hrt und der erwartete Wert oder Werte zur�ckgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="b721d-147">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b721d-148">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b721d-148">Remarks</span></span>

<span data-ttu-id="b721d-149">Eigenschaftsattribute nur auf Property-Objekte, d. h., durch Implementieren Objekte zugegriffen werden können die [IMAPIProp: IUnknown](imapipropiunknown.md) Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b721d-149">Property attributes can only be accessed on property objects, that is, objects implementing the [IMAPIProp : IUnknown](imapipropiunknown.md) interface.</span></span> <span data-ttu-id="b721d-150">MAPI-Eigenschaften für ein OLE-Objekt strukturierter Speicher zur Verfügung zu stellen, **OpenIMsgOnIStg** erstellt eine [IMessage: IMAPIProp](imessageimapiprop.md) Objekt auf der Basis der OLE- **IStorage** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="b721d-150">To make MAPI properties available on an OLE structured storage object, **OpenIMsgOnIStg** builds an [IMessage : IMAPIProp](imessageimapiprop.md) object on top of the OLE **IStorage** object.</span></span> <span data-ttu-id="b721d-151">Die Eigenschaftenattribute für solche Objekte können festgelegt oder mit [SetAttribIMsgOnIStg](setattribimsgonistg.md) geändert und mit [GetAttribIMsgOnIStg](getattribimsgonistg.md)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-151">The property attributes on such objects can be set or altered with [SetAttribIMsgOnIStg](setattribimsgonistg.md) and retrieved with [GetAttribIMsgOnIStg](getattribimsgonistg.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b721d-152">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b721d-152">Notes to callers</span></span>

<span data-ttu-id="b721d-153">Eine Sofortnachrichtensitzung sollte mit [OpenIMsgSession](openimsgsession.md) geöffnet werden, bevor **OpenIMsgOnIStg** aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b721d-153">A message session should be opened with [OpenIMsgSession](openimsgsession.md) before **OpenIMsgOnIStg** is called.</span></span> <span data-ttu-id="b721d-154">Einen gültigen _LpMsgSess_ -Parameter stellen mit Sures, dass die neue Nachricht wird innerhalb einer Sofortnachrichtensitzung erstellt, sodass es geschlossen wird, wenn die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b721d-154">Supplying a valid  _lpMsgSess_ parameter make sures that the new message is created within a message session so that it is closed when the session is closed.</span></span> <span data-ttu-id="b721d-155">Wenn _LpMsgSess_ NULL ist, wird die Nachricht unabhängig von einer Nachricht Sitzung erstellt.</span><span class="sxs-lookup"><span data-stu-id="b721d-155">If  _lpMsgSess_ is NULL, the message is created independently of any message session.</span></span> <span data-ttu-id="b721d-156">Wenn der Clientanwendung oder Dienstanbieter, die die Nachricht erstellt nicht, er als auch alle zugehörigen Anlagen freigegeben und Tabellen öffnen, Arbeitsspeicher ist verloren und beenden die Anwendung verursachen.</span><span class="sxs-lookup"><span data-stu-id="b721d-156">If the client application or service provider that created the message does not release it, as well as all its attachments and open tables, memory is leaked and may cause the application to terminate.</span></span> 
  
<span data-ttu-id="b721d-157">MAPI verwendet, die auf den _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ für die meisten Zuweisung von virtuellem Speicher und zur Freigabe, insbesondere für die Verwendung von Clientanwendungen Speicher beim Aufruf von Schnittstellen, um Funktionen wie [IMAPIProp::GetProps](imapiprop-getprops.md) und [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="b721d-157">MAPI uses the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation, in particular to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="b721d-158">Die _LpAllocateBuffer_, _LpAllocateMore_und _LpFreeBuffer_ Zeiger sind optional, wenn die Funktion **OpenIMsgOnIStg** mit einem gültigen _LpMapiSup_ Parameter aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b721d-158">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ pointers are optional when the **OpenIMsgOnIStg** function is called with a valid  _lpMapiSup_ parameter.</span></span> 
  
<span data-ttu-id="b721d-159">Da Umgang mit einem zugrunde liegenden OLE-Objekt muss MAPI auch OLE Zuweisung von virtuellem Speicher verwenden.</span><span class="sxs-lookup"><span data-stu-id="b721d-159">Because it is dealing with an underlying OLE object, MAPI also needs to use OLE memory allocation.</span></span> <span data-ttu-id="b721d-160">Weitere Informationen zu OLE-strukturierte Speicherobjekte und OLE-arbeitsspeicherreservierung, finden Sie unter der _OLE Programmer's Reference_.</span><span class="sxs-lookup"><span data-stu-id="b721d-160">For more information about OLE structured storage objects and OLE memory allocation, see the  _OLE Programmer's Reference_.</span></span> 
  
<span data-ttu-id="b721d-161">Wenn Sie ein gültiger Wert für _LpMapiSup_angegeben ist, unterstützt **IMessage** die Flags MAPI_DIALOG und ATTACH_DIALOG durch Aufrufen der [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) -Methode, um eine Benutzeroberfläche für die [IMAPIProp::CopyTo](imapiprop-copyto.md) bereitzustellen und [IMessage::DeleteAttach](imessage-deleteattach.md) -Methoden.</span><span class="sxs-lookup"><span data-stu-id="b721d-161">If a valid value is supplied for  _lpMapiSup_, **IMessage** supports the MAPI_DIALOG and ATTACH_DIALOG flags by calling the [IMAPISupport::DoProgressDialog](imapisupport-doprogressdialog.md) method to supply a progress user interface for the [IMAPIProp::CopyTo](imapiprop-copyto.md) and [IMessage::DeleteAttach](imessage-deleteattach.md) methods.</span></span> <span data-ttu-id="b721d-162">Darüber hinaus versucht die [IMessage::ModifyRecipients](imessage-modifyrecipients.md) -Methode, kurzfristige-Eintragsbezeichner durch Aufrufen der [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) -Methode und tätigen von Anrufen auf das resultierende Address Book-Objekt in langfristige-Eintragsbezeichner zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="b721d-162">Also, the [IMessage::ModifyRecipients](imessage-modifyrecipients.md) method attempts to convert short-term entry identifiers to long-term entry identifiers by calling the [IMAPISupport::OpenAddressBook](imapisupport-openaddressbook.md) method and making calls on the resulting address book object.</span></span> <span data-ttu-id="b721d-163">**Wenn NULL für _LpMapiSup_übergeben wird, ignoriert MAPI_DIALOG und ATTACH_DIALOG IMessageund kurzfristige-Eintragsbezeichner ohne Konvertierung speichert.**</span><span class="sxs-lookup"><span data-stu-id="b721d-163">If NULL is passed for  _lpMapiSup_, **IMessage** ignores MAPI_DIALOG and ATTACH_DIALOG and stores short-term entry identifiers without conversion.</span></span> 
  
<span data-ttu-id="b721d-164">Das **IStorage** -Objekt, das durch den Parameter _LpStg_ auf muss in der Beispielcodezeilen oder Accessor-Modus geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-164">The **IStorage** object pointed to by the  _lpStg_ parameter must be opened in either the STGM_READ or STGM_READWRITE mode.</span></span> <span data-ttu-id="b721d-165">Wenn der Accessor-Modus verwendet wird, muss auch der STGM_TRANSACTED Modus festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-165">If the STGM_READWRITE mode is used, the STGM_TRANSACTED mode must also be set.</span></span> 
  
<span data-ttu-id="b721d-166">Auf den der _LpfMsgCallRelease_ -Parameter die Callback-Funktion ist optional. Wenn dieser Parameter sollte es für den [MSGCALLRELEASE](msgcallrelease.md) Funktionsprototyp basieren.</span><span class="sxs-lookup"><span data-stu-id="b721d-166">The callback function pointed to by the  _lpfMsgCallRelease_ parameter is optional; if provided, it should be based on the [MSGCALLRELEASE](msgcallrelease.md) function prototype.</span></span> <span data-ttu-id="b721d-167">Die **IMessage** -Schnittstelle wird aufgerufen, wenn die Anzahl der Verweise des **IStorage** **IMessage**- auf - Objekts durch den letzten Aufruf die **Release** -Methode NULL festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="b721d-167">The **IMessage** interface calls it when the reference count of the **IMessage**-on- **IStorage** object is set to zero by the last call to its **Release** method.</span></span> <span data-ttu-id="b721d-168">Die Callback-Funktion wird meist die zugrunde liegende **IStorage** -Schnittstelle frei.</span><span class="sxs-lookup"><span data-stu-id="b721d-168">The callback function is commonly used to free the underlying **IStorage** interface.</span></span> <span data-ttu-id="b721d-169">**IMessage** wird nicht versucht, auf das **IStorage** -Objekt, das durch den Parameter _LpStg_ nach dem Ändern des Rückrufs auf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="b721d-169">**IMessage** will not attempt to access the **IStorage** object pointed to by the  _lpStg_ parameter after making the callback.</span></span> 
  
<span data-ttu-id="b721d-170">Einige Clients oder Anbieter möglicherweise zusätzliche Daten schreiben auf das **IStorage** -Objekt über welche **IMessage** selbst schreibt die [SaveChanges](imapiprop-savechanges.md) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b721d-170">Some clients or providers might write additional data to the **IStorage** object beyond what **IMessage** itself writes when its [SaveChanges](imapiprop-savechanges.md) method is called.</span></span> <span data-ttu-id="b721d-171">Der Client oder Anbieter können das Flag IMSG_NO_ISTG_COMMIT **IMessage** verhindern, dass die OLE- **IStorage::Commit** -Methode aufrufen, während der Verarbeitung eines Anrufs **SaveChanges** . In diesem Fall muss der Client oder Anbieter selbst **IStorage** -Objekt Wenn ein commit für die zusätzlichen Daten geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-171">The client or provider can use the IMSG_NO_ISTG_COMMIT flag to prevent **IMessage** from calling the OLE **IStorage::Commit** method while processing a **SaveChanges** call; in this case the client or provider must itself commit the **IStorage** object when the additional data is written.</span></span> <span data-ttu-id="b721d-172">Um dies zu erleichtern, garantiert die Implementierung **IMessage** nennen Sie alle Substorages im beginnend mit der Zeichenfolge "_", d. h., mit zwei unterstrichen **IStorage** -Objekt erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b721d-172">To aid in this, the **IMessage** implementation guarantees to name all substorages it creates in the **IStorage** object starting with the string "__", that is, with two underscores.</span></span> <span data-ttu-id="b721d-173">Der Client oder Anbieter kann Namenskonflikte vermeiden, indem Sie seine Substorage Namen aus diesem Namespace beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b721d-173">The client or provider can avoid name collisions by keeping its substorage names out of this namespace.</span></span> 
  
<span data-ttu-id="b721d-174">MAPI definiert nicht das Verhalten von mehreren open-Vorgängen für eine-Unterobjekt einer Nachricht, wie eine Anlage, einen Datenstrom oder eingebettete Nachricht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b721d-174">MAPI does not define the behavior of multiple open operations performed on a subobject of a message, such as an attachment, a stream, or an embedded message.</span></span> <span data-ttu-id="b721d-175">MAPI ermöglicht derzeit ein Unterobjekt, die noch einmal geöffnet werden geöffnet ist, aber MAPI führt des Vorgangs zum Öffnen, indem erhöht den Referenzzähler für das vorhandene Objekt öffnen und sie an den Client oder Anbieter, die die [IMessage::OpenAttach aufgerufen ](imessage-openattach.md)oder [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="b721d-175">MAPI currently allows a subobject that is already open to be opened once more, but MAPI performs the open operation by incrementing the reference count for the existing open object and returning it to the client or provider that called the [IMessage::OpenAttach](imessage-openattach.md) or [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method.</span></span> <span data-ttu-id="b721d-176">Dies bedeutet, dass der angeforderte für den ersten Vorgang zum Öffnen einer Unterobjekts Zugriff den Zugriff für alle nachfolgenden open Operationen, unabhängig von der durch die Vorgänge angeforderte Zugriff bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="b721d-176">This means the access requested for the first open operation on a subobject is the access provided for all subsequent open operations, regardless of the access requested by the operations.</span></span> 
  
<span data-ttu-id="b721d-177">Das Verfahren für die Platzierung einer Nachricht in einer Anlage lautet die [IMAPIProp::OpenProperty](imapiprop-openproperty.md) -Methode mit der ID Schnittstelle IID_IMessage aufrufen.</span><span class="sxs-lookup"><span data-stu-id="b721d-177">The correct procedure for placing a message into an attachment is to call the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method with an interface identifier of IID_IMessage.</span></span> <span data-ttu-id="b721d-178">**OpenProperty** unterstützt derzeit auch Erstellung von Nachrichtenanlagen verfügbar direkt auf die OLE- **IStorage** -Schnittstelle, d. h., mithilfe des Bezeichners für IID_IStorage-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="b721d-178">**OpenProperty** currently also supports creation of message attachments available directly on the OLE **IStorage** interface, that is, using the IID_IStorage interface identifier.</span></span> <span data-ttu-id="b721d-179">**IStorage** Access wird unterstützt, um eine einfache Möglichkeit, ein Microsoft Word-Dokument in eine Anlage zu versetzen, ohne Sie zu konvertieren zu oder von der OLE- **IStream** -Schnittstelle zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="b721d-179">**IStorage** access is supported to allow an easy way to put a Microsoft Word document into an attachment without converting it to or from the OLE **IStream** interface.</span></span> <span data-ttu-id="b721d-180">Allerdings **IMessage** vorhersehbar verhält sich möglicherweise nicht **OpenIMsgOnIStg** einen **IStorage** Zeiger auf die Anlagendaten übergeben, und klicken Sie dann die Objekte in der falschen Reihenfolge freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="b721d-180">However, **IMessage** may not behave predictably if **OpenIMsgOnIStg** is passed an **IStorage** pointer to the attachment data and then the objects are released in the wrong order.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b721d-181">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="b721d-181">MFCMAPI reference</span></span>

<span data-ttu-id="b721d-182">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b721d-182">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b721d-183">**Datei**</span><span class="sxs-lookup"><span data-stu-id="b721d-183">**File**</span></span>|<span data-ttu-id="b721d-184">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="b721d-184">**Function**</span></span>|<span data-ttu-id="b721d-185">**Comment**</span><span class="sxs-lookup"><span data-stu-id="b721d-185">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b721d-186">File.cpp</span><span class="sxs-lookup"><span data-stu-id="b721d-186">File.cpp</span></span>  <br/> |<span data-ttu-id="b721d-187">LoadMSGToMessage</span><span class="sxs-lookup"><span data-stu-id="b721d-187">LoadMSGToMessage</span></span>  <br/> |<span data-ttu-id="b721d-188">MFCMAPI (engl.) verwendet die **OpenIMsgOnIStg** -Methode zum Öffnen einer IMessage-Schnittstelle, über die. MSG-Datei so, dass die Datei mit MAPI bearbeitet werden kann.</span><span class="sxs-lookup"><span data-stu-id="b721d-188">MFCMAPI uses the **OpenIMsgOnIStg** method to open an IMessage interface on top of the .MSG file so that the file may be manipulated with MAPI.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b721d-189">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b721d-189">See also</span></span>

- [<span data-ttu-id="b721d-190">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="b721d-190">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

