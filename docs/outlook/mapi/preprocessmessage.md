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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437245"
---
# <a name="preprocessmessage"></a><span data-ttu-id="f34ce-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="f34ce-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="f34ce-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f34ce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f34ce-105">Definiert eine Funktion, die Nachrichteninhalte oder das Format einer Nachricht vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f34ce-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f34ce-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f34ce-106">Header file:</span></span>  <br/> |<span data-ttu-id="f34ce-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="f34ce-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="f34ce-108">Definierte Funktion implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f34ce-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="f34ce-109">Transportanbieter</span><span class="sxs-lookup"><span data-stu-id="f34ce-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="f34ce-110">Definierte Funktion, die von:</span><span class="sxs-lookup"><span data-stu-id="f34ce-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="f34ce-111">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="f34ce-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="f34ce-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f34ce-112">Parameters</span></span>

 <span data-ttu-id="f34ce-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="f34ce-113">_lpvSession_</span></span>
  
> <span data-ttu-id="f34ce-114">[in] Zeiger auf die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f34ce-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="f34ce-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="f34ce-115">_lpMessage_</span></span>
  
> <span data-ttu-id="f34ce-116">[in] Zeiger auf die nachricht, die vorverarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f34ce-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="f34ce-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="f34ce-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="f34ce-118">[in] Zeiger auf das Adressbuch, aus dem der Benutzer Empfänger für die Nachricht auswählen soll.</span><span class="sxs-lookup"><span data-stu-id="f34ce-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="f34ce-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="f34ce-119">_lpFolder_</span></span>
  
> <span data-ttu-id="f34ce-120">[in, out] Zeiger auf einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="f34ce-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="f34ce-121">Bei der Eingabe zeigt  _der lpFolder-Parameter_ auf den Ordner, der nachrichten enthält, die vorverarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f34ce-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="f34ce-122">Bei der Ausgabe  _zeigt lpFolder_ auf den Ordner, in dem vorverarbeitete Nachrichten platziert wurden.</span><span class="sxs-lookup"><span data-stu-id="f34ce-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="f34ce-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="f34ce-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="f34ce-124">[in] Zeiger auf die [MAPIAllocateBuffer-Funktion,](mapiallocatebuffer.md) die zum Zuordnen von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f34ce-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="f34ce-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="f34ce-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="f34ce-126">[in] Zeiger auf die [MAPIAllocateMore-Funktion,](mapiallocatemore.md) die verwendet werden soll, um bei Bedarf zusätzlichen Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="f34ce-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="f34ce-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="f34ce-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="f34ce-128">[in] Zeiger auf die [MAPIFreeBuffer-Funktion,](mapifreebuffer.md) die zum Freispeichern verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f34ce-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="f34ce-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="f34ce-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="f34ce-130">[out] Zeiger auf die Anzahl der Nachrichten im Array, auf die der  _lpppMessage-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="f34ce-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="f34ce-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="f34ce-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="f34ce-132">[out] Zeiger auf einen Zeiger auf ein Array von Zeigern auf vorverarbeitete oder anderweitig generierte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="f34ce-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="f34ce-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="f34ce-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="f34ce-134">[out] Zeiger auf eine optionale zurückgegebene [ADRLIST-Struktur,](adrlist.md) in der vorverarbeitete Empfänger auflistet werden, für die die Nachricht nicht zustellbar ist.</span><span class="sxs-lookup"><span data-stu-id="f34ce-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="f34ce-135">Weitere Informationen zum Inhalt dieser Liste finden Sie unter [IMAPISupport::StatusRecips-Methode.](imapisupport-statusrecips.md)</span><span class="sxs-lookup"><span data-stu-id="f34ce-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f34ce-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f34ce-136">Return value</span></span>

<span data-ttu-id="f34ce-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="f34ce-137">S_OK</span></span>
  
> <span data-ttu-id="f34ce-138">Nachrichteninhalte wurden erfolgreich vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f34ce-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f34ce-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f34ce-139">Remarks</span></span>

<span data-ttu-id="f34ce-140">Ein Nachrichtenvorprozessor des Transportanbieters kann während der Nachrichtenvorverarbeitung eine Statusanzeige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="f34ce-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="f34ce-141">Es sollte jedoch niemals ein Dialogfeld angezeigt werden, das eine Benutzerinteraktion während der Nachrichtenvorverarbeitung erfordert.</span><span class="sxs-lookup"><span data-stu-id="f34ce-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="f34ce-142">Wenn ein Präprozessor einer ausgehenden Nachricht große Datenmengen hinzufügt, sollten bestimmte Verfahren befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="f34ce-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="f34ce-143">Diese Art von Nachricht kann in einem serverbasierten Nachrichtenspeicher gespeichert werden, was dazu führt, dass der Präprozessor auf einen Remotespeicher zu zugegriffen hat, was eine zeitaufwändige Prozedur ist.</span><span class="sxs-lookup"><span data-stu-id="f34ce-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="f34ce-144">Um dies zu vermeiden, sollte der Präprozessor über eine Option verfügen, mit der Daten gespeichert werden können, die viel Speicherplatz in einem lokalen Nachrichtenspeicher enthalten und einen Verweis auf diesen lokalen Speicher in der Nachricht bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="f34ce-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="f34ce-145">Der Präprozessor sollte keine der Objekte los, die ursprünglich an die **PreprocessMessage-basierte** Funktion übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="f34ce-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="f34ce-146">Bevor der MAPI-Spooler eine **PreprocessMessage-Funktion** aufrufen kann, muss der Transportanbieter die Funktion in einem Aufruf der [IMAPISupport::RegisterPreprocessor-Methode](imapisupport-registerpreprocessor.md) registriert haben.</span><span class="sxs-lookup"><span data-stu-id="f34ce-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="f34ce-147">Nach dem Aufrufen **einer PreprocessMessage-Funktion** kann der Spooler die Übermittlung einer Nachricht erst fortsetzen, wenn die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f34ce-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="f34ce-148">Der MAPI-Spooler besitzt die Aufgabe, Nachrichten zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="f34ce-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="f34ce-149">Dies bedeutet, dass die ursprüngliche Nachricht niemals in einem Array von Nachrichtenzeigern platziert wird und kein Aufruf der **SubmitMessage-Methoden** erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="f34ce-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f34ce-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f34ce-150">See also</span></span>



[<span data-ttu-id="f34ce-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="f34ce-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="f34ce-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="f34ce-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="f34ce-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="f34ce-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

