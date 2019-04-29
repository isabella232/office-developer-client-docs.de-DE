---
title: Unterstützen des Objektzugriffs und-Vergleichs
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
# <a name="supporting-object-access-and-comparison"></a>Unterstützen des Objektzugriffs und-Vergleichs

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter können die [IMAPISupport:: OpenEntry](imapisupport-openentry.md) -und [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) -Methoden verwenden, um Objekte zu öffnen und zu vergleichen, die zu Ihrem Anbieter oder anderen Anbietern gehören: 
  
Wie [IMAPISession:: OpenEntry](imapisession-openentry.md) für Clients können Anbieter die OpenEntry-Methode Ihres **** Support-Objekts verwenden, um auf ein Objekt zuzugreifen, solange Sie die Eintrags-ID des Objekts kennen. Im Gegensatz zur Session-Methode erfordert die Support-Methode, dass Sie eine gültige Eintrags-ID im _lpEntryID_ -Parameter angeben. Er darf nicht NULL sein. 
  
Um zu veranschaulichen, wie ein Transportanbieter **IMAPISupport:: OpenEntry**verwenden kann, betrachten Sie das folgende Szenario. Der Transportanbieter hat eine Nachricht im Rich-Text-Format erhalten und weiß nicht, ob der Zielempfänger dieses Format verarbeiten kann. Vor der Übermittlung der Nachricht muss der Transportanbieter folgende Schritte ausführen:
  
1. Rufen Sie die [IMessage::](imessage-getrecipienttable.md) getrecipientable-Methode der Nachricht auf, um auf die Empfängertabelle und die Eintrags-ID des Empfängers, seine **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft zuzugreifen.
    
2. Führen Sie die Eintrags-ID an **IMAPISupport:: OpenEntry** , um den Empfänger zu öffnen, in der Regel entweder ein Messaging-Benutzer oder eine Verteilerliste. Der _lpInterface_ -Parameter sollte auf NULL festgelegt werden, da der Anbieter den Objekttyp des Empfängers nicht vorzeitig kennen kann. Die openEntry- **** Methode des Support-Objekts ruft [IMAPISession:: OpenEntry](imapisession-openentry.md) auf, um den für den Empfänger Verantwortlichen Adressbuchanbieter zu bestimmen. Das Session-Objekt ruft dann die entsprechende openEntry- **** Methode des Adressbuch Anbieters auf, um den Empfänger zu öffnen und einen Schnittstellenzeiger an den Transportanbieter zurückzugeben. 
    
3. Rufen Sie die [IMAPIProp::](imapiprop-getprops.md) GetProps-Methode des Empfängers auf, um die zugehörige **PR_SEND_RICH_INFO** ([pidtagsendrichinfo (](pidtagsendrichinfo-canonical-property.md))-Eigenschaft abzurufen. Wenn **PR_SEND_RICH_INFO** auf true festgelegt ist, kann der Empfänger formatierten Text verarbeiten. 
    
Wenn Sie mehrere Objekte von anderen Anbietern geöffnet haben, müssen Sie möglicherweise herausfinden, ob zwei Eintragsbezeichner auf dasselbe Objekt verweisen. Sie können beispielsweise eine kurzfristige Eintrags-ID und eine langfristige Eintrags-ID haben, und diese Bezeichner können das gleiche Objekt nicht identifizieren. Um eine redundante Verarbeitung zu vermeiden, rufen Sie die [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) -Methode auf, um diese Eintragsbezeichner zu vergleichen. Sie müssen diese Methode für den Vergleich der Eintragsbezeichner verwenden, da Eintragsbezeichner nicht direkt verglichen werden können. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

