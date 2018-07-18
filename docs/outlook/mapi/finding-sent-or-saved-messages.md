---
title: Suchen nach gesendeten oder gespeicherten Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6e8b618e477475e8e7f45c266791086af63d8bfb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791695"
---
# <a name="finding-sent-or-saved-messages"></a>Suchen nach gesendeten oder gespeicherten Nachrichten

  
  
**Betrifft**: Outlook 
  
 **Um alle ausgehenden Nachrichten zu suchen, die Sie gespeichert oder gesendet**
  
1. Rufen Sie [IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) , um den Ordner zu vergleichen, der Ihre gesendeten Nachrichten mit den Ordner enthält, die Ihre eingehenden Nachrichten enthält. 
    
2. Legen Sie den Parameter _lpEntryID1_ So zeigen Sie auf **PR_IPM_SENTMAIL_ENTRYID** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) und _lpEntryID2_ **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) auf.
    
Beachten Sie, dass Sie entweder Nachrichten löschen, nachdem sie gesendet oder eine der gesendeten Nachrichten in einen anderen Ordner verschoben haben, diese Strategie nicht funktionsfähig ist. 
  
Wenn Sie sich bei der Prüfung einer eingehenden Nachricht feststellen, dass die Eigenschaften, die normalerweise von einem Transportanbieter festgelegt sind nicht vorhanden sind, können Sie davon ausgehen, dass die Nachricht von einem Transportanbieter nie behandelt wurde. Diese Eigenschaften umfassen:
  
- **PR_RECEIVED_BY** -Eigenschaften 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

