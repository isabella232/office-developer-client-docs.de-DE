---
title: PreprocessMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PreprocessMessage
api_type:
- COM
ms.assetid: dda50325-74b3-445e-986e-115f6536561f
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 22562e1177c9a649bc66b25b5e8e9e6ecc8e397c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795310"
---
# <a name="preprocessmessage"></a><span data-ttu-id="dfb20-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="dfb20-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="dfb20-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="dfb20-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="dfb20-105">Definiert eine Funktion, die vorverarbeitet Nachrichteninhalt oder das Format einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="dfb20-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="dfb20-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="dfb20-106">Header file:</span></span>  <br/> |<span data-ttu-id="dfb20-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="dfb20-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="dfb20-108">Definierte Funktion von implementiert:</span><span class="sxs-lookup"><span data-stu-id="dfb20-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="dfb20-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="dfb20-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="dfb20-110">Definierte Funktion aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="dfb20-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="dfb20-111">MAPI-Warteschlange</span><span class="sxs-lookup"><span data-stu-id="dfb20-111">MAPI spooler</span></span>  <br/> |
   
```cpp
HRESULT PreprocessMessage(
  LPVOID lpvSession,
  LPMESSAGE lpMessage,
  LPADRBOOK lpAdrBook,
  LPMAPIFOLDER lpFolder,
  LPALLOCATEBUFFER AllocateBuffer,
  LPALLOCATEMORE AllocateMore,
  LPFREEBUFFER FreeBuffer,
  ULONG FAR * lpcOutbound,
  LPMESSAGE FAR * FAR * lpppMessage,
  LPADRLIST FAR * lppRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="dfb20-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfb20-112">Parameters</span></span>

 <span data-ttu-id="dfb20-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="dfb20-113">_lpvSession_</span></span>
  
> <span data-ttu-id="dfb20-114">[in] Zeiger auf die Sitzung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dfb20-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="dfb20-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="dfb20-115">_lpMessage_</span></span>
  
> <span data-ttu-id="dfb20-116">[in] Zeiger auf die Nachricht vorverarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="dfb20-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="dfb20-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="dfb20-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="dfb20-118">[in] Zeiger auf das Adressbuch von dem der Benutzer Empfänger der Nachricht wählen sollten.</span><span class="sxs-lookup"><span data-stu-id="dfb20-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="dfb20-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="dfb20-119">_lpFolder_</span></span>
  
> <span data-ttu-id="dfb20-120">[in, out] Zeiger in einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="dfb20-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="dfb20-121">Zeigt bei der Eingabe der _LpFolder_ -Parameter auf den Ordner, der vorverarbeitet werden Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="dfb20-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="dfb20-122">Ausgabe _LpFolder_ zeigt auf den Ordner, in dem vorverarbeitete Nachrichten abgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="dfb20-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="dfb20-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="dfb20-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="dfb20-124">[in] Zeiger auf die Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) , Speicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="dfb20-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="dfb20-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="dfb20-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="dfb20-126">[in] Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, mit der zusätzlichen Arbeitsspeicher zugewiesen werden, in denen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dfb20-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="dfb20-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="dfb20-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="dfb20-128">[in] Zeiger auf die [MAPIFreeBuffer](mapifreebuffer.md) -Funktion verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="dfb20-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="dfb20-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="dfb20-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="dfb20-130">[out] Zeiger auf die Anzahl der Nachrichten in der Matrix, durch den Parameter _LpppMessage_ auf zeigt.</span><span class="sxs-lookup"><span data-stu-id="dfb20-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="dfb20-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="dfb20-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="dfb20-132">[out] Zeiger auf einen Zeiger auf ein Array von Zeigern für vorverarbeitet oder andernfalls Nachrichten generiert.</span><span class="sxs-lookup"><span data-stu-id="dfb20-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="dfb20-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="dfb20-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="dfb20-134">[out] Zeiger auf eine optionale zurückgegebenen [ADRLIST](adrlist.md) -Struktur, auflisten Präprozessor erkannt Empfänger für die Nachricht nicht zugestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="dfb20-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="dfb20-135">Weitere Informationen über den Inhalt dieser Liste finden Sie unter der [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="dfb20-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="dfb20-136">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="dfb20-136">Return value</span></span>

<span data-ttu-id="dfb20-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="dfb20-137">S_OK</span></span>
  
> <span data-ttu-id="dfb20-138">Nachrichteninhalt wurden erfolgreich vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="dfb20-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dfb20-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dfb20-139">Remarks</span></span>

<span data-ttu-id="dfb20-140">Ein Adressbuchhierarchie Nachricht Präprozessor kann eine Statusanzeige während der vorverarbeitung Nachricht darstellen.</span><span class="sxs-lookup"><span data-stu-id="dfb20-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="dfb20-141">Sie sollten jedoch noch nie ein Dialogfeld Benutzereingriff während der vorverarbeitung Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="dfb20-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="dfb20-142">Wenn ein Präprozessor große Datenmengen eine ausgehende Nachricht hinzufügt, müssen bestimmte Verfahren folgen.</span><span class="sxs-lookup"><span data-stu-id="dfb20-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="dfb20-143">Nachrichten dieses Typs kann in einem serverbasierten Nachrichtenspeicher gespeichert werden, verursacht des Präprozessors auf einen remote-Speicher sehr zeitaufwendig zugreifen.</span><span class="sxs-lookup"><span data-stu-id="dfb20-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="dfb20-144">Um dies vermeiden möchten, sollte der Präprozessor eine Option, die Ihnen zum Speichern von Daten, die eine große Menge an Speicherplatz in einem lokalen Nachrichtenspeicher akzeptiert, und geben Sie einen Verweis auf diesen lokalen Speicher in der Nachricht ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="dfb20-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="dfb20-145">Der Präprozessor sollte nicht mit den Objekten, die ursprünglich übergeben an die Funktion **PreprocessMessage** basierend freigeben.</span><span class="sxs-lookup"><span data-stu-id="dfb20-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="dfb20-146">Bevor die MAPI-Warteschlange eine **PreprocessMessage** -Funktion aufgerufen werden kann, muss der Adressbuchhierarchie die Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert haben.</span><span class="sxs-lookup"><span data-stu-id="dfb20-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="dfb20-147">Nach dem Aufrufen einer Funktion **PreprocessMessage** , kann nicht die Warteschlange weiterhin eine Nachricht senden, bis der Funktion zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dfb20-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="dfb20-148">Die MAPI-Warteschlange besitzt die Aufgabe übermitteln von Nachrichten an.</span><span class="sxs-lookup"><span data-stu-id="dfb20-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="dfb20-149">Dies bedeutet, dass die ursprüngliche Nachricht nie in ein Array von Zeigern Nachricht befindet und dass ein Anruf an die Methoden **SubmitMessage** nie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="dfb20-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="dfb20-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dfb20-150">See also</span></span>



[<span data-ttu-id="dfb20-151">IAddrBook: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="dfb20-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="dfb20-152">IMAPIFolder: IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="dfb20-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="dfb20-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="dfb20-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

