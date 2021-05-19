---
title: Implementieren eines Anmeldeobjekts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 41e5c88c-d79d-4e9f-81f4-c4365cfaa15d
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f9d77313012c2d133dc9352707ebc5e0c69c9973
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433045"
---
# <a name="implementing-a-logon-object"></a>Implementieren eines Anmeldeobjekts

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Jedes Adressbuch, jeder Nachrichtenspeicher und jeder Transportanbieter instanziiert ein Anmeldeobjekt im Rahmen der Implementierung von [IABProvider::Logon](iabprovider-logon.md), [IMSProvider::Logon](imsprovider-logon.md)oder [IXPProvider::TransportLogon](ixpprovider-transportlogon.md). Anmeldeobjekte implementieren Methoden, die MAPI-Dienstclientanforderungen unterstützen. Je nach Typ des Dienstanbieters unterstützt Ihr Anmeldeobjekt eine der folgenden Schnittstellen. 
  
|**Benutzeroberfläche des Anmeldeobjekts**|**Dienstanbieter**|
|:-----|:-----|
|[IABLogon : IUnknown](iablogoniunknown.md) <br/> |Adressbuchanbieter  <br/> |
|[IMSLogon : IUnknown](imslogoniunknown.md) <br/> |Anbieter des Nachrichtenspeichers  <br/> |
|[IXPLogon : IUnknown](ixplogoniunknown.md) <br/> |Transportanbieter  <br/> |
   
Adressbuch- und Nachrichtenspeicheranbieter implementieren die folgenden Features in ihren Anmeldeobjekten:
  
- Unterstützung für Ereignisbenachrichtigungen (**Advise-** und **Unadvise-Methoden).** Eine Übersicht über die Ereignisbenachrichtigung finden Sie unter [Ereignisbenachrichtigung in MAPI](event-notification-in-mapi.md). Weitere Informationen zur Unterstützung von Benachrichtigungen in Ihrem Anmeldeobjekt finden Sie unter [Supporting Event Notification](supporting-event-notification.md). 
    
- Vergleich der Eintrags-ID (**CompareEntryIDs-Methode).** Allgemeine Informationen zu Eintragsbezeichnern finden Sie unter [MAPI Entry Identifiers](mapi-entry-identifiers.md). Weitere Informationen zum Vergleichen von Eintragsbezeichnern in der **CompareEntryIDs-Methode** des Anmeldeobjekts finden Sie unter [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Zugriff auf zusätzliche Fehlerinformationen (**GetLastError-Methode).** Weitere Informationen zum Behandeln von Fehlern in MAPI finden Sie unter [Error Handling in MAPI](error-handling-in-mapi.md). 
    
- Zugriff auf Objekte, die vom Dienstanbieter implementiert werden (**OpenEntry-Methode).** Weitere Informationen finden Sie unter [Supporting Object Access and Comparison](supporting-object-access-and-comparison.md).
    
- Zugriff auf ein Statusobjekt (**OpenStatusEntry-Methode).** Allgemeine Informationen zu Statusobjekten finden Sie unter [MAPI Status Objects](mapi-status-objects.md). Spezifische Informationen zum Implementieren eines Statusobjekts finden Sie unter [Status Object Implementation](status-object-implementation.md).
    
- Ein Abmeldevorgang (**Logoff-Methode).** Weitere Informationen finden Sie unter [Shutting Down a Service Provider](shutting-down-a-service-provider.md).
    
Wenn Ihr Anbieter ein Adressbuchanbieter ist, implementieren Sie auch die folgenden Methoden und zugehörigen Features:
  
- [IABLogon::GetOneOffTable,](iablogon-getoneofftable.md) um eine Auflistung der Vorlagen zur Verfügung zu stellen, die Sie beim Erstellen neuer Empfänger unterstützen. Weitere Informationen finden Sie unter [One-Off Tables](one-off-tables.md) oder [Implementing a Provider One-Off Table](implementing-a-provider-one-off-table.md).
    
- [IABLogon::OpenTemplateID,](iablogon-opentemplateid.md) um Zugriff auf die Implementierung eines Empfängers zu ermöglichen, dessen Daten sich in einem Host-Adressbuchanbieter befinden. Weitere Informationen finden Sie unter [Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md). 
    
- [IABLogon::P repareRecips,](iablogon-preparerecips.md) um sicherzustellen, dass die entsprechenden Eigenschaften für alle Empfänger in einer Empfängerliste verfügbar sind. Weitere Informationen finden Sie unter [IABLogon::P repareRecips](iablogon-preparerecips.md). 
    
Das Anmeldeobjekt eines Transportanbieters, das [IXPLogon : IUnknown](ixplogoniunknown.md)implementiert, ist ganz anders als die Anmeldeobjekte, die von den anderen Typen von Dienstanbietern implementiert werden. Sie verfügt nur über zwei Features, die mit den anderen Anmeldeobjekten gemeinsam sind: Zugriff auf ein Statusobjekt über die [IXPLogon::OpenStatusEntry-Methode](ixplogon-openstatusentry.md) und einen Abmeldevorgang über die [IXPLogon::TransportLogoff-Methode.](ixplogon-transportlogoff.md) Transportanbieter implementieren die folgenden eindeutigen Features in ihren Anmeldeobjekten: 
  
- Registrierung für Adresstypen ([IXPLogon::AddressTypes-Methode).](ixplogon-addresstypes.md) Weitere Informationen zum Registrieren eines Adresstyps finden Sie unter [Transport Provider und MAPI Spooler Operational Model](transport-provider-and-mapi-spooler-operational-model.md).
    
- Steuerung der Nachrichtenübertragung ([IXPLogon::StartMessage](ixplogon-startmessage.md), [IXPLogon::EndMessage](ixplogon-endmessage.md)und [IXPLogon::SubmitMessage-Methoden).](ixplogon-submitmessage.md) Weitere Informationen finden Sie unter [Message Reception Model](message-reception-model.md), [Interacting with the MAPI Spooler](interacting-with-the-mapi-spooler.md)und [Message Submission Model](message-submission-model.md).
    
- Interne Statusüberprüfung ([IXPLogon::ValidateState-Methode).](ixplogon-validatestate.md) 
    
- Möglichkeit zum Herunterladen oder Hochladen von Nachrichten bei Bedarf ([IXPLogon::FlushQueues-Methode).](ixplogon-flushqueues.md) Weitere Informationen finden Sie unter [Implementieren der FlushQueues-Methode](implementing-the-flushqueues-method.md).
    
- Möglichkeit zum Abfragen ausstehender Nachrichten ([IXPLogon::P oll-Methode).](ixplogon-poll.md) Weitere Informationen finden Sie unter [Message Reception Model](message-reception-model.md).
    
- Erkennung des Leerlaufzustands ([IXPLogon::Idle-Methode).](ixplogon-idle.md) 
    
- Interaktion mit dem MAPI-Spooler ([IXPLogon::TransportNotify-Methode).](ixplogon-transportnotify.md) 
    
## <a name="see-also"></a>Siehe auch



[Implementieren der Dienstanbieteranmeldung](implementing-service-provider-logon.md)

