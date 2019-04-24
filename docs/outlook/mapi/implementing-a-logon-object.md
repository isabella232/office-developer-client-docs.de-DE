---
title: Implementieren eines Anmelde Objekts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332844"
---
# <a name="implementing-a-logon-object"></a>Implementieren eines Anmelde Objekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jedes Adressbuch, jeder Nachrichtenspeicher und jeder Transportanbieter instanziiert ein LOGON-Objekt als Teil seiner Implementierung von [IABProvider:: LOGON](iabprovider-logon.md), [IMSProvider:: LOGON](imsprovider-logon.md)oder [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md). Anmeldeobjekte implementieren Methoden, die MAPI-Dienst Clientanforderungen unterstützen. Je nach Typ des Dienstanbieters unterstützt Ihr Logon-Objekt eine der folgenden Schnittstellen. 
  
|**Benutzeroberfläche des Anmelde Objekts**|**Dienstanbieter**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Adressbuchanbieter  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Nachrichtenspeicher Anbieter  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Transport Anbieter  <br/> |
   
Adressbuch-und Nachrichtenspeicher Anbieter implementieren die folgenden Features in ihren anmeldeobjekten:
  
- Unterstützung für Ereignisbenachrichtigungen (Methoden "**Advise** " und "Unadvise"). **** Eine Übersicht über die Ereignisbenachrichtigung finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Weitere Informationen zur Unterstützung von Benachrichtigungen in Ihrem LOGON-Objekt finden Sie unter [UnterstützenDe Ereignisbenachrichtigung](supporting-event-notification.md). 
    
- Vergleich der Eintragsbezeichner (**CompareEntryIDs** -Methode). Allgemeine Informationen zu Eintrags Bezeichnern finden Sie unter [MAPI Entry Identifiers](mapi-entry-identifiers.md). Weitere Informationen zum Vergleichen von Eintrags-IDs in der **CompareEntryIDs** -Methode Ihres LOGON-Objekts finden Sie unter [Unterstützung des objektZugriffs und-Vergleichs](supporting-object-access-and-comparison.md).
    
- Zugriff auf zusätzliche Fehlerinformationen (**getlasterroraufzurufen** -Methode). Weitere Informationen zum Behandeln von Fehlern in MAPI finden Sie unter [Error Handling in MAPI](error-handling-in-mapi.md). 
    
- Zugriff auf Objekte, die vom Dienstanbieter implementiert**** werden (OpenEntry-Methode). Weitere Informationen finden Sie unter [unterstützen des Objektzugriffs und-Vergleichs](supporting-object-access-and-comparison.md).
    
- Zugriff auf ein Statusobjekt (**OpenStatusEntry** -Methode). Allgemeine Informationen zu Statusobjekten finden Sie unter [MAPI-Statusobjekte](mapi-status-objects.md). Spezifische Informationen zum Implementieren eines Status-Objekts finden Sie unter [Status Object Implementation](status-object-implementation.md).
    
- Ein ABMELDEPROZESS**** (Abmelde Methode). Weitere Informationen finden Sie unter [Herunterfahren eines Dienstanbieters](shutting-down-a-service-provider.md).
    
Wenn es sich bei Ihrem Anbieter um einen Adressbuchanbieter handelt, implementieren Sie auch die folgenden Methoden und zugehörigen Features:
  
- [IABLogon:: GetOneOffTable](iablogon-getoneofftable.md) , um eine Liste der Vorlagen bereitzustellen, die Sie für das Erstellen neuer Empfänger unterstützen. Weitere Informationen finden Sie unter [einmalige Tabellen](one-off-tables.md) oder [Implementieren einer Anbieter-einmaligen Tabelle](implementing-a-provider-one-off-table.md).
    
- [IABLogon::](iablogon-opentemplateid.md) opentemplatecode, um den Zugriff auf die Implementierung eines Empfängers bereitzustellen, dessen Daten in einem Host Adressbuchanbieter gespeichert sind. Weitere Informationen finden Sie unter [fungieren als ein fremder Adressbuchanbieter](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P reparerecips](iablogon-preparerecips.md) , um sicherzustellen, dass die entsprechenden Eigenschaften für alle Empfänger in einer Empfängerliste zur Verfügung stehen. Weitere Informationen finden Sie unter [IABLogon::P reparerecips](iablogon-preparerecips.md). 
    
Das Anmeldeobjekt eines Transportanbieters, das [IXPLogon: IUnknown](ixplogoniunknown.md)implementiert, unterscheidet sich ganz von den von den anderen Typen von Dienstanbietern implementierten anmeldeobjekten. Mit den anderen LOGON-Objekten haben Sie nur zwei Features: Zugriff auf ein Status-Objekt über die [IXPLogon:: OpenStatusEntry](ixplogon-openstatusentry.md) -Methode und einen Abmeldevorgang über die [IXPLogon:: TransportLogoff](ixplogon-transportlogoff.md) -Methode. Transport Anbieter implementieren die folgenden eindeutigen Features in ihren anmeldeobjekten: 
  
- Registrierung für Adresstypen ([IXPLogon:: AddressTypes](ixplogon-addresstypes.md) -Methode). Weitere Informationen zum Registrieren eines Adresstyps finden Sie unter [Transport Anbieter und MAPI-Spooler-Betriebsmodell](transport-provider-and-mapi-spooler-operational-model.md).
    
- Steuerung der Nachrichtenübermittlung ([IXPLogon:: StartMessage](ixplogon-startmessage.md), [IXPLogon:: EndMessage](ixplogon-endmessage.md)und [IXPLogon:: SubmitMessage](ixplogon-submitmessage.md) -Methoden). Weitere Informationen finden Sie unter [Nachrichtenempfangs Modell](message-reception-model.md), [Interaktion mit dem MAPI](interacting-with-the-mapi-spooler.md)-Spooler und [Nachrichten Übermittlungs Modell](message-submission-model.md).
    
- Interne Statusüberprüfung ([IXPLogon:: ValidateState](ixplogon-validatestate.md) -Methode). 
    
- Möglichkeit zum Herunterladen oder Hochladen von Nachrichten bei Bedarf ([IXPLogon:: FlushQueues](ixplogon-flushqueues.md) -Methode). Weitere Informationen finden Sie unter [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md).
    
- Möglichkeit zum Abfragen ausstehender Nachrichten ([IXPLogon::P oll](ixplogon-poll.md) -Methode). Weitere Informationen finden Sie unter [Message reception Model](message-reception-model.md).
    
- Leerlaufstatus Erkennung ([IXPLogon:: idle](ixplogon-idle.md) -Methode). 
    
- Interaktion mit dem MAPI-Spooler ([IXPLogon:: TransportNotify](ixplogon-transportnotify.md) -Methode). 
    
## <a name="see-also"></a>Siehe auch



[Implementieren der Dienstanbieter Anmeldung](implementing-service-provider-logon.md)

