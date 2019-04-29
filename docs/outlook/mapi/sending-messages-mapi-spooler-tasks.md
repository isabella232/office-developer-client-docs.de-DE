---
title: Senden von Nachrichten MAPI-Warteschlange Aufgaben
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 81c65f21-03ba-43eb-a6d4-d311e660ac5c
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 8a6730cca5c75a888afb5ff0a44f1e2a0a6465e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420199"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="ab5b9-103">Senden von Nachrichten: MAPI-Spooler-Aufgaben</span><span class="sxs-lookup"><span data-stu-id="ab5b9-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="ab5b9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab5b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab5b9-105">Die MAPI-Warteschlange ist bei der �bertragung beteiligt, wenn der Nachrichtenspeicher mit einem Transportanbieter nicht eng verkn�pft ist, wenn den eng gekoppelten Speicher und Transport einen Empf�nger nicht verarbeiten k�nnen und die Nachricht Vorverarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="ab5b9-106">**Nach der erforderlichen Vorverarbeitung f�hrt die MAPI-Warteschlange die folgenden Schritte aus:**</span><span class="sxs-lookup"><span data-stu-id="ab5b9-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="ab5b9-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="ab5b9-108">Der Transportanbieter sendet die Nachricht an alle Empfänger, deren **PR_RESPONSIBILITY** ([pidtagresponsibility (](pidtagresponsibility-canonical-property.md))-Eigenschaft auf false festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="ab5b9-109">Ruft die entsprechende Funktion ([RemovePreprocessInfo](removepreprocessinfo.md)) zum Bereinigen zusätzlicher Informationen auf, die der Nachricht zur Verwendung während der Vorverarbeitung hinzugefügt wurden, wenn die **PR_PREPROCESS** ([pidtagpreprocess (](pidtagpreprocess-canonical-property.md))-Eigenschaft festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="ab5b9-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="ab5b9-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="ab5b9-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="ab5b9-113">Hebt die Sperre der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="ab5b9-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="ab5b9-115">Anschließend wird die Nachricht in den Ordner kopiert, der durch die Eintrags-ID in der **PR_SENTMAIL_ENTRYID** ([pidtagsentmailentryid (](pidtagsentmailentryid-canonical-property.md))-Eigenschaft identifiziert wird, wenn Sie nicht durch die Verarbeitung der gesendeten Nachrichten eines Messaging-Hooks ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="ab5b9-116">Schließlich wird die Nachricht gelöscht, wenn die **PR_DELETE_AFTER_SUBMIT** ([pidtagdeleteaftersubmit (](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf true festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="ab5b9-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    

