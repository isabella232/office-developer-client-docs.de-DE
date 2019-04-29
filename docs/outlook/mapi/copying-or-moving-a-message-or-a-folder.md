---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Zuletzt geändert: 20 November, 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413500"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="3206f-103">Kopieren oder Verschieben einer Nachricht oder eines Ordners</span><span class="sxs-lookup"><span data-stu-id="3206f-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="3206f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3206f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3206f-105">Ein Client kann eine der vier Methoden zum Kopieren oder Verschieben einer Nachricht oder eines Ordners verwenden:</span><span class="sxs-lookup"><span data-stu-id="3206f-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="3206f-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="3206f-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="3206f-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="3206f-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="3206f-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="3206f-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="3206f-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="3206f-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="3206f-110">Durch Festlegen der entsprechenden Flags und Parameter können **CopyTo** und **CopyProps** wie **CopyFolder** oder **CopyMessages**ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="3206f-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="3206f-111">Berücksichtigen Sie bei der Entscheidung, welche Methode aufgerufen werden soll, die folgenden Probleme:</span><span class="sxs-lookup"><span data-stu-id="3206f-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="3206f-112">Kopieren oder bewegen Sie einen Ordner oder eine Nachricht?</span><span class="sxs-lookup"><span data-stu-id="3206f-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="3206f-113">Wie viel wissen Sie über den Ordner oder die Nachricht, der verschoben oder kopiert werden soll?</span><span class="sxs-lookup"><span data-stu-id="3206f-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="3206f-114">Wie viele der Eigenschaften des Ordners oder der Nachricht werden verschoben oder kopiert?</span><span class="sxs-lookup"><span data-stu-id="3206f-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="3206f-115">Sie können die **IMAPIProp** -Methoden verwenden, um einen Ordner oder eine Nachricht zu kopieren oder zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="3206f-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="3206f-116">**IMAPIFolder:: CopyMessages** funktioniert nur mit Nachrichten; **IMAPIFolder:: CopyFolder** funktioniert nur mit Ordnern.</span><span class="sxs-lookup"><span data-stu-id="3206f-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="3206f-117">Während die Verwendung der **IMAPIFolder** -Methoden keine Kenntnis der vom Ordner oder der zu verschiebenden Nachricht unterstützten Eigenschaften erfordert, müssen Sie über Kenntnisse verfügen, um die **IMAPIProp** -Methoden verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="3206f-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="3206f-118">Mit **IMAPIProp:: CopyProps**müssen Sie in der Lage sein, explizit anzugeben, welche der Ordner-oder Nachrichteneigenschaften Sie kopieren oder verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="3206f-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="3206f-119">Wenn Sie alle Eigenschaften mit **IMAPIProp:: CopyTo**kopieren oder verschieben möchten, müssen Sie explizit angeben, welche davon ausgeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3206f-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="3206f-120">Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="3206f-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="3206f-121">Die Anzahl der Eigenschaften, die kopiert oder verschoben werden können, kann sich auf die Entscheidung für die zu verwendende Methode auswirken.</span><span class="sxs-lookup"><span data-stu-id="3206f-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="3206f-122">Wenn Sie mehrere Nachrichten kopieren oder ändern, rufen Sie **IMAPIFolder:: CopyMessages**auf.</span><span class="sxs-lookup"><span data-stu-id="3206f-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="3206f-123">Alternativ können Sie **IMAPIProp:: CopyProps** aufrufen, um nur die **PR_CONTAINER_CONTENTS** ([pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))-Eigenschaft des Ordners zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3206f-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="3206f-124">Im folgenden Verfahren wird gezeigt, wie Sie **CopyMessages**verwenden.</span><span class="sxs-lookup"><span data-stu-id="3206f-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="3206f-125">So kopieren oder verschieben Sie eine oder mehrere Nachrichten</span><span class="sxs-lookup"><span data-stu-id="3206f-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="3206f-126">Suchen gültiger Eintragsbezeichner für die Quell-und Zielordner.</span><span class="sxs-lookup"><span data-stu-id="3206f-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="3206f-127">Öffnen Sie diese Ordner im Lese-/Schreibzugriff, indem Sie entweder [IMAPISession:: OpenEntry](imapisession-openentry.md) oder [IMsgStore:: OpenEntry](imsgstore-openentry.md) aufrufen und das MAPI_MODIFY-Flag festlegen.</span><span class="sxs-lookup"><span data-stu-id="3206f-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="3206f-128">Stellen Sie sicher, dass der von **OpenEntry** zurückgegebene Schnittstellenzeiger ein **IMAPIFolder** -Schnittstellenzeiger ist.</span><span class="sxs-lookup"><span data-stu-id="3206f-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="3206f-129">Wenn dies nicht der Fall ist, wandeln Sie ihn in den LPMAPIFOLDER-Typ um.</span><span class="sxs-lookup"><span data-stu-id="3206f-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="3206f-130">Erstellen Sie ein Array von Eintrags Bezeichnern, die die eine oder mehrere Nachrichten darstellen, die kopiert oder verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="3206f-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="3206f-131">Rufen Sie **IMAPIFolder:: CopyMessages** auf, wobei die folgenden Flags festgelegt sind:</span><span class="sxs-lookup"><span data-stu-id="3206f-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="3206f-132">MESSAGE_MOVE, wenn Sie einen Verschiebungsvorgang ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="3206f-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="3206f-133">MESSAGE_DIALOG, und übergeben Sie ein Fensterhandle im _ulUIParam_ -Parameter, wenn der Ordner eine Statusanzeige anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="3206f-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="3206f-134">Geben Sie die **IMAPIFolder** -Zeiger für die Quell-und Zielordner frei.</span><span class="sxs-lookup"><span data-stu-id="3206f-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="3206f-135">Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie die **IMAPIFolder:: CopyFolder** -oder **IMAPIProp:: CopyTo** -Methode des Quellordners auf.</span><span class="sxs-lookup"><span data-stu-id="3206f-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="3206f-136">Rufen Sie die **IMAPIProp:: CopyProps** -Methode auf, um einige der Eigenschaften eines Ordners zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="3206f-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="3206f-137">Um die meisten Eigenschaften eines Ordners zu kopieren, rufen Sie **IMAPIProp:: CopyTo**auf.</span><span class="sxs-lookup"><span data-stu-id="3206f-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="3206f-138">Wenn Sie beispielsweise die Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) eines Ordners kopieren möchten, haben Sie folgende Möglichkeiten:</span><span class="sxs-lookup"><span data-stu-id="3206f-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="3206f-139">Rufen Sie **IMAPIFolder:: CopyFolder** auf, um alle Ordner Eigenschaften zu kopieren und die unerwünschten Dateien aus dem neuen Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="3206f-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="3206f-140">Rufen Sie **CopyTo** auf, und schließen Sie alle Eigenschaften des Ordners außer für **PR_DISPLAY_NAME** und **PR_COMMENT**aus.</span><span class="sxs-lookup"><span data-stu-id="3206f-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="3206f-141">Rufen Sie **CopyProps**auf, und übergeben Sie **PR_DISPLAY_NAME** und **PR_COMMENT** im Include-Array.</span><span class="sxs-lookup"><span data-stu-id="3206f-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="3206f-142">In diesem Fall ist **CopyProps** die beste Wahl, da es verwendet werden soll, um eine kleine Gruppe von Eigenschaften zu kopieren und am einfachsten zu implementieren ist.</span><span class="sxs-lookup"><span data-stu-id="3206f-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="3206f-143">Um nur Ordner Eigenschaften zu kopieren oder zu verschieben, ohne Nachrichten hinzufügen, rufen Sie die **IMAPIProp:: CopyTo** -Methode des Ordners auf, und schließen Sie die folgenden Eigenschaften aus:</span><span class="sxs-lookup"><span data-stu-id="3206f-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="3206f-144">**PR_CONTAINER_CONTENTS** ([Pidtagcontainercontents (](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3206f-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="3206f-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([Pidtagfolderassociatedcontents (](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3206f-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="3206f-146">Die Copy-Methoden können S_OK zurückgeben, was bedeutet, dass der gesamte Erfolg, MAPI_W_PARTIAL_COMPLETION, der teilweiser Erfolg angibt, oder ein Fehler.</span><span class="sxs-lookup"><span data-stu-id="3206f-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="3206f-147">Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie das **HR_FAILED** -Makro, um auf einen spezifischeren Fehler zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="3206f-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="3206f-148">Weitere Informationen finden Sie unter [Verwenden von Makros zur Fehlerbehandlung](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="3206f-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="3206f-149">Wenn Sie Nachrichten aus einem Nachrichtenspeicher in einen anderen kopieren und Unicode von beiden nicht unterstützt wird, beachten Sie, dass Informationen aufgrund der Konvertierung von Codeseiten verloren gehen können.</span><span class="sxs-lookup"><span data-stu-id="3206f-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="3206f-150">In der Regel können Sie nicht wissen, ob die Nachrichtenspeicher ein oder beide Formate unterstützen, sodass es unmöglich ist, zu bestimmen, ob Texteigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen kopiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3206f-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="3206f-151">Wenn Sie Unicode unterstützen, versuchen Sie, eine Unicode-Kopie auszuführen. Wenn Sie mit dem Fehlerwert MAPI_E_BAD_CHARWIDTH fehlschlägt, greifen Sie auf ASCII zu.</span><span class="sxs-lookup"><span data-stu-id="3206f-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

