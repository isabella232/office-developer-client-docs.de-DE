---
title: Löschen einer Nachricht
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 9ed166b4-6b7b-478f-bbe5-4115bb818ac0
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: c8d46ac6f47eb4dc68aebfa4562403ef1b738213
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791518"
---
# <a name="deleting-a-message"></a><span data-ttu-id="5c332-103">Löschen einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="5c332-103">Deleting a Message</span></span>

  
  
<span data-ttu-id="5c332-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5c332-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5c332-105">Ein Client kann eine Nachricht löschen, wenn es geöffnet ist und der Benutzer ist es lesen oder wenn es geschlossen wird, und der Benutzer wird die Inhaltstabelle anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5c332-105">A client can delete a message when it is open and the user is reading it, or when it is closed and the user is viewing the contents table.</span></span> <span data-ttu-id="5c332-106">Um ein Benutzer eine Nachricht versehentlich entfernen zu schützen, definiert MAPI Löschen von Nachrichten als zwei Schritten zusammen:</span><span class="sxs-lookup"><span data-stu-id="5c332-106">To protect a user from inadvertently removing a message, MAPI defines message deletion as a two step process:</span></span>
  
1. <span data-ttu-id="5c332-107">Markieren Sie eine Nachricht zum Löschen, indem Sie in den Ordner, die als den Ordner Gelöschte Objekte festgelegt wurde verschoben – Ordners, dessen Eintrags-ID in der **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))-Eigenschaft gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="5c332-107">Mark a message for deletion by moving it to the folder that has been designated as the Deleted Items folder — the folder whose entry identifier is stored in the **PR_IPM_WASTEBASKET_ENTRYID** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md)) property.</span></span> 
    
2. <span data-ttu-id="5c332-108">Entfernen Sie die Meldung durch Aufrufen der Methode [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) .</span><span class="sxs-lookup"><span data-stu-id="5c332-108">Remove the message by calling the [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) method.</span></span> 
    
<span data-ttu-id="5c332-109">Wenn ein Benutzer beschließt, eine Nachricht in einem anderen Ordner als dem Ordner Gelöschte Objekte löschen, markieren Sie es zum Löschen.</span><span class="sxs-lookup"><span data-stu-id="5c332-109">When a user chooses to delete a message in a folder other than the Deleted Items folder, mark it for deletion.</span></span> <span data-ttu-id="5c332-110">Nur, wenn ein Benutzer Nachrichten von in den Ordner Gelöschte Elemente auswählt sollten die Nachrichten physisch aus der Arbeitsstation entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="5c332-110">Only when a user selects messages from within the Deleted Items folder should the messages be physically removed from the workstation.</span></span> <span data-ttu-id="5c332-111">Sie können der Benutzer aufgefordert, stellen Sie sicher, dass der Benutzer wirklich für die direkte Verwendung den Löschvorgang ausführen.</span><span class="sxs-lookup"><span data-stu-id="5c332-111">You can prompt the user to verify that the user really intended to perform the deletion.</span></span>
  
 <span data-ttu-id="5c332-112">**So löschen Sie eine Nachricht**</span><span class="sxs-lookup"><span data-stu-id="5c332-112">**To delete a message**</span></span>
  
1. <span data-ttu-id="5c332-113">Bestätigen Sie mit dem Benutzer, dass der Löschvorgang bevorstehenden beabsichtigt ist.</span><span class="sxs-lookup"><span data-stu-id="5c332-113">Confirm with the user that the impending deletion is intentional.</span></span>
    
2. <span data-ttu-id="5c332-114">Bestimmen Sie das übergeordnete Element des Ordners gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c332-114">Determine the parent of the folder to be deleted.</span></span> <span data-ttu-id="5c332-115">Wenn sie den Ordner Gelöschte Objekte oder einen Unterordner im Ordner Gelöschte Elemente ist, rufen Sie [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) , um die Nachricht zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="5c332-115">If it is the Deleted Items folder or a subfolder within the Deleted Items folder, call [IMAPIFolder::DeleteMessages](imapifolder-deletemessages.md) to remove the message.</span></span> 
    
3. <span data-ttu-id="5c332-116">Wenn der Ordner nicht in den Ordner Gelöschte Objekte enthalten ist, rufen Sie [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) mit der MESSAGE_MOVE-Flag, die Nachricht in den Ordner Gelöschte Elemente zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="5c332-116">If the folder is not contained within the Deleted Items folder, call [IMAPIFolder::CopyMessages](imapifolder-copymessages.md) with the MESSAGE_MOVE flag set to relocate the message to the Deleted Items folder.</span></span> 
    

