---
title: Optionale Funktionen für Adressbuchanbieter
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
# <a name="optional-features-for-address-book-providers"></a>Optionale Funktionen für Adressbuchanbieter

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt viele optionale Features für Adressbuchanbieter. Zu den häufiger implementierten Features gehören:
  
- Agieren als ausländischer Anbieter, indem Einträge aus einem ihrer Container dem Container eines anderen Anbieters hinzugefügt werden können.
    
- Fungieren als Hostanbieter durch Hinzufügen von Einträgen von einem anderen Anbieter zu einem ihrer Container.
    
- Erweiterte Suche.
    
- Präfix Bildlauf durch Inhaltstabellen.
    
- Unterstützung für Verteilerlisten.
    
- Unterstützung für Ereignisbenachrichtigung.
    
In der folgenden Tabelle werden diese optionalen Features und ihre Implementierung kurz beschrieben:
  
|**Funktion**|**VorGehensWeise**|
|:-----|:-----|
|Bereitstellen von Vorlagen zum Erstellen von Einträgen für Nachrichtenempfänger Listen  <br/> |Implementieren Sie die [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) -Methode. Weitere Informationen finden Sie unter [einmalige Tabellen](one-off-tables.md) und Implementieren von [einmaligen Tabellen](implementing-one-off-tables.md).  <br/> |
|Gruppieren von Empfängern in einer benannten Einheit  <br/> |Unterstützen Sie die Eigenschaften von Verteilerlisten, indem Sie die [IDistList: IMAPIContainer](idistlistimapicontainer.md) -Schnittstelle implementieren.  <br/> |
|Fungieren als fremder Adressbuchanbieter, indem Einträge in einem anderen Anbieter zu einem Container hinzugefügt werden können  <br/> | Unterstützung des Bindens von Code an Daten im Hostanbieter durch:  <br/>  Unterstützen der **PR_TEMPLATEID** ([pidtagtemplateid (](pidtagtemplateid-canonical-property.md))-Eigenschaft für Messagingbenutzer und Verteilerlisten. Weitere Informationen finden Sie unter [Address Book Identifiers](address-book-identifiers.md).  <br/>  Implementieren der [IABLogon::](iablogon-opentemplateid.md) opentemplatecollection-Methode. Weitere Informationen finden Sie unter [fungieren als ein fremder Adressbuchanbieter](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Fungieren als Host-Adressbuchanbieter durch Einfügen von Einträgen von einem anderen Anbieter  <br/> |Unterstützen der Bindung von Daten an Code von einem fremden Anbieter durch Aufrufen der [IMAPISupport::](imapisupport-opentemplateid.md) opentemplatecollection-Methode. Weitere Informationen finden Sie unter [fungieren als Host-Adressbuchanbieter](acting-as-a-host-address-book-provider.md).  <br/> |
|Präfix Bildlauf  <br/> |Unterstützung von Einschränkungen für Containerinhalts Tabellen. Weitere Informationen finden Sie unter [Informationen zu Einschränkungen](about-restrictions.md).  <br/> |
|Erweiterte Suche in einem Container  <br/> |Unterstützung der **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md))-Eigenschaft für Container. Weitere Informationen finden Sie unter [Implementieren der erweiterten Suche](implementing-advanced-searching.md).  <br/> |
|Ereignisbenachrichtigung  <br/> |Implementieren Sie die Methoden [IABLogon:: Advise](iablogon-advise.md) und [IABLogon:: Unadvise](iablogon-unadvise.md) . Weitere Informationen finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md) und [unterstützende Ereignisbenachrichtigung](supporting-event-notification.md).  <br/> |
   
Bei Ereignisbenachrichtigungen wird Ihre **IABLogon:: Advise** -Methode von MAPI aufgerufen, wenn ein Client **IAddrBook:: Advise** anruft, um sich für Benachrichtigungen in einem ihrer Container, Messagingbenutzer oder Verteilerlisten zu registrieren. Da jedoch eine unterstützende Ereignisbenachrichtigung optional ist, können Sie MAPI_E_NO_SUPPORT von diesen Methoden zurückgeben. MAPI empfiehlt jedoch, dass Sie zumindest Benachrichtigungen für Ihre Inhaltstabellen unterstützen und Sie dazu ermuntern, alle Arten von Objekt Benachrichtigungen zu unterstützen, mit Ausnahme von _fnevSearchComplete_ und dem _fnevCriticalError_ -Ereignis, um einen Wert hinzuzufügen. 
  

