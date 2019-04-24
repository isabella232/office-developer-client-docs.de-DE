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
ms.openlocfilehash: a3982520cb1c745874a938962ece075a294b6257
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351380"
---
# <a name="preprocessmessage"></a><span data-ttu-id="997af-103">PreprocessMessage</span><span class="sxs-lookup"><span data-stu-id="997af-103">PreprocessMessage</span></span>

  
  
<span data-ttu-id="997af-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="997af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="997af-105">Definiert eine Funktion, die den Nachrichteninhalt oder das Format einer Nachricht vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="997af-105">Defines a function that preprocesses message contents or the format of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="997af-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="997af-106">Header file:</span></span>  <br/> |<span data-ttu-id="997af-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="997af-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="997af-108">Definierte Funktion, implementiert von:</span><span class="sxs-lookup"><span data-stu-id="997af-108">Defined function implemented by:</span></span>  <br/> |<span data-ttu-id="997af-109">Transport Anbieter</span><span class="sxs-lookup"><span data-stu-id="997af-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="997af-110">Definierte Funktion, aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="997af-110">Defined function called by:</span></span>  <br/> |<span data-ttu-id="997af-111">MAPI-Spooler</span><span class="sxs-lookup"><span data-stu-id="997af-111">MAPI spooler</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="997af-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="997af-112">Parameters</span></span>

 <span data-ttu-id="997af-113">_lpvSession_</span><span class="sxs-lookup"><span data-stu-id="997af-113">_lpvSession_</span></span>
  
> <span data-ttu-id="997af-114">in Zeiger auf die zu verwendende Sitzung.</span><span class="sxs-lookup"><span data-stu-id="997af-114">[in] Pointer to the session to be used.</span></span> 
    
 <span data-ttu-id="997af-115">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="997af-115">_lpMessage_</span></span>
  
> <span data-ttu-id="997af-116">in Zeiger auf die Nachricht, die vorverarbeitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="997af-116">[in] Pointer to the message to be preprocessed.</span></span> 
    
 <span data-ttu-id="997af-117">_lpAdrBook_</span><span class="sxs-lookup"><span data-stu-id="997af-117">_lpAdrBook_</span></span>
  
> <span data-ttu-id="997af-118">in Zeiger auf das Adressbuch, aus dem der Benutzer Empfänger für die Nachricht auswählen soll.</span><span class="sxs-lookup"><span data-stu-id="997af-118">[in] Pointer to the address book from which the user should select recipients for the message.</span></span> 
    
 <span data-ttu-id="997af-119">_lpFolder_</span><span class="sxs-lookup"><span data-stu-id="997af-119">_lpFolder_</span></span>
  
> <span data-ttu-id="997af-120">[in, out] Zeiger auf einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="997af-120">[in, out] Pointer to a folder.</span></span> <span data-ttu-id="997af-121">Bei der Eingabe zeigt der Parameter _lpFolder_ auf den Ordner mit Nachrichten, die vorverarbeitet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="997af-121">On input, the  _lpFolder_ parameter points to the folder that contains messages to be preprocessed.</span></span> <span data-ttu-id="997af-122">Bei der Ausgabe zeigt _lpFolder_ auf den Ordner, in dem vorverarbeitete Nachrichten abgelegt wurden.</span><span class="sxs-lookup"><span data-stu-id="997af-122">On output,  _lpFolder_ points to the folder where preprocessed messages have been placed.</span></span> 
    
 <span data-ttu-id="997af-123">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="997af-123">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="997af-124">in Zeiger auf die [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion, die zum Reservieren von Arbeitsspeicher verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="997af-124">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="997af-125">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="997af-125">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="997af-126">in Zeiger auf die [MAPIAllocateMore](mapiallocatemore.md) -Funktion, die verwendet werden soll, um bei Bedarf zusätzlichen Arbeitsspeicher zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="997af-126">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory where required.</span></span> 
    
 <span data-ttu-id="997af-127">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="997af-127">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="997af-128">in Zeiger auf die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion, die verwendet werden, um Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="997af-128">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="997af-129">_lpcOutbound_</span><span class="sxs-lookup"><span data-stu-id="997af-129">_lpcOutbound_</span></span>
  
> <span data-ttu-id="997af-130">Out Zeiger auf die Anzahl der Nachrichten im Array, auf die durch den _lpppMessage_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="997af-130">[out] Pointer to the number of messages in the array pointed to by the  _lpppMessage_ parameter.</span></span> 
    
 <span data-ttu-id="997af-131">_lpppMessage_</span><span class="sxs-lookup"><span data-stu-id="997af-131">_lpppMessage_</span></span>
  
> <span data-ttu-id="997af-132">Out Zeiger auf einen Zeiger auf ein Array von Zeigern auf vorverarbeitete oder anderweitig generierte Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="997af-132">[out] Pointer to a pointer to an array of pointers to preprocessed or otherwise generated messages.</span></span> 
    
 <span data-ttu-id="997af-133">_lppRecipList_</span><span class="sxs-lookup"><span data-stu-id="997af-133">_lppRecipList_</span></span>
  
> <span data-ttu-id="997af-134">Out Zeiger auf eine optionale zurückgegebene [ADRLIST](adrlist.md) -Struktur, die Vorprozessor-erkannte Empfänger auflistet, für die die Nachricht unzustellbar ist.</span><span class="sxs-lookup"><span data-stu-id="997af-134">[out] Pointer to an optional returned [ADRLIST](adrlist.md) structure, listing preprocessor-detected recipients for which the message is undeliverable.</span></span> <span data-ttu-id="997af-135">Weitere Informationen zu den Inhalten dieser Liste finden Sie unter der [IMAPISupport:: StatusRecips](imapisupport-statusrecips.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="997af-135">For more information about the contents of this list, see the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="997af-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="997af-136">Return value</span></span>

<span data-ttu-id="997af-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="997af-137">S_OK</span></span>
  
> <span data-ttu-id="997af-138">Der Nachrichteninhalt wurde erfolgreich vorverarbeitet.</span><span class="sxs-lookup"><span data-stu-id="997af-138">Message contents were successfully preprocessed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="997af-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="997af-139">Remarks</span></span>

<span data-ttu-id="997af-140">Ein Transportanbieter-Nachrichten Präprozessor kann während der Nachrichten Vorverarbeitung eine Statusanzeige darstellen.</span><span class="sxs-lookup"><span data-stu-id="997af-140">A transport-provider message preprocessor can present a progress indicator during message preprocessing.</span></span> <span data-ttu-id="997af-141">Es sollte jedoch nie ein Dialogfeld angezeigt werden, das die Benutzerinteraktion während der Nachrichten Vorverarbeitung erfordert.</span><span class="sxs-lookup"><span data-stu-id="997af-141">However, it should never present a dialog box requiring user interaction during message preprocessing.</span></span> 
  
<span data-ttu-id="997af-142">Wenn ein Präprozessor große Datenmengen zu einer ausgehenden Nachricht hinzufügt, sollten bestimmte Verfahren befolgt werden.</span><span class="sxs-lookup"><span data-stu-id="997af-142">When a preprocessor adds large amounts of data to an outbound message, certain procedures should be followed.</span></span> <span data-ttu-id="997af-143">Diese Art von Nachricht kann in einem Server basierten Nachrichtenspeicher gespeichert werden, wodurch der Präprozessor auf einen Remotespeicher zugreift, ein zeitaufwändiger Vorgang.</span><span class="sxs-lookup"><span data-stu-id="997af-143">This type of message can be stored in a server-based message store, causing the preprocessor to access a remote store, a time-consuming procedure.</span></span> <span data-ttu-id="997af-144">Um dies zu vermeiden, sollte der Präprozessor über eine Option verfügen, die es ermöglicht, Daten zu speichern, die sehr viel Speicherplatz in einem lokalen Nachrichtenspeicher benötigen, und einen Verweis auf diesen lokalen Speicher in der Nachricht bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="997af-144">To avoid having to do so, the preprocessor should have an option that enables it to store data that takes a large amount of space in a local message store and to provide a reference to that local store in the message.</span></span> 
  
<span data-ttu-id="997af-145">Der Präprozessor sollte keines der Objekte freigeben, die ursprünglich an die **PreprocessMessage** -basierte Funktion übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="997af-145">The preprocessor should not release any of the objects originally passed to the **PreprocessMessage** based function.</span></span> 
  
<span data-ttu-id="997af-146">Bevor der MAPI-Spooler eine **PreprocessMessage** -Funktion aufrufen kann, muss der Transportanbieter die Funktion bei einem Aufruf der [IMAPISupport:: RegisterPreprocessor](imapisupport-registerpreprocessor.md) -Methode registriert haben.</span><span class="sxs-lookup"><span data-stu-id="997af-146">Before the MAPI spooler can call a **PreprocessMessage** function, the transport provider must have registered the function in a call to the [IMAPISupport::RegisterPreprocessor](imapisupport-registerpreprocessor.md) method.</span></span> <span data-ttu-id="997af-147">Nach dem Aufrufen einer **PreprocessMessage** -Funktion kann der Spooler keine Nachricht mehr senden, bis die Funktion zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="997af-147">After calling a **PreprocessMessage** function, the spooler cannot continue submitting a message until the function returns.</span></span> 
  
<span data-ttu-id="997af-148">Der MAPI-Spooler besitzt die Aufgabe, Nachrichten zu übermitteln.</span><span class="sxs-lookup"><span data-stu-id="997af-148">The MAPI spooler owns the task of submitting messages.</span></span> <span data-ttu-id="997af-149">Dies bedeutet, dass die ursprüngliche Nachricht nie in einem Array von Nachrichten Zeigern angeordnet wird, und dass ein Aufruf der **SubmitMessage** -Methoden nie erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="997af-149">This means the original message is never placed in an array of message pointers and that a call to the **SubmitMessage** methods is never required.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="997af-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="997af-150">See also</span></span>



[<span data-ttu-id="997af-151">IAddrBook : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="997af-151">IAddrBook : IMAPIProp</span></span>](iaddrbookimapiprop.md)
  
[<span data-ttu-id="997af-152">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="997af-152">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="997af-153">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="997af-153">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

