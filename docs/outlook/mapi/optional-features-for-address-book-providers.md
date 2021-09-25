---
title: Optionale Features für Adressbuchanbieter
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 3c1e3e80cf7c3f3f2b7608b1c57079353ac7338e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567130"
---
# <a name="optional-features-for-address-book-providers"></a>Optionale Features für Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele optionale Features für Adressbuchanbieter. Einige der am häufigsten implementierten Features sind:
  
- Fungiert als fremder Anbieter, indem Einträge aus einem Ihrer Container dem Container eines anderen Anbieters hinzugefügt werden können.
    
- Fungiert als Hostanbieter, indem Einträge von einem anderen Anbieter zu einem Ihrer Container hinzugefügt werden.
    
- Erweiterte Suche.
    
- Präfix-Bildlauf durch Inhaltstabellen.
    
- Unterstützung für Verteilerlisten.
    
- Unterstützung für Ereignisbenachrichtigungen.
    
In der folgenden Tabelle werden diese optionalen Features und ihre Implementierung kurz beschrieben:
  
|**Feature**|**Implementierung**|
|:-----|:-----|
|Bereitstellen von Vorlagen zum Erstellen von Einträgen für Nachrichtenempfängerlisten  <br/> |Implementieren Sie die [IABLogon::GetOneOffTable-Methode.](iablogon-getoneofftable.md) Weitere Informationen finden Sie unter ["Einmalige Tabellen"](one-off-tables.md) und ["Implementieren von One-Off Tabellen".](implementing-one-off-tables.md)  <br/> |
|Gruppieren von Empfängern in einer benannten Einheit  <br/> |Unterstützen Sie die Eigenschaften von Verteilerlisten, indem Sie die [IDistList : IMAPIContainer-Schnittstelle](idistlistimapicontainer.md) implementieren.  <br/> |
|Als fremder Adressbuchanbieter fungieren, indem Einträge zu einem Container in einem anderen Anbieter hinzugefügt werden können  <br/> | Unterstützung von Bindungscode an Daten im Hostanbieter durch:  <br/>  Unterstützen der **eigenschaft PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)) für Messagingbenutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Adressbuchbezeichner.](address-book-identifiers.md)  <br/>  Implementieren der [IABLogon::OpenTemplateID-Methode.](iablogon-opentemplateid.md) Weitere Informationen finden Sie unter ["Handeln als fremder Adressbuchanbieter".](acting-as-a-foreign-address-book-provider.md)  <br/> |
|Fungieren als Hostadressbuchanbieter durch Einfügen von Einträgen von einem anderen Anbieter  <br/> |Unterstützung der Bindung von Daten an Code von einem fremden Anbieter durch Aufrufen der [IMAPISupport::OpenTemplateID-Methode.](imapisupport-opentemplateid.md) Weitere Informationen finden Sie unter ["Fungieren als Hostadressbuchanbieter".](acting-as-a-host-address-book-provider.md)  <br/> |
|Präfix-Bildlauf  <br/> |Unterstützen von Einschränkungen für Containerinhaltstabellen. Weitere Informationen finden Sie unter ["Einschränkungen".](about-restrictions.md)  <br/> |
|Erweiterte Suche in einem Container  <br/> |Unterstützen Sie die **Eigenschaft PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) für Container. Weitere Informationen finden Sie unter [Implementieren der erweiterten Suche.](implementing-advanced-searching.md)  <br/> |
|Ereignisbenachrichtigung  <br/> |Implementieren Sie die [IABLogon::Advise-](iablogon-advise.md) und [IABLogon::Unadvise-Methoden.](iablogon-unadvise.md) Weitere Informationen finden Sie unter ["Ereignisbenachrichtigung in MAPI"](event-notification-in-mapi.md) und ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md)  <br/> |
   
Für Ereignisbenachrichtigungen wird Ihre **IABLogon::Advise-Methode** von der MAPI aufgerufen, wenn ein Client **IAddrBook::Advise aufruft,** um sich für Benachrichtigungen in einem Ihrer Container, Messagingbenutzer oder Verteilerlisten zu registrieren. Da die Unterstützung von Ereignisbenachrichtigungen jedoch optional ist, können Sie MAPI_E_NO_SUPPORT von diesen Methoden zurückgeben. MapI empfiehlt jedoch, zumindest Benachrichtigungen in Inhaltsverzeichnissen zu unterstützen, und empfiehlt Ihnen, alle Arten von Objektbenachrichtigungen mit Ausnahme von  _fnevSearchComplete_ und dem  _fnevCriticalError-Ereignis_ zu unterstützen, um einen Wert hinzuzufügen. 
  

