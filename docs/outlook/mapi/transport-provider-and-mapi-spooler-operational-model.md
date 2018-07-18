---
title: Transportanbieter und MAPI-Spooler-Betriebsmodell
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b0f8d8f0-fed7-4a7c-bc40-e935f159591d
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 0e6c38091e5b2e10e82012bc470ea41037f57c7d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795761"
---
# <a name="transport-provider-and-mapi-spooler-operational-model"></a>Transportanbieter und MAPI-Spooler-Betriebsmodell

  
  
**Betrifft**: Outlook 
  
Transport-Anbieter Initialisierung, beim Starten, Verarbeitung, Herunterfahren und Deinitialization werden durch eine Reihe von Anrufe von der MAPI-Warteschlange an der Adressbuchhierarchie durchgeführt. Die Anrufe sind wie folgt berechnet:
  
1. Die MAPI-Warteschlange die [XPProviderInit](xpproviderinit.md) -Funktion, ein Support-Objekt übergibt, ruft der Provider-Objekt ab und überprüft, dass der Adressbuchhierarchie und MAPI-Warteschlange eine kompatible MAPI-Versionsnummern unterstützen. 
    
2. Die MAPI-Warteschlange Ruft die [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) -Methode von der [IXPProvider: IUnknown](ixpprovideriunknown.md) Schnittstelle. Zwischen den MAPI-Warteschlange und der Adressbuchhierarchie mit den Anmeldeinformationen im aktuellen Abschnitt des Profils wird eine Sitzung eingerichtet. Der Transportdienst zurückgegeben ein Anmeldung-Objekt. 
    
3. Die [IXPLogon::AddressTypes](ixplogon-addresstypes.md) -Methode aufgerufen, die MAPI-Warteschlange. Der Transportdienst gibt eine Liste der eindeutige Bezeichner (UIDs) und e-Mail-Adresstypen akzeptiert. 
    
4. Der Transportdienst die [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) -Methode aufgerufen, um eine Zeile in der Tabelle der MAPI-Status zu erstellen. 
    
5. Die MAPI-Warteschlange die [IXPLogon::TransportNotify](ixplogon-transportnotify.md) -Methode aufgerufen, um die Nachrichtenübermittlung und Empfang von Nachrichten zu aktivieren. 
    
6. Wenn von der Adressbuchhierarchie bei der Rückkehr für den Anruf **TransportLogon** angefordert, ruft die MAPI-Warteschlange in regelmäßigen Abständen die [IXPLogon::Idle](ixplogon-idle.md) -Methode. Verarbeitung im Leerlauf ist nützlich, wenn der Adressbuchhierarchie muss Fragen Sie das zugrunde liegenden messaging-System für neue Nachrichten oder andere Aufgaben niedrige Priorität. 
    
7. Die MAPI-Warteschlange und Adressbuchhierarchie Nachrichten senden und empfangen. Weitere Informationen finden Sie unter [Nachricht Übermittlung](message-submission-model.md) und [Nachricht Empfang-Modell](message-reception-model.md). Die MAPI-Warteschlange verarbeitet Transport Anfragen und ruft Support, Nachricht und Attachment-Objekte.
    
8. Die MAPI-Warteschlange die **TransportNotify** -Methode aufgerufen, um die Nachrichtenübermittlung und Empfang von Nachrichten zu deaktivieren. 
    
9. Die MAPI-Warteschlange-Freigaben für die Anmeldung und Anbieter-Objekte. Weitere Informationen finden Sie unter der [IXPProvider::Shutdown](ixpprovider-shutdown.md) -Methode. 
    

