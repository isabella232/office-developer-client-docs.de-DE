---
title: Suchen nach gesendeten oder gespeicherten Nachrichten
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 6b6714a5-7f36-4a72-9a2a-0d7fdf0e21b7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 77d7173a6a62a375108f0d8bcffa3b99237417b2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588000"
---
# <a name="finding-sent-or-saved-messages"></a>Suchen nach gesendeten oder gespeicherten Nachrichten

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
 **So suchen Sie alle ausgehenden Nachrichten, die Sie gespeichert oder gesendet haben**
  
1. Rufen [Sie IMsgStore::CompareEntryIDs](imsgstore-compareentryids.md) auf, um den Ordner, der Ihre gesendeten Nachrichten enthält, mit dem Ordner zu vergleichen, der Ihre eingehenden Nachrichten enthält. 
    
2. Legen Sie den  _Parameter lpEntryID1_ so fest, **dass er** auf PR_IPM_SENTMAIL_ENTRYID ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md)) und den  _Parameter lpEntryID2_ verweist, um auf **PR_PARENT_ENTRYID** ([PidTagParentEntryId](pidtagparententryid-canonical-property.md)) zu verweisen.
    
Beachten Sie, dass diese Strategie nicht funktioniert, wenn Sie nachrichten löschen, nachdem sie gesendet wurden oder eine der gesendeten Nachrichten in einen anderen Ordner verschoben haben. 
  
Wenn Sie bei der Untersuchung einer eingehenden Nachricht feststellen, dass die Eigenschaften fehlen, die normalerweise von einem Transportanbieter festgelegt werden, können Sie davon ausgehen, dass die Nachricht nie von einem Transportanbieter verarbeitet wurde. Zu diesen Eigenschaften zählen:
  
- **PR_RECEIVED_BY** Eigenschaften 
    
- **PR_MESSAGE_DOWNLOAD_TIME** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))
    
- **PR_TRANSPORT_MESSAGE_HEADERS** ([PidTagTransportMessageHeaders](pidtagtransportmessageheaders-canonical-property.md))
    
- **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md))
    
- **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md))
    
- **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md))
    

