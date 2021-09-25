---
title: MAPI-Dienstanbieterobjekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: f8ade454-2450-49e6-a76f-93801055a7e5
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: ef29ad25d08358f8791734e76d770f07e9eef9dd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59610153"
---
# <a name="mapi-service-provider-objects"></a>MAPI-Dienstanbieterobjekte

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter implementieren viele Objekte. Einige werden hauptsächlich von der MAPI und einige von Clientanwendungen verwendet. Einige Objekte werden von allen Arten von Dienstanbietern implementiert. Der Rest ist für einen einzelnen Anbietertyp spezifisch. In der folgenden Tabelle werden alle Dienstanbieterobjekte beschrieben.
  
|**Dienstanbieterobjekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuchcontainer  <br/> |Enthält Empfängerinformationen für einen Adressbuchanbieter im aktiven Profil; Adressbuchanbieter können über ein oder mehrere Adressbuchcontainer verfügen.  <br/> |
|Attachment  <br/> |Enthält zusätzliche Daten, z. B. eine Datei oder ein OLE-Objekt, die einer Nachricht zugeordnet werden sollen.  <br/> |
|Steuerelement  <br/> |Aktiviert oder deaktiviert eine Schaltfläche und initiiert die Verarbeitung, wenn auf die Schaltfläche geklickt wird.  <br/> |
|Verteilerliste  <br/> |Beschreibt eine Gruppierung einzelner Nachrichtenempfänger.  <br/> |
|Ordner  <br/> |Enthält Nachrichten und andere Nachrichtencontainer.  <br/> |
|Anmeldung  <br/> |Behandelt Ereignisbenachrichtigungen von Dienstanbietern und Clientanforderungen.  <br/> |
|Messaging-Benutzer  <br/> |Beschreibt einen einzelnen Empfänger einer Nachricht.  <br/> |
|Nachricht  <br/> |Enthält Informationen, die an einen oder mehrere Empfänger gesendet werden können.  <br/> |
|Nachrichtenspeicher  <br/> |Fungiert als hierarchisch organisierte Datenbank von Nachrichten.  <br/> |
|Anbieter  <br/> |Behandelt das Starten und Herunterfahren von Dienstanbietern.  <br/> |
|Spooler-Hook  <br/> |Führt eine spezielle Verarbeitung für eingehende und ausgehende Nachrichten aus.  <br/> |
|Status  <br/> |Ermöglicht den Zugriff auf den Status des Dienstanbieters.  <br/> |
|Tabelle  <br/> |Bietet Zugriff auf eine Zusammenfassungsansicht der Objektdaten im Zeilen- und Spaltenformat, ähnlich einer Datenbanktabelle.  <br/> |
   
Alle Dienstanbieter implementieren ein Anbieterobjekt und ein Anmeldeobjekt. Anbieterobjekte dienen ausschließlich der Buchführung. sie werden von mapi verwendet, um die Start- und Herunterfahren-Prozesse zu steuern. Anmeldeobjekte bedient einige Clientanforderungen indirekt. Beispielsweise verarbeitet das Anmeldeobjekt des Nachrichtenspeicheranbieters die Benachrichtigungsregistrierung und Anforderungen zum Öffnen von Nachrichtenspeicherobjekten. 
  
Anbieter- und Anmeldeobjekte implementieren je nach Typ des Dienstanbieters, der die Implementierung bereitstellt, eine andere Schnittstelle. Ein Nachrichtenspeicheranbieter implementiert die [IMSProvider : IUnknown-](imsprovideriunknown.md) und [IMSLogon : IUnknown-Schnittstellen](imslogoniunknown.md) in seinen Anbieter- und Anmeldeobjekten, ein Adressbuchanbieter implementiert die [IABProvider : IUnknown-](iabprovideriunknown.md) und [IABLogon : IUnknown-Schnittstellen,](iablogoniunknown.md) und ein Transportanbieter implementiert die [IXPProvider : IUnknown-](ixpprovideriunknown.md) und [IXPLogon : IUnknown-Schnittstellen.](ixplogoniunknown.md) 
  
Nachrichtenhookanbieter implementieren Spooler-Hookobjekte oder Objekte, die eingehende und ausgehende Nachrichten filtern.
  
Dienstanbieter verwenden in der Regel nur wenige Objekte. Am häufigsten verwenden sie ein Supportobjekt, das MAPI bereitstellt, um Clientanforderungen zu implementieren. Das Supportobjekt wird für den Anbietertyp angepasst, der es verwendet. Für alle Dienstanbieter umfasst das Supportobjekt Methoden für die Behandlung von Ereignisbenachrichtigungen, das Anzeigen von Konfigurationseigenschaften, das Öffnen von Objekten und die Fehlerbehandlung. Die restlichen Methoden sind spezifisch für ihre Verwendung. Es gibt angepasste Versionen für Adressbuch-, Nachrichtenspeicher- und Transportanbieter sowie für konfigurationsunterstützung. Beispielsweise zeigt das Adressbuchunterstützungsobjekt Details und benutzerdefinierte Empfängerdialogfelder an. Das Supportobjekt für den Nachrichtenspeicher unterstützt Kopier- und Verschiebungsvorgänge für Ordner und Nachrichten. Das Supportobjekt des Transportanbieters enthält Methoden zum Vereinfachen der Interaktion mit dem MAPI-Spooler. 
  
Einige Dienstanbieter verwenden Tabellendaten und Eigenschaftsdatenobjekte – Von MAPI implementierte Hilfsprogrammobjekte. Tabellendatenobjekte ermöglichen Dienstanbietern das Verwalten der zugrunde liegenden Daten einer Tabelle. Eigenschaftendatenobjekte ermöglichen Dienstanbietern das Festlegen des Objekt- und Eigenschaftszugriffs. 
  
Transportanbieter, die das Transport Neutral Encapsulation Format (TNEF) zum Übertragen von Eigenschaften unterstützen, verwenden ein TNEF-Objekt, das mapi zur Unterstützung der [ITnef : IUnknown-Schnittstelle](itnefiunknown.md) implementiert. Weitere Informationen finden Sie unter [Entwickeln eines TNEF-Enabled-Transportanbieters.](developing-a-tnef-enabled-transport-provider.md) 
  
## <a name="see-also"></a>Siehe auch



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Entwickeln eines TNEF-Enabled-Transportanbieters](developing-a-tnef-enabled-transport-provider.md)

