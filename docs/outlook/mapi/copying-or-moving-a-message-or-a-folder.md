---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Zuletzt geändert: 08 November 2011'
ms.openlocfilehash: 97e7c90c2fdc715d7d0749300cc62854fffa6447
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563982"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="7e998-103">Kopieren oder Verschieben einer Nachricht oder eines Ordners</span><span class="sxs-lookup"><span data-stu-id="7e998-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="7e998-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e998-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e998-105">Ein Client können eine der vier Methoden zum Kopieren oder verschieben Sie eine Nachricht oder einen Ordner:</span><span class="sxs-lookup"><span data-stu-id="7e998-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="7e998-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="7e998-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="7e998-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="7e998-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="7e998-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="7e998-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="7e998-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="7e998-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="7e998-110">Durch Festlegen der entsprechenden Flags und Parameter, können **CopyTo** und **CopyProps** vorgenommen werden, genau wie **CopyFolder** oder **CopyMessages**arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7e998-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="7e998-111">Berücksichtigen Sie die folgenden Aspekte bei der Entscheidung, welche Methode aufgerufen:</span><span class="sxs-lookup"><span data-stu-id="7e998-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="7e998-112">Sie kopieren oder Verschieben eines Ordners oder einer Nachricht?</span><span class="sxs-lookup"><span data-stu-id="7e998-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="7e998-113">Wie viel wissen Sie zu dem Ordner oder eine Nachricht verschoben oder kopiert werden?</span><span class="sxs-lookup"><span data-stu-id="7e998-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="7e998-114">Wie viele des Ordners oder des Nachrichteneigenschaften verschoben oder kopiert werden?</span><span class="sxs-lookup"><span data-stu-id="7e998-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="7e998-115">Die **IMAPIProp** Methoden können Sie kopieren oder Verschieben eines Ordners oder einer Nachricht.</span><span class="sxs-lookup"><span data-stu-id="7e998-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="7e998-116">**IMAPIFolder::CopyMessages** ist für Nachrichten nur vorgesehen. **IMAPIFolder::CopyFolder** arbeitet mit nur Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e998-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="7e998-117">Während die Verwendung der Methoden **IMAPIFolder** nicht erforderlich sind keine Kenntnisse über die Eigenschaften, die durch den Ordner oder die Nachricht kopiert oder verschoben werden unterstützt, benötigen Sie Kenntnisse die **IMAPIProp** Methoden verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7e998-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="7e998-118">Mit **IMAPIProp::CopyProps**müssen Sie möglicherweise explizit welche Ordner oder eine Nachricht-Eigenschaften angeben, die Sie kopieren oder verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="7e998-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="7e998-119">Mit **IMAPIProp::CopyTo**es sei denn, Sie verwenden möchten, kopieren oder verschieben Sie alle Eigenschaften, müssen Sie explizit angeben, welche ausgeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e998-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="7e998-120">Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="7e998-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="7e998-121">Die Anzahl der Eigenschaften kopiert oder verschoben werden, kann Ihre Entscheidung über die zu verwendende Methode auswirken.</span><span class="sxs-lookup"><span data-stu-id="7e998-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="7e998-122">Wenn Sie kopieren oder verschieben mehrere Nachrichten, rufen Sie **IMAPIFolder::CopyMessages**.</span><span class="sxs-lookup"><span data-stu-id="7e998-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="7e998-123">Es wird eine andere Auswahl **IMAPIProp::CopyProps** zum Kopieren von nur den Ordner **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))-Eigenschaft aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="7e998-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="7e998-124">Das folgende Verfahren zeigt, wie **CopyMessages**verwenden.</span><span class="sxs-lookup"><span data-stu-id="7e998-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="7e998-125">Kopieren oder Verschieben einer oder mehrerer Nachrichten</span><span class="sxs-lookup"><span data-stu-id="7e998-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="7e998-126">Suchen Sie gültige-Eintragsbezeichner für die Quell- und Ziel-Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e998-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="7e998-127">Öffnen Sie diese Ordner im Lese-/Schreibmodus durch Aufrufen von [IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md) und das MAPI_MODIFY-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="7e998-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="7e998-128">Überprüfen Sie, ob der von **OpenEntry** zurückgegebene Schnittstellenzeiger einen **IMAPIFolder** -Schnittstelle auf.</span><span class="sxs-lookup"><span data-stu-id="7e998-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="7e998-129">Wenn dies nicht der Fall ist, wird es in den LPMAPIFOLDER-Typ umgewandelt.</span><span class="sxs-lookup"><span data-stu-id="7e998-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="7e998-130">Erstellen Sie ein Array von Eintragsbezeichner, die eine oder mehrere Nachrichten kopiert oder verschoben werden darstellt.</span><span class="sxs-lookup"><span data-stu-id="7e998-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="7e998-131">Rufen Sie mit dem folgenden Flags **IMAPIFolder::CopyMessages** :</span><span class="sxs-lookup"><span data-stu-id="7e998-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="7e998-132">MESSAGE_MOVE, wenn einen Verschiebevorgang ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="7e998-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="7e998-133">MESSAGE_DIALOG und übergeben Sie ein Fenster behandeln im _UlUIParam_ -Parameter, wenn Sie den Ordner eine Statusanzeige anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="7e998-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="7e998-134">Freigeben Sie die **IMAPIFolder** Zeiger für die Quell- und Ziel-Ordner.</span><span class="sxs-lookup"><span data-stu-id="7e998-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="7e998-135">Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie **IMAPIFolder::CopyFolder** oder **IMAPIProp::CopyTo** -Methode des Quellordners.</span><span class="sxs-lookup"><span data-stu-id="7e998-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="7e998-136">Um einige der Eigenschaften für einen Ordner zu kopieren, rufen Sie die **IMAPIProp::CopyProps** -Methode.</span><span class="sxs-lookup"><span data-stu-id="7e998-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="7e998-137">Um die meisten Eigenschaften des Ordners zu kopieren, rufen Sie **IMAPIProp::CopyTo**.</span><span class="sxs-lookup"><span data-stu-id="7e998-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="7e998-138">Wenn Sie eines Ordners **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) Eigenschaften kopieren möchten, müssen Sie die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="7e998-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="7e998-139">Rufen Sie **IMAPIFolder::CopyFolder** zum Kopieren aller Ordnereigenschaften, und klicken Sie dann die unerwünschte Elemente aus den neuen Ordner löschen.</span><span class="sxs-lookup"><span data-stu-id="7e998-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="7e998-140">Rufen Sie **CopyTo** , und schließen Sie alle Eigenschaften des Ordners mit Ausnahme **PR_DISPLAY_NAME** und **PR_COMMENT aus**.</span><span class="sxs-lookup"><span data-stu-id="7e998-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="7e998-141">Rufen Sie **CopyProps**, übergeben Sie **PR_DISPLAY_NAME** und **PR_COMMENT** im Array einschließen.</span><span class="sxs-lookup"><span data-stu-id="7e998-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="7e998-142">In diesem Fall **CopyProps** ist die beste Wahl, da es zum Kopieren Sie einer kleinen Gruppe von Eigenschaften verwendet werden soll und die einfachste Anruf implementieren.</span><span class="sxs-lookup"><span data-stu-id="7e998-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="7e998-143">Zum Kopieren oder Verschieben nur die Ordnereigenschaften, ohne Nachrichten, rufen Sie den Ordner **IMAPIProp::CopyTo** -Methode und ausgeschlossen werden Sie die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="7e998-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="7e998-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e998-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="7e998-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="7e998-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="7e998-146">Die Copy-Methoden können S_OK, insgesamt Erfolgsmeldung MAPI_W_PARTIAL_COMPLETION, zurück, der partiellen Erfolg oder Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="7e998-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="7e998-147">Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie das Makro **HR_FAILED** , um eine genauere Fehler zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="7e998-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="7e998-148">Weitere Informationen finden Sie unter [Verwendung von Makros Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="7e998-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="7e998-149">Wenn Sie Nachrichten von einem Informationsspeicher zu einer anderen kopieren und Unicode nicht, durch die beiden unterstützt wird, beachten Sie, dass Informationen verloren aufgrund der Konvertierung von Seiten werden kann.</span><span class="sxs-lookup"><span data-stu-id="7e998-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="7e998-150">In der Regel können Sie nicht wissen, wenn die Nachrichtenspeicher für eine oder beide Formate unterstützen leicht zu bestimmen, ob Eigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen mit Text kopieren nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="7e998-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="7e998-151">Wenn Unicode unterstützt werden, versuchen Sie, eine Kopie des Unicode-ausführen. Wenn sie mit den Fehlerwert MAPI_E_BAD_CHARWIDTH fehlschlägt, greifen Sie auf ASCII.</span><span class="sxs-lookup"><span data-stu-id="7e998-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

