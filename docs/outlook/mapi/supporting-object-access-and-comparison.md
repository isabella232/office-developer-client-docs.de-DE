---
title: Unterstützen des Objektzugriffs und -vergleichs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2b62f92325fcebf8cd3f0c86d28d98e7ff511ee2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429033"
---
# <a name="supporting-object-access-and-comparison"></a>Unterstützen des Objektzugriffs und -vergleichs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter können die [Methoden IMAPISupport::OpenEntry](imapisupport-openentry.md) und [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) verwenden, um Objekte zu öffnen und zu vergleichen, die zu ihrem Anbieter oder zu anderen Anbietern gehören: 
  
Wie [IMAPISession::OpenEntry](imapisession-openentry.md) für Clients können Anbieter die **OpenEntry-Methode** ihres Supportobjekts verwenden, um auf jedes Objekt zu zugreifen, solange sie den Eintragsbezeichner des Objekts kennen. Im Gegensatz zur Sitzungsmethode erfordert die Supportmethode, dass Sie einen gültigen Eintragsbezeichner im  _lpEntryID-Parameter_ angeben. Es kann nicht NULL sein. 
  
Um zu veranschaulichen, wie ein Transportanbieter **IMAPISupport::OpenEntry** verwenden kann, sollten Sie das folgende Szenario berücksichtigen. Der Transportanbieter hat eine Im Rich-Text-Format formatierte Nachricht empfangen und weiß nicht, ob der Zielempfänger dieses Format verarbeiten kann. Vor dem Senden der Nachricht muss der Transportanbieter die folgenden Schritte tun:
  
1. Rufen Sie die [IMessage::GetRecipientTable-Methode](imessage-getrecipienttable.md) der Nachricht auf, um auf die Empfängertabelle und die Eintrags-ID des Empfängers zu zugreifen, deren **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) -Eigenschaft.
    
2. Übergeben Sie die Eintrags-ID **an IMAPISupport::OpenEntry,** um den Empfänger zu öffnen, in der Regel entweder einen Messagingbenutzer oder eine Verteilerliste. Der  _lpInterface-Parameter_ sollte auf NULL festgelegt werden, da der Anbieter den Objekttyp des Empfängers nicht im Voraus kennen kann. Die **OpenEntry-Methode des Supportobjekts** ruft [IMAPISession::OpenEntry auf,](imapisession-openentry.md) um den Adressbuchanbieter zu ermitteln, der für den Empfänger verantwortlich ist. Das Sitzungsobjekt ruft dann die **OpenEntry-Methode** des entsprechenden Adressbuchanbieters auf, um den Empfänger zu öffnen und einen Schnittstellenzeiger an den Transportanbieter zurückzukehren. 
    
3. Rufen Sie die [IMAPIProp::GetProps-Methode](imapiprop-getprops.md) des Empfängers auf, um die **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) abzurufen. Wenn **PR_SEND_RICH_INFO** true festgelegt ist, kann der Empfänger formatierten Text verarbeiten. 
    
Wenn Sie mehrere Objekte von anderen Anbietern geöffnet haben, müssen Sie möglicherweise herausfinden, ob zwei Eintragsbezeichner auf dasselbe Objekt verweisen. Beispielsweise verfügen Sie möglicherweise über einen kurzfristigen Eintragsbezeichner und einen langfristigen Eintragsbezeichner, und diese Bezeichner können dasselbe Objekt identifizieren oder nicht. Um eine redundante Verarbeitung zu vermeiden, rufen Sie die [IMAPISupport::CompareEntryIDs-Methode](imapisupport-compareentryids.md) auf, um diese Eintragsbezeichner zu vergleichen. Sie müssen diese Methode für den Eintragsbezeichnervergleich verwenden, da Eintragsbezeichner nicht direkt verglichen werden können. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

