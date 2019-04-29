---
title: MAPI-Dienstanbieter Objekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 0976e986a33d8b96366a84527f227bd05ef7845e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432268"
---
# <a name="mapi-service-provider-objects"></a>MAPI-Dienstanbieter Objekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter implementieren viele Objekte. Einige werden hauptsächlich von MAPI verwendet, andere werden von Clientanwendungen verwendet. Einige Objekte werden von allen Arten von Dienstanbietern implementiert; die übrigen sind für einen einzelnen Anbietertyp spezifisch. In der folgenden Tabelle werden alle Dienstanbieter Objekte beschrieben.
  
|**Dienstanbieterobjekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuchcontainer  <br/> |Enthält Empfängerinformationen für einen Adressbuchanbieter im aktiven Profil; Adressbuchanbieter können über einen oder mehrere Adressbuchcontainer verfügen.  <br/> |
|Attachment  <br/> |Enthält zusätzliche Daten wie eine Datei oder ein OLE-Objekt, die einer Nachricht zugeordnet werden sollen.  <br/> |
|Control  <br/> |Aktiviert oder deaktiviert eine Schaltfläche und initiiert die Verarbeitung, wenn auf die Schaltfläche geklickt wird.  <br/> |
|Verteilerliste  <br/> |Beschreibt eine Gruppierung einzelner Nachrichtenempfänger.  <br/> |
|Ordner  <br/> |Enthält Nachrichten und andere Nachrichtencontainer.  <br/> |
|Anmeldung  <br/> |Behandelt Dienstanbieter-Ereignisbenachrichtigung und Clientanforderungen.  <br/> |
|Messaging Benutzer  <br/> |Beschreibt einen einzelnen Empfänger einer Nachricht.  <br/> |
|Nachricht  <br/> |Enthält Informationen, die an einen oder mehrere Empfänger gesendet werden können.  <br/> |
|Nachrichtenspeicher  <br/> |Fungiert als hierarchisch organisierte Datenbank mit Nachrichten.  <br/> |
|Anbieter  <br/> |Behandelt das Starten und Herunterfahren des Dienstanbieters.  <br/> |
|Spooler-Hook  <br/> |Führt eine spezielle Verarbeitung für eingehende und ausgehende Nachrichten aus.  <br/> |
|Status  <br/> |Ermöglicht den Zugriff auf den Status des Dienstanbieters.  <br/> |
|Tabelle  <br/> |Ermöglicht den Zugriff auf eine Zusammenfassungsansicht von Objektdaten im Zeilen-und Spaltenformat, ähnlich wie bei einer Datenbanktabelle.  <br/> |
   
Alle Dienstanbieter implementieren ein Provider-Objekt und ein LOGON-Objekt. Anbieterobjekte sind ausschließlich für die Buchhaltung; Sie werden von MAPI verwendet, um die Prozesse zum Starten und Herunterfahren zu steuern. Anmeldeobjekte Dienst einige Clientanforderungen indirekt. Beispielsweise verarbeitet das Anmeldeobjekt des Nachrichtenspeicher Anbieters die Benachrichtigungs Registrierung und die Anforderungen zum Öffnen von Nachrichtenspeicher Objekten. 
  
Anbieter-und Anmeldeobjekte implementieren eine andere Schnittstelle, je nach Typ des Dienstanbieters, der die Implementierung bereitstellt. Ein Nachrichtenspeicher Anbieter implementiert die [IMSProvider: IUnknown](imsprovideriunknown.md) -und [IMSLogon: IUnknown](imslogoniunknown.md) -Schnittstellen in seinem Provider-und LOGON-Objekt, ein Adressbuchanbieter implementiert die [IABProvider: IUnknown](iabprovideriunknown.md) und [IABLogon: IUnknown](iablogoniunknown.md) Schnittstellen, und ein Transportanbieter implementiert die Schnittstellen [IXPProvider: IUnknown](ixpprovideriunknown.md) und [IXPLogon: IUnknown](ixplogoniunknown.md) . 
  
Nachrichten Hook-Anbieter implementieren Spooler-Hook-Objekte oder Objekte, die eingehende und ausgehende Nachrichten filtern.
  
Dienstanbieter verwenden in der Regel nur wenige Objekte. Am häufigsten verwenden Sie ein Unterstützungsobjekt, das MAPI zur Implementierung von Clientanforderungen bereitstellt. Das Support-Objekt ist für den Anbietertyp angepasst, der es verwendet. Für alle Dienstanbieter beinhaltet das Support-Objektmethoden für die Behandlung von Ereignisbenachrichtigungen, die Anzeige von Konfigurationseigenschaften, öffnenden Objekten und die Fehlerbehandlung. Die restlichen Methoden sind spezifisch für die Verwendung; Es gibt angepasste Versionen für Adressbuch, Nachrichtenspeicher und Transportanbieter sowie für Konfigurationsunterstützung. Beispielsweise zeigt das Adressbuch-Support-Objektdetails und benutzerdefinierte Empfänger Dialogfelder an. Das Nachrichtenspeicher-Support Objekt unterstützt Kopier-und Verschiebungsvorgänge für Ordner und Nachrichten. Das Transportanbieter-Unterstützungsobjekt enthält Methoden zum erleichtern der Interaktion mit dem MAPI-Spooler. 
  
Einige Dienstanbieter verwenden Tabellendaten und Eigenschaftendaten Objekte, die von MAPI implementiert werden. Mit Tabellendaten Objekten können Dienstanbieter die zugrunde liegenden Daten einer Tabelle verwalten. Mit Eigenschaftendaten Objekten können Dienstanbieterobjekt-und Eigenschaftenzugriff festlegen. 
  
Transportanbieter, die das Transport Neutral Encapsulation Format (TNEF) für die Übertragung von Eigenschaften unterstützen, verwenden ein TNEF-Objekt, das von MAPI zur Unterstützung der [ITnef: IUnknown](itnefiunknown.md) -Schnittstelle implementiert wird. Weitere Informationen finden Sie unter [Entwickeln eines TNEF-fähigEn Transport Anbieters](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Siehe auch



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Entwickeln eines TNEF-fähigen Transport Anbieters](developing-a-tnef-enabled-transport-provider.md)

