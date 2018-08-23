---
title: MAPI-Dienstanbieterobjekten
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 85a67216822360bcaf9544389f79980891951757
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584856"
---
# <a name="mapi-service-provider-objects"></a>MAPI-Dienstanbieterobjekten

  
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter implementieren viele Objekte. Einige werden hauptsächlich von MAPI verwendet, und einige von Clientanwendungen verwendet werden. Einige Objekte werden alle Typen der Dienstanbieter implementiert. die restlichen zu einem einzigen Anbieter spezifisch sind. Die folgende Tabelle beschreibt alle Service Provider-Objekte.
  
|**Dienstanbieterobjekts**|**Beschreibung**|
|:-----|:-----|
|Adressbuchcontainer  <br/> |Enthält die Empfängerinformationen für eine Adressbuchanbieter in das aktive Profil. von adressbuchanbietern implementierte können eine oder mehrere Address Book Container verfügen.  <br/> |
|Anlage  <br/> |Enthält zusätzliche Daten enthält, wie eine Datei oder das OLE-Objekt mit einer Meldung zugeordnet werden soll.  <br/> |
|Steuerelement  <br/> |Aktiviert oder deaktiviert eine Schaltfläche und initiiert verarbeiten, wenn auf die Schaltfläche geklickt wird.  <br/> |
|Verteilerliste  <br/> |Beschreibt eine Gruppierung von einzelnen Empfängern.  <br/> |
|Ordner  <br/> |Nachrichten und andere Container Nachricht enthält.  <br/> |
|Logon  <br/> |Handles service Provider-Ereignis Benachrichtigung und Client-Anforderungen.  <br/> |
|Messaging-Benutzer  <br/> |Beschreibt einen einzelnen Empfänger einer Nachricht.  <br/> |
|Nachricht  <br/> |Enthält Informationen, die an einen oder mehrere Empfänger gesendet werden kann.  <br/> |
|Nachrichtenspeicher  <br/> |Fungiert als hierarchisch organisiert Datenbank von Nachrichten.  <br/> |
|Provider  <br/> |Handles service Provider beim Starten und beenden.  <br/> |
|Warteschlange hook  <br/> |Führt eine besondere Verarbeitung für eingehende und ausgehende Nachrichten.  <br/> |
|Status  <br/> |Bietet Zugriff auf den Dienstanbieter Zustand.  <br/> |
|Tabelle  <br/> |Bietet Zugriff auf eine Zusammenfassungsansicht der Objektdaten Zeile und Spalte, ähnlich wie in in einer Datenbanktabelle.  <br/> |
   
Alle Dienstanbieter Implementieren einer Anbieter-Objekts und eines Objekts Anmeldung. Provider-Objekte sind ausschließlich für Buchhaltung; Sie werden von MAPI verwendet, die beim Starten und beenden Prozesse steuern. Logon-Objekten service indirekt einige Clientanforderungen. Beispielsweise die Nachricht Speichern des Anbieters Anmeldung Objekt Handles benachrichtigungsregistrierung und Anforderungen an die Nachricht Store-Objekte zu öffnen. 
  
Anbieter und Anmeldung implementiert eine andere Schnittstelle Abhängigkeit vom Dienstanbieter, die die Implementierung bereitstellt. Ein Nachricht Speicher-Anbieter implementiert die [IMSProvider: IUnknown](imsprovideriunknown.md) und [IMSLogon: IUnknown](imslogoniunknown.md) Schnittstellen in seinem Anbieter und Logon-Objekten, die eine Adresse Buch Anbieter implementiert die [IABProvider: IUnknown](iabprovideriunknown.md) und [IABLogon: IUnknown](iablogoniunknown.md) Schnittstellen und eines Transportdienstes implementiert die [IXPProvider: IUnknown](ixpprovideriunknown.md) und [IXPLogon: IUnknown](ixplogoniunknown.md) Schnittstellen. 
  
Nachricht Hook Anbieter implementieren Warteschlange Hook Objekte oder Objekte, die eingehende und ausgehende Nachrichten zu filtern.
  
Dienstanbieter verwenden in der Regel nur wenige Objekte. Am häufigsten verwenden sie eine Support-Objekt, das MAPI bereitstellt, mit denen Clientanforderungen implementieren. Das Support-Objekt wird für den Typ des Anbieters angepasst, die verwendet wird. Für alle-Dienstanbieter enthält das Support-Objekt Methoden zum Behandeln von ereignisbenachrichtigung, Konfigurationseigenschaften, Objekte öffnen und Fehlerbehandlung anzeigen. Die übrigen Methoden sind speziell für die Verwendung. angepasste Versionen für das Adressbuch Nachrichtenspeicher und Transportanbieter und für die Konfiguration sind vorhanden. Das Adresse Adressbuch Support-Objekt zeigt beispielsweise Details und benutzerdefinierte Empfänger Dialogfelder. Der Nachrichtenspeicher-Objekt unterstützt Kopie unterstützen und verschieben Sie Vorgänge für Ordner und Nachrichten. Der Anbieter Support Transportobjekt enthält Methoden für die Erleichterung der Interaktion mit der MAPI-Warteschlange. 
  
Einige Dienstanbieter verwenden Tabelle Daten und -Eigenschaft Datenobjekte – Dienstprogramm von MAPI implementierte Objekte. Tabelle Datenobjekte aktivieren-Dienstanbieter die zugrunde liegenden Daten einer Tabelle zu verwalten. Datenobjekte für die Eigenschaft aktivieren-Dienstanbieter-Objekt und -Eigenschaft festlegen. 
  
Transportanbieter, die die Transport Neutral Encapsulation Format (TNEF) unterstützen, für die Übertragung von Eigenschaften verwenden ein TNEF-Objekt, das MAPI zur Unterstützung implementierte der [ITnef: IUnknown](itnefiunknown.md) Schnittstelle. Weitere Informationen finden Sie unter [Developing eines Transportdienstes TNEF-Enabled](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Siehe auch



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Entwickeln eines TNEF-fähigen Transportanbieters](developing-a-tnef-enabled-transport-provider.md)

