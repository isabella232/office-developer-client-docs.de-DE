---
title: Implementieren eine Anmeldung-Objekt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: e23c73931c9051b61d30b7ea7e9c54d06a4d9c33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792534"
---
# <a name="implementing-a-logon-object"></a>Implementieren eine Anmeldung-Objekt

  
  
**Betrifft**: Outlook 
  
Jedes Adressbuch, Nachrichtenspeicher und Transport-Provider instanziiert ein Anmeldeobjekt als Teil der Implementierung der [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Logon-Objekten Implementieren von Methoden, mit deren Hilfe MAPI-Client Serviceanfragen. Je nach Typ des Dienstanbieters wird Ihr Anmeldeobjekt eine der folgenden Schnittstellen unterstützen. 
  
|**Anmeldung-Objektschnittstelle**|**Dienstanbieter**|
|:-----|:-----|
|[IABLogon: IUnknown](iablogoniunknown.md) <br/> |-Adressbuchanbieter  <br/> |
|[IMSLogon: IUnknown](imslogoniunknown.md) <br/> |Nachricht Speicheranbieter  <br/> |
|[IXPLogon: IUnknown](ixplogoniunknown.md) <br/> |Transportdienst  <br/> |
   
Adressbuch und Meldung von nachrichtenspeicheranbietern implementierte die folgenden Features in ihrer Anmeldung Objekte:
  
- Unterstützung für ereignisbenachrichtigung (**Advise** und **Unadvise** -Methoden). Eine Übersicht über ereignisbenachrichtigung finden Sie unter [Event Notification in MAPI](event-notification-in-mapi.md). Weitere Informationen zur Unterstützung von Benachrichtigung in Ihrer Anmeldung-Objekt finden Sie unter [Ereignisbenachrichtigung unterstützen](supporting-event-notification.md). 
    
- Vergleich der Eintrag Bezeichner **(Eintragsbezeichner)** . Allgemeine Informationen zu Eintragsbezeichner finden Sie unter [MAPI-Eintragsbezeichner](mapi-entry-identifiers.md). Weitere Informationen zum Vergleichen von Eintragsbezeichner in **Ihrer Anmeldung-Objekt-Eintragsbezeichner** finden Sie unter [Vergleich und unterstützende Objektzugriff](supporting-object-access-and-comparison.md).
    
- Zugriff auf zusätzliche Fehlerinformationen (**GetLastError** -Methode). Weitere Informationen zur Behandlung von Fehlern in MAPI finden Sie unter [Fehlerbehandlung in MAPI](error-handling-in-mapi.md). 
    
- Zugriff auf Objekte, die vom Dienstanbieter (**OpenEntry** -Methode) implementiert. Weitere Informationen finden Sie unter [Vergleich und unterstützende Object Access](supporting-object-access-and-comparison.md).
    
- Zugriff auf ein Statusobjekt (**OpenStatusEntry** -Methode). Allgemeine Informationen zu Status-Objekten finden Sie unter [MAPI-Status-Objekten](mapi-status-objects.md). Bestimmte Informationen zum Implementieren der Statusobjekt finden Sie unter [Implementierung der Status-Objekts](status-object-implementation.md).
    
- Ein Prozess der Abmeldung (**Logoff (** Methode)). Weitere Informationen finden Sie unter [Herunterfahren nach unten a Service Provider](shutting-down-a-service-provider.md).
    
Wenn der Anbieter eine Adressbuchanbieter ist, implementieren Sie die auch die folgenden Methoden und die zugehörigen Features:
  
- [GetOneOffTable](iablogon-getoneofftable.md) , um eine Liste der Vorlagen bereitzustellen, die für das Erstellen von neuen Empfänger unterstützt. Weitere Informationen finden Sie unter [Einmaligen Tabellen](one-off-tables.md) oder [Implementieren einer einmaligen Anbieter-Tabelle](implementing-a-provider-one-off-table.md).
    
- [OpenTemplateID](iablogon-opentemplateid.md) für den Zugriff auf die Implementierung eines Empfängers, dessen Daten in einer Host-Adressbuchanbieter befindet. Weitere Informationen finden Sie unter [als einen fremden Adressbuchanbieter fungiert](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::PrepareRecips](iablogon-preparerecips.md) , um sicherzustellen, dass die entsprechenden Eigenschaften für alle Empfänger in einer Empfängerliste verfügbar sind. Weitere Informationen finden Sie unter [IABLogon::PrepareRecips](iablogon-preparerecips.md). 
    
Eines Transportdienstes Anmeldung-Objekt, das implementiert [IXPLogon: IUnknown](ixplogoniunknown.md), unterscheidet sich von der Logon-Objekten, die von anderen Typen der Dienstanbieter implementiert. Es wurde die Anmeldung Objekte nur zwei Features: Zugriff auf ein Statusobjekt über die [IXPLogon::OpenStatusEntry](ixplogon-openstatusentry.md) -Methode und eine Abmeldung über die [IXPLogon::TransportLogoff](ixplogon-transportlogoff.md) -Methode. Transportanbieter implementieren die folgenden eindeutigen Features in ihrer Anmeldung Objekte: 
  
- Registrierung für Adresstypen ([IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode). Weitere Informationen zum Registrieren eines Adresstyps finden Sie unter [Adressbuchhierarchie und MAPI-Warteschlange betriebliche Modell](transport-provider-and-mapi-spooler-operational-model.md).
    
- Steuerung der Nachrichtenübermittlung ([IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)und [IXPLogon::SubmitMessage](ixplogon-submitmessage.md) -Methoden). Weitere Informationen finden Sie unter [Nachricht Empfang Modell](message-reception-model.md) [interagieren mit der MAPI-Warteschlange](interacting-with-the-mapi-spooler.md)und [Nachricht Übermittlung Modell](message-submission-model.md).
    
- Überprüfung der internen Zustand ([IXPLogon::ValidateState](ixplogon-validatestate.md) -Methode). 
    
- Möglichkeit zum Herunterladen und Hochladen von Nachrichten bei Bedarf ([IXPLogon::FlushQueues](ixplogon-flushqueues.md) -Methode). Weitere Informationen finden Sie unter [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md).
    
- Die Möglichkeit, die Abfrage für ausstehende Nachrichten ([IXPLogon::Poll](ixplogon-poll.md) -Methode). Weitere Informationen finden Sie unter [Message Empfang Model](message-reception-model.md).
    
- Leerlauf Erkennung ([IXPLogon::Idle](ixplogon-idle.md) -Methode). 
    
- Interaktion mit der MAPI-Warteschlange ([IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode). 
    
## <a name="see-also"></a>Siehe auch



[Implementieren von Service Provider Anmeldung](implementing-service-provider-logon.md)

