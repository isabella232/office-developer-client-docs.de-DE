---
title: OBJEKTE des MAPI-Dienstanbieters
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
# <a name="mapi-service-provider-objects"></a>OBJEKTE des MAPI-Dienstanbieters

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Dienstanbieter implementieren viele Objekte. Einige werden hauptsächlich von MAPI und andere von Clientanwendungen verwendet. Einige Objekte werden von allen Arten von Dienstanbietern implementiert. Der Rest ist für einen einzelnen Anbietertyp spezifisch. In der folgenden Tabelle werden alle Dienstanbieterobjekte beschrieben.
  
|**Dienstanbieterobjekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuchcontainer  <br/> |Enthält Empfängerinformationen für einen Adressbuchanbieter im aktiven Profil. Adressbuchanbieter können über einen oder mehrere Adressbuchcontainer verfügen.  <br/> |
|Attachment  <br/> |Enthält zusätzliche Daten, z. B. eine Datei oder ein OLE-Objekt, die einer Nachricht zugeordnet werden sollen.  <br/> |
|Steuerelement  <br/> |Aktiviert oder deaktiviert eine Schaltfläche und initiiert die Verarbeitung, wenn auf die Schaltfläche geklickt wird.  <br/> |
|Verteilerliste  <br/> |Beschreibt eine Gruppierung einzelner Nachrichtenempfänger.  <br/> |
|Ordner  <br/> |Enthält Nachrichten und andere Nachrichtencontainer.  <br/> |
|Anmeldung  <br/> |Behandelt Ereignisbenachrichtigungen und Clientanforderungen des Dienstanbieters.  <br/> |
|Messagingbenutzer  <br/> |Beschreibt einen einzelnen Empfänger einer Nachricht.  <br/> |
|Message  <br/> |Enthält Informationen, die an einen oder mehrere Empfänger gesendet werden können.  <br/> |
|Nachrichtenspeicher  <br/> |Dient als hierarchische Geordnete Datenbank von Nachrichten.  <br/> |
|Anbieter  <br/> |Behandelt das Starten und Herunterfahren des Dienstanbieters.  <br/> |
|Spooler-Hook  <br/> |Führt eine spezielle Verarbeitung für eingehende und ausgehende Nachrichten durch.  <br/> |
|Status  <br/> |Bietet Zugriff auf den Status des Dienstanbieters.  <br/> |
|Tabelle  <br/> |Bietet Zugriff auf eine Zusammenfassungsansicht von Objektdaten im Zeilen- und Spaltenformat, ähnlich einer Datenbanktabelle.  <br/> |
   
Alle Dienstanbieter implementieren ein Anbieterobjekt und ein Anmeldeobjekt. Anbieterobjekte sind ausschließlich für die Buchhaltung; sie werden von MAPI verwendet, um die Start- und Herunterfahrensprozesse zu steuern. Anmeldeobjekte verarbeiten einige Clientanforderungen indirekt. Das Anmeldeobjekt des Nachrichtenspeicheranbieters verarbeitet beispielsweise die Benachrichtigungsregistrierung und Anforderungen zum Öffnen von Nachrichtenspeicherobjekten. 
  
Anbieter- und Anmeldeobjekte implementieren je nach Typ des Dienstanbieters, der die Implementierung liefert, eine andere Schnittstelle. Ein Nachrichtenspeicheranbieter implementiert die [ImSProvider : IUnknown](imsprovideriunknown.md) und [IMSLogon : IUnknown-Schnittstellen](imslogoniunknown.md) in seinen Anbieter- und Anmeldeobjekten, ein Adressbuchanbieter implementiert die [IABProvider : IUnknown](iabprovideriunknown.md) und [IABLogon : IUnknown-Schnittstellen,](iablogoniunknown.md) und ein Transportanbieter implementiert die [IXPProvider : IUnknown](ixpprovideriunknown.md) und [IXPLogon : IUnknown-Schnittstellen.](ixplogoniunknown.md) 
  
Nachrichtenhakenanbieter implementieren Spooler-Hook-Objekte oder Objekte, die eingehende und ausgehende Nachrichten filtern.
  
Dienstanbieter verwenden in der Regel nur wenige Objekte. Am häufigsten verwenden sie ein Supportobjekt, das MAPI zur Implementierung von Clientanforderungen zur Verfügung stellt. Das Supportobjekt wird für den Anbietertyp angepasst, der es verwendet. Für alle Dienstanbieter umfasst das Supportobjekt Methoden zum Behandeln von Ereignisbenachrichtigungen, zum Anzeigen von Konfigurationseigenschaften, zum Öffnen von Objekten und zur Fehlerbehandlung. Die restlichen Methoden sind spezifisch für ihre Verwendung. Es gibt angepasste Versionen für Adressbuch-, Nachrichtenspeicher- und Transportanbieter sowie für die Konfigurationsunterstützung. Das Adressbuchunterstützungsobjekt zeigt beispielsweise Details und benutzerdefinierte Empfängerdialogfelder an. Das Unterstützungsobjekt für den Nachrichtenspeicher unterstützt Kopier- und Verschiebevorgänge für Ordner und Nachrichten. Das Supportobjekt des Transportanbieters enthält Methoden zur Erleichterung der Interaktion mit dem MAPI-Spooler. 
  
Einige Dienstanbieter verwenden Tabellendaten- und Eigenschaftsdatenobjekte – Hilfsobjekte, die MAPI implementiert. Tabellendatenobjekte ermöglichen Dienstanbietern die Verwaltung der zugrunde liegenden Daten einer Tabelle. Eigenschaftendatenobjekte ermöglichen Dienstanbietern das Festlegen des Objekt- und Eigenschaftszugriffs. 
  
Transportanbieter, die das Transport Neutral Encapsulation Format (TNEF) für die Übertragung von Eigenschaften unterstützen, verwenden ein TNEF-Objekt, das MAPI implementiert, um die [ITnef : IUnknown-Schnittstelle](itnefiunknown.md) zu unterstützen. Weitere Informationen finden Sie unter [Developing a TNEF-Enabled Transport Provider](developing-a-tnef-enabled-transport-provider.md). 
  
## <a name="see-also"></a>Siehe auch



[ITnef : IUnknown](itnefiunknown.md)
  
[IMSProvider : IUnknown](imsprovideriunknown.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)
  
[IABProvider : IUnknown](iabprovideriunknown.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)
  
[IXPProvider : IUnknown](ixpprovideriunknown.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)


[Entwickeln eines TNEF-Enabled-Transportanbieters](developing-a-tnef-enabled-transport-provider.md)

