---
title: Löschen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 663eebfcd1b8862b22d8c822957024c4f31499de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433164"
---
# <a name="deleting-a-message"></a><span data-ttu-id="68db3-103">Löschen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="68db3-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="68db3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68db3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68db3-105">Ein Client kann eine Nachricht löschen, wenn Sie geöffnet ist und der Benutzer Sie liest, oder wenn Sie geschlossen ist und der Benutzer die Tabelle Inhalt anzeigt.</span><span class="sxs-lookup"><span data-stu-id="68db3-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="68db3-106">Um zu verhindern, dass ein Benutzer versehentlich eine Nachricht entfernt, definiert MAPI das Löschen von Nachrichten als zweistufigen Prozess:</span><span class="sxs-lookup"><span data-stu-id="68db3-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="68db3-107">Markieren Sie eine Nachricht zum Löschen, indem Sie Sie in den Ordner bewegen, der als Ordner "Gelöschte Elemente" festgelegt wurde – den Ordner, dessen Eintragsbezeichner in der **PR_IPM_WASTEBASKET_ENTRYID** ([pidtagipmwastebasketentryid (](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="68db3-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="68db3-108">Entfernen Sie die Nachricht, indem Sie die [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="68db3-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="68db3-109">Wenn ein Benutzer eine Nachricht in einem anderen Ordner als dem Ordner "Gelöschte Elemente" löscht, markieren Sie ihn zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="68db3-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="68db3-110">Nur, wenn ein Benutzer Nachrichten aus dem Ordner "Gelöschte Elemente" auswählt, sollten die Nachrichten physisch von der Arbeitsstation entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="68db3-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="68db3-111">Sie können den Benutzer auffordern, zu überprüfen, ob der Benutzer den Löschvorgang wirklich ausführen wollte.</span><span class="sxs-lookup"><span data-stu-id="68db3-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="68db3-112">**So löschen Sie eine Nachricht**</span><span class="sxs-lookup"><span data-stu-id="68db3-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="68db3-113">Bestätigen Sie mit dem Benutzer, dass die bevorstehende Löschung beabsichtigt ist.</span><span class="sxs-lookup"><span data-stu-id="68db3-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="68db3-114">Bestimmen Sie das übergeordnete Element des zu löschenden Ordners.</span><span class="sxs-lookup"><span data-stu-id="68db3-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="68db3-115">Wenn es sich um den Ordner "Gelöschte Elemente" oder einen Unterordner im Ordner "Gelöschte Elemente" handelt, rufen Sie [IMAPIFolder::D eletemessages](imapifolder-deletemessages.md) auf, um die Nachricht zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="68db3-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="68db3-116">Wenn der Ordner nicht im Ordner "Gelöschte Elemente" enthalten ist, rufen Sie [IMAPIFolder:: CopyMessages](imapifolder-copymessages.md) , wobei das MESSAGE_MOVE-Flag festgelegt ist, um die Nachricht in den Ordner "Gelöschte Elemente" zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="68db3-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

