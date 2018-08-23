---
title: MAPI implementierte Objekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: d212a86aae0503a5e02a5a7ecddb83db10a4d664
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572375"
---
# <a name="mapi-implemented-objects"></a>MAPI implementierte Objekte
  
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI implementierte mehrere Objekte für die Verwendung durch Clientanwendungen und -Dienstanbieter. Session-Objekt ermöglicht Clients Sitzung Services, Zugriff auf Tabellen und zur Kommunikation mit-Dienstanbieter verwenden. Das Address Book-Objekt stellt Clients integrierte Zugriff auf alle der verschiedenen adressbuchanbietern implementierte. 
  
MAPI stellt mehrere Tabelle und den Status Objekte für Clients zum Anzeigen und Überwachen der Sitzung und Service Provider-Informationen verwendet werden. Beispielsweise bietet MAPI ein Profil und einer Nachricht Service-Tabelle mit Informationen zu allen im aktuellen Profil Dienste Nachricht mit Informationen zu allen der Profile, die auf dem Computer installiert sind. MAPI bietet drei verschiedenen Statuswerte Objekte: eines, Teilsystems insgesamt, einen für die MAPI-Warteschlange und einen für die integrierte Adressbuch darstellt. 
  
MAPI implementierte vier verschiedene Objekte für die Verwaltung der Konfigurations des Message-Dienste, Service Provider und Profile. Clients und -Dienstanbieter verwenden des Anbieters für und Profil Section-Objekten; Diese Objekte aktivieren sie zum Konfigurieren von Dienstanbietern und Zugreifen auf Profileigenschaften. Clients verwenden nur Messagingdiensts und Profile Administration-Objekten, die Objekte, die die Verwaltung von Message-Dienste und Profilen unterstützen. 
  
MAPI-Dienstanbieter zwei Objekte bereit: ein Support-Objekt und ein TNEF-Objekt. Alle-Dienstanbieter verwenden Sie eine oder mehrere Support-Objekte. Es gibt vier verschiedene Support-Objekt Implementierungen. MAPI stellt eine Implementierung zur Unterstützung der Konfiguration als auch bestimmte Implementierungen für Adressbuch, Nachrichtenspeicher und Transportanbieter nicht unterstützt. Das TNEF-Objekt wird von Transportanbieter verwendet, die die Transport Neutral Encapsulation Format (TNEF) unterstützen.
  
Zwei Hilfsobjekte, Tabellendaten und Eigenschaftendaten, werden in der Regel vom Dienstanbieter verwendet. Tabelle Datenobjekte Hilfe bei der Implementierung von Table-Objekten; Eigenschaft Daten Objekte Hilfe Set und View-Eigenschaftenzugriff und Hilfe bei der Implementierung der [IMAPIProp: IUnknown](imapipropiunknown.md), die Basis-Eigenschaft-Schnittstelle. 
  
In der folgenden Tabelle werden den Zweck für jedes Objekt, das MAPI implementierte zusammengefasst.
  
|**MAPI-Objekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuch  <br/> |Bietet Zugriff auf die integrierte Ansicht der Empfängerinformationen, die alle Anbieter Address Book in das aktive Profil gehört.  <br/> |
|Verwalten von Diensten  <br/> |Bietet Zugriff auf Informationen zum Dienst für die Konfiguration.  <br/> |
|Profilverwaltung  <br/> |Ermöglicht den Zugriff auf die Profilinformationen für die Konfiguration.  <br/> |
|Profilabschnitt  <br/> |Ein Teil eines Profils verwendet, um eine bestimmte Nachricht-Dienst oder den Dienstanbieter beschreiben.  <br/> |
|Eigenschaftendaten  <br/> |Wird der Zugriff auf Eigenschaften, und hilft Ihnen **IMAPIProp**implementieren.  <br/> |
|Des Anbieters für  <br/> |Bietet Zugriff auf Informationen zu Anbietern für die Konfiguration.  <br/> |
|Sitzung  <br/> |Stellt eine Verbindung mit der zugrunde liegenden messaging-Systeme und bietet Zugriff auf Ressourcen von MAPI-Clients.  <br/> |
|Status  <br/> |Bietet Zugriff auf den Status des MAPI-Subsystems, Adressbuch oder die MAPI-Warteschlange.  <br/> |
|Support  <br/> |Hilft Dienstanbieter Clientanforderungen.  <br/> |
|Tabelle  <br/> |Bietet Zugriff auf eine Zusammenfassungsansicht der Objektdaten Zeile und Spalte, ähnlich wie in in einer Datenbanktabelle.  <br/> |
|Tabellendaten  <br/> |Zugriff auf die zugrunde liegenden Tabellendaten verwaltet und Table-Objekte implementiert.  <br/> |
|TNEF  <br/> |Unterstützt die Verwendung von Transport Neutral Encapsulation Format (TNEF).  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen den, die von MAPI implementierte Objekte, die von dem sie erben Schnittstellen und die Komponenten, die sie verwenden. 
  
**Von MAPI implementierte Objekte**
  
![Von MAPI implementierte Objekte] (media/amapi_68.gif "Von MAPI implementierte Objekte")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [MAPI-Objekt und Übersicht über die Benutzeroberfläche](mapi-object-and-interface-overview.md)

