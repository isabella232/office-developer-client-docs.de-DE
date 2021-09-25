---
title: Implementieren eines Anmeldeobjekts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 4fbc8dbbb3ed82ec4b5f519b96a25ac674df1119
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59584304"
---
# <a name="implementing-a-logon-object"></a>Implementieren eines Anmeldeobjekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jedes Adressbuch, jeder Nachrichtenspeicher und jeder Transportanbieter instanziiert ein Anmeldeobjekt im Rahmen der Implementierung von [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Anmeldeobjekte implementieren Methoden, die MAPI-Dienstclientanforderungen unterstützen. Je nach Typ des Dienstanbieters unterstützt das Anmeldeobjekt eine der folgenden Schnittstellen. 
  
|**Anmeldeobjektschnittstelle**|**Dienstleister**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Adressbuchanbieter  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Nachrichtenspeicheranbieter  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Transportanbieter  <br/> |
   
Adressbuch- und Nachrichtenspeicheranbieter implementieren die folgenden Features in ihren Anmeldeobjekten:
  
- Unterstützung für Ereignisbenachrichtigungen (**Methoden "Raten"** und **"Unadvise").** Eine Übersicht über die Ereignisbenachrichtigung finden Sie unter [Ereignisbenachrichtigung in MAPI.](event-notification-in-mapi.md) Weitere Informationen zur Unterstützung von Benachrichtigungen in Ihrem Anmeldeobjekt finden Sie unter ["Unterstützende Ereignisbenachrichtigung".](supporting-event-notification.md) 
    
- Eintragsbezeichnervergleich (**CompareEntryIDs-Methode).** Allgemeine Informationen zu Eintragsbezeichnern finden Sie unter [MAPI-Eintragsbezeichner.](mapi-entry-identifiers.md) Weitere Informationen zum Vergleichen von Eintragsbezeichnern in der **CompareEntryIDs-Methode** Ihres Anmeldeobjekts finden Sie unter [Unterstützen von Objektzugriff und Vergleich.](supporting-object-access-and-comparison.md)
    
- Zugriff auf zusätzliche Fehlerinformationen (**GetLastError-Methode).** Weitere Informationen zum Behandeln von Fehlern in mapi finden Sie unter [Fehlerbehandlung in MAPI](error-handling-in-mapi.md). 
    
- Zugriff auf Vom Dienstanbieter implementierte Objekte (**OpenEntry-Methode).** Weitere Informationen finden Sie unter [Unterstützen des Objektzugriffs und -vergleichs.](supporting-object-access-and-comparison.md)
    
- Zugriff auf ein Statusobjekt (**OpenStatusEntry-Methode).** Allgemeine Informationen zu Statusobjekten finden Sie unter [MAPI Status Objects](mapi-status-objects.md). Spezifische Informationen zum Implementieren eines Statusobjekts finden Sie unter [Status Object Implementation](status-object-implementation.md).
    
- Ein Abmeldevorgang (**Abmeldemethode).** Weitere Informationen finden Sie unter [Herunterfahren eines Dienstanbieters.](shutting-down-a-service-provider.md)
    
Wenn Ihr Anbieter ein Adressbuchanbieter ist, implementieren Sie auch die folgenden Methoden und zugehörigen Features:
  
- [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) zum Bereitstellen einer Liste der Vorlagen, die Sie für das Erstellen neuer Empfänger unterstützen. Weitere Informationen finden Sie unter ["Einmalige Tabellen"](one-off-tables.md) oder ["Implementieren eines Anbieters One-Off Tabelle".](implementing-a-provider-one-off-table.md)
    
- [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) ermöglicht den Zugriff auf die Implementierung eines Empfängers, dessen Daten sich in einem Hostadressbuchanbieter befinden. Weitere Informationen finden Sie unter ["Handeln als fremder Adressbuchanbieter".](acting-as-a-foreign-address-book-provider.md) 
    
- [IABLogon::P repareRecips,](iablogon-preparerecips.md) um sicherzustellen, dass die entsprechenden Eigenschaften für alle Empfänger in einer Empfängerliste verfügbar sind. Weitere Informationen finden Sie unter [IABLogon::P repareRecips](iablogon-preparerecips.md). 
    
Das Anmeldeobjekt eines Transportanbieters, das [IXPLogon : IUnknown](ixplogoniunknown.md)implementiert, unterscheidet sich erheblich von den Anmeldeobjekten, die von den anderen Typen von Dienstanbietern implementiert werden. Mit den anderen Anmeldeobjekten sind nur zwei Features gemeinsam: der Zugriff auf ein Statusobjekt über die [IXPLogon::OpenStatusEntry-Methode](ixplogon-openstatusentry.md) und ein Abmeldevorgang über die [IXPLogon::TransportLogoff-Methode.](ixplogon-transportlogoff.md) Transportanbieter implementieren die folgenden einzigartigen Features in ihren Anmeldeobjekten: 
  
- Registrierung für Adresstypen ([IXPLogon::AddressTypes-Methode).](ixplogon-addresstypes.md) Weitere Informationen zum Registrieren eines Adresstyps finden Sie unter [Transport provider and MAPI Spooler Operational Model.](transport-provider-and-mapi-spooler-operational-model.md)
    
- Steuerung der Nachrichtenübertragung ([IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)und [IXPLogon::SubmitMessage-Methoden).](ixplogon-submitmessage.md) Weitere Informationen finden Sie unter ["Nachrichtenempfangsmodell",](message-reception-model.md) ["Interaktion mit dem MAPI-Spooler"](interacting-with-the-mapi-spooler.md)und ["Nachrichtenübermittlungsmodell".](message-submission-model.md)
    
- Interne Zustandsüberprüfung ([IXPLogon::ValidateState-Methode).](ixplogon-validatestate.md) 
    
- Möglichkeit zum Herunterladen oder Hochladen von Nachrichten bei Bedarf ([IXPLogon::FlushQueues-Methode).](ixplogon-flushqueues.md) Weitere Informationen finden Sie unter [Implementieren der FlushQueues-Methode.](implementing-the-flushqueues-method.md)
    
- Möglichkeit zum Abfragen ausstehender Nachrichten ([IXPLogon::P oll-Methode).](ixplogon-poll.md) Weitere Informationen finden Sie unter [Nachrichtenempfangsmodell.](message-reception-model.md)
    
- Leerlaufstatuserkennung ([IXPLogon::Idle-Methode).](ixplogon-idle.md) 
    
- Interaktion mit dem MAPI-Spooler ([IXPLogon::TransportNotify-Methode).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>Siehe auch



[Implementieren der Dienstanbieteranmeldung](implementing-service-provider-logon.md)

