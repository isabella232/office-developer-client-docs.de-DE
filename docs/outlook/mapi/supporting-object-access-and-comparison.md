---
title: Unterstützen des Objektzugriffs und Vergleichs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aac7c6c5-6896-4824-ba36-81bb292777a9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 2152cfbb91f2e343ebcee3f5b717a29805df1d25
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795692"
---
# <a name="supporting-object-access-and-comparison"></a>Unterstützen des Objektzugriffs und Vergleichs

  
  
**Betrifft**: Outlook 
  
Dienstanbieter können die Methoden [IMAPISupport::OpenEntry](imapisupport-openentry.md) und [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) öffnen und den Vergleich von Objekten, die an ihren Anbieter oder an andere Anbieter gehören: 
  
Wie [IMAPISession::OpenEntry](imapisession-openentry.md) für Clients Anbieter für ihre Support-Objekt **OpenEntry** -Methode können Sie ein beliebiges Objekt zuzugreifen, wie lange sie das Objekt Eintrags-ID kennen. Im Gegensatz zu der Sitzung-Methode erfordert die Support-Methode an, dass Sie eine gültige Eingabe-ID in der _LpEntryID_ -Parameter angeben. Es darf nicht NULL sein. 
  
Zur Veranschaulichung ein Transportdienstes **IMAPISupport::OpenEntry**Verwendung anhand des folgenden Szenarios. Der Transportdienst hat erhalten eine Nachricht im RTF-Format formatiert und weiß nicht, ob der Ziel-Empfänger dieses Format verarbeitet werden kann. Vor der Übermittlung einer Nachricht, muss der Adressbuchhierarchie folgende Aktionen ausführen:
  
1. Rufen Sie die Nachricht [IMessage::GetRecipientTable](imessage-getrecipienttable.md) -Methode, um die Empfänger Tabelle und Eintrags-ID des Empfängers, dessen **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))-Eigenschaft zugreifen.
    
2. Übergeben Sie der Eintrags-ID an **IMAPISupport::OpenEntry** zum Öffnen des Empfängers an, in der Regel entweder eine messaging Benutzer oder Verteilerliste aus. Der Parameter _LpInterface_ sollte auf NULL festgelegt werden, da der Anbieter vorausschauendes den Objekttyp des Empfängers nicht bekannt ist. Die des Unterstützungsobjekts **OpenEntry** Methode ruft [IMAPISession::OpenEntry](imapisession-openentry.md) um Adressbuchanbieter verantwortlich für den Empfänger zu bestimmen. Session-Objekt ruft dann die entsprechende-Adressbuchanbieter **OpenEntry** -Methode, um den Empfänger zu öffnen und einen Schnittstellenzeiger auf der Adressbuchhierarchie zurückgegeben werden. 
    
3. Rufen Sie den Empfänger [IMAPIProp::GetProps](imapiprop-getprops.md) -Methode zum Abrufen der Eigenschaft **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)). Wenn **PR_SEND_RICH_INFO** auf TRUE festgelegt ist, kann der Empfänger formatierten Text behandeln. 
    
Wenn Sie mehrere Objekte von anderen Anbietern geöffnet haben, müssen Sie hier erfahren Sie, ob zwei Eintragsbezeichner auf dasselbe Objekt verweisen. Angenommen, Sie möglicherweise eine kurzfristigen Eintrags-ID und langfristige Eintrags-ID Bezeichner und können nicht das gleiche Objekt identifiziert werden können. Redundante Verarbeitung zu vermeiden, rufen Sie die [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) -Methode, um diese Eintragsbezeichner verglichen werden soll. Sie müssen diese Methode für den Vergleich von Eintrags-ID verwenden, da Eintragsbezeichner direkt verglichen werden können. 
  
## <a name="see-also"></a>Siehe auch



[MAPI-Dienstanbieter](mapi-service-providers.md)

