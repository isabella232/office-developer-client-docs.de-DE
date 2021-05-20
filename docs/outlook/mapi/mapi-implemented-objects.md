---
title: MAPI-implementierte Objekte
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 5d07c259-0ceb-4ea5-98b4-b01720edfe2a
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 86aa8451b5b127764134f1a3a905366fd014d0c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430630"
---
# <a name="mapi-implemented-objects"></a>MAPI-implementierte Objekte
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI implementiert mehrere Objekte für die Verwendung durch Clientanwendungen und Dienstanbieter. Das Sitzungsobjekt ermöglicht Clients die Verwendung von Sitzungsdiensten, den Zugriff auf Tabellen und die Kommunikation mit Dienstanbietern. Das Adressbuchobjekt bietet Clients integrierten Zugriff auf alle verschiedenen Adressbuchanbieter. 
  
MAPI stellt mehrere Tabellen- und Statusobjekte für Clients zur Anzeige und Überwachung von Sitzungs- und Dienstanbieterinformationen zur Verfügung. Beispielsweise stellt MAPI eine Profiltabelle mit Informationen zu allen auf dem Computer installierten Profilen und eine Nachrichtendiensttabelle mit Informationen zu allen Nachrichtendiensten im aktuellen Profil zur Verfügung. MAPI bietet drei verschiedene Statusobjekte: eines, das das allgemeine Subsystem darstellt, eines für den MAPI-Spooler und eines für das integrierte Adressbuch. 
  
MAPI implementiert vier verschiedene Objekte zum Verwalten der Konfiguration von Nachrichtendiensten, Dienstanbietern und Profilen. Sowohl Clients als auch Dienstanbieter verwenden Anbieterverwaltungs- und Profilabschnittsobjekte. Diese Objekte ermöglichen ihnen das Konfigurieren von Dienstanbietern und den Zugriff auf Profileigenschaften. Clients verwenden nur Nachrichtendienst- und Profilverwaltungsobjekte, die Objekte, die die Verwaltung von Nachrichtendiensten und Profilen unterstützen. 
  
MAPI stellt zwei Objekte für Dienstanbieter zur Verfügung: ein Supportobjekt und ein TNEF-Objekt. Alle Dienstanbieter verwenden ein oder mehrere Supportobjekte. Es gibt vier verschiedene Supportobjektimplementierungen. MAPI stellt eine Implementierung zur Unterstützung der Konfiguration sowie spezifische Implementierungen zur Unterstützung von Adressbuch-, Nachrichtenspeicher- und Transportanbietern zur Unterstützung zur Unterstützung von. Das TNEF-Objekt wird von Transportanbietern verwendet, die das Transport Neutral Encapsulation Format (TNEF) unterstützen.
  
Zwei Hilfsobjekte, Tabellendaten und Eigenschaftsdaten, werden in der Regel von Dienstanbietern verwendet. Tabellendatenobjekte helfen bei der Implementierung von Tabellenobjekten. Eigenschaftsdatenobjekte helfen beim Festlegen und Anzeigen des Eigenschaftenzugriffs und bei der Implementierung von [IMAPIProp : IUnknown](imapipropiunknown.md), der Basiseigenschaftsschnittstelle. 
  
In der folgenden Tabelle wird der Zweck für jedes von MAPI implementierte Objekt zusammengefasst.
  
|**MAPI-Objekt**|**Beschreibung**|
|:-----|:-----|
|Adressbuch  <br/> |Bietet Zugriff auf die integrierte Ansicht von Empfängerinformationen, die zu allen Adressbuchanbietern im aktiven Profil gehören.  <br/> |
|Nachrichtendienstverwaltung  <br/> |Bietet Zugriff auf Nachrichtendienstinformationen für die Konfiguration.  <br/> |
|Profilverwaltung  <br/> |Bietet Zugriff auf Profilinformationen für die Konfiguration.  <br/> |
|Abschnitt "Profil"  <br/> |Ein Teil eines Profils, das zum Beschreiben eines bestimmten Nachrichtendiensts oder Dienstanbieters verwendet wird.  <br/> |
|Eigenschaftendaten  <br/> |Behält den Zugriff auf Eigenschaften bei und hilft bei der Implementierung **von IMAPIProp**.  <br/> |
|Anbieterverwaltung  <br/> |Bietet Zugriff auf Dienstanbieterinformationen für die Konfiguration.  <br/> |
|Sitzung  <br/> |Stellt eine Verbindung zu zugrunde liegenden Messagingsystemen dar und bietet Clients Zugriff auf MAPI-Ressourcen.  <br/> |
|Status  <br/> |Bietet Zugriff auf den Status des MAPI-Subsystems, des Adressbuchs oder des MAPI-Spoolers.  <br/> |
|Support  <br/> |Hilft Dienstanbietern bei der Verarbeitung von Clientanforderungen.  <br/> |
|Tabelle  <br/> |Bietet Zugriff auf eine Zusammenfassungsansicht von Objektdaten im Zeilen- und Spaltenformat, ähnlich einer Datenbanktabelle.  <br/> |
|Tabellendaten  <br/> |Behält den Zugriff auf zugrunde liegende Tabellendaten bei und implementiert Tabellenobjekte.  <br/> |
|TNEF  <br/> |Unterstützt die Verwendung des Transport Neutral Encapsulation Format (TNEF).  <br/> |
   
Die folgende Abbildung zeigt die Beziehung zwischen den von MAPI implementierten Objekten, den Schnittstellen, von denen sie erben, und den Komponenten, die sie verwenden. 
  
**Von MAPI implementierte Objekte**
  
![Objekte, die MAPI implementiert Objekte,](media/amapi_68.gif "die MAPI implementiert")
  
## <a name="see-also"></a>Siehe auch

- [IMAPIProp : IUnknown](imapipropiunknown.md)
- [Übersicht über das MAPI-Objekt und die Schnittstelle](mapi-object-and-interface-overview.md)

