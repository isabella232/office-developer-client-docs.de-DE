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
ms.openlocfilehash: ff40eddf63e67f45495e90c1a960e45b7cc6cfb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795499"
---
# <a name="sending-messages-mapi-spooler-tasks"></a><span data-ttu-id="5e7fc-103">Senden von Nachrichten: MAPI-Warteschlange Aufgaben</span><span class="sxs-lookup"><span data-stu-id="5e7fc-103">Sending Messages: MAPI Spooler Tasks</span></span>

  
  
<span data-ttu-id="5e7fc-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e7fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e7fc-105">Die MAPI-Warteschlange ist bei der �bertragung beteiligt, wenn der Nachrichtenspeicher mit einem Transportanbieter nicht eng verkn�pft ist, wenn den eng gekoppelten Speicher und Transport einen Empf�nger nicht verarbeiten k�nnen und die Nachricht Vorverarbeitung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-105">The MAPI spooler is involved in the message transmission process when the message store is not tightly coupled with a transport provider, when the tightly coupled store and transport cannot handle a recipient, and when the message requires preprocessing.</span></span>
  
 <span data-ttu-id="5e7fc-106">**Nach der erforderlichen Vorverarbeitung f�hrt die MAPI-Warteschlange die folgenden Schritte aus:**</span><span class="sxs-lookup"><span data-stu-id="5e7fc-106">**After any necessary preprocessing, the MAPI spooler performs the following steps:**</span></span>
  
1. <span data-ttu-id="5e7fc-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-107">If the message is not locked, locks the message by using the [IMsgStore::SetLockState](imsgstore-setlockstate.md) method.</span></span> 
    
2. <span data-ttu-id="5e7fc-108">Hat der Adressbuchhierarchie die Nachricht an alle Empfänger zu senden, die ihre **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md))-Eigenschaft auf FALSE festgelegt sein.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-108">Has the transport provider send the message to all recipients that have their **PR_RESPONSIBILITY** ([PidTagResponsibility](pidtagresponsibility-canonical-property.md)) property set to FALSE.</span></span> 
    
3. <span data-ttu-id="5e7fc-109">Ruft die entsprechende Funktion ([RemovePreprocessInfo](removepreprocessinfo.md)) zum Bereinigen von zusätzliche Informationen, die an die Nachricht für die Verwendung während der vorverarbeitung, wenn die **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md))-Eigenschaft festgelegt wurde hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-109">Calls the appropriate function ([RemovePreprocessInfo](removepreprocessinfo.md)) for cleaning up any additional information that was added to the message for use during preprocessing if the **PR_PREPROCESS** ([PidTagPreprocess](pidtagpreprocess-canonical-property.md)) property has been set.</span></span> <span data-ttu-id="5e7fc-110">This function is specified when the transport provider registers its preprocessor function.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-110">This function is specified when the transport provider registers its preprocessor function.</span></span> 
    
4. <span data-ttu-id="5e7fc-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span><span class="sxs-lookup"><span data-stu-id="5e7fc-p102">Calls [IMsgStore::FinishedMsg](imsgstore-finishedmsg.md) method. In **FinishedMsg**, the message store provider:</span></span>
    
  - <span data-ttu-id="5e7fc-113">Hebt die Sperre der Nachricht.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-113">Unlocks the message.</span></span>
    
  - <span data-ttu-id="5e7fc-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-114">Calls the [IMAPISupport::DoSentMail](imapisupport-dosentmail.md) method to perform outbound hook processing if a messaging hook provider exists.</span></span> <span data-ttu-id="5e7fc-115">Dann wird die Nachricht kopiert, zu dem Ordner, der durch die Eintrags-ID in der Eigenschaft **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) bezeichnet, wenn nicht durch eine messaging abgelöst des Hook Anbieter Verarbeitung von Nachrichten gesendet.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-115">It then copies the message to the folder identified by the entry identifier in the **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) property, if not superseded by a messaging hook provider's sent message processing.</span></span> <span data-ttu-id="5e7fc-116">Schließlich löscht die Nachricht, wenn die **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md))-Eigenschaft auf TRUE festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="5e7fc-116">Finally, it deletes the message if the **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) property has been set to TRUE.</span></span> 
    
