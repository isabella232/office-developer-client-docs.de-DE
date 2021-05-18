---
title: Kopieren oder Verschieben einer Nachricht oder eines Ordners
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 72290fd3-00d7-4055-bbfa-0c47b6e0f62d
description: 'Letzte Änderung: 08. November 2011'
ms.openlocfilehash: c5e92c44d7078560ed84d72b3477d5cf2e809353
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413500"
---
# <a name="copying-or-moving-a-message-or-a-folder"></a><span data-ttu-id="d82f6-103">Kopieren oder Verschieben einer Nachricht oder eines Ordners</span><span class="sxs-lookup"><span data-stu-id="d82f6-103">Copying or moving a message or a folder</span></span>
  
<span data-ttu-id="d82f6-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d82f6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d82f6-105">Ein Client kann eine von vier Methoden verwenden, um eine Nachricht oder einen Ordner zu kopieren oder zu verschieben:</span><span class="sxs-lookup"><span data-stu-id="d82f6-105">A client can use one of four methods to copy or move a message or a folder:</span></span>
  
- [<span data-ttu-id="d82f6-106">IMAPIFolder::CopyFolder</span><span class="sxs-lookup"><span data-stu-id="d82f6-106">IMAPIFolder::CopyFolder</span></span>](imapifolder-copyfolder.md)
    
- [<span data-ttu-id="d82f6-107">IMAPIFolder::CopyMessages</span><span class="sxs-lookup"><span data-stu-id="d82f6-107">IMAPIFolder::CopyMessages</span></span>](imapifolder-copymessages.md)
    
- [<span data-ttu-id="d82f6-108">IMAPIProp::CopyTo</span><span class="sxs-lookup"><span data-stu-id="d82f6-108">IMAPIProp::CopyTo</span></span>](imapiprop-copyto.md)
    
- [<span data-ttu-id="d82f6-109">IMAPIProp::CopyProps</span><span class="sxs-lookup"><span data-stu-id="d82f6-109">IMAPIProp::CopyProps</span></span>](imapiprop-copyprops.md)
    
<span data-ttu-id="d82f6-110">Durch Festlegen der entsprechenden Flags und Parameter können **CopyTo** und **CopyProps** wie **CopyFolder** oder **CopyMessages funktionieren.**</span><span class="sxs-lookup"><span data-stu-id="d82f6-110">By setting the appropriate flags and parameters, **CopyTo** and **CopyProps** can be made to work just like **CopyFolder** or **CopyMessages**.</span></span> <span data-ttu-id="d82f6-111">Berücksichtigen Sie die folgenden Probleme bei der Entscheidung, welche Methode sie aufrufen soll:</span><span class="sxs-lookup"><span data-stu-id="d82f6-111">Consider the following issues when deciding which method to call:</span></span>
  
- <span data-ttu-id="d82f6-112">Kopieren oder verschieben Sie einen Ordner oder eine Nachricht?</span><span class="sxs-lookup"><span data-stu-id="d82f6-112">Are you copying or moving a folder or a message?</span></span>
    
- <span data-ttu-id="d82f6-113">Wie viel wissen Sie über den Ordner oder die Nachricht, der verschoben oder kopiert werden soll?</span><span class="sxs-lookup"><span data-stu-id="d82f6-113">How much do you know about the folder or message to be moved or copied?</span></span>
    
- <span data-ttu-id="d82f6-114">Wie viele Eigenschaften des Ordners oder der Nachricht werden verschoben oder kopiert?</span><span class="sxs-lookup"><span data-stu-id="d82f6-114">How many of the folder or message's properties will be moved or copied?</span></span>
    
<span data-ttu-id="d82f6-115">Sie können die **IMAPIProp-Methoden** verwenden, um einen Ordner oder eine Nachricht zu kopieren oder zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="d82f6-115">You can use the **IMAPIProp** methods to copy or move either a folder or a message.</span></span> <span data-ttu-id="d82f6-116">**IMAPIFolder::CopyMessages** kann nur mit Nachrichten verwendet werden. **IMAPIFolder::CopyFolder funktioniert** nur mit Ordnern.</span><span class="sxs-lookup"><span data-stu-id="d82f6-116">**IMAPIFolder::CopyMessages** works with messages only; **IMAPIFolder::CopyFolder** works with folders only.</span></span> 
  
<span data-ttu-id="d82f6-117">Während die Verwendung der **IMAPIFolder-Methoden** keine Kenntnisse der eigenschaften erfordert, die vom Ordner oder der Nachricht unterstützt werden, um kopiert oder verschoben zu werden, müssen Sie über einige Kenntnisse verfügen, um die **IMAPIProp-Methoden verwenden zu** können.</span><span class="sxs-lookup"><span data-stu-id="d82f6-117">Whereas using the **IMAPIFolder** methods does not require any knowledge of the properties supported by the folder or message to be copied or moved, you must have some knowledge to use the **IMAPIProp** methods.</span></span> <span data-ttu-id="d82f6-118">Mit **IMAPIProp::CopyProps** müssen Sie explizit angeben können, welche der Ordner- oder Nachrichteneigenschaften Sie kopieren oder verschieben möchten.</span><span class="sxs-lookup"><span data-stu-id="d82f6-118">With **IMAPIProp::CopyProps**, you must be able to explicitly specify which of the folder or message properties that you want to copy or move.</span></span> <span data-ttu-id="d82f6-119">Mit **IMAPIProp::CopyTo** müssen Sie explizit angeben, welche Eigenschaften ausgeschlossen werden sollen, es sei denn, Sie möchten alle Eigenschaften kopieren oder verschieben.</span><span class="sxs-lookup"><span data-stu-id="d82f6-119">With **IMAPIProp::CopyTo**, unless you want to copy or move all of the properties, you must explicitly specify which ones should be excluded.</span></span> <span data-ttu-id="d82f6-120">Weitere Informationen zu diesen Methoden finden Sie unter [Kopieren von MAPI-Eigenschaften](copying-mapi-properties.md).</span><span class="sxs-lookup"><span data-stu-id="d82f6-120">For more information about these methods, see [Copying MAPI Properties](copying-mapi-properties.md).</span></span>
  
<span data-ttu-id="d82f6-121">Die Anzahl der zu kopierenden oder zu verschobenen Eigenschaften kann sich auf Ihre Entscheidung über die zu verwendende Methode auswirken.</span><span class="sxs-lookup"><span data-stu-id="d82f6-121">The number of properties to be copied or moved can affect your decision as to which method to use.</span></span> <span data-ttu-id="d82f6-122">Wenn Sie mehrere Nachrichten kopieren oder verschieben, rufen Sie **IMAPIFolder::CopyMessages auf.**</span><span class="sxs-lookup"><span data-stu-id="d82f6-122">If you are copying or moving multiple messages, call **IMAPIFolder::CopyMessages**.</span></span> <span data-ttu-id="d82f6-123">Alternativ können Sie **IMAPIProp::CopyProps** aufrufen, um nur die **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) des Ordners zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d82f6-123">An alternate choice is to call **IMAPIProp::CopyProps** to copy only the folder's **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)) property.</span></span> <span data-ttu-id="d82f6-124">Im folgenden Verfahren wird die Verwendung von **CopyMessages veranschaulicht.**</span><span class="sxs-lookup"><span data-stu-id="d82f6-124">The following procedure shows how to use **CopyMessages**.</span></span> 
  
### <a name="to-copy-or-move-one-or-more-messages"></a><span data-ttu-id="d82f6-125">So kopieren oder verschieben Sie eine oder mehrere Nachrichten</span><span class="sxs-lookup"><span data-stu-id="d82f6-125">To copy or move one or more messages</span></span>
  
1. <span data-ttu-id="d82f6-126">Suchen Sie nach gültigen Eintragsbezeichnern für die Quell- und Zielordner.</span><span class="sxs-lookup"><span data-stu-id="d82f6-126">Locate valid entry identifiers for the source and destination folders.</span></span>
    
2. <span data-ttu-id="d82f6-127">Öffnen Sie diese Ordner im Lese-/Schreibmodus, indem Sie [entweder IMAPISession::OpenEntry](imapisession-openentry.md) oder [IMsgStore::OpenEntry](imsgstore-openentry.md) aufrufen und das MAPI_MODIFY festlegen.</span><span class="sxs-lookup"><span data-stu-id="d82f6-127">Open these folders in read/write mode by calling either [IMAPISession::OpenEntry](imapisession-openentry.md) or [IMsgStore::OpenEntry](imsgstore-openentry.md) and setting the MAPI_MODIFY flag.</span></span> 
    
3. <span data-ttu-id="d82f6-128">Überprüfen Sie, ob der von **OpenEntry zurückgegebene Schnittstellenzeiger** ein **IMAPIFolder-Schnittstellenzeiger** ist.</span><span class="sxs-lookup"><span data-stu-id="d82f6-128">Check that the interface pointer returned from **OpenEntry** is an **IMAPIFolder** interface pointer.</span></span> <span data-ttu-id="d82f6-129">Andern falls nicht, wird es in den LPMAPIFOLDER-Typ umgeknapst.</span><span class="sxs-lookup"><span data-stu-id="d82f6-129">If not, cast it to the LPMAPIFOLDER type.</span></span> 
    
4. <span data-ttu-id="d82f6-130">Erstellen Sie ein Array von Eintragsbezeichnern, die eine oder mehrere Nachrichten darstellen, die kopiert oder verschoben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d82f6-130">Create an array of entry identifiers representing the one or more messages to be copied or moved.</span></span> 
    
5. <span data-ttu-id="d82f6-131">Rufen **Sie IMAPIFolder::CopyMessages mit** den folgenden Flags auf:</span><span class="sxs-lookup"><span data-stu-id="d82f6-131">Call **IMAPIFolder::CopyMessages** with the following flags set:</span></span> 
    
   - <span data-ttu-id="d82f6-132">MESSAGE_MOVE, wenn Sie einen Verschiebevorgang ausführen möchten.</span><span class="sxs-lookup"><span data-stu-id="d82f6-132">MESSAGE_MOVE, if you want to perform a move operation.</span></span> 
    
   - <span data-ttu-id="d82f6-133">MESSAGE_DIALOG und übergeben Sie ein Fensterhandle im  _ulUIParam-Parameter,_ wenn der Ordner eine Statusanzeige anzeigen soll.</span><span class="sxs-lookup"><span data-stu-id="d82f6-133">MESSAGE_DIALOG and pass a window handle in the  _ulUIParam_ parameter, if you want the folder to show a progress indicator.</span></span> 
    
6. <span data-ttu-id="d82f6-134">Geben Sie **die IMAPIFolder-Zeiger** für die Quell- und Zielordner frei.</span><span class="sxs-lookup"><span data-stu-id="d82f6-134">Release the **IMAPIFolder** pointers for the source and destination folders.</span></span> 
    
<span data-ttu-id="d82f6-135">Wenn Sie den vollständigen Inhalt eines Ordners in einen anderen Ordner kopieren möchten, rufen Sie die **IMAPIFolder::CopyFolder-** oder **IMAPIProp::CopyTo-Methode** des Quellordners auf.</span><span class="sxs-lookup"><span data-stu-id="d82f6-135">If you want to copy the complete contents of a folder to another folder, call the source folder's **IMAPIFolder::CopyFolder** or **IMAPIProp::CopyTo** method.</span></span> 
  
<span data-ttu-id="d82f6-136">Rufen Sie die **IMAPIProp::CopyProps-Methode** auf, um einige Eigenschaften eines Ordners zu kopieren.</span><span class="sxs-lookup"><span data-stu-id="d82f6-136">To copy a few of a folder's properties, call its **IMAPIProp::CopyProps** method.</span></span> <span data-ttu-id="d82f6-137">Um die meisten Eigenschaften eines Ordners zu kopieren, rufen Sie **IMAPIProp::CopyTo auf.**</span><span class="sxs-lookup"><span data-stu-id="d82f6-137">To copy most of a folder's properties, call **IMAPIProp::CopyTo**.</span></span> 
  
<span data-ttu-id="d82f6-138">Wenn Sie beispielsweise die Eigenschaften **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) und **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) eines Ordners kopieren möchten, haben Sie die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="d82f6-138">For example, if you want to copy a folder's **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) and **PR_COMMENT** ([PidTagComment](pidtagcomment-canonical-property.md)) properties, you have the following options:</span></span>
  
- <span data-ttu-id="d82f6-139">Rufen **Sie IMAPIFolder::CopyFolder auf,** um alle Ordnereigenschaften zu kopieren und die unerwünschten Eigenschaften dann aus dem neuen Ordner zu löschen.</span><span class="sxs-lookup"><span data-stu-id="d82f6-139">Call **IMAPIFolder::CopyFolder** to copy all of the folder properties and then delete the unwanted ones from the new folder.</span></span> 
    
- <span data-ttu-id="d82f6-140">Rufen **Sie CopyTo** auf, und schließen Sie alle Eigenschaften des Ordners aus, mit Ausnahme von **PR_DISPLAY_NAME** und **PR_COMMENT**.</span><span class="sxs-lookup"><span data-stu-id="d82f6-140">Call **CopyTo** and exclude all of the folder's properties except for **PR_DISPLAY_NAME** and **PR_COMMENT**.</span></span> 
    
- <span data-ttu-id="d82f6-141">Rufen **Sie CopyProps** auf, **PR_DISPLAY_NAME** und **PR_COMMENT** im include-Array übergeben.</span><span class="sxs-lookup"><span data-stu-id="d82f6-141">Call **CopyProps**, passing **PR_DISPLAY_NAME** and **PR_COMMENT** in the include array.</span></span> 
    
<span data-ttu-id="d82f6-142">In diesem Fall ist **CopyProps** die beste Wahl, da es zum Kopieren einer kleinen Gruppe von Eigenschaften verwendet werden soll und der einfachste Aufruf zur Implementierung ist.</span><span class="sxs-lookup"><span data-stu-id="d82f6-142">In this case, **CopyProps** is the best choice because it is meant to be used to copy a small set of properties and is the easiest call to implement.</span></span> 
  
<span data-ttu-id="d82f6-143">Um nur Ordnereigenschaften zu kopieren oder zu verschieben, ohne Nachrichten zu enthalten, rufen Sie die **IMAPIProp::CopyTo-Methode** des Ordners auf, und schließen Sie die folgenden Eigenschaften aus:</span><span class="sxs-lookup"><span data-stu-id="d82f6-143">To copy or move only folder properties, without including messages, call the folder's **IMAPIProp::CopyTo** method and exclude the following properties:</span></span> 
  
- <span data-ttu-id="d82f6-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d82f6-144">**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))</span></span>
    
- <span data-ttu-id="d82f6-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="d82f6-145">**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))</span></span>
    
<span data-ttu-id="d82f6-146">Die Kopiermethoden können S_OK zurückgeben, was den Gesamterfolg angibt, MAPI_W_PARTIAL_COMPLETION, einen Teilerfolg oder einen Fehler angibt.</span><span class="sxs-lookup"><span data-stu-id="d82f6-146">The copy methods can return S_OK, indicating total success, MAPI_W_PARTIAL_COMPLETION, indicating partial success, or an error.</span></span> <span data-ttu-id="d82f6-147">Wenn MAPI_W_PARTIAL_COMPLETION zurückgegeben wird, verwenden Sie **HR_FAILED** Makro, um auf einen spezifischeren Fehler zu zugreifen.</span><span class="sxs-lookup"><span data-stu-id="d82f6-147">If MAPI_W_PARTIAL_COMPLETION is returned, use the **HR_FAILED** macro to access a more specific error.</span></span> <span data-ttu-id="d82f6-148">Weitere Informationen finden Sie unter [Using Macros for Error Handling](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="d82f6-148">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
  
<span data-ttu-id="d82f6-149">Wenn Sie Nachrichten aus einem Nachrichtenspeicher in einen anderen kopieren und Unicode von beiden nicht unterstützt wird, beachten Sie, dass Informationen aufgrund der Codeseitenkonvertierung verloren gehen können.</span><span class="sxs-lookup"><span data-stu-id="d82f6-149">If you copy messages from one message store to another and Unicode is not supported by both, be aware that information can be lost due to code page conversion.</span></span> <span data-ttu-id="d82f6-150">In der Regel können Sie nicht wissen, ob die Nachrichtenspeicher ein oder beide Formate unterstützen, was es unmöglich macht, zu bestimmen, ob Texteigenschaften als ASCII-Zeichenfolgen oder als Unicode-Zeichenfolgen kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="d82f6-150">Usually you cannot know if the message stores support one or both formats, making it impossible to determine whether to copy text properties as ASCII strings or as Unicode strings.</span></span> <span data-ttu-id="d82f6-151">Wenn Sie Unicode unterstützen, versuchen Sie, eine #A0 durchzuführen. Wenn ein Fehler mit dem Fehlerwert MAPI_E_BAD_CHARWIDTH, greifen Sie auf ASCII zurück.</span><span class="sxs-lookup"><span data-stu-id="d82f6-151">If you support Unicode, try to perform a Unicode copy; if it fails with the error value MAPI_E_BAD_CHARWIDTH, resort to ASCII.</span></span>
  

