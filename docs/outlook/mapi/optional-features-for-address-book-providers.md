---
title: Optionale Features für Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414571"
---
# <a name="optional-features-for-address-book-providers"></a>Optionale Features für Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele optionale Features für Adressbuchanbieter. Zu den am häufigsten implementierten Features gehören:
  
- Als fremder Anbieter agieren, indem Sie zulassen, dass Einträge aus einem Ihrer Container dem Container eines anderen Anbieters hinzugefügt werden.
    
- Als Hostanbieter agieren, indem Sie Einträge von einem anderen Anbieter zu einem Ihrer Container hinzufügen.
    
- Erweiterte Suche.
    
- Präfix beim Bildlauf durch Inhaltstabellen.
    
- Unterstützung für Verteilerlisten.
    
- Unterstützung für Ereignisbenachrichtigungen.
    
In der folgenden Tabelle werden diese optionalen Features und deren Implementierung kurz beschrieben:
  
|**Feature**|**Implementierung**|
|:-----|:-----|
|Bereitstellungsvorlagen zum Erstellen von Einträgen für Nachrichtenempfängerlisten  <br/> |Implementieren Sie [die IABLogon::GetOneOffTable-Methode.](iablogon-getoneofftable.md) Weitere Informationen finden Sie unter [One-Off Tables](one-off-tables.md) and [Implementing One-Off Tables](implementing-one-off-tables.md).  <br/> |
|Gruppieren von Empfängern in einer benannten Einheit  <br/> |Unterstützen Sie die Eigenschaften von Verteilerlisten, indem Sie die [IDistList : IMAPIContainer-Schnittstelle](idistlistimapicontainer.md) implementieren.  <br/> |
|Agieren als fremder Adressbuchanbieter, indem Sie zulassen, dass Einträge zu einem Container in einem anderen Anbieter hinzugefügt werden  <br/> | Unterstützung von Bindungscode an Daten im Hostanbieter durch:  <br/>  Unterstützung der **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) -Eigenschaft für Messagingbenutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Adressbuchbezeichner](address-book-identifiers.md).  <br/>  Implementieren der [IABLogon::OpenTemplateID-Methode.](iablogon-opentemplateid.md) Weitere Informationen finden Sie unter [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Agieren als Host-Adressbuchanbieter durch Einfügen von Einträgen von einem anderen Anbieter  <br/> |Unterstützung von Bindungsdaten an Code von einem fremden Anbieter durch Aufrufen der [IMAPISupport::OpenTemplateID-Methode.](imapisupport-opentemplateid.md) Weitere Informationen finden Sie unter [Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).  <br/> |
|Präfix-Bildlauf  <br/> |Supporteinschränkungen für Containerinhaltstabellen. Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).  <br/> |
|Erweiterte Suche in einem Container  <br/> |Unterstützt die **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) -Eigenschaft für Container. Weitere Informationen finden Sie unter [Implementing Advanced Searching](implementing-advanced-searching.md).  <br/> |
|Ereignisbenachrichtigung  <br/> |Implementieren Sie [die Methoden IABLogon::Advise](iablogon-advise.md) und [IABLogon::Unadvise.](iablogon-unadvise.md) Weitere Informationen finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [Unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).  <br/> |
   
Für Ereignisbenachrichtigungen wird Ihre **IABLogon::Advise-Methode** von MAPI aufgerufen, wenn ein Client **IAddrBook::Advise** aufruft, um sich für Benachrichtigungen in einem Ihrer Container, Messagingbenutzer oder Verteilerlisten zu registrieren. Da die Unterstützung der Ereignisbenachrichtigung jedoch optional ist, können Sie MAPI_E_NO_SUPPORT methoden zurückgeben. MapI empfiehlt jedoch, dass Sie mindestens Benachrichtigungen in Ihren Inhaltstabellen unterstützen und ermutigt Sie, alle Arten von Objektbenachrichtigungen zu unterstützen, mit Ausnahme von  _fnevSearchComplete_ und dem  _fnevCriticalError-Ereignis,_ um einen Mehrwert hinzuzufügen. 
  

