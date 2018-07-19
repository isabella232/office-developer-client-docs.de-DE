---
title: IMAPIFolderCreateMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CreateMessage
api_type:
- COM
ms.assetid: e0222afa-c148-4735-a603-cac7be6c91f9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 8d7e6dfbf9e6a751845adb2319b66462bcde651f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792095"
---
# <a name="imapifoldercreatemessage"></a><span data-ttu-id="c199d-103">IMAPIFolder::CreateMessage</span><span class="sxs-lookup"><span data-stu-id="c199d-103">IMAPIFolder::CreateMessage</span></span>

  
  
<span data-ttu-id="c199d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c199d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c199d-105">Erstellt eine neue Nachricht an.</span><span class="sxs-lookup"><span data-stu-id="c199d-105">Creates a new message.</span></span>
  
```cpp
HRESULT CreateMessage(
  LPCIID lpInterface,
  ULONG ulFlags,
  LPMESSAGE FAR * lppMessage
);
```

## <a name="parameters"></a><span data-ttu-id="c199d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c199d-106">Parameters</span></span>

 <span data-ttu-id="c199d-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c199d-107">_lpInterface_</span></span>
  
> <span data-ttu-id="c199d-108">[in] Ein Zeiger auf die Schnittstelle-ID (IID), die die Schnittstelle, greifen Sie auf die neue Nachricht verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c199d-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the new message.</span></span> <span data-ttu-id="c199d-109">Gültige Schnittstelle Bezeichnern enthalten IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer und IID_IMAPIFolder.</span><span class="sxs-lookup"><span data-stu-id="c199d-109">Valid interface identifiers include IID_IUnknown, IID_IMAPIProp, IID_IMAPIContainer, and IID_IMAPIFolder.</span></span> <span data-ttu-id="c199d-110">Übergeben von NULL wird eine Nachricht an die e-Mail-Schnittstelle zurück, die [IMessage: IMAPIProp](imessageimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="c199d-110">Passing NULL causes the message store provider to return the standard message interface, [IMessage : IMAPIProp](imessageimapiprop.md).</span></span> 
    
 <span data-ttu-id="c199d-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c199d-111">_ulFlags_</span></span>
  
> <span data-ttu-id="c199d-112">[in] Eine Bitmaske aus Flags, die steuert, wie die Nachricht erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c199d-112">[in] A bitmask of flags that controls how the message is created.</span></span> <span data-ttu-id="c199d-113">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="c199d-113">The following flags can be set:</span></span>
    
<span data-ttu-id="c199d-114">ITEMPROC_FORCE</span><span class="sxs-lookup"><span data-stu-id="c199d-114">ITEMPROC_FORCE</span></span>
  
> <span data-ttu-id="c199d-115">Gibt an, dass die Nachricht für Informationsspeicher für Persönliche Ordner (PST) Regeln verarbeiten, bevor der Speicher jeder listening Client die Ankunft der neuen Nachricht informiert.</span><span class="sxs-lookup"><span data-stu-id="c199d-115">Indicates to the personal folder store (PST) that the message is eligible for rules processing before the store notifies any listening client of the arrival of the new message.</span></span> <span data-ttu-id="c199d-116">Nur regelverarbeitung gilt für neue Nachrichten, die auf einem Server, der nicht auf einem Microsoft Exchange Server ist erstellt werden, da Exchange Server Regeln für Nachrichten auf dem Server verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="c199d-116">Rules processing only applies to new messages that are created on a server that is not a Microsoft Exchange Server, because Exchange Server processes rules for messages on the server.</span></span> <span data-ttu-id="c199d-117">Aus diesem Grund muss vom Anbieter oder vom Client beim Erstellen der Nachricht übergeben dieses Flag in Kombination mit dem Speichern einer Nachricht mit [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) mit NON_EMS_XP_SAVE, die angibt, dass der Server nicht mit einem Exchange-Server ist.</span><span class="sxs-lookup"><span data-stu-id="c199d-117">Therefore, the provider or client creating the message must pass this flag in combination with saving a message with [IMAPIPProp::SaveChanges](imapiprop-savechanges.md) using NON_EMS_XP_SAVE, which indicates that the server is not an Exchange Server.</span></span> 
    
<span data-ttu-id="c199d-118">MAPI_ASSOCIATED</span><span class="sxs-lookup"><span data-stu-id="c199d-118">MAPI_ASSOCIATED</span></span> 
  
> <span data-ttu-id="c199d-119">Die Nachricht zu erstellenden sollte in der zugehörigen Inhaltstabelle anstelle der standard Inhaltstabelle enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="c199d-119">The message to be created should be included in the associated contents table instead of the standard contents table.</span></span> <span data-ttu-id="c199d-120">Benutzerinteraktion werden zugeordnete Nachrichten ausgeblendet.</span><span class="sxs-lookup"><span data-stu-id="c199d-120">Associated messages are hidden from user interaction.</span></span>
    
<span data-ttu-id="c199d-121">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="c199d-121">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="c199d-122">**CreateMessage** darf erfolgreich, auch wenn der Vorgang zum Erstellen eines nicht vollständig ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c199d-122">**CreateMessage** is allowed to succeed even if the create operation has not fully completed.</span></span> <span data-ttu-id="c199d-123">Dies bedeutet, dass die neue Nachricht möglicherweise nicht sofort mit dem Anrufer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="c199d-123">This implies that the new message might not be immediately available to the caller.</span></span> 
    
 <span data-ttu-id="c199d-124">_lppMessage_</span><span class="sxs-lookup"><span data-stu-id="c199d-124">_lppMessage_</span></span>
  
> <span data-ttu-id="c199d-125">[out] Ein Zeiger auf einen Zeiger auf die neu erstellte Nachricht.</span><span class="sxs-lookup"><span data-stu-id="c199d-125">[out] A pointer to a pointer to the newly created message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c199d-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c199d-126">Return value</span></span>

<span data-ttu-id="c199d-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="c199d-127">S_OK</span></span> 
  
> <span data-ttu-id="c199d-128">Die Nachricht wurde erfolgreich erstellt.</span><span class="sxs-lookup"><span data-stu-id="c199d-128">The message was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c199d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c199d-129">Remarks</span></span>

<span data-ttu-id="c199d-130">Die **IMAPIFolder::CreateMessage** -Methode erstellt eine neue Nachricht mit generischen oder zugehörigen Inhalte und weist einen Eintrag Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="c199d-130">The **IMAPIFolder::CreateMessage** method creates a new message with generic or associated content and assigns an entry identifier.</span></span> <span data-ttu-id="c199d-131">Die Eintrags-ID besteht aus einer, die den Nachricht Speicheranbieter darstellt und einen Teil, der die einzelne Nachricht darstellt.</span><span class="sxs-lookup"><span data-stu-id="c199d-131">The entry identifier consists of a part that represents the message store provider and a part that represents the individual message.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c199d-132">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="c199d-132">Notes to implementers</span></span>

<span data-ttu-id="c199d-133">Sie können auswählen, ob alle erforderlichen Nachrichteneigenschaften in **CreateMessage** oder in der Nachricht [IMAPIProp::SaveChanges](imapiprop-savechanges.md) -Methode festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="c199d-133">You can choose whether to set all of the required message properties in **CreateMessage** or in the message's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method.</span></span> <span data-ttu-id="c199d-134">Sie müssen keinen diese Eigenschaften zur Verfügung zu stellen, bis eine erfolgreiche speichern aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="c199d-134">You do not have to make these properties available until a successful save has occurred.</span></span> 
  
<span data-ttu-id="c199d-135">Weitere Informationen zum Arbeiten mit zugehörigen Informationen finden Sie unter [Folder-Associated Informationen](folder-associated-information-tables.md) und [Inhalt Tabellen](contents-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c199d-135">For more information about how to work with associated information, see [Folder-Associated Information Tables](folder-associated-information-tables.md) and [Contents Tables](contents-tables.md).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="c199d-136">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="c199d-136">Notes to callers</span></span>

<span data-ttu-id="c199d-137">Einige Nachricht-Anbieter ermöglichen die Eintrags-ID der neuen Nachricht verfügbar sein soll, unmittelbar nachdem **CreateMessage** zurückgegeben. andere Anbieter Nachricht verzögert ihre Verfügbarkeit, bis die Nachricht gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="c199d-137">Some message store providers allow the entry identifier of the new message to be available immediately after **CreateMessage** returns; other message store providers delay its availability until the message is saved.</span></span> <span data-ttu-id="c199d-138">Da nicht alle Anbieter Nachricht einen Eintrag Bezeichner für eine neue Nachricht generieren, bis Sie die Nachricht **IMAPIProp::SaveChanges** -Methode aufgerufen haben, können Sie möglicherweise nicht auf die Eintrags-ID zugreifen, wenn **CreateMessage** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c199d-138">Because not all message store providers generate an entry identifier for a new message until you have called the message's **IMAPIProp::SaveChanges** method, you may be unable to access the entry identifier when **CreateMessage** returns.</span></span> <span data-ttu-id="c199d-139">Darüber hinaus kann die neue Nachricht nicht in den Ordner Inhaltstabelle enthalten, bis der Speichervorgang.</span><span class="sxs-lookup"><span data-stu-id="c199d-139">Also, the new message may not be included in the folder's contents table until the save occurs.</span></span> 
  
<span data-ttu-id="c199d-140">Erwarten Sie die Eintrags-ID zugewiesen, um die neue Nachricht nicht nur in der aktuellen Nachrichtenspeicher eindeutig, aber die sich am ehesten in allen der Nachrichtenspeicher sein, die gleichzeitig geöffnet sind.</span><span class="sxs-lookup"><span data-stu-id="c199d-140">Expect the entry identifier assigned to the new message to be unique not only in the current message store, but most likely across all of the message stores that are open at the same time.</span></span> <span data-ttu-id="c199d-141">Eine Ausnahme zu dieser Regel tritt auf, wenn mehrere Einträge für einen Nachrichtenspeicher im Profil angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="c199d-141">One exception to this rule occurs when multiple entries for a message store appear in the profile.</span></span> <span data-ttu-id="c199d-142">Daraufhin wird die Nachrichtenspeicher mehrmals geöffnet werden soll und Eintragsbezeichner dupliziert werden.</span><span class="sxs-lookup"><span data-stu-id="c199d-142">This causes the message store to be opened multiple times and entry identifiers to be duplicated.</span></span> 
  
<span data-ttu-id="c199d-143">Rufen Sie der Ordner Postausgang **IMAPIFolder::CreateMessage** -Methode, um eine ausgehende Nachricht zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="c199d-143">To create an outgoing message, call the Outbox folder's **IMAPIFolder::CreateMessage** method.</span></span> 
  
<span data-ttu-id="c199d-144">Wenn Sie einen Ordner löschen, der eine neue Nachricht enthält, bevor die Nachricht gespeichert wird, sind die Ergebnisse nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c199d-144">If you delete a folder that contains a new message before the message is saved, the results are undefined.</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c199d-145">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="c199d-145">MFCMAPI reference</span></span>

<span data-ttu-id="c199d-146">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c199d-146">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c199d-147">**Datei**</span><span class="sxs-lookup"><span data-stu-id="c199d-147">**File**</span></span>|<span data-ttu-id="c199d-148">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="c199d-148">**Function**</span></span>|<span data-ttu-id="c199d-149">**Comment**</span><span class="sxs-lookup"><span data-stu-id="c199d-149">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c199d-150">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="c199d-150">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="c199d-151">CFolder::OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="c199d-151">CFolder::OnNewMessage</span></span>  <br/> |<span data-ttu-id="c199d-152">MFCMAPI (engl.) wird die **IMAPIFolder::CreateMessage** -Methode zum Erstellen und speichern Sie eine neue Nachricht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c199d-152">MFCMAPI uses the **IMAPIFolder::CreateMessage** method to create and save a new message.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c199d-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c199d-153">See also</span></span>



[<span data-ttu-id="c199d-154">IMAPIProp::SaveChanges</span><span class="sxs-lookup"><span data-stu-id="c199d-154">IMAPIProp::SaveChanges</span></span>](imapiprop-savechanges.md)
  
[<span data-ttu-id="c199d-155">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="c199d-155">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)


[<span data-ttu-id="c199d-156">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="c199d-156">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

