---
title: Unterstützen des Objektzugriffs und -vergleichs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 9383cd11a9183032d2aeaa7621b72592700e977c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59609473"
---
# <a name="supporting-object-access-and-comparison"></a>Unterstützen des Objektzugriffs und -vergleichs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter können die Methoden [IMAPISupport::OpenEntry](imapisupport-openentry.md) und [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) verwenden, um Objekte zu öffnen und zu vergleichen, die zu ihrem Anbieter oder zu anderen Anbietern gehören: 
  
Wie [IMAPISession::OpenEntry](imapisession-openentry.md) für Clients können Anbieter die **OpenEntry-Methode** ihres Supportobjekts verwenden, um auf jedes Objekt zuzugreifen, solange sie den Eintragsbezeichner des Objekts kennen. Im Gegensatz zur Sitzungsmethode erfordert die Unterstützungsmethode, dass Sie einen gültigen Eintragsbezeichner im  _LpEntryID-Parameter_ angeben. Er darf nicht NULL sein. 
  
Um zu veranschaulichen, wie ein Transportanbieter **IMAPISupport::OpenEntry** verwenden kann, betrachten Sie das folgende Szenario. Der Transportanbieter hat eine im Rich-Text-Format formatierte Nachricht erhalten und weiß nicht, ob der Zielempfänger dieses Format verarbeiten kann. Vor der Zustellung der Nachricht muss der Transportanbieter Folgendes tun:
  
1. Rufen Sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) der Nachricht auf, um auf die Empfängertabelle und den Eintragsbezeichner des Empfängers zuzugreifen, **deren PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft.
    
2. Übergeben Sie den Eintragsbezeichner an **IMAPISupport::OpenEntry,** um den Empfänger zu öffnen, in der Regel ein Messagingbenutzer oder eine Verteilerliste. Der  _lpInterface-Parameter_ sollte auf NULL festgelegt werden, da der Anbieter den Objekttyp des Empfängers nicht vorab erkennen kann. Die **OpenEntry-Methode** des Supportobjekts ruft [IMAPISession::OpenEntry](imapisession-openentry.md) auf, um den für den Empfänger verantwortlichen Adressbuchanbieter zu ermitteln. Das Sitzungsobjekt ruft dann die **OpenEntry-Methode** des entsprechenden Adressbuchanbieters auf, um den Empfänger zu öffnen und einen Schnittstellenzeiger an den Transportanbieter zurückzugeben. 
    
3. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Empfängers auf, um die **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) -Eigenschaft abzurufen. Wenn **PR_SEND_RICH_INFO** auf TRUE festgelegt ist, kann der Empfänger formatierten Text verarbeiten. 
    
Wenn Sie mehrere Objekte von anderen Anbietern geöffnet haben, müssen Sie möglicherweise herausfinden, ob zwei Eintragsbezeichner auf dasselbe Objekt verweisen. Beispielsweise verfügen Sie möglicherweise über einen kurzfristigen Eintragsbezeichner und einen langfristigen Eintragsbezeichner, und diese Bezeichner können dasselbe Objekt identifizieren oder nicht. Um redundante Verarbeitung zu vermeiden, rufen Sie die [IMAPISupport::CompareEntryIDs-Methode](imapisupport-compareentryids.md) auf, um diese Eintragsbezeichner zu vergleichen. Sie müssen diese Methode für den Eintragsbezeichnervergleich verwenden, da Eintragsbezeichner nicht direkt verglichen werden können. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

